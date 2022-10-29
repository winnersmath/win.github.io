---
layout: post
current: post
cover: assets/built/images/javascript.png
navigation: True
title: javascript Study
date: 2022-10-29 11:00:00
tags: [javascript]
class: post-template
subclass: "post tag-javascript"
author: winners

---

Javascript
Chapter 27.배열

```python
const Queue=(function(){
function Queue(array=[]){
if(!Array.isArray(array)){
throw new TypeError(`${array} is not an array`);
}
this.array=array;
}
Queue.prototype={
constructor:Queue,
enqueue(value){
return this.array.push(value);
},
dequeue(){
return this.array.shift();
},
entries(){
return [...this.array];
}};
return Queue;
}());
const queue = new Queue([1,2,3]);
console.log(queue.entries());
queue.enqueue(3);
console.log(queue.entries());
queue.dequeue();
console.log(queue.entries());
```

큐를 클래스로 구현

```python
class Queue{
    #array;
    constructor(array=[]){
        if(!Array.isArray(array)){
            throw new TypeError(`${array} is not an array`);
        }
        this.#array=array;
    }
    enqueue(value){
        return this.#array.push(value);
    }
    dequeue(){
        return this.#array.shift();
    }
    entries(){
        return[...this.#array];
    }}
const queue=new Queue([1,2]);
console.log(queue.entries());
queue.enqueue(3);
console.log(queue.entries());
queue.dequeue();
console.log(queue.entries());
```

concat : 원본 배열은 변경되지 않는다.

push와 unshift 메서드는 concat 메서드로 대체할 수 있다.

차이점 : push와 unshift는 원본 배열을 변경하지만 concat은 원본 배열을 변경하지 않는다.
