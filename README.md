# Install atom-config

```
$ git clone https://github.com/johnrlive/atom-config/
$ cd atom-config
$ bash install_packages.sh
```

# Key Mappings:

### Terminal Plus
```
terminal-plus:new =  `cmd-shift-t`
terminal-plus:toggle =  `ctrl-``
```

### Imdone Atom
```
Open Tasks Board =  `Alt+T`
Todays Journal =  `Alt+J`
```

# Packages:

### Theme Packages
[apm install seti-ui](https://atom.io/themes/seti-ui) - default ui-theme
[atom-material-syntax-dark](https://atom.io/packages/atom-material-syntax-dark) - default syntax theme

### System Packages
- [vim-mode-plus](https://atom.io/packages/vim-mode-plus) - vim-mode improved.
- [symbols-tree-view](https://atom.io/packages/symbols-tree-view) - just like taglist or tagbar for VIM.
- auto-detect-indentation
- highlight-selected
- emmet
- clipboard-plus
- quick-editor

****

### File settings
- file-icons
- advanced-open-file
- open-recent
- project-manager
- project-plus
- [Expose](https://atom.io/packages/expose/) - Quick tab overview of open files. Similar to Mac OSX Exposé / Mission Control, Firefox Tab Group, Safari and Chrome Tab Overview, etc.
- [tabs-to-spaces](https://atom.io/packages/tabs-to-spaces) - Provides the ability to convert between leading tabs and spaces in a document

****

### Productivity Packages
- [imdone-atom](https://atom.io/packages/imdone-atom) - A hackable task-board in your code.
- jumpy
- toggle-quotes

****

### Minimap Packages
- minimap
- minimap-autohide
- minimap-codeglance
- minimap-cursorline
- minimap-find-and-replace
- minimap-hide
- minimap-highlight-selected

****

### HTML Packages
- less-than-slash

****

### Color Packages
- pigments
- color-picker

****

### Django Package
- [atom-django](https://atom.io/packages/atom-django) - Build Django apps faster with Atom.

****

### Linter Packages
- linter - needed for linter packages to work
- linter-htmlhint - for HTML
- linter-jshint - for javascript
- linter-bootlint - for bootstrap
- linter-scss-lint - for scss
- linter-ansible-linting - for Ansible

****

### Python Packages
- atom-beautify

****

### Terminal Packages
- [terminal-plus](https://atom.io/packages/terminal-plus) - A terminal package, complete with themes and more.

****

### Misc. Packages
- rest-client

****

## Misc.
Further customisation for linter-flake8 & Python to follow PEP8

Here I’ll show you how you can configure Atom to follow PEP8, the official Python styling guide.

First, open the __Atom –> Preferences__ window.

1. Use spaces instead of tabs.

Scroll down the Settings panel until you see the Soft Tabs option. Make sure it’s checked. This setting will convert tabs into spaces automatically.

![alt text](http://www.marinamele.com/wp-content/uploads/2015/06/atom-settings-1024x950.png "Atom settings")

2. Set the tab length to 4 spaces

A little below the Soft Tab setting, you”ll see the __Tab Length__. Set it to __4__ spaces.

3. Automatic PEP8 validation.

If you installed the linter-flake8 package discussed in the previous section, you already have automatic PEP8 validation :-)

Keybindings customisation

In the same Preferences panel, you can see the Keybindings menu on the left. There, you’ll find a list of all the default keybindings active in your Atom editor.

However, by default, Atom confirms an autocomplete suggestion with both the Tab and Enter keys. But I only want to use the Tab key.

In order to disable Enter as an autocomplete confirm key, we need to go to the Keybindings menu where you’ll see a link that says your keymap file. Click on that link to open the __keymap.cson__ file.

There, you need to write:

# Disable Enter key for confirming an autocomplete suggestion
'atom-text-editor:not(mini).autocomplete-active':
  'enter': 'editor:newline'

# Disable Enter key for confirming an autocomplete suggestion
'atom-text-editor:not(mini).autocomplete-active':
  'enter': 'editor:newline'
Save the file and you’ll see the changes immediately. No need to restart Atom :-)
