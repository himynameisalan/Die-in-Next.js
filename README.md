# Next.js-Quick-Start

# Chapter1: Create helloworld project
1. Create folder >> mkdir helloworld
2. Go to folder >> cd helloworld
3. Initial project info (user "-y" for default info) >> npm init -y
4. Install next.js package >> npm install --save react react-dom next
5. Modify project info, add "scripts" in package.json. 
```javascript
"scripts": {
  "dev": "next",
  "build": "next build",
  "start": "next start"
}
```
6. Create folder "pages".
7. Create file "index.js in "pages".
8. Add codes in "index.js".
```javascript
export default () => <div>Welcome to next.js!</div>
```
9. Run project >> npm run dev
10. Preview project @ http://localhost:3000

# Chapter2: Try Bootstrap for grid system
1. Download Boostrap. https://getbootstrap.com/docs/4.1/getting-started/download/
2. Move "boostrap.min.css" in project folder.
3. Install "next-css" to make Next.js + CSS happen (Read this! https://github.com/zeit/next-plugins/tree/master/packages/next-css) >> npm install --save @zeit/next-css
4. Import "bootstrap.min.css". Add codes in "index.js" (the stylesheet will be compiled to .next/static/style.css)
import "../bootstrap.min.css"
5. Create file "_Document.js" to include ".next/static/style.css".
```javascript
import Document, { Head, Main, NextScript } from 'next/document'
export default class MyDocument extends Document {
  render() {
    return (
      <html>
        <Head>
          <link rel="stylesheet" href="/_next/static/style.css" />
        </Head>
        <body>
          <Main />
          <NextScript />
        </body>
      </html>
    )
  }
}
```
6. Create file "next.config.js" in project folder.
```javascript
const withCSS = require('@zeit/next-css')
module.exports = withCSS()
```
7. Use bootstrap grid system! https://getbootstrap.com/docs/4.1/layout/grid/ (tutorial: https://www.youtube.com/watch?v=ZFALVm8J-7M)
