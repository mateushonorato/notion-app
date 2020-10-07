# Notion for Linux

This is a meta repo that contains scripts / stuff needed to build Notion for Linux. 
The present fork is just a modification of [jaredallard/notion-app](https://github.com/jaredallard/notion-app) that uses the Windows release of Notion (instead of macOS), which is currently updated more frequently.

## Alternatives

If you're on Arch Linux, there is a package in the AUR called `notion-app`.

## How?

The electron sources are pulled out of the Mac OSX dmg and then ran with a Linux version of Electron, yeah, it's that easy.

## Customizing

Modify `config.sh` before running `build.sh` or `makepkg -si`

```bash
ELECTRON_VERSION=x.x.x electron version to use
NOTION_VERSION=x.x.x notion dmg to download
```

## Installing

Ensure you have the dependencies installed:

 * 7zip (p7zip-full on ubuntu)

Clone the repo, `cd` inside the folder and run `./build.sh`

## Recommendation

![](https://user-images.githubusercontent.com/16874139/93667628-c98cb100-faca-11ea-85e2-5fdca2a93a36.png)

This script is fully compatible with [notion-enhancer](https://github.com/dragonwocky/notion-enhancer). You can use it to get some awesome extra features, themes and also get rid of the awful white scrollbars in dark mode. If you already have Node installed, just run:

`npx notion-enhancer apply -y`

If you don't have Node installed, just search for installation instructions [here](https://nodejs.org/en/download/package-manager/) or go to [notion-enhancer](https://github.com/dragonwocky/notion-enhancer)'s repository for other installation methods.

## Uninstalling
 - Run `./uninstall.sh`

Or manually:
 - Delete the application `rm -rf /opt/notion`
 - Delete desktop entry `rm -r ~/.local/share/applications/Notion.desktop`
 - Delete `rm /usr/bin/notion`

## License

MIT
