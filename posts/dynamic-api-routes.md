---
title: 'Dynamic API Routes in Next.js'
date: '2023-05-03'
---

API routes support **dynamic routes**, and follow the same file naming rules used for pages.

For example, the API route _`pages/api/post/[pid].js`_ has the following code:

```
export default function handler(req, res) {
  const { pid } = req.query
  res.end(`Post: ${pid}`)
}

```

Now, a request to _`/api/post/abc`_ will respond with the text: _`Post: abc`_.
