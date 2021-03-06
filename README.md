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
- [See](https://superuser.com/questions/1365258/how-to-change-the-dark-blue-in-wsl-to-something-brighter) dark blue.
-  `code .` in the directory you're working in
- Confirm in lower-left corner that you're on the intended distro
- Avoid using a folder mounted on /mnt/c/ as that can lead to lag
- Disable QuickEdit mode in Options to avoid having to hit <Enter> and having a suspended program
- In VSCode, turn off file polling for `.git` files which causes an 'Unable to write index file' error on Github desktop.
In Open Remote Settings >
```
"remote.WSL.fileWatcher.polling": true,
"files.watcherExclude": {
    "**/.git/**": true
}
```
- Update to WSL 2 by following these [instructions](https://docs.microsoft.com/en-us/windows/wsl/install-win10). If you cannot `sudo apt-get update`, these [tips](https://github.com/microsoft/WSL/issues/4285#issuecomment-522201021) will help.
- If the vim plugin messes with the built-in Ctrl+F search functionality, set `"vim.handleKeys": { "<C-f>": false }` in settings.


### Python
- Under Extensions, install the Python extension and reload VSCode
- <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> to
  - select the Python interpreter
  - configure Python testing
  - run test discovery (can be toggled to on-save)

### Rails
- Follow the official Rails guide. If you get an error during the `gem install rails` phase, this [post](https://stackoverflow.com/questions/37720892/you-dont-have-write-permissions-for-the-var-lib-gems-2-3-0-directory) helped, although I used a later version of Ruby (3.0.0).


