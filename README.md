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

## Using Visual Studio Code with Windows Subsystem for Linux
- `code .` in the directory you're working in (should have a `venv` folder)
- Confirm in lower-left corner that you're on the intended distro
- Under Extensions, install the Python extension and reload VSCode
- <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> to
  - select the Python interpreter
  - configure Python testing
  - run test discovery (can be toggled to on-save)
