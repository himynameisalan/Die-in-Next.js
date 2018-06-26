# Die-in-Next.js
# Chapter1: Create helloworld project
1. Create folder >> mkdir helloworld
2. Go to folder >> cd helloworld
3. Initial project info (user "-y" for default info) >> npm init -y
4. Install next.js package >> npm install --save react react-dom next
5. Modify project info, add "scripts" in package.json. 
    "scripts": {
      "dev": "next",
      "build": "next build",
      "start": "next start"
    }
6. Create folder "pages".
7. Create file "index.js in "pages".
8. Add codes in "index.js".
    export default () => <div>Welcome to next.js!</div>
9. Run project >> npm run dev
10. Preview project @ http://localhost:3000
