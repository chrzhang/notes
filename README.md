## Make a GitHub Pages static website for a React project
- Have a React app in a **public** GitHub repo
  - In a pinch, use `create_react_app` to bootstrap a project
- In the app folder, `npm install gh-pages --save-dev`
- Add `"homepage": "http://<username>.github.io/<repo>"` as the first item in `package.json`
- Add the following to the `scripts` section in `package.json`
  - ```
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
    ```
- `npm run deploy`
