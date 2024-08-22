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

>## 전역변수

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

>## 지역변수

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

>## 상수

```javascript

// 상수
const MY_VALUE1 = 123;
console.log(MY_VALUE1);

// const로 선언된 변수이므로 값을 변경할 수 없다(에러)
MY_VALUE1 = 1;
```
>## 데이터타입

```javascript
// 1) 지금 바로 익혀야 하는 데이터 타입
// Number
let sampleValue1 = 123;
console.log(typeof sampleValue1);

// Boolean, 논리값(true,false만 표현가능)
let sampleValue2 = true;
console.log(typeof sampleValue2);

// 쌍,홑 따옴표로 감싼 경우 문자열로 인식
let sampleValue3 = "Hello World";
console.log(typeof sampleValue3);

// 2) 시간을 두고 천천히 익혀야 하는 데이터 타입
// 객체 (Object)
let sampleValue4 = new Date();
console.log(typeof sampleValue4);

// null - 비어있는 객체(Object)
let sampleValue5 = null;
console.log(typeof sampleValue5);

// 선언만 하고 값이 정의되지 않은 상태 (Undefined)
let sampleValue6;
console.log(typeof sampleValue6);
```

>## 형식문자

```javascript
const num = 123.45;
const str = "hello";
const bool = true;

const obj = new Date();
const arr = [1,2,3];
const json = {"a" :123, "b":234};

// 1) 숫자 표현을 위한 형식 문자
// 숫자 형식이 아닌 경우 정상적으로 표시되지 않는다

console.group("숫자값 출력하기");
console.log("숫자값 출력하기 = %d", num);
console.log("숫자값 출력하기 = %d", str);
console.log("숫자값 출력하기 = %d", true);
console.log("숫자값 출력하기 = %d", obj);
console.log("숫자값 출력하기 = %d", arr);
console.log("숫자값 출력하기 = %d", json);
console.groupEnd(); 

// 2)숫자 이외의 표현을 위한 형식 문자
// 문자열 뿐만 아니라 모든 형태의 데이터를 출력할 수 있다
console.group("문자열 출력하기");
console.log("문자열 출력하기 = %s",num);
console.log("문자열 출력하기 = %s",str);
console.log("문자열 출력하기 = %s",true);
console.log("문자열 출력하기 = %s",obj);
console.log("문자열 출력하기 = %s",arr);
console.log("문자열 출력하기 = %s",json);

// 3) 복합 사용
const student = "자바스크립트 학생";
const age = 20;
console.group("복합사용");
console.log("%s님의 나이는 %d세 입니다.",student, age);
console.groupEnd();

```

# 03-연산자

>## 산술연산자

```javascript
const a = 5;
const b = 3;
console.log(a + b);
console.log(a - b);
console.log(a - b);

const x = 5;
const y = 3;
const z = x + y -2;
console.log(z)

const myValue1 = 10;
const myValue2 = 4;
console.log(myValue1 / myValue2);

const myValue3 = 4;
const myValue4 = 3;
console.log(myValue3 / myValue4);

const myString1 = "Hello";
const myString2 = "World";
console.log(myString1 + myString2);

console.log("안녕하세요" + 123);
console.log("안녕하세요" + true);
console.log("안녕하세요" + null);

```


>## 대입연산자

```javascript
let myNumber1 = 123;
let myNumber2 = 234;
let myResult = myNumber1 + myNumber2;
console.log(myResult);

let myNumber3 = 1;
let myNumber4 = 2;

myNumber3 = 200;
myNumber4 = 300;
console.log(myNumber3);
console.log(myNumber4);

let selfValue = 300;
selfValue = selfValue +300;
console.log(selfValue);

```



>## 단항연산


```javascript

let x = 100;

x += 10;
console.log(x); //110

x -= 30;
console.log(x); //80

x *= 2;
console.log(x); //160

x /= 5;
console.log(x); //32

x %= 10;
console.log(x); //2

```


>## 증감연산자

```javascript

let selfPlus = 1;
console.log(selfPlus); //1

selfPlus++;
console.log(selfPlus); //2

++selfPlus;
console.log(selfPlus); //3

let prevValue = 1;

let prevResult = 100 + ++prevValue;

console.log(prevResult); //102
console.log(prevValue); //2

let nextValue = 1;

let nextResult = 100 + nextValue++;

console.log(nextResult); //101
console.log(nextValue); //2


```



