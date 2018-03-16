# JS Setup
Instructions for JS development environment setup with VSCode and ESLint

## Install Node.js
Install latest version of Node.js with default settings (https://nodejs.org/en/download/). On Linux, you may need to add the node/bin folder to the path manually.

## Install Visual Studio Code
1. Download Visual Studio Code and install it with default settings (https://code.visualstudio.com/).
2. Zou can open a project folder inside Visual Studio Code by clicking File > "Open Folder..." or by right clicking on the folder in Windows Explorer and clicking "Open with Code".
3. Install ESLint extension for VSCode by selecting View > Extensions and typing it into the search field.
4. If terminal is not open in the bottom of the text editor pane, open it by selecting View > "Integrated Terminal" menu option (or ``CTRL + ` ``).
5. Install ESLint package for Node.js by typing `npm install -g eslint` to the terminal.
6. Optionally set up a key shortcut for linting. Select File > Preferences > "Keyboard Shortcuts" and search for `executeAutoFix` to set a keyboard shortcut for the linting (e.g. `CTRL+E D`).

## Choose a coding style
Two fairly popular ESLint preset are AirBnB and Standard-JS. Choose `Standard` for a more flexible, `AirBnB` for a very strict code style check.
1. Install
   - AirBnB: `npm install -g eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react`
   - Standard: `npm install -g eslint-config-standard eslint-plugin-import eslint-plugin-node eslint-plugin-promise`
2. Edit `.eslintrc` configuration
   - AirBnB: `{ "extends": "airbnb" }`
   - Standard: `{ "extends": "standard" }`
3. To allow global variables to be recognized, add one or more of the following to the config file:
```json
"env": {
    "browser": true,
    "node": true,
    "jasmine": true
},
```

For `AirBnB`, you can find a sample config in the `config` folder, which contains some basic rules to start with.
   
Note: you can edit each and every rule by adding it under the `rules` key in `.eslintrc` (sample file included in `config` folder).

## Usage
If ESLint extension is turned on, all `.js` files are automatically checked for errors when opened and during edition (you can turn this off in Settings). You may need to run the fix more than once to fix all issues (and some issues can only be fixed by hand).
