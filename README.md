
### Custom-Markdown


> Modify pagedown to support tables, strikethroughs, code blocks, etc.  
修改 [pagedown](https://github.com/ujifgc/pagedown) 添加table支持 添加删除线 以及代码块。

> 特性：极简(11k) 支持度较好 高度自定义

### Usage

```javascript
import Markdown from './Markdown';

const markdown = new Markdown.Converter()

let md = '_this_ is **easy** to `use`.';

let html = markdown.makeHtml(md)

console.log(html);
//<p><em>this</em> is <strong>easy</strong> to <code>use</code>.</p>
```

### Build

**方式1**

1. 安装  
```bash
    yarn add rollup --dev 
    npm install uglify-js -g 
``` 

2. 使用  
```bash
    yarn rollup Markdown.js --format cjs --file dist/Markdown_cjs.js
```

2. 压缩  
```bash
    uglifyjs dist/Markdown_cjs.js -m -o dist/Markdown.min.js
```


**方式2** 
1. 安装  
```bash
    // 全局安装 uglify
    npm install uglify-js -g 
    // 安装依赖
    yarn
```

2. build
```bash
    yarn build
```