# 04-프로그램 흐름제어
>## if

```javascript
// 1. 논리값을 사용한 경우
console.group("1.논리값을 사용한 경우");

console.log("배고픈데");

const have_money = true;

if (have_money){
    console.log("식당에서");
}
console.log("밥을 먹자");

console.groupEnd();

//2. 숫자형 값을 사용한 경우
console.group("2.숫자형 값을 사용한 경우");

const money1 = 10000;

if(money1){
    console.log("택시를 타고");
}

console.log("집에 가자");

console.groupEnd();

//3. 비교식을 사용한 조건문
console.group("3.비교식을 사용한 조건문");

const money2 = 12000;

if(money2 >= 5000){
    const k = money2 - 5000;
    console.log("선물을 사고 %d원 남는다",k);
}

console.groupEnd();

//4. 논리식을 사용한 조건문 (AND)
console.group("4.논리식을 사용한 조건문 (AND")
const x1 = true;
const y1 = true;

if (x1 && y1){
    console.log("x1 && y1 조건은 참입니다");
}

const x2 = true;
const y2 = false;

if (x2 && y2){
    // AND 연산은 하나라도 거짓이 포함되어 있다면 결과가 거짓이므로 아래의 조건문은 실행되지 않는다
    console.log("x2 && y2 조건은 참입니다"); 
}
console.groupEnd();

// 5.논리식을 사용한 조건문 (OR)
console.group("5.논리식을 사용한 조건문 (OR)")
const x3 = true;
const y3 = true;

if (x3 || y3){
    console.log("x3 || y3 조건은 참입니다");
}

const x4 = true;
const y4 = false;

if (x4 || y4){
    console.log("x4 || y4 조건은 참입니다");
}
console.groupEnd();

```

>## else if

```javascript

const point = 72;

if(point>90){
    console.log("A학점");
}
else if(point>80){
    console.log("B학점");
}
else if(point>70){
    console.log("C학점");
}
else if(point>60){
    console.log("D학점");
}
else {
    console.log("F학점");
}

```

>## switch

```javascript

// 1.Switch 기본 구문
console.group("1.Switch 기본 구문");
const 국어 = "B";

switch(국어){
    case 'A' :
        console.log("A학점입니다");
        break;
    case 'B' :
        console.log("B학점입니다");
        break;
    case 'C' :
        console.log("C학점입니다");
        break;
    default :
        console.log("C학점 미만입니다");
        break;
    }

console.groupEnd();
// 2. break가 없는 경우
console.group("2. break가 없는 경우 ");
const 영어 = "A";
switch(영어){
    case 'A' :
        console.log("A학점입니다");
        
    case 'B' :
        console.log("B학점입니다");
        
    case 'C' :
        console.log("C학점입니다");
        
    default :
        console.log("C학점 미만입니다");
        
    }
console.groupEnd();

// 3. 의도적으로 break 조절하기

console.group("3. 의도적으로 break 조절하기");

const 수학 = "B";

switch(수학){
    case 'A':
    case 'B':
    case 'C':
        console.log("이 과목을 Pass 했습니다.");
        break;
    default :
        console.log("이 과목을 Pass 하지 못했습니다.");
        break;
}
console.groupEnd();

//4. break의 조건을 식으로 설정하는 경우
console.group("4. break의 조건을 식으로 설정하는 경우");

const 과학 = 69;
switch(과학 >70){
    case true:
        console.log("이 과목을 Pass 했습니다.");
        break;
    case false:
        console.log("이 과목을 Pass 하지 못했습니다.");
        break;
}
console.groupEnd();

```

>## while

>>### 구구단

```javascript

let x=2;

while(x<10){
    let y=1;
    while(y<10){
        const z = x*y;
        console.log("%d X %d = %d",x,y,z);
        y++;
    }
    x++;
    console.log("");
}


```

>>### 합계 구하기

```javascript
let x = 0;
let i = 0;

while (i <= 10){
    x += i;
    console.log("i=%d,x=%d",i,x);
    i++;
}
console.log("1부터 10까지의 합: "+ x);

```

>>### 10증가

```javascript
let a =0;
while (a<100){
    console.log("a=%d",a);
    a+=10;
}

```

>>### 2감소

```javascript
let b = 10;
while(b>0){
    console.log("b=%d",b);
    b-=2;
}
console.log("b의 최종값=%d",b);

```

