
### Custom-Markdown


> Modify pagedown to support `tables`, `strikethroughs`, `code blocks`, etc.  
修改 [pagedown](https://github.com/ujifgc/pagedown) 添加table支持 添加删除线 以及代码块。

> 特性：极简(10k) 支持度较好 高度自定义

<br /> 

### Usage

```javascript
import Markdown from './Markdown';

const converter = new Markdown.Converter()

let md = '_this_ is **easy** to `use`.';

let html = converter.makeHtml(md)

console.log(html);
//<p><em>this</em> is <strong>easy</strong> to <code>use</code>.</p>


// Hooks 

converter.hooks.chain("preConversion", function (text) {
    // This is the string before conversion
    return text.replace(/\b(a\w*)/gi, "**$1**");
});

converter.hooks.chain("plainLinkText", function (url) {
    // This is the matching URL link
    return "This is a link to " + url.replace(/^https?:\/\//, "");
});

converter.hooks.chain("postConversion", function (html) {
    // This is the converted HTML string
    return html
});
 

/**
 * Other Hook :
 * 添加代码高亮支持
 * postCodeGamut
 * 
 * postNormalization
 * preBlockGamut
 * postBlockGamut
 * preSpanGamut
 * postSpanGamut 
 * /

```

<br /> 

### Build

```js
方式1 

    1. 安装  
        yarn add rollup --dev
        npm install uglify-js -g
     
    2. 使用  
        yarn rollup Markdown.js --format cjs --file dist/Markdown_cjs.js
    
    3. 压缩  
        uglifyjs dist/Markdown_cjs.js -m -o dist/Markdown.min.js

方式2

    1. 安装    
        npm install uglify-js -g  // 全局安装 uglify
        yarn // 安装依赖

    2. build  
        yarn build
 
```
<br /> 

### 支持情况

<br />

 
**标题** 
 
<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/biaoti.png" width="50%" />
 

**文本与分割线** 

<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/wenben.png" width="50%" />


**引用** 

<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/yinyong.png" width="50%" />
 

**图片**   

<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/tupian.png" width="50%" />


**列表** 

<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/liebiao.png" width="50%" />


**代码** 

<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/daima.png" width="50%" />


**高亮** 

<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/gaoliang.png" width="50%" />


**表格** 

<img src="https://raw.githubusercontent.com/forzys/custom-markdown/main/img/biaoge.png" width="50%" />

 
