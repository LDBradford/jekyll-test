---
layout: single
title: "Scripting Automated Deployments"
permalink: /blog/scripting-automated-deployments/
categories: [testing, ops]
tags: [automation, deploy, scripts]
summary: "Capture the steps for testing deployment scripts before the site is tied to a live publishing pipeline."
---

Use this draft to outline a deployment trial run. Document the invocation of `bundle exec jekyll build`, how to swap branches safely, and the checklist for validating that plugins like `jekyll-remote-theme` remain compatible with automation tooling.

## Checklist

- Confirm builds work in both the `air` and `default` skins.
- Run spell check on generated HTML before publishing.
- Rotate a screenshot for each step to keep the guide visual and easy to follow.

## Notes

Keep a log of timestamps for each automated run and note any warnings emitted so regressions are easy to detect.
