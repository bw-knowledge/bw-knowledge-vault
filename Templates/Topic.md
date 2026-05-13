---
aliases:
---

# Resources 

<%*
// Get the current note's name (without .md extension)
const noteName = tp.file.title;

// Read the current Articles.base file
const articlesBasePath = "Bases/Articles.base";
let articlesBaseContent = await app.vault.adapter.read(articlesBasePath);

// Check if a view with this name already exists
const viewNameRegex = new RegExp(`  - type: table\\s+name: ${noteName}`, 'i');
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
      - author
      - source
      - watched
    sort:
      - property: file.name
        direction: DESC
    columnSize:
      file.name: 261
      note.source: 218`;

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