# 05-기본문법 활용

>## 변수의 스코프

```javascript
// 1. var 중복선언
if(false){
    var num1 = 100;
    console.log("블록 안: "+ num1);
}
console.log("블록 밖:" +num1);
// if문의 실행 여부에 따라 num1이 선언되므로 if 문의 실행여부에 num1의 식별가능 여부가 결정됨.
// num1을 식별하지 못할 경우 정의되지 않은 값 undefined가 된다


// 2. 조건문이 실행되는 경우
if(true){
    
    var num2 = 100;
    console.log("블록 안: "+num2);
}
console.log("블록 밖: "+ num2);


// 3. let 중복 선언
let num3 = 100;
if(true){
    // 블록 밖에서 생성된 변수를 블록 안에서 사용가능
    let num4= num3+ 100;
    console.log("블록 안 : "+num4);
}

console.log("블록 밖 : "+num4);
// let으로 선언된 변수는 if문의 실행 여부와 관계없이 블록을 빠져나올 수 없다.--> 프로그램 에러

// 4. for문의 초기식을 let으로 선언한 경우
for(let j=0; j<10; j++){
    console.log("반복문 안::: "+j);
}
console.log("반복문 밖::: "+j);
// for문의 초기식도 {}에 속한것으로 보기 떄문에 j값은 for블록을 빠져나올 수 없다.

// 5. 선언되지 않은 변수의 경우
// let 키워드는 반드시 선언->할당의 순서로만 사용가능함
x=100;
let x;
console.log(x);

```

>## if,if

```javascript
const point = 78;

if (point>=70){
    console.log('합격입니다');

    if(point>90){
        console.log("A");
    }
    else if(point>80){
        console.log("B");
    }
    else{
        console.log("C");
    }
}
else{
    console.log("불합격입니다.");
}

```

>## if,for

```javascript

const k = 5;

// k의 범위를 결정하는 조건문 -> k를 2~9사이로 제한함

if(k>1 && k<10){
    for(let i=1; i<10; i++){
        console.log("%d X %d = %d",k ,i ,k*i );
    }
}
    else{
        console.log("2~9사이의 수식만 출력합니다.");
    }


```

>## for,if

>>### 짝수,홀수의 합

```javascript

let a = 0;
let b = 0;

// i 가 1~10까지 1씩 증가하는 동안 반복
for(let i = 1; i<=10; i++){
    if(i%2 ==0){
        console.log("%d(은)는 짝수",i);
        a += i;
    }
    else{
        console.log("%d(은)는 홀수",i);
        b += i;
    }
}

console.log("1~10까지 짝수들의 합: %d",a);
console.log("1~10까지 홀수들의 합: %d",b);

```

>>### 공배수

```javascript

const x = 3;
const y = 5;

let sum = 0; //공배수의 총 합을 저장할 변수

for(let i=1;i<=100;i++){
    if(i%(x*y)==0){
        console.log(i);
        sum+=i;
    }
}

console.log("%d과 %d의 공배수의 총 합: %d",x,y,sum);

```

>>### 마지막 회차 생략

```javascript

console.group("변수 < 최대값")

for(let i = 1; i<10 ; i++){
    if( i+1 < 10){
        console.log(i);
    }
}
console.groupEnd();

console.group("변수 <= 최대값")

for(let i = 1; i<=9 ; i++){
    if( i<9){
        console.log(i);
    }
}
console.groupEnd();

console.groupEnd();

console.group("글자 사이에 콤마 넣기")

let str = "";
for(let i = 1; i<10 ; i++){
    str +=i;

    if(i+1 < 10){
        str += ",";
    }
}
console.log(str);
console.groupEnd();

```

>## for,for

```javascript

for(let i=0; i<3;i++){
    console.group("i에 대한 반복 수행 시작 >> i=%d",i);

    for(let j=0;j<2;j++){
        console.log("i=%d,j=%d",i,j);
    }
    console.groupEnd();
}

```

>>### 구구단

```javascript

for(let i=2;i<10;i++){
    console.group("%d단",i);
    for(let j=1;j<10;j++){
        console.log("%d X %d = %d",i,j,i*j);
    }
    console.groupEnd();
}

```

>>### 별찍기
1. 왼쪽 삼각형

```javascript

for(let i=0;i<7;i++){
    let str="";
    for(let j=0;j<i+1;j++){
        str+="*";
    }
    console.log(str);
}


```
2. 왼쪽 아래 삼각형

