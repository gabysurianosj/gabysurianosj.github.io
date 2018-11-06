---
layout: post
title:      "Things I wish I knew early on (JS)"
date:       2018-11-06 07:59:09 -0500
permalink:  things_i_wish_i_knew_early_on_js
---


Things you must know (I wish I knew from the very beginning) about JavaScript: 

1. Shortcut notations for objects and arrays: 

Do this: 
```
var car = {
  colour:'red',
  wheels:4,
  hubcaps:'spinning',
  age:4
}
```

and avoid this: 
```
var car = new Object();
car.colour = 'red';
car.wheels = 4;
car.hubcaps = 'spinning';
car.age = 4;
```

2. Avoiding looping and conditions: 

Do this:
```
var numbers = [3,342,23,22,124];
numbers.sort(function(a,b){return b - a});
alert(numbers[0]);
```

and avoid this:
```
var numbers = [3,342,23,22,124];
var max = 0;
for(var i=0;i<numbers.length;i++){
  if(numbers[i] > max){
    max = numbers[i];
  }
}
alert(max);
```

