### 变复数

根据输入号码返回单数或复数形式的单词. `如果第一个参数是`目的`,它将通过返回一个函数来使用闭包,该函数可以自动复数不会简单地结束的单词`小号

如果提供的字典包含这个词. `如果`NUM`或者是`-1`要么`1`,返回单词的单数形式. `如果`NUM`是任何其他数字,返回复数形式. `省略第三个参数来使用单数字+的默认值`小号,或者在必要时提供定制的复数词. 如果第一个参数是目的,通过返回一个可以使用提供的字典来解析正确复数形式的单词的函数来利用闭包. 

```js
const pluralize = (val, word, plural = word + 's') => {
  const _pluralize = (num, word, plural = word + 's') =>
    [1, -1].includes(Number(num)) ? word : plural;
  if (typeof val === 'object') return (num, word) => _pluralize(num, word, val[word]);
  return _pluralize(val, word, plural);
};
```

```js
pluralize(0, 'apple'); // 'apples'
pluralize(1, 'apple'); // 'apple'
pluralize(2, 'apple'); // 'apples'
pluralize(2, 'person', 'people'); // 'people'

const PLURALS = {
  person: 'people',
  radius: 'radii'
};
const autoPluralize = pluralize(PLURALS);
autoPluralize(2, 'person'); // 'people'
```