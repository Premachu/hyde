---
layout: page
title: Adding pages
---


To add pages to the header you just have to set `layout:page`, rather than post.

There is some some "liquid" code in includes/sidebar.html that looks for all top-level documents classed as "page" and makes sidebar links to the

## Example

Create a new file in the top-level/root directory called `cv.md`. 

Paste the following code and commit the new file

```
---
layout: page
title: CV
---

This is my CV
```

The header/sidebar should now have a link to your CV

## Adding download

If you want to add a download, i.e. a PDF of your CV, rather than MD file, then don't add ".md" extension onto the end of your file and it will be a download link. 

