# ES5

##### Array.property.slice.call(arguments, 0)

> 1. slice是一个函数；他的参数有两个，用来从一个数组中从新得到一个数组，而参数是开始截取的位置，和结束截取的位置。并且不会破坏原有的数组。

> 2. call(arguments, 0)中的arguments是Array.property.slice这个函数的运行环境，【因为slice没有加（）去立即调用自己，所以现在是一个未调用的函数】；

> 3. call()  方法接收两个参数：
    一个是在其中运行函数的 **作用域** ，另一个是 **参数数组**。其中，第二个参数可以是Array 的实例，也可以是arguments 对象.


```

    var s1 = {color: 'blue' };


    function changeColor(){
        console.log(this.color);
    }

    changeColor.call(s1);       //blue

```

> 4. call(arguments, 0) 中，第二个参数 0 是传给 slice 函数的参数，从头开始复制一遍类数组的第一个参数， 返回一个他们组成的 数组。