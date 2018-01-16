### solverpn

解决了给定的数学表达式[反向波兰标记](https://en.wikipedia.org/wiki/Reverse_Polish_notation)如果有无法识别的符号或者表达错误,则会引发适当的错误. `有效的经营者是: `+`,`-`,`\*`,`/`,`^`,`\*\*`(`^`&`\*\*

是指数符号,是相同的). `这段代码不支持任何一元运算符. `使用字典,`运营商`指定每个运算符的匹配数学运算`与string.replace()`用正则表达式来替换`^`同`**`,`string.split()`标记字符串和`array.filter()`删除空的令牌`array.foreach()`解析每一个`符号`,将其评估为数字值或运算符,并解决数学表达式. 将数字值转换为浮点数并推送到`堆`,而运营商则使用该评估`运营商`字典和流行元素从堆应用操作. 

```js
const solveRPN = rpn => {
  const OPERATORS = {
    '*': (a, b) => a * b,
    '+': (a, b) => a + b,
    '-': (a, b) => a - b,
    '/': (a, b) => a / b,
    '**': (a, b) => a ** b
  };
  const [stack, solve] = [
    [],
    rpn
      .replace(/\^/g, '**')
      .split(/\s+/g)
      .filter(el => !/\s+/.test(el) && el !== '')
  ];
  solve.forEach(symbol => {
    if (!isNaN(parseFloat(symbol)) && isFinite(symbol)) {
      stack.push(symbol);
    } else if (Object.keys(OPERATORS).includes(symbol)) {
      const [a, b] = [stack.pop(), stack.pop()];
      stack.push(OPERATORS[symbol](parseFloat(b), parseFloat(a)));
    } else {
      throw `${symbol} is not a recognized symbol`;
    }
  });
  if (stack.length === 1) return stack.pop();
  else throw `${rpn} is not a proper RPN. Please check it and try again`;
};
```

```js
solveRPN('15 7 1 1 + - / 3 * 2 1 1 + + -'); // 5
solveRPN('2 3 ^'); // 8
```