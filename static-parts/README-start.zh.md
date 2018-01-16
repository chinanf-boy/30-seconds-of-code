![Logo](/logo.png)

# 30秒的代码

[![License](https://img.shields.io/badge/license-CC0--1.0-blue.svg)](https://github.com/Chalarangelo/30-seconds-of-code/blob/master/LICENSE) [![npm Downloads](https://img.shields.io/npm/dt/30-seconds-of-code.svg)](https://www.npmjs.com/package/30-seconds-of-code) [![npm Version](https://img.shields.io/npm/v/30-seconds-of-code.svg)](https://www.npmjs.com/package/30-seconds-of-code) [![Gitter chat](https://img.shields.io/badge/chat-on%20gitter-4FB999.svg)](https://gitter.im/30-seconds-of-code/Lobby) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![Travis Build](https://travis-ci.org/Chalarangelo/30-seconds-of-code.svg?branch=master)](https://travis-ci.org/Chalarangelo/30-seconds-of-code) [![Insight.io](https://img.shields.io/badge/insight.io-Ready-brightgreen.svg)](https://insight.io/github.com/Chalarangelo/30-seconds-of-code/tree/master/?source=0) [![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg)](https://github.com/Flet/semistandard) [![ProductHunt](https://img.shields.io/badge/producthunt-vote-orange.svg)](https://www.producthunt.com/posts/30-seconds-of-code)

> 策划收集有用的JavaScript片段,你可以在30秒或更少的时间内理解. 

-   使用<kbd>CTRL</kbd>+<kbd>F</kbd>要么<kbd>命令</kbd>+<kbd>F</kbd>搜索一个片段. 
-   捐款欢迎,请阅读[贡献指南](CONTRIBUTING.md). 
-   代码片段写在es6中,使用[babel翻译](https://babeljs.io/)以确保向后兼容. 
-   您可以将这些代码片段导入您选择的文本编辑器(vscode,atom,sublime)中,使用在[这个回购](https://github.com/Rob-Rychs/30-seconds-of-code-texteditorsnippets). 
-   你可以将这些片段导入到alfred 3中[这个文件](https://github.com/lslvxy/30-seconds-of-code-alfredsnippets). 

#### 包

⚠️**警告: **片段不是生产准备好的. 

你可以找到一个包含所有片段的包[NPM](https://www.npmjs.com/package/30-seconds-of-code). 

```bash
# With npm
npm install 30-seconds-of-code

# With yarn
yarn add 30-seconds-of-code
```

cdn链接

-   [es2017 full(umd)](https://unpkg.com/30-seconds-of-code)
-   [es5缩小(umd)](https://unpkg.com/30-seconds-of-code/dist/_30s.es5.min.js)

<details>

**浏览器**

> 重要的是: 更换`SRC`与完整版本链接和所需的目标规格(如es5缩小)): 

```html
<script src="https://unpkg.com/30-seconds-of-code"></script>
<script>
  _30s.average(1, 2, 3);
</script>
```

**节点**

```js
// CommonJS
const _30s = require('30-seconds-of-code');
_30s.average(1, 2, 3);

// ES Modules
import _30s from '30-seconds-of-code';
_30s.average(1, 2, 3);
```

直接导入片段: 

```js
// CommonJS
const { average } = require('30-seconds-of-code');
average(1, 2, 3);

// ES Modules
import { average } from '30-seconds-of-code';
average(1, 2, 3);
```

</details>

## 目录