```javascript

for(let i=0;i<7;i++){
    let str="";
    for(let j=0;j<7-i;j++){
        str+="*";
    }
    console.log(str);
}

```
3. 오른쪽 삼각형

```javascript

for(let i=0;i<7;i++){
    let str="";
    let a="";
    for(let j=0;j<i+1;j++){
        str+="*";
        
    }
    for(let b=0;b<7-i;b++){
        a+=" "
    }
    console.log(a,str);
}

```


>## 연습문제
>>### 문제 1
##### for문을 사용하여 0부터 10미만의 정수 중에서 홀수만을 큰수부터 출력하시오.
  
  ```javascript
  for(let i=9;i>-1;i-=2){
    console.log(i);
}

  ```
  
>>### 문제 2
##### while문을 사용하여 0 부터 10 미만의 정수 중에서 홀수만을 큰수부터 출력하시오.

```javascript
let i= 9;
while(i>-1){
    console.log(i);
    i-=2;
}
```

>>### 문제 3
##### 1부터 20 미만의 정수 중에서 2 또는 3의 배수인 수의 총합을 구하시오

```javascript
let sum=0;
for(let i=1;i<20;i++){
    if(i%2===0||i%3===0){
        sum+=i;
 }
}
console.log(sum);
```

>>### 문제 4
##### 두 개의 주사위를 던졌을 때, 눈의 합이 6이 되는 모든 경우의 수를 출력하고 경우의 수는 총 몇가지 인지를 아래와 같이 출력하는 코드를 작성하시오.
 ```
 [ 1, 5 ]
 [ 2, 4 ]
 [ 3, 3 ]
 [ 4, 2 ]
 [ 5, 1 ]
경우의 수는 5개 입니다.
```

```javascript
let count =0;
for(let i=1;i<7;i++){
    for(let j=1;j<7;j++){
        if(i+j==6){
            console.log("[ %d, %d ]",i,j);
            count++;
        }
    }
}
console.log("경우의 수는 %d개 입니다.",count);
```


>>### 문제 5
##### for문을 중첩하여 실행하여 아래와 같은 출력 결과를 만드시오.
```
0 1 2 3 
1 2 3 4 
2 3 4 5 
3 4 5 6
```

```javascript

for(let i=0;i<4;i++){
    let str="";
    for(j=0;j<4;j++){
        str+=i+j;
        if(j+1 <4){
            str+=" ";
        }//공백 맨마지막 없애기
    }
    console.log(str);
}
```


>>### 문제 6
##### 아래와 같은 출력 결과가 나타나도록 중첩 반복문을 for 문 형식으로 구현하시오.
```
 1
 12
 123
 1234
 12345
 123456
 1234567
```

```javascript
for(let i=0;i<8;i++){
    let str="";
    for(let j=1;j<i+1;j++){
        str+=j;
    }
    console.log(str);
}
```


>>### 문제 7
#####  number라는 변수를 정의하고 1 혹은 2의 값을 임의로 할당하시오. 이 변수에는 1이나 2밖에 저장될 수 없습니다.구구단 프로그램을 만들고자 한다.전체를 출력하는 구구단이 아니라 number가 1일 때는 홀수 단(3, 5, 7, 9), number가 2일 때는 입력하면 짝수 단(2, 4, 6, 8)을 출력하는 프로그램을 완성하시오

- 풀이 1
   
```javascript
let number=1;
if(number==1){
    for(let i=2;i<10;i+=2){
        console.group("%d단",i);
        for(let j=1;j<10;j++){
            console.log("%d X %d = %d",i,j,i*j);
        }
        console.groupEnd();
    }

}
else if(number==2){
    for(let i=3;i<10;i+=2){
        console.group("%d단",i);
        for(let j=1;j<10;j++){
            console.log("%d X %d = %d",i,j,i*j);
        }
        console.groupEnd();
    }
}
else{
    console.log("1이나 2를 입력하세요");
}

```
   
- 풀이 2
   
```javascript
const number =1;
let start =number == 2?2:3;

for (let i =start; i<10; i+=2){
    for(let j=1; j<10;j++){
        console.log("%d X %d = %d",i,j,i*j);
    }
}
```
- 풀이 3

