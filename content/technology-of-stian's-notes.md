---
title: "technology of stian's notes"
---

- This site is based on two main technologies. First I take all my notes on Roam, and export the JSON.
- Then I use **roam-export** to process the output. This script is pretty messy, but has a lot of neat features
    - automatically resolve embeds and block-embeds
    - queries
        - (I've got this working, but it's not quite integrated yet)
    - advanced link handling
        - use a heuristic to see where I've added an external URL to a topic
        - for pages that are not part of the export, either convert internal URLs to external URLs, or turn them bold (to distinguish from links that actually go to internal pages with content)
    - automatically determine pages to export
        - right now, it exports all pages linked directly from the about page, as well as any page or block that has the `public` tag. (If the tag is top-level on a page, the whole page is exported, but if I have a block on a daily page I want to export, I can just add that tag, and the whole block+children is exported as a page)
- Finally, I send the output to Gatsby, using a **Aengus McMillin**'s **gatsby-theme-brain** and **Aravind Balla's** **gatsby-theme-andy**, which gives the nice theme and automatic link preview.
- I have many ideas on how to improve this
    - Commenting, maybe even inline (using **Hypothes.is** or something else?)
    - Tag some pages as blog posts, which get a date, a stream of posts, an RSS feed etc
    - Render highlights (^^) correctly
    - Enable folding of long pages (example https://www.loom.com/share/246622d45cb844559ecfc2543ff1d55c using **react-treeview**)
    - Interlinking with other people's **digital garden**s