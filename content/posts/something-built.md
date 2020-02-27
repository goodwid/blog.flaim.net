---
date: 2020-02-27
title: "Something built"
cover: "https://unsplash.it/400/300/?random?build"
categories:
    - JavaScript
    - Node
tags:
    - github
    - code
---

## RSS

So, once upon a time I made a [PR monitor](https://www.npmjs.com/package/pr-monitor) for GitHub so I could get an aggregate view of all the PRs in all our org's repos, and stay on top of them.  It worked great, I use it many many times daily. Adding in a Chrome extension today that supports RSS feeds led me to wonder if could generate XML from the JSON output of the tool.  Yes, for sure, since really, everything exists as an npm package, even if it's 5 years old and was last built in node 4.  So yeah.. in the end, I realized that RSS wasn't the right tool for the job, but I did end up with an Express endpoint that returns JSON PR data.  Good times.

```js
router.get('/pulls', async (req, res) => {
  const results = await PRs();
  res.json(results);
});
```

Today, I made a thing.