```javascript
const number = 1;

for(let i= 4-number; i<10; i+=2){
    for(let j=1; j<10; j++){
        console.log("%d X %d =%d",i,j,i*j);
    }
}
```   
   


# 06-배열

>## 배열 만들기

>## 배열 원소접근

>## 반복문 활용

>## 원소의 총합,평균

>## 최대값

>## 역순 배치

>## 정렬

>>### 선택정렬

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

>>### 버블정렬

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

>## 2차배열

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
>>### 2차배열 탐색

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
>>### 가변배열

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
>## 변수 그룹

```javascript

// 변수들의 그룹으로서의 JSON  정의

const student = {
    // key : value, key : value ....의 형식으로 나열
    // 숫자, boolean, null, undefined는 따옴표  적용 안함

    studno : 10101,
    grade : 1,
    name : "학생1",
    phoneno : "010-1234-5678"
}


// 1) 각 데이터 출력하기
// 데이터에 접근하는 기본적인 방법은 객체이름.하위정보이름 --> 90%이상의 경우에서 이 방식이 사용됨.

console.group("출력 type1");
console.log("학번: " + student.studno);
console.log("학년: " + student.grade);
console.log("이름: " + student.name);
console.log("연락처: " + student.phoneno);
console.groupEnd();

// JSON의 key 이름을 배열의 인덱스 처럼 활용

console.group("출력 type2");
console.log("학번: " + student['studno']);
console.log("학년: " + student['grade']);
console.log("이름: " + student['name']);
console.log("연락처: " + student['phoneno']);
console.groupEnd();

// 2) 접근하고자 하는 하위 변수의 이름을 동적으로 설정해야 할 경우 type2가 활용된다

const keyName = "phoneno";
console.log(student[keyName]);

// 3) JSON 데이터 탐색하기 (1)
// JSON의 key 를 배열로 반환하는 명령

const keys = Object.getOwnPropertyNames(student);
console.log(keys);

// 추출한 key 이름은 배열이므로 반복문 처리가 가능하다
for(const k of keys){
    console.group(k);
    // 추출된 key이름값(k)을 활용하여 실 데이터에 동적 접근이 가능하다.
    console.log(student[k]);
    console.groupEnd();
}

// 3) JSON 데이터 탐색하기 (2)
// JSON 객체의 key를 선언된 변수(k)에 순차적으로 할당하며 모든 key를 탐색한다
for(const k in student){
    console.group(k);
    console.log(student[k]);
    console.groupEnd();
}

```

>## 복합 자료 구조

```javascript

// 다양한 데이터 타입을 포함하는 복합 자료구조
const company = {
    name : "(주)굿모닝컴퍼니",
    since : 2024,
    department : ["기획팀","디자인팀","개발팀"]
};

// JSON 데이터에 접근하는 방법( 점으로 연결 또는 배열처럼 접근)-> 점을 통한 접근을 권장함

console.log(company.name)                        //점으로 연결
console.log(company['since']);                   //배열처럼 연결
console.log(company.department[0]);              //점으로 연결
console.log(company.department[1]);              //점으로 연결 
console.log(company['department'][2]);           //배열처럼 연결

```


>## 계층 구조

```javascript
// 1) 다른 JSON 객체를 value로 포함하는 경우

//단일  형태의 JSON
const centerPoint = {
    x: 5,
    y:10
};

const circle1 = {
    center: centerPoint,
    radius: 5.10
};

console.group("circle1");
console.log("원의 중심점: (%d,%d)",circle1.center.x, circle1.center.y);
console.log("원의 반지름: %d",circle1.radius);
console.groupEnd();

//2) 계층적으로 정의된 경우

const circle2 = {
    center:{
        x:5,y:10
    },
    radius:5.10
};
console.group("circle2");
console.log("원의 중심점: (%d,%d)",circle2.center.x, circle2.center.y);
console.log("원의 반지름: %d",circle2.radius);
console.groupEnd();

```

>## 목록 구조
>>### 1

