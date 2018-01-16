### memoize的

返回memoized(缓存)的功能. 

通过实例化一个新的创建一个空的缓存`地图`object.return函数,通过首先检查函数的输出是否已经被缓存,或者如果没有,则存储并返回. `该`功能`必须使用关键字才能让memoized函数拥有它`这个`上下文更改,如果必要. 允许访问`高速缓存通过将其设置为返回函数的属性. 

```js
const memoize = fn => {
  const cache = new Map();
  const cached = function(val) {
    return cache.has(val) ? cache.get(val) : cache.set(val, fn.call(this, val)) && cache.get(val);
  };
  cached.cache = cache;
  return cached;
};
```

```js
// See the `anagrams` snippet.
const anagramsCached = memoize(anagrams);
anagramsCached('javascript'); // takes a long time
anagramsCached('javascript'); // returns virtually instantly since it's now cached
console.log(anagramsCached.cache); // The cached anagrams map
```