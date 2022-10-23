---
layout: post
current: post
cover: assets/built/images/javascript.png
navigation: True
title: javascript Study
date: 2022-10-11 15:00:00
tags: [javascript]
class: post-template
subclass: "post tag-javascript"
author: winners
---

Regular Expression (RegExp)  
문자열 함수 exec(), text(), match(), matchAll(), search(), replace(), replaceAll(), split() 등을 사용할 때, 대상으로 하는 문자의 종류가 많을 때 이를 포괄적으로 표현하기 위한 방법이다.  
기본적으로 선언하는 방법은 두 가지다.

const re = /ab+c/g;  
const re = new RegExp('ab+c','g');

후자는 RegExp라는 JS 기본 내장 클래스를 사용하는 방법이다.  
지정해야 하는 특정 문자를 변수를 통해 받아오는 경우에는 이 방법을 사용한다.  
첫번째 매개변수는 지정하는 문자 혹은 범위를, 두번째 매개변수는 지정한 범위로 검색할 때 부여할 조건/속성이다.  
먼저 문자의 종류를 구분하는 방법이다.

[abc] / [a-c] : 대괄호 안의 범위만큼의 문자만

[^abc] / [^a-c] : 대괄호 안의 범위만큼의 문자를 제외

\d / \D : 0~9의 모든 숫자. 대문자로 쓸 경우 숫자를 제외한 모든 문자

\w / \W : 모든 숫자와 알파벳 대소문자. 대문자로 쓸 경우 이를 제외한 문자

\s / \S : 모든 종류의 공백. space, tab, form feed, line feed, etc.

a|b : a 혹은 b

- 나머지는 Character classes 참고
