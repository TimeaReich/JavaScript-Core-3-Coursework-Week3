# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
x on line 4 is defined inside the function, so in it not accessible outside of it. Console.log on line 7 does not 'see' inside the function so it logs 1.

## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
The console.log on line 33 will output 10, and the console.log on line 34 is undefined, because y is defined inside the function.

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.
The console.log on line 53 will print 9, because we are not calling the function, we are just returning the x that was defined on line 45, if we would console.log the function console.log(f2(y)) it would be x would be 10.

For the console.log on line 63, val is an object, val.x is 9 and than 10, when val is returned on line 59 it will print {x:10}.
