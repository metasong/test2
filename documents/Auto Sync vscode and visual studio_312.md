
# Auto Sync vscode and visual studio
---
author: Jason Song <metaseed@gmail.com>
version: 1.0.0
tag: []
enable: [toc]
---
## Goal
use vscode to edit, and visual studio to debug, resharper, build...
use <kbd>Alt</kbd>+<kbd>E</kbd> to auto swith between vscode and visualstudio, the document and the line:column is kept
## Extensions used
### vscode
in vscode install: [Open in Editor](https://marketplace.visualstudio.com/items?itemName=generalov.open-in-editor-vscode) and config the 
```
"alt-editor.name": "visualstudio" 
```
shortcut <kbd>Alt</kbd>+<kbd>E</kbd>

### visual studio
install [Open in Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.OpeninVisualStudioCode)
and set the shortcut: <kbd>Alt</kbd>+<kbd>E</kbd>

Turn on `Tools - Options - Projects and Solutions - General - Track Active Item In Solution Explorer`
