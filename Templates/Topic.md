---
aliases:
---

# Resources 

<%*
// Get the current note's name (without .md extension)
const noteName = tp.file.title;
const escapeRegExp = (value) => value.replace(/[.*+?^${}()|[\]\\]/g, "\\$&");

// Read the current Articles.base file
const articlesBasePath = "Bases/Articles.base";
let articlesBaseContent = await app.vault.adapter.read(articlesBasePath);

// Check if a view with this name already exists
const viewNameRegex = new RegExp(`  - type: table\\s+name: ${escapeRegExp(noteName)}(?:\\r?\\n|$)`, 'i');
const viewExists = viewNameRegex.test(articlesBaseContent);

if (!viewExists) {
    // Create the new view configuration
    const newView = `  - type: table
    name: ${noteName}
    filters:
      or:
        - file.hasLink("${tp.file.path(true)}")
    order:
      - file.name
      - formula.Domain
      - author
      - source
      - watched
    sort:
      - property: file.name
        direction: DESC
    columnSize:
      file.name: 261
      formula.Domain: 197
      source: 218`;

    // Find the last view in the file and add the new one after it
    const viewsEndRegex = /(\n\n---\n)/;
    if (viewsEndRegex.test(articlesBaseContent)) {
        // If there's a separator at the end, add before it
        articlesBaseContent = articlesBaseContent.replace(viewsEndRegex, `\n${newView}$1`);
    } else {
        // Otherwise, add at the end
        articlesBaseContent += `\n${newView}`;
    }
    
    // Write the updated content back to Articles.base
    await app.vault.adapter.write(articlesBasePath, articlesBaseContent);
}
_%>

![[Articles.base#<% tp.file.title %>]]
