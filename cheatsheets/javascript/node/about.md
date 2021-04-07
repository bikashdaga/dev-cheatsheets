---
title: About
description: What is Node and what can you do with it?
---

Node (or "Node.js", or less commonly "NodeJS") is a **server-side** runtime environment for JavaScript. It is an alternative to the **browser** runtime environment (which was the first place JS was used).

Node can process JavaScript on a machine locally or in the cloud, even without a desktop display or a browser installed.

So Node lets you run scripts and applications and use libraries in a similary way to how Python, Java and PHP have done since they were created.

For interest, [Deno][] is another server-side environment of JS. 

[Deno]: https://michaelcurrin.github.io/dev-resources/resources/javascript/deno/


## What can Node do?

Node can be used for the following, among other use-cases.

- Web scraping
- CLI tools
- Desktop applications
    - e.g. VS Code, WhatApp
    - Often built with Electron.
- Web applications
    - Rendering dynamic website content.
        - In the same way that PHP or Python web servers generate and return HTML pages.
        - You might host your app as a server on AWS (such as with EC2 or Kubernetes) or [Vercel](https://vercel.com/) (they actually turn your app into multiple server-less endpoints..
    - It can be used to make a REST API, sending and receiving JSON data. 
        - The Express library is a common choice here.
        - Again might host your app on AWS or Vercel.
    - Serverless computing.
        - Scale cheaply and fast, having your script run in parallel, adapting as demand changes.
        - Use AWS _Lambda_ or Netlify _Functions_.
    - Single-Page Applications. 
        - Like using [React](https://github.com/MichaelCurrin/react-quickstart), [Vue](https://github.com/MichaelCurrin/vue-quickstart) or [Docsify](https://github.com/MichaelCurrin/docsify-js-template). Where there is one `index.html` and the multi-page site experience is create dynamically using JavaScript.
        - For the common use-case, a Node server is unnecessary to serve a SPA. So you can use any static hosting site to make your site public.
    - Rendering static sites. 
        - Like using [VuePress](https://github.com/MichaelCurrin/vuepress-quickstart), [Nuxt](https://github.com/MichaelCurrin/nuxt-default-quickstart) or [Hexo](https://github.com/MichaelCurrin/hexo-quickstart).
        - Use static hosting as for SPA.
    - Hybrid sites.
        - Nuxt renders static content for the initial load and for search engine crawlers, then switches to SPA experience.
        - Next lets you choose between server-side rendering and statically rendered content, probably on different routes in the same app too.
- Mobile apps
    - Like using React Native.
- Games (web or desktop or mobile)

### Node as a build tool

Note that if have a Single-Page Application or a static site, you run Node to generate build output (a directory of HTML, JS, CSS and images).

Then the content gets stored somewhere for public access _static_ content.

At the point, Node is no longer needed.

For example, you can use Nginx, a Python webserver (the builtin `http.server`) or VS Code's Live Server. Or deploy to GitHub Pages, Netlify or AWS S3.

But of course, when you want to continue developing your app, you'll use Node to test it and then deploy it.


## Run JS directly

Node can run JS scripts directly.

```sh
$ node hello.js
```

Or you can use enter the interactive console in your terminal.

```sh
$ node
```
```
Welcome to Node.js v14.13.1.
> console.log('Hello, World!')
Hello, World!
```


## Node as a dev tool

Node can perform the following, using NPM:

- Package management.
    - Download packages.
    - Upgrade packages when newer ones are available - especially useful for security updates.
- Linting. e.g. `npm run lint` or `npx eslint .`
- Formatting. e.g. `npm run fmt` or `npx prettier -w .
- Run tests. e.g. `npm test`
- Run typechecks - if using TypeScript. e.g. `npm run compile`
- Do production builds
    - Minify to reduce the size of the content to be downloaded.
    - Bundle - to collect all your JS modules and external libraries and bundle as a single JS file.
    - Transpile - convert newer JS to older JS syntax, or from JSX or TypeScript to plain JS.

Using these tasks means that you improve the code quality and performance of your app, which improves the lifes of your developer team and of end-users.

You can setup a JavaScript project that is a SPA but that doesn't need Node.

Here is a Vue-based application. Rather than loading Vue using a `script` tag in the HTML, rather the newer ESModule syntax is used. So within the JS script there is an import of Vue from a CDN and the browser knows to download this and use it.

- [![MichaelCurrin - vue-frontend-quickstart](https://img.shields.io/static/v1?label=MichaelCurrin&message=vue-frontend-quickstart&color=blue&logo=github)](https://github.com/MichaelCurrin/vue-frontend-quickstart)