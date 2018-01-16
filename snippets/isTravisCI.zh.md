### istravisci

检查当前的环境是否[travis ci](https://travis-ci.org/). 

检查当前环境是否有`特拉维斯`和`CI`环境变量 ([参考](https://docs.travis-ci.com/user/environment-variables/#Default-Environment-Variables)). 

```js
const isTravisCI = () => 'TRAVIS' in process.env && 'CI' in process.env;
```

```js
isTravisCI(); // true (if code is running on Travis CI)
```