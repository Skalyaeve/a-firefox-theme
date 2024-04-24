# <p align="center">A theme for firefox</p>
![](https://github.com/Skalyaeve/images-1/blob/main/screenshot/firefox-theme.png)

## Install - Linux
- Download [the firefox theme](https://addons.mozilla.org/fr/firefox/addon/dark-pixels/)
- Firefox search bar -> type `about:config` -> accept
- `about:config` search bar -> type `toolkit.legacyUserProfileCustomizations.stylesheets` -> set to `true`
- Terminal ->
```sh
name=a-firefox-theme
git clone https://github.com/Skalyaeve/$name.git
file=userChrome.css
dir=$(find ~/.mozilla -maxdepth 1 -name "*firefox*")
find $dir -type d -name *.default* | xargs -I {} mkdir -p {}/chrome
find $dir -type d -name *.default* | xargs -I {} mv {}/chrome/$file {}/chrome/$file.bak 2>/dev/null
find $dir -type d -name *.default* | xargs -I {} cp $name/src/$file {}/chrome
rm -rf $name
```
> *Font [here](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/Terminus.zip)*

## Install - Windows
- Uninstall Windows
- Install Linux
- Follow the Linux walkthrough

