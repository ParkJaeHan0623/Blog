---
title: Javascript
author: ParkJaehan
date: 2024-08-22
category: Javascript
layout: post
---

# 01-Javascript 시작하기

```javascript

console.group("MyMessage1");    //출력하는 내용을 그룹으로 묶음
console.log("안녕하세요. Javascript1");
console.log("안녕하세요. Javascript2");
console.log("안녕하세요. Javascript3");
console.groupEnd(); //그룹으로 묶기 끝

console.group("MyMessage2");    //출력하는 내용을 그룹으로 묶음
console.log("안녕하세요. Javascript4");

console.group("My Message2-1"); //그룹안에 하위그룹 생성
console.log("안녕하세요. Javascript5");
console.log("안녕하세요. Javascript6");
console.groupEnd(); //하위 그룹으로 묶기 끝
console.groupEnd(); //그룹으로 묶기 끝

// 소스코드 실행    Ctrl + Alt + N
```
# 02-변수와 데이터 타입

### 전역변수

```javascript

// 1)변수의 선언과 할당

// 변수의 선언
var myNumber1;
// 할당
myNumber1=100;
console.log(myNumber1);

// 2) 변수의 선언과 할당 통합

var myNumber2 =100;
console.log(myNumber2);

// 3) 변수값 변경하기

// 한번 만들어진 변수는 다른 값으로 교체 가능

myNumber2=456;
console.log(myNumber2);

// 4) 변수의 재선언

// 원칙적으로 한번 선언한 변수는 재선언이 불가능함
// JS의 전역변수는 재선언이 가능
// 이는 일반적인 프로그래밍 언어의 규칙에 위배되므로 전역변수를 위한 'var'키워드의 사용은 권장되지 않음

var myNumber3 = 300;
console.log(myNumber3);
// 동일 변수 재선언
var myNumber3 = 456;
console.log(myNumber3);

```

### 지역변수

```javascript
// 1) 선언, 할당

// 선언
let myNumber1;
// 할당
myNumber1 = 100;
console.log(myNumber1);

// 2) 선언, 할당 통합

let myNumber2 = 200;
console.log(myNumber2);

// 중복 선언 금지(에러)
// let myNumber3 = 1;
// console.log(myNumber3);

// let myNumber3 = 10;
// console.log(myNumber3);
```

### 상수

```javascript

// 상수
const MY_VALUE1 = 123;
console.log(MY_VALUE1);

// const로 선언된 변수이므로 값을 변경할 수 없다(에러)
MY_VALUE1 = 1;
```
### 데이터타입
```javascript
```
### 형식문자
```javascript
```
### 변수출력
```javascript
```


# 03-연산자


# 04-프로그램 흐름제어

# 05-기본문법 활용

# 06-배열

### 배열 만들기

### 배열 원소접근

### 반복문 활용

### 원소의 총합,평균

### 최대값

### 역순 배치

### 정렬

> 선택정렬

```javascript
const data = [3, 5, 1, 4, 2];
console.log(data);

for(let i =0; i<data.length-1;i++){
    for(j=0; j<data.length-1-i;j++){
        if(data[j]>data[j+1]){
            const tmp = data[j];
            data[j]=data[j+1];
            data[j+1]=tmp;

            console.log("%d회차",i+1,data);    
        }
    }
}
console.log("결과:",data);
```

> 버블정렬

```javascript
const data = [3, 5, 1, 4, 2];
console.log(data);

for(let i =0; i<data.length-1;i++){
    for(j=0; j<data.length-1-i;j++){
        if(data[j]>data[j+1]){
            const tmp = data[j];
            data[j]=data[j+1];
            data[j+1]=tmp;

            console.log("%d회차",i+1,data);    
        }
    }
}
console.log("결과:",data);
```

### 2차배열

```javascript
const a =[1,2];
const b =[4,5,6,7];
const arr1= [a,b];
console.log(arr1);

const arr2 = [[1,2,3],[4,5,6,7]];
console.log(arr2);
console.log(arr2[0]);
console.log(arr2[1]);

console.log(arr2[0][0]);
console.log(arr2[0][1]);
console.log(arr2[1][0]);
console.log(arr2[1][1]);
console.log(arr2[1][2]);
console.log(arr2[1][3]);

// Array 클래스를 통한 2차 배열

const c = new Array(10,20,30);
const d = new Array(50,60,70);
const arr3 = new Array(c,d);
console.log(arr3);

const arr4 = new Array(new Array(10,20,30),new Array(50,60,70));
console.log(arr4);
```
> 2차배열 탐색

```javascript
const a =[1,2];
const b =[4,5,6,7];
const arr1= [a,b];
console.log(arr1);

const arr2 = [[1,2,3],[4,5,6,7]];
console.log(arr2);
console.log(arr2[0]);
console.log(arr2[1]);

console.log(arr2[0][0]);
console.log(arr2[0][1]);
console.log(arr2[1][0]);
console.log(arr2[1][1]);
console.log(arr2[1][2]);
console.log(arr2[1][3]);

// Array 클래스를 통한 2차 배열

const c = new Array(10,20,30);
const d = new Array(50,60,70);
const arr3 = new Array(c,d);
console.log(arr3);

const arr4 = new Array(new Array(10,20,30),new Array(50,60,70));
console.log(arr4);
```
> 가변배열

```javascript
const a = [1,3,5,7,9];
const b = [2,4,6];

const arr = [a,b];

console.log(arr);

for(let i = 0; i<arr.length; i++){
    console.log(arr[i]);
    for(let j =0; j<arr[i].length; j++){
        console.log(arr[i][j]);
    }
}
```

# 07-JSON
### 변수 그룹

```javascript
```