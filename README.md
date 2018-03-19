# js-interview-questions

## Introduction

To be a good frontend developer, being good at CSS is no longer sufficient. Gone are the days where you build static websites with jQuery and CSS. As of 2018, if you plan to be a good frontend developer and remain as one, you are expected to know at least 1 - 2 JavaScript Frameworks (Angular, React, Vue, Ember, Meteor, etc). But in the rush to pick up frameworks, many have lost sight of what it means to be a frontend/JavaScript developer. 

To be proficient at frontend developer, you will need to appreciate the ins and outs of JavaScript. Knowing how to componentize Angular or React components, what the React LifeCycles are, how to dispatch actions to reducers, are well and good. Take it a step further, and dive a little deeper. Start with understanding how the language works. 

Understanding how JavaScript works at the core will definitely be worth your time and energy. As frameworks come and go, what will keep you in demand and also enable you to create and build better software is the core skills and knowledge of JavaScript. 

Over the next few months, I plan to pen down the many quirks and problems that confuse frontend developers, and also hope to build up and strengthen my own understanding and grasp of the language.


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


## Async await

```
async function asyncFunc(num) {
  const result = promiseA();
  return result + num;
}

function promiseA() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(10);
    }, 1000);
  });
}

asyncFunc(10);

```
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
+ https://thomashunter.name/blog/the-javascript-event-loop-presentation/
+ Is `const` immutable?