```javascript

// 목록의 아이템으로 사용될 JSON 객체 정의하기
const student1 ={
    studno:10101,
    grade:1,
    name:'학생1'
};

const student2 ={
    studno:20202,
    grade:1,
    name:'학생2'
};

// 목록 구조를 갖는 JSON 객체
const classRoom = {
    student: [student1,student2]
};
console.log(classRoom);

// 배열의 기본 특성을 활용하여 반복문으로 접근할 수 있다.
for(let i=0;i<classRoom.student.length;i++){
    console.group(i + "번째 학생");
    console.log(" >> 학번: " + classRoom.student[i].studno);
    console.log(" >> 학년: " + classRoom.student[i].grade);
    console.log(" >> 이름: " + classRoom.student[i].name);
    console.groupEnd();
}

// for~of 문을 사용할 경우 몇번쨰 항목인지를 알기 위해서는 반복문 시작전에
// 별도의 초기식과 반복문 안에 별도의 증감식을 추가해야한다

let i = 0;
for(const s of classRoom.student){
    console.group(i + "번째 학생");
    console.log(" >> 학번: " + classRoom.student[i].studno);
    console.log(" >> 학년: " + classRoom.student[i].grade);
    console.log(" >> 이름: " + classRoom.student[i].name);
    console.groupEnd();
    i++; //증감식
}

```

>>### 2

```javascript

// 배열의 원소로서 JSON 구조를 직접 명시하기
const classRoom = {
    student:[{
        studno:10101,
        grade:1,
        name:'학생1'
    },{
        studno:20202,
        grade:2,
        name:'학생2'
    }]
};

for(let i=0;i<classRoom.student.length;i++){
    console.group(i + "번째 학생");
    console.log(" >> 학번: " + classRoom.student[i].studno);
    console.log(" >> 학년: " + classRoom.student[i].grade);
    console.log(" >> 이름: " + classRoom.student[i].name);
    console.groupEnd();
}

```

>>### 3

```javascript
// 가장 일반적인 형태의 목록 구조
// 목록을 구성하는 배열 외에 목록을 설명하기 위한 부가 정보도 함께 포함

const bbs = {
    title : "공지사항",
    count : 4,
    item : [
        {id: 1, subject: '첫 번째 게시물 제목'},
        {id: 2, subject: '두 번째 게시물 제목'},
        {id: 3, subject: '세 번째 게시물 제목'},
        {id: 4, subject: '네 번째 게시물 제목'},
    ]
};

console.log("게시판 이름 : " + bbs.title);
console.log("전체 게시물 수 : " + bbs.count);

// 일반 for문
console.group("일반 for 문");
for(let i =0; i<bbs.item.length; i++){
    console.log("[" + bbs.item[i].id + "]" + bbs.item[i].subject);
}
console.groupEnd();

//for~of 문
console.group("for~of 문");
for(let k of bbs.item){
    console.log("[" + k.id + "]" + k.subject);
}
console.groupEnd();

```



>## JSON 확장

```javascript
// 1) 존재하지 않는 key 를 사용하는 경우

const foo = {
    name : "자바스크립트",
    age : 19
};

// 존재하지 않는 값에 대한 출력 --> undefined
console.log(foo.email);

// 존재하지 않는 값을 활용한 연산 (age를 aga로 오타가 났다고 가정)
// undefined +1 --> 숫자가 아닌 결과값이 되므로 Not A Number를 의미하는 NAN이 출력됨

const nextAge = foo.aga +1;
console.log(nextAge);

// 2) 존재하지 않는 key에 대한 대입
foo.email = "hello@world.com"
console.log(foo);

// 3) 빈 객체 확장
const myJson = {};
console.log(myJson);

for(let i =0; i<10; i++){
    const key = "value" + i;
    myJson[key] = i * 100;
}
console.log(myJson);

```



>## 참조 복사

```javascript
// 값 복사 -> 일반 변수끼리의 복사
let a = 100;
let b = a;
console.log("a = " + a + ", " + "b = " + b);

a++;
// 일반 변수끼리 복사한 경우 원본이 변경되어도 복사본에는 영향이 없음
console.log("a = " + a + ", " + "b = " + b);

// 참조복사(얕은 복사)
// 배열,JSON, 객체 끼리의 복사는 참조처리가 된다
// 원본을 수정하면 복사본도 함께 수정된다(반대의 경우도 마찬가지)

const user = {
    name : "Lee"
};

const member = user;
console.log(user);
console.log(member);

member.name = "Kim"
console.log(user);
console.log(member);



// 값 복사(깊은 복사)

const a1 = [1,2,3];
const a2 = new Array(a1.length);

// 배열을 온전히 값 복사하기 위해서는 원소끼리 개별복사 해야함
for(let i =0; i<a1.length;i++){
    a2[i] = a1[i];
}

// 배열 객체가 갖는 메서드를 활용한 깊은 복사 방법 --> const 새로운 변수 = 원본배열.slice();
const a3 = a1.slice();

console.log(a1);
console.log(a2);
console.log(a3);

a1[0] += 100;

console.log(a1);
console.log(a2);
console.log(a3);

// JSON의 깊은 복사

const addr = {
    city : '서울',
    gu : '서초'
};

// 깊은 복사를 수행할 빈 JSON 객체를 생성

const copy = {};

for(let key in addr){
    copy [key] = addr [key];
}

console.log(addr);
console.log(copy);

addr.gu = '강남';

console.log(addr);
console.log(copy);

// JS 가 제공하는 기능 활용하기
const copy2 = {};

Object.assign(copy2,addr);
console.log(copy2);

```


