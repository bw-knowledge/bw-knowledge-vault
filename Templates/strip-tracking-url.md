<%*
const file = tp.file.find_tfile(tp.file.path(true));
const cache = app.metadataCache.getFileCache(file);
const frontmatter = cache?.frontmatter;

if (frontmatter?.source) {
  try {
    const u = new URL(frontmatter.source);
    
    // Strip text fragments
    if (u.hash.startsWith(':~:text=')) u.hash = '';
    
    // Strip tracking params
    ['utm_source','utm_medium','utm_campaign','utm_term','utm_content','utm_id',
     'fbclid','gclid','msclkid','mc_eid','mc_cid',
     '_ga','_gl','ref','twclid','igshid'].forEach(p => u.searchParams.delete(p));
    
    const cleaned = u.toString();
    if (cleaned !== frontmatter.source) {
      await app.fileManager.processFrontMatter(file, fm => {
        fm.source = cleaned;
      });
    }
  } catch (e) { /* invalid URL, leave as-is */ }
}
%>