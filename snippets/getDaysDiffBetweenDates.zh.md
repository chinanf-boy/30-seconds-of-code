### getdaysdiffbetweendates

返回两个日期之间的差异(以天计). 

计算两者之间的差异(以天计)`日期`对象. 

```js
const getDaysDiffBetweenDates = (dateInitial, dateFinal) =>
  (dateFinal - dateInitial) / (1000 * 3600 * 24);
```

```js
getDaysDiffBetweenDates(new Date('2017-12-13'), new Date('2017-12-22')); // 9
```