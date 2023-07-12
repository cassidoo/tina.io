---
title: Self-hosted TinaCMS powered by Vercel KV & NextAuth
date: '2023-06-30T04:00:00.000Z'
last_edited: '2023-06-30T04:00:00.000Z'
author: Kelly Davis
prev: content/blog/self-hosted-datalayer.md
---

Earlier this year, we [released](/blog/self-hosted-datalayer/ "released") the first iteration of self-hosted TinaCMS. The initial [demo](https://github.com/tinacms/tina-self-hosted-demo/tree/274c0d9ee004629ff0cef2539b56c88324abd8f8) relied on Tina Cloud for auth and used MongoDB for the data layer. That was the first step in freeing TinaCMS users from vendor lock-in, but there were limitations, such as requiring a custom auth implementation when not using Tina Cloud and requiring MongoDB for the data layer. Since then, we've been hard at work on improving our self-hosted offering to make it easier to get started and less dependent on other vendor services (including our own). Today we are excited to announce the next iteration of our self-hosted Tina demo, leveraging [Vercel KV](https://vercel.com/docs/storage/vercel-kv) for the data layer and [NextAuth.js](NextAuth.js) for auth. It is now possible for a developer to setup a fully functioning [Next.js](https://nextjs.org/) site running TinaCMS relying on only GitHub for source control and Vercel for hosting, auth, and data management.

Internally Tina uses LevelDB as an abstraction over the 
