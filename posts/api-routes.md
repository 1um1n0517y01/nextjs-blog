---
title: 'A Good Use Case of API Routes in Next.js '
date: '2023-05-03'
---

API Routes let you create an **API endpoint** inside a Next.js app. You can do so by creating a function inside the **_pages/api_** directory that has the following format:

```
// req = HTTP incoming message, res = HTTP server response
export default function handler(req, res) {
  // ...
}
```

A good use case for API Routes is **handling form input**. For example, you can create a form on your page and have it send a POST request to your API Route. You can then write code to directly save it to your database. The API Route code will not be part of your client bundle, so you can safely write server-side code.

For example:

```
export default function handler(req, res) {
const email = req.body.email;
// Then save email to your database, etc...
}
```
