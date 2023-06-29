
### custom-markdown
    Modify pagedown to support tables, strikethroughs, code blocks, etc.

### Usage

```
import Markdown from './Markdown';

const markdown = new Markdown.Converter()

let md = '_this_ is **easy** to `use`.';

let html = markdown.makeHtml(md)

console.log(html); 
// <em>this</em> is <strong>easy</strong> to <code>use</code>.
```

### Build

**方式1**

1. 安装  
```
    yarn add rollup --dev 
    npm install uglify-js -g 
``` 

2. 使用  
```
    yarn rollup Markdown.js --format cjs --file dist/Markdown_cjs.js
```

2. 压缩  
```
    uglifyjs dist/Markdown_cjs.js -m -o dist/Markdown.min.js
    
```


**方式2** 
1. 安装  
``` 
    // 全局安装 uglify
    npm install uglify-js -g 
    // 安装依赖
    yarn
``` 
2. build
```
    yarn build
```