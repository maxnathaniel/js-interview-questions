# js-interview-questions


## Functions

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

## Promises

Promise.resolve(1)
.then(data => 1 + 1)
.then(() => {throw new Error(10)})
.catch(err => 1 + 1)
.then(data => data * 2)
.then(console.log)
.catch(console.error);

function promisesTest() {

}

## Event Loop
function executionTest() {
  console.log('1');
  setTimeout(() => {
    console.log('2');
  }, 0);
  console.log('3');
}

executionTest();

## Closure


## Open Ended Questions
+ What is Lexical Scope?
+ What is `this` keyword?
+ When is the scope of a function created?
+ What is hoisting?
+ What is a closure?