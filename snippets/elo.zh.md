### ELO

计算两个或两个以上的对手之间使用的新的评级[Elo评级制度](https://en.wikipedia.org/wiki/Elo_rating_system). 

它需要一系列的预评级,并返回一个包含post-rating的数组. 阵列应该从最佳表演者到最差表演者(赢家 - >失败者). `使用指数`\*\*`运算符和数学运算符计算每个对手的期望分数(获胜的机会),并通过评级计算每个回合的新评级,使用每个排列来以成对方式计算每个玩家的后elo评级. `省略第二个参数来使用默认值K系数32. 

```js
const elo = ([...ratings], kFactor = 32, selfRating) => {
  const [a, b] = ratings;
  const expectedScore = (self, opponent) => 1 / (1 + 10 ** ((opponent - self) / 400));
  const newRating = (rating, i) =>
    (selfRating ƜƜ rating) + kFactor * (i - expectedScore(i ? a : b, i ? b : a));
  if (ratings.length === 2) {
    return [newRating(a, 1), newRating(b, 0)];
  } else {
    for (let i = 0; i < ratings.length; i++) {
      let j = i;
      while (j < ratings.length - 1) {
        [ratings[i], ratings[j + 1]] = elo([ratings[i], ratings[j + 1]], kFactor);
        j++;
      }
    }
  }
  return ratings;
};
```

```js
// Standard 1v1s
elo([1200, 1200]); // [1216, 1184]
elo([1200, 1200], 64); // [1232, 1168]
// 4 player FFA, all same rank
elo([1200, 1200, 1200, 1200]).map(Math.round); // [1246, 1215, 1185, 1154]
/*
For teams, each rating can adjusted based on own team's average rating vs.
average rating of opposing team, with the score being added to their
own individual rating by supplying it as the third argument.
*/
```