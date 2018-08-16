# Composing Software
*(.toc)*
## [Introduction](https://medium.com/javascript-scene/composing-software-an-introduction-27b72500d6ea)
> Composition: “The act of combining parts or elements to form a whole.” ~ Dictionary.com

`(f ∘ g)(x) = f(g(x))`
```js
const g = n => n + 1;
const f = n => n * 2;
const wait = time => new Promise(
  (resolve, reject) => setTimeout(
    resolve,
    time
  )
);
wait(300)
  .then(() => 20)
  .then(g)
  .then(f)
  .then(value => console.log(value)) // 42
;
```
> If you’re chaining, you’re composing.
```js
const trace = label => value => {
  console.log(`${ label }: ${ value }`);
  return value;
};

trace('your name:')('jason')
/*
your name: jason
*/
```
```js
// pipe(...fns: [...Function]) => x => y
const pipe = (...fns) => x => fns.reduce((y, f) => f(y), x);
```

