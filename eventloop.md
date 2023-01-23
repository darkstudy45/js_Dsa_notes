# Event loop

what are you js ? 

ans: A single-thereaded non-blocking asynchronous concurrent languge.I have a call stack an event loop a callback queue some other apis and stuff. 

**I have :**

- Call stack 

- Heap 



js v8 engine have **heap & stack**

webapis have **dom ,ajax, settimeout .**



## The call stack

**one thread == one call stack == one thing at a time .**

```js
function multiply(a,b){
    return a*b;

}
function square(n){
    return multiply(n,n)
}
function printsquare(n){
    var squared = square(n)
    console.log(squared)
}

printsquare(4);
```

The stack will look like this : 

<img src="file:///home/oem/.config/marktext/images/2023-01-23-13-52-13-image.png" title="" alt="" width="566">





In stack which called last will be exucuted first 

**Rule of thumb: who come last go first.**

The borowser the error is shown like call stack . 







another code 

```js
function foo(){
    return foo();
}
foo()
```

The call stack will look like this. 

![](/home/oem/.config/marktext/images/2023-01-23-13-55-18-image.png)

**ultimately there will be an error of maximum call stack size exceeded.**







## blocking .

**what happens when things are slow .**



synchronous code is code that is executed in a blocking manner. This means that the program will wait for the current piece of synchronous code to complete before moving on to the next piece of code.





## blocking code solution *Asynchronus*







```js
console.log("Hi");
setTimeout(fucntion,)
```





![](/home/oem/.config/marktext/images/2023-01-23-15-23-39-ezgif.com-gif-maker.gif)
