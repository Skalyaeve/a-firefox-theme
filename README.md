# A firefox theme

### Preview
![](https://github.com/Skalyaeve/a-firefox-theme/blob/main/preview.png)

### How to install (Linux)
- [Download](https://addons.mozilla.org/fr/firefox/addon/dark-pixels/) the firefox theme
- Firefox search bar -> type `about:config` -> accept
- `about:config` search bar -> type `toolkit.legacyUserProfileCustomizations.stylesheets` -> set `true`
- Terminal -> run this:
```sh
git clone https://github.com/Skalyaeve/a-firefox-theme.git
cd a-firefox-theme
file=userChrome.css
find ~/.mozilla/firefox/ -type d -name "*.default*" | xargs -I {} mkdir -p {}/chrome
find ~/.mozilla/firefox/ -type d -name "*.default*" | xargs -I {} mv {}/chrome/$file {}/chrome/$file.bak 2>/dev/null
find ~/.mozilla/firefox/ -type d -name "*.default*" | xargs -I {} cp srcs/$file {}/chrome
```

### How to install (Windows)
- Uninstall Windows
- Install Linux
- Follow the Linux walkthrough
