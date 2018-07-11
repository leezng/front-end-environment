# front-end-environment

## Sublime 基础配置

进入 Preferences > Settings

```json
{
  "folder_exclude_patterns":
  [
    "node_modules",
    ".svn",
    ".git",
    ".hg",
    "CVS"
  ],
  "rulers":
  [
    80
  ],
  "tab_size": 2,
  "translate_tabs_to_spaces": true,
  "word_wrap": true
}
```

## Package Control

通过命令 ctrl+` 或点击 View > Show Console，进入Console界面，执行以下[命令](https://packagecontrol.io/installation)

```js
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

## Package Control 常用包

进入 Preferences > Package Settings  > Package Control > Settings-User

```json
{
  "bootstrapped": true,
  "in_process_packages":
  [
  ],
  "installed_packages":
  [
    "AlignTab",
    "AutoFileName",
    "BracketHighlighter",
    "ConvertToUTF8",
    "DocBlockr",
    "Emmet",
    "HTML-CSS-JS Prettify",
    "JS Snippets",
    "JSX",
    "LESS",
    "MarkdownEditing",
    "Nodejs",
    "Package Control",
    "SideBarEnhancements",
    "SublimeLinter",
    "SublimeLinter-csslint",
    "SublimeLinter-html-tidy",
    "SublimeLinter-jshint",
    "Trimmer",
    "URLEncode",
    "Vue Syntax Highlight"
  ]
}
```

## electron 安装卡死在node install.js

配置 `.npmrc`

```
registry=https://registry.npm.taobao.org
sass_binary_site=https://npm.taobao.org/mirrors/node-sass/
phantomjs_cdnurl=http://npm.taobao.org/mirrors/phantomjs
electron_mirror=http://npm.taobao.org/mirrors/electron/
```

配置 `.yarnrc`
```
registry "https://registry.npm.taobao.org"
sass_binary_site "https://npm.taobao.org/mirrors/node-sass/"
phantomjs_cdnurl "http://npm.taobao.org/mirrors/phantomjs"
electron_mirror "http://npm.taobao.org/mirrors/electron/"
```
