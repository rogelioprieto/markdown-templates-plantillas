

# How to setup Markdown in SublimeText 3?

## Problem:
How to setup SublimeText to recognize Markdown syntax and preview the result.

## Solution:
Install two packages and setup a shortcut.

## Step by step

### 1. Install Package Control

Open SublimeText. Use one of the following methods to install Package Control:

**Option 1.** Using the Command Palette

Open the command palette.  
Win/Linux: ```ctrl+shift+p```, Mac: ```cmd+shift+p```  
Type ```Install Package Control```, press ```enter```


**Option 2.** Using Menu  
Open the ```Tools``` menu.  
Select ```Install Package Control…```

### 2. Install ```Markdown Editing``` package

Before of this, close all MarkDown flavored files you have open in Sublime 3, then restart. This will prevent an error: ```"error loading syntax file"```.

Win/Linux: ```ctrl+shift+p```, Mac: ```cmd+shift+p```  
Type ```Install Package Control```, press ```enter```  
Type ```markdown editing```, press ```enter```.

### 3. Install ```Markdown Preview``` package

Win/Linux: ```ctrl+shift+p```, Mac: ```cmd+shift+p```  
Type ```Install Package Control```, press ```enter```  
Type ```markdown preview```, press ```enter```.


### 4. Configure shortcut to "compile" (preview)

Edit your "Key Bindings - User" file by using the menu items: ```Preferences > Key Bindings - User``` (or use the Command Palette).

Add the following entry to your "Key Bindings - User" file. If you have other key bindings in your file, be sure there are commas between them.

```css
 { "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} }
```

(Optional) If you want to use control+b for the build command, instead of the MarkdownEditing bold command, add the following entry to your "Key Bindings - User" file. If you have other key bindings in your file, be sure there are commas between them.


```css
[
 { "keys": ["ctrl+b"], "command": "build" }
]
```
Save the key bindings file.


When working on a Markdown file, type ```alt+m``` to generate an HTML preview of your document that will open in your default browser. (You can also call the Markdown Preview command using the Command Palette. You hit ```control+shift+p``` to call up the Command Palette, then type "Preview", select "Markdown Preview: Python Markdown: Preview in Browser", and hit enter.)

### 6. Set keyboard shortcut for bold an italic font style.

Finally if you want to activate ```ctrl+b``` for **bold** and ```ctrl+i``` for _italic_ you can add:

```css
[
    // { "keys": ["ctrl+b"], "command": "build" },
     { "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} },

     { 
    "keys": ["ctrl+b"], 
    "command": "insert_snippet", 
    "args": {"contents": "**${0:$SELECTION}**"}
    },
    { 
    "keys": ["ctrl+i"], 
    "command": "insert_snippet",
    "args": {"contents": "_${0:$SELECTION}_"}
    }


]
```


### Source 1:

<http://plaintext-productivity.net/2-04-how-to-set-up-sublime-text-for-markdown-editing.html>

### Source 2:

<https://geekytheory.com/como-escribir-en-markdown-con-sublime-text>
