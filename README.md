# EME [![version](https://img.shields.io/github/release/egoist/eme.svg?style=flat-square)](https://github.com/egoist/eme/releases) [![downloads](https://img.shields.io/github/downloads/egoist/eme/total.svg?style=flat-square)](https://github.com/egoist/eme/releases) [![downloads latest](https://img.shields.io/github/downloads/egoist/eme/latest/total.svg?style=flat-square)](https://github.com/egoist/eme/releases/latest) [![build](https://github.com/egoist/eme/workflows/Build_Check/badge.svg)](https://circleci.com/gh/egoist/eme) [![donate](https://img.shields.io/badge/$-donate-ff69b4.svg?maxAge=2592000&style=flat-square)](#donate)

![preview](/media/preview.png)

## Download

You can manually download the latest release [here](https://github.com/egoist/eme/releases)

## Features

- It just suits, show editor or preview or both just as you wish.
- Focus mode, writing without distractions.
- Exportable, from Markdown to HTML/PDF... You name it.
- Supporting math typesetting, good for students and professionals.
- Auto-sync files to GitHub Gist after being saved, optional.

## WIKI

- [Key bindings](https://github.com/egoist/eme/wiki/Key-bindings)
- [...more](https://github.com/egoist/eme/wiki)

## Contribute

Pull requests are always welcome! Check out the [these issues](https://github.com/egoist/eme/issues?q=is%3Aissue+is%3Aopen+label%3A%22contribution+welcome%22) to get started fast.


1. [Fork](https://help.github.com/articles/fork-a-repo/) this repository to your own GitHub account and then [clone](https://help.github.com/articles/cloning-a-repository/) it to your local device
2. Install the dependencies: `yarn`
3. Build the code and watch for changes: `yarn watch`
4. In a new tab, start the application: `yarn start`

If you want to build the binary for a specified platform, run the command:

```bash
$ yarn mac    # .dmg
$ yarn win    # .exe
$ yarn linux  # .deb
```

After that, you'll see the binaries in the `./dist` folder!

## Donate

If you are enjoying this app, please consider making a donation to keep it alive, I will try my best to dedicate more time or even full time to work on it. 😉

- [Donate via Paypal](https://www.paypal.me/egoistian/10)
- [Donate via Wechat](http://ww4.sinaimg.cn/large/a15b4afegw1f72ib6rj67j20u00tvgnj.jpg)
- [Donate via Alipay](http://ww4.sinaimg.cn/large/a15b4afegw1f72ib54hybj20qo0nndh5.jpg)
- [Donate via Bitcoin](http://ww4.sinaimg.cn/large/a15b4afegw1f72icbcu0gj202s02sdfl.jpg) `1NUSDCWti9FBJLiUxaLY1zJnwcSDc5Tfci`

If you are not available for this, simply spreading the word for us would help too!

## License

MIT &copy; [EGOIST](https://github.com/egoist)

## New notes

### Install yarn

```
brew install yarn
```

### Build it on mac

```
yarn mac

yarn run v1.22.19
$ electron-builder --mac --config electron-builder.json
/bin/sh: electron-builder: command not found
```

```
yarn add electron-builder --dev

yarn add v1.22.19
[1/4] 🔍  Resolving packages...
warning electron-builder > app-builder-lib > electron-osx-sign@0.6.0: Please use @electron/osx-sign moving forward. Be aware the API is slightly different
warning electron-builder > app-builder-lib > @electron/universal > asar@3.2.0: Please use @electron/asar moving forward.  There is no API change, just a package name change
[2/4] 🚚  Fetching packages...
error app-builder-lib@23.6.0: The engine "node" is incompatible with this module. Expected version ">=14.0.0". Got "12.22.12"
error Found incompatible module.
info Visit https://yarnpkg.com/en/docs/cli/add for documentation about this command.
```

The local node version is too lower. And I found that the node was installed by `nvm`. So let's update it!

```
nvm install v14.0.0 --reinstall-packages-from=current
```
> If we try to upgrade the version of node too high, it may cause some new errors. So we just upgrade it to the minimum version.
