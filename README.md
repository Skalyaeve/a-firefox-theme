# A firefox theme
![](https://github.com/Skalyaeve/images/blob/main/screenshot/firefox-theme.png)

## Install - Linux
- Download [the firefox theme](https://addons.mozilla.org/fr/firefox/addon/dark-pixels/)
- Firefox search bar -> type `about:config` -> accept
- `about:config` search bar -> type `toolkit.legacyUserProfileCustomizations.stylesheets` -> set to `true`
- Terminal -> run this:
```sh
git clone https://github.com/Skalyaeve/a-firefox-theme.git
cd a-firefox-theme
file=src/userChrome.css
dir=$(find $HOME/.mozilla -maxdepth 1 -type d -name *firefox*)
find $dir -type d -name *.default* | xargs -I {} mkdir -p {}/chrome
find $dir -type d -name *.default* | xargs -I {} mv {}/chrome/$file {}/chrome/$file.bak 2>/dev/null
find $dir -type d -name *.default* | xargs -I {} cp srcs/$file {}/chrome
cd .. && rm -rf a-firefox-theme
```

## How to install - Windows
- Uninstall Windows
- Install Linux
- Follow the Linux walkthrough
