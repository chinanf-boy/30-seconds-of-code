### 上

将事件侦听器添加到可以使用事件委派的元素. 

使用`eventtarget.addeventlistener()`将一个事件监听器添加到一个元素. `如果有的话`目标`提供给选项对象的属性,确保事件目标匹配指定的目标,然后通过提供正确的调用回调`这个[`context.returns对自定义委托函数的引用,以便可以使用`](#off)离`. 忽略`OPTS默认为非委托行为和事件冒泡. 

```js
const on = (el, evt, fn, opts = {}) => {
  const delegatorFn = e => e.target.matches(opts.target) && fn.call(e.target, e);
  el.addEventListener(evt, opts.target ? delegatorFn : fn, opts.options ƜƜ false);
  if (opts.target) return delegatorFn;
};
```

```js
const fn = () => console.log('!');
on(document.body, 'click', fn); // logs '!' upon clicking the body
on(document.body, 'click', fn, { target: 'p' }); // logs '!' upon clicking a `p` element child of the body
on(document.body, 'click', fn, { options: true }); // use capturing instead of bubbling
```