>## 구조 분해

```javascript

const object = {a:1,b:2,c:3};
const {a,b,c} = object;

// JSON에서 필요한 값만 추출하여 새로운 상수로 만들어줌
// -->object 에는 {}에 명시된 항목과 동일한 key를 갖는 데이터가 존재해야함
console.log(a);
console.log(b);
console.log(c);

// 구조분해를 활용하여 기존 데이터와 추가적인 값을 병합한 새로운 객체 생성
// --> '...'뒤에 오는 변수명은 반드시 원본 객체 이름이어야한다

const origin = {name: 'javascript',age: 25};
const newdata1 = {...origin,gender:'M'};
console.log(newdata1);

// 구조분해를 통한 새로운 데이터 생성시 원본과 동일한 이름의 속성이 있다면 원본 데이터를 수정한다.

const newdata2 = {...origin, age:30, gender:'F'};
console.log(newdata2);

```


>## 옵셔널 체이닝

```javascript

// ES5에서 존재하지 않는 key 혹은 멤버변수에 접근하는 경우
const user ={};

// user 안에 address가 정의되지 않았으므로 undefined
// console.log(user.address);

// address 자체가 정의되지 않은 상태에서 하위 기능에 접근하므로 에러
// console.log(user.address.city);

// ES5의 해결책 --> 단계별로 객체가 존재하는지 검사
// console.log(user && user.address && user.address.city);

// "객체이름?"은 해당 객체가 undefined나 null이면 평가를 중지하고 undefined를 반환한다

console.log(user?.address?.city);

console.log("프로그램 종료");
```
- JS에 추가된지 얼마 되지 않는 문법이므로 IE는 지원하지 않음
- 옵셔널 체이닝은 존재하지 않아도 괜찮은 대상에게만 사용하고 반드시 존재해야하는 개체에게는 if 문으로 존재 여부를 검사하는 유효성 검사를 수행하는것이 좋다.



# 08-함수

>## 함수의 사용

```javascript
function sayHello(){
    console.log("Hello JavaScript");
    console.log("안녕하세요 자바스크립트");
}

sayHello();

for( let i = 0; i<5; i++){
    sayHello();
}

```

>## 파라미터

```javascript
function f(x) {
    let y = x +1;
    console.log(y);
}
f(100);
f(50);
f(10);

```

>>### 다중 파라미터

```javascript
function sum(x,y,z){
    let result = x + y + z;
    console.log(result);
}

sum(1,2,3);
sum(500,100,200);
```

>>### 파라미터 생략

```javascript
function foo(x,y){
    console.log("x=" + x + ",y=" + y);

    let result = 0;
    if(x != undefined){result +=x;}
    if(y != undefined){result +=y;}

    console.log("result=" + result);

}

foo(100,200);
foo(500);
foo();

```


>>### 파라미터 기본값

```javascript
function bar(x=1,y=2){
    console.log("x=" + x + ",y=" + y);
    let result = x + y;
    console.log("result=" + result);
}

bar(100,200);
bar(500);
bar();

```

>## 리턴

```javascript
function getTimes(x,y){
    const z = x*y;
    return z;
}

const a = getTimes(123,45);
console.log(a);

const b = getTimes(123,45) +10000;
console.log(b);

console.log(getTimes(100,20));
```

>## 실행 중단

```javascript
function doLogin(userId,userPw){
    if(!userId){
        return "아이디를 입력하세요";
    }
    if(!userPw){
        return "비밀번호를 입력하세요";
    }
    return "로그인"
}

console.log(doLogin("",""));
console.log(doLogin("hello",""));
console.log(doLogin("hello","world"));
```
