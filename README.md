# Testing particles with Pixijs and webpack.  

<img src="https://evofan.github.io/pixijs_particle_v5_webpack/pic_screenshot_spark.jpg" width="50%">  

**DEMO**  
[https://evofan.github.io/pixijs_particle_v5_webpack/dist/](https://evofan.github.io/pixijs_particle_v5_webpack/dist/)  

**USAGE**  
`npm install`  
`npm run build`  
`npm run start`  
http://localhost:8080/

reference  

**Advanced Game Design with HTML5 and JavaScript**  
[https://www.amazon.co.jp/Advanced-Game-Design-HTML5-JavaScript/dp/1430258004](https://www.amazon.co.jp/Advanced-Game-Design-HTML5-JavaScript/dp/1430258004)  
Customize "Chapter 8 Particle Effect" so that it can be used with pixijs.  

**javascript - How to skip over an element in .map()? - Stack Overflow**  
[https://stackoverflow.com/questions/24806772/how-to-skip-over-an-element-in-map](https://stackoverflow.com/questions/24806772/how-to-skip-over-an-element-in-map)  

**"Type specification method" and "Type of basic type" of TypeScript**  
[https://www.wakuwakubank.com/posts/499-typescript-type/](https://www.wakuwakubank.com/posts/499-typescript-type/)  
>array, array in array, object, object in array  

**TypeScript re-introduction-JavaScript is a "soft" statically typed language with "TypeScript that doesn't work hard"**    
[https://employment.en-japan.com/engineerhub/entry/2019/04/16/103000](https://employment.en-japan.com/engineerhub/entry/2019/04/16/103000)  
>Recommended settings of tsconfig.json  

for alert  
`ncu`  
`ncu -u`  
`npm install`  
if error  
`npm i -f`  

**webpack4, CopyWebpackPlugin, version up error**    
[https://tadtadya.com/webpack4-error-of-version-up-of-copywebpackplugin/](https://tadtadya.com/webpack4-error-of-version-up-of-copywebpackplugin/)   

```
-----------------------------------------------------------  
new CopyPlugin([{ from: "src/assets", to: "assets" }]) // error.
↓
new CopyPlugin({
  patterns: [
    {
      from: "src/assets", to: "assets" // use 'patterns' property, ok.
    }
  ]
})
-----------------------------------------------------------
```
"webpack": "^4.43.0", -> "webpack": "^4.44.2",  

for node-forge0.9.0 alert  
C:\Users\USER\Documents\pixijs_particle_v5_webpack`npm install -D node-forge`  
node-forge@0.10.0  
uninstall package-lock.json  
`npm install`  

**Webpack初心者がWebpack、Babelの設定でハマった点**  
[https://qiita.com/uwattotaitai/items/35ab2f248f53faa98fe3](https://qiita.com/uwattotaitai/items/35ab2f248f53faa98fe3)  
>２・webpack-cliが４以降だとwebpack-dev-serverの起動コマンドが違う
```
  "scripts": {
    "build": "webpack",
    "start": "webpack-dev-server",
↓
  "scripts": {
    "build": "webpack",
    "start": "webpack serve",
```

**Module '"../../webpack/types"' has no exported member 'Plugin'**  
[https://github.com/DefinitelyTyped/DefinitelyTyped/issues/49528](https://github.com/DefinitelyTyped/DefinitelyTyped/issues/49528)  
>import { Plugin } from 'webpack';  
>replaced with  
>import { WebpackPluginInstance as Plugin } from 'webpack';  

**npmでパッケージの特定のバージョンをインストールする**  
[https://qiita.com/448jp/items/58c5cbd5576c07177b8d](https://qiita.com/448jp/items/58c5cbd5576c07177b8d)  
>npm install -D pixi.js@5.3.9  

**webpackを4から5にアップデートしたら起きたこと。**  
[https://tadtadya.com/update-webpack-from-4-to-5/](https://tadtadya.com/update-webpack-from-4-to-5/)  
>webpack	4.44.2 -> 5.3.2, 5.4.0, 5.8.0  
>webpack-cli 3.3.12 -> 4.1.0, 4.2.0  

**バッチ（.bat）をダブルクリックで実行後、ウィンドウを閉じないようにする**  
[https://ameblo.jp/one-of-the-wnet/entry-10111695003.html](https://ameblo.jp/one-of-the-wnet/entry-10111695003.html)  
>最後のコマンドの前に  
`cmd /k`
>をつける。  

**npmてインストールされているパッケーシを、npm-check-updatesでまとめてアッフデートする方法 - NxWorld**  
[https://www.nxworld.net/npm-check-updates.html](https://www.nxworld.net/npm-check-updates.html)  
>特定のパッケージを除外  
`ncu -u -x xxx`

Pixi.jsのみアップデートしたくない場合
```
-----------------------------------------------------------  
[====================] 21/21 100%
Checking C:\Users\user\Documents\pixijs_particle_v5_webpack\package.json
 @babel/core          ^7.14.3  →  ^7.15.0
 @babel/preset-env    ^7.14.4  →  ^7.15.0
 copy-webpack-plugin   ^8.1.1  →   ^9.0.1
 html-webpack-plugin   ^5.3.1  →   ^5.3.2
 npm-check-updates    ^11.6.0  →  ^11.8.3
 pixi.js               ^5.3.9  →   ^6.1.0
 source-map-loader     ^1.1.3  →   ^3.0.0
 ts-loader             ^8.3.0  →   ^9.2.5
 typescript            ^4.3.2  →   ^4.3.5
 webpack              ^5.38.1  →  ^5.48.0
 webpack-cli           ^4.7.0  →   ^4.7.2
 ws                    ^7.4.6  →   ^8.0.0

Run ncu -u to upgrade package.json

C:\Users\user\Documents\pixijs_particle_v5_webpack>ncu -u -x pixi.js
Upgrading C:\Users\user\Documents\pixijs_particle_v5_webpack\package.json
[====================] 20/20 100%

 @babel/core          ^7.14.3  →  ^7.15.0
 @babel/preset-env    ^7.14.4  →  ^7.15.0
 copy-webpack-plugin   ^8.1.1  →   ^9.0.1
 html-webpack-plugin   ^5.3.1  →   ^5.3.2
 npm-check-updates    ^11.6.0  →  ^11.8.3
 source-map-loader     ^1.1.3  →   ^3.0.0
 ts-loader             ^8.3.0  →   ^9.2.5
 typescript            ^4.3.2  →   ^4.3.5
 webpack              ^5.38.1  →  ^5.48.0
 webpack-cli           ^4.7.0  →   ^4.7.2
 ws                    ^7.4.6  →   ^8.0.0

Run npm install to install new versions.
-----------------------------------------------------------
```
