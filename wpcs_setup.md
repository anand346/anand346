### Prerequisites
- XAMPP installed
- PHP path set
- Composer installed
- Git installed


1.Open terminal in `D:/` drive and run 
```bash

git clone https://github.com/WordPress/WordPress-Coding-Standards WPCS

```

2. Go into WPCS
cd
```bash
cd WPCS
```

3. Install dependencies
```bash
composer install
```

4. Set path to Environment Variable of `D:\WPCS\vendor\bin`

5. Install VS Code extension `PHP Sniffer and Beautifier`

6. Open `Settings.json` by pressing `Ctrl+Shift+p`

7. Add these lines in the end of file
```bash
"phpsab.executablePathCBF": "D:\\WPCS\\vendor\\squizlabs\\php_codesniffer\\bin\\phpcbf.bat",
"phpsab.executablePathCS": "D:\\WPCS\\vendor\\squizlabs\\php_codesniffer\\bin\\phpcs.bat",
"phpsab.autoRulesetSearch": false,
"phpsab.standard": "WordPress",
"[php]": {
    "editor.defaultFormatter": "valeryanm.vscode-phpsab"
},
"files.eol": "\n",
```
8. Restart VS Code

9. Aditionally comment out these lines from `settings.json` if available

```
//   "editor.quickSuggestionsDelay": 1000,
//   "editor.hover.enabled": false,
//   "editor.accessibilitySupport": "off",
```

and add these lines

```

  "editor.linkedEditing": true,
  "editor.tabSize": 4,
  "editor.detectIndentation": false,
  "editor.formatOnSave": true,
  "window.title": "${activeEditorLong}${separator}${rootName}",

```

