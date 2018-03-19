# js-interview-questions


## Functions
```
function f1() {
  const a = 10;
  f2();
}

function f2() {
  console.log(a + 10);
  return a + 10;
}

f1();

function f3() {
  const a = 10;
  return () => {
    console.log(a + 10);
    return a + 10;
  }
}

const f4 = f3();
f4();
```

## Promises

```
Promise.resolve(1)
.then(data => 1 + 1)
.then(() => {throw new Error(10)})
.catch(err => 1 + 1)
.then(data => data * 2)
.then(console.log)
.catch(console.error);

function promisesTest() {

}
```

## Event Loop

```
function executionTest() {
  console.log('1');
  setTimeout(() => {
    console.log('2');
  }, 0);
  console.log('3');
}

executionTest();
```

## Closure

## This

```
const obj = {
  a: 10,
  b: function() {
    return this.a;
  }
}

obj.b();

const funcA = obj.b;
funcA();

const obj = {
  a: 10,
  b: () => {
    return this.a;
  }
}

obj.b();

function funcB() {
  return this;
}

funcB();

obj.b = funcB;
obj.b();

```

## Open Ended Questions
+ What is Lexical Scope?
+ What is `this` keyword?
+ When is the scope of a function created?
+ https://stackoverflow.com/questions/7291734/javascript-scope-issue-variable-not-being-identified
+ What is hoisting?
+ What is a closure?
+ How does the event loop work?
+ https://stackoverflow.com/questions/19743354/does-javascript-event-queue-have-priority
+ https://stackoverflow.com/questions/43592229/promise-then-job-execution-order/43592450#43592450
+ https://stackoverflow.com/questions/7575589/how-does-javascript-handle-ajax-responses-in-the-background/7575649#7575649

