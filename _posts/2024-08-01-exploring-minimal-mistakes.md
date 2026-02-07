---
layout: single
title: "Exploring Minimal Mistakes Layouts"
permalink: /blog/exploring-minimal-mistakes/
categories: [testing, feature]
tags: [minimal-mistakes, layout, experiment]
summary: "A quick tour through the skin and layout options available in Minimal Mistakes."
---

Minimal Mistakes comes with a ton of layout and skin combinations that make testing different configurations easy. This post walks through toggling between the `air` and `default` skins, swapping sidebar behaviors, and verifying the layout responds to media queries.

## Layout Notes

- Toggle `minimal_mistakes_skin` to compare color pairs.
- Use the `header: blur` option to see how the navigation reacts.
- Mix in `sidebar: false` for full-width content experiments to ensure the templating holds up.

## Testing Tips

Try mocking long-form content with nested sections to ensure the typography scales gracefully. Adjust margin utilities directly in `_sass/_custom.scss` (or a similar include) to confirm the theme keeps its rhythm.
