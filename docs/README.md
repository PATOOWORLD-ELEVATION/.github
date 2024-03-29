## Versions of `node-gyp` that are earlier than v9.x.x

Please look thru your error log for the string `gyp info using node-gyp@` and if that version number is less than the [current release of node-gyp](https://github.com/nodejs/node-gyp/releases) then __please upgrade__ using [these instructions](https://github.com/nodejs/node-gyp/blob/main/docs/Updating-npm-bundled-node-gyp.md) and then try your command again.

## `node-sass` is deprecated

Please be aware that the package [`node-sass` is deprecated](https://github.com/sass/node-sass#node-sass) so you should actively seek alternatives.  You can try:
```
npm uninstall node-sass
npm install sass --save
# or ...
npm install --global node-sass@latest
```
`node-sass` projects _may_ work by downgrading to Node.js v14 but [that release is end-of-life](https://github.com/nodejs/release#release-schedule).
But in any case, please avoid opening new `node-sass` issues on this repo because we [cannot help much](https://github.com/nodejs/node-gyp/issues?q=is%3Aissue+label%3A%22Node+Sass+--%3E+Dart+Sass%22+).

## Issues finding the installed Visual Studio

In cmd, [`npm config set msvs_version 20xx`](https://github.com/nodejs/node-gyp#on-windows) with ___xx___ matching your locally installed version of Visual Studio.
