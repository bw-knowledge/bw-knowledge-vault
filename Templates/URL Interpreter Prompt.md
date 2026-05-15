You are extracting key information from an article for a company knowledge vault.

The article content has been scraped from a webpage and may contain non-article material such as navigation menus, sponsored content, advertisements, newsletter signup forms, comments sections, "related articles" links, footer content, and promotional callouts. IGNORE all such content. Extract only from the article's main editorial body.

In particular:
- People, Places, Numbers, Things, and Concepts must come from the article's editorial content only — NOT from inline ads, sponsor callouts, webinar promos, sidebar widgets, or "trending now" sections.
- Numbers extracted from sponsor callouts ("Only 7 seats left", "Save 50%", subscriber counts, comment counts) are NOT part of the article's substantive claims and must be excluded.
- Headlines must reflect what the article argues, not what advertisements alongside it promote.

Output the following sections in markdown. Do not include any preamble or explanation outside these sections.

In summary, [the most interesting aspect of the article, delivered as a complete declarative statement starting with this exact phrase].

## Suggested Topics

[Freely suggest 1–3 topic names that best describe what this article is ABOUT. Choose names that are concise (1–3 words), specific enough to be useful but general enough to gather multiple related articles over time. Plain text, comma-separated. Do NOT use [[wikilinks]].]

{MATCHED_TOPICS_SECTION}

## Headlines

- **[A bold, declarative headline ending with a period.]** [1–2 supporting sentences with the specifics from the article.]
- **[Next headline.]** [Supporting sentences.]
- [3–5 headlines total]

## Things

- **People:** [comma-separated names mentioned in the article's editorial content]
- **Places:** [comma-separated places, organisations, or product surfaces]
- **Numbers:** [specific statistics, dates, quantities from the article — semicolon-separated. Exclude promotional numbers like seat counts, discount percentages, or subscriber counts that aren't part of the article's substantive claims.]
- **Things:** [products, tools, frameworks, named systems discussed in the article]
- **Concepts:** [abstract concepts and terms of art from the article]

---

Article title: {TITLE}
Article source: {URL}

Article content:
{CONTENT}