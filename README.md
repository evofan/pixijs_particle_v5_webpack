# Testing particles with Pixijs and webpack.  

![https://raw.githubusercontent.com/evofan/pixijs_particle_v5_webpack/master/pic_screenshot_spark.jpg](https://raw.githubusercontent.com/evofan/pixijs_particle_v5_webpack/master/pic_screenshot_spark.jpg "image")  

**DEMO**  
[https://evofan.github.io/pixijs_particle_v5_webpack/dist/](https://evofan.github.io/pixijs_particle_v5_webpack/dist/)  

reference  

**Advanced Game Design with HTML5 and JavaScript**  
[https://www.amazon.co.jp/Advanced-Game-Design-HTML5-JavaScript/dp/1430258004](https://www.amazon.co.jp/Advanced-Game-Design-HTML5-JavaScript/dp/1430258004)  
Customize "Chapter 8 Particle Effect" so that it can be used with pixijs.  

**javascript - How to skip over an element in .map()? - Stack Overflow**  
[https://stackoverflow.com/questions/24806772/how-to-skip-over-an-element-in-map](https://stackoverflow.com/questions/24806772/how-to-skip-over-an-element-in-map)  

**「型指定の方法」と「基本型の種類」**  
"Type specification method" and "Type of basic type" of TypeScript  
[https://www.wakuwakubank.com/posts/499-typescript-type/](https://www.wakuwakubank.com/posts/499-typescript-type/)  
>array, array in array, object, object in array  

**TypeScript再入門 ― 「がんばらないTypeScript」で、JavaScriptを“柔らかい”静的型付き言語に**  
TypeScript re-introduction-JavaScript is a "soft" statically typed language with "TypeScript that doesn't work hard"  
[https://employment.en-japan.com/engineerhub/entry/2019/04/16/103000](https://employment.en-japan.com/engineerhub/entry/2019/04/16/103000)  
>Recommended settings of tsconfig.json  

**警告対処**  
> ncu  
> ncu -u  
> npm install  
errorが出た場合は  
> npm i -f  

**2020.9.18修正**  
webpack4, CopyWebpackPluginのバージョンアップでエラー  
[https://tadtadya.com/webpack4-error-of-version-up-of-copywebpackplugin/](https://tadtadya.com/webpack4-error-of-version-up-of-copywebpackplugin/)  
>webpackおなじみの、バージョンアップのオプション変更でエラーが出ました。  

↑を参考に修正  
```
-----------------------------------------------------------  
new CopyPlugin([{ from: "src/assets", to: "assets" }]) // ここがbuild時にエラー
↓
new CopyPlugin({
  patterns: [
    {
      from: "src/assets", to: "assets" // patternsプロパティの中に入れればok
    }
  ]
})
-----------------------------------------------------------
```
    
エラー前のver.  
"webpack": "^4.43.0",  
↓  
エラー出て修正した時のver.  
"webpack": "^4.44.2",  

node-forgeの0.9.0警告はncuで上がらなかったので直接インストール  
C:\Users\USER\Documents\pixijs_particle_v5_webpack`npm install -D node-forge`  
node-forge@0.10.0  
package-lock.jsonを一度消して  
`npm install`  
