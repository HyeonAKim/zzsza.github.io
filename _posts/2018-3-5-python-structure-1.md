---
layout: post
title:  "파이썬 자료형(1)"
subtitle: 변수유형,표현
categories: python
tags: structure
comments: true
---
- 에듀위드 파이썬을 활용한 기초컴퓨터 프로그래밍 강의를 바탕으로 정리한 내용입니다.


<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

* [1. 변수](#1-변수)
* [2. 변수의 유형 = 자료형(DataType)](#2-변수의-유형-자료형datatype)
	* [문자열 표현](#문자열-표현)
	* [문자열 저장](#문자열-저장)
	* [숫자 100 과 문자'100'의 차이](#숫자-100-과-문자100의-차이)
* [3. 수식의 표현](#3-수식의-표현)
	* [우선순위](#우선순위)
	* [변수 연산](#변수-연산)
* [4. 입력과 출력](#4-입력과-출력)
* [5. 정리](#5-정리)

<!-- /code_chunk_output -->

## 1. 변수

변수는 간단히 값을 넣을 수 있는 상자라고 표현한다. 모든 이에게 이름이 있듯이 각 상자(변수)에도 이름을 지어줘야 한다.

이름을 지어줄 때는 몇 가지 규칙이 있다.  
1) 영문,숫자,'_'로 구성된다.  
2) 공백을 포함할 수 없다.  
3) 숫자로 시작할 수 없다.  
4) 대문자와 소문자르 구분한다.  

반드시 지켜야할 규칙은 아니지만 암묵적 규칙이 하나 있다.
* 변수의 이름은 변수를 잘 설명할 수 있어야한다.

## 2. 변수의 유형 = 자료형(DataType)

마치 사람의 성격에 따라 외향적, 내향적으로 나뉘듯이   
변수도 값의 성격에 따라 숫자형, 문자형으로 나뉜다.
다른 말로 자료형(DataType)이라고 한다.

숫자형은 정수형, 실수형 ,복소수형이 포함된다.
문자형은 알파벳, 한글, 0~9 문자인 숫자, 기호 등이 포함된다.

### 문자열 표현
python에서 문자열을 정의할 때는 다음과 같은 방법으로 표현할 수 있다.

1) " " : 큰따옴표로 표현  
2) ' ' : 작은따옴표로 표현  
3) """ """ : 큰따옴표 3개로 표현  
4) ''' ''' : 작은따옴표 3개로 표현  

1번과 2번은 사실상 의미의 차이는 없다.
다음과 같이 문장내에 작은따옴표나 큰따옴표가 존재할 경우 구분을 위해 사용한다.
```
"hyun's house"
'she say "I want it"'
```

3번과 4번은 여러 문장일 경우에 사용한다.

### 문자열 저장
문자열은 메모리에 어떻게 저장될까?  
'100'을 입력할때 메모리 한자리마다 '1','0','0' 문자가 저장된다.  
그리고 각 문자에 순번이 부여된다.

name 이란 변수에 '박보검'을 넣고 순번을 확인해보자.
```python
name = '박보검'
name[0]
name[1]
name[2]
```
![스크린샷 2018-03-04 오후 9.50.49](https://i.imgur.com/sf0BvJv.png)

**순번은 0부터 시작하는 것을 기억하자**

박보검을 조금 더 다정하게 불러보자 :)
```python
name[1:3]
```
![스크린샷 2018-03-04 오후 9.55.12](https://i.imgur.com/uSdHzdq.png)
이를 범위 출력이라고 하는데 **[시작위치 : 끝위치 +1]** 이렇게 작성해야 한다.

### 숫자 100 과 문자'100'의 차이

숫자 100과 문자 100은 메모리에 다르게 저장된다.  
숫자 100일 경우는 하나의 메모리공간에 담긴다.   
반면 문자 100은 3개의 메모리공간에 담긴다.

![스크린샷 2018-03-04 오후 10.02.00](https://i.imgur.com/a9KUcoe.png)

## 3. 수식의 표현

### 우선순위
우리가 사칙연산을 할 때 덧셈 뺄셈 곱셈이 있을 경우 곱셈을 먼저 하듯이 python에서도 수식의 우선순위가 있다. 우선 순위는 다음과 같다.

1. () : 괄호
2. ** : 지수표현
3. +,- : 양수,음수
4. *,/,//,% : 곱셈,나눗셈, 몫, 나머지
5. +,- : 덧셈, 뺄셈

### 변수 연산

변수와 수와의 연산이 가능하다.
```python
x = 3
x = x + 10
```
![스크린샷 2018-03-04 오후 10.10.37](https://i.imgur.com/IFNuOmX.png)

동일한 연산을 다음과 같이 간단하게 표현이 가능하다.
```python
x = 3
x += 10
```
![스크린샷 2018-03-04 오후 10.13.20](https://i.imgur.com/sPhfE22.png)

변수가 문자열일때는 덧셈기호가 문자열 결합역할을 한다.

```python
name = '박보검'
say = '님 안녕하세요'
name+say
```
![스크린샷 2018-03-04 오후 10.18.00](https://i.imgur.com/BRtuvEc.png)


## 4. 입력과 출력
python 에서 입력과 출력은 매우 간단하다.
입력은 input, 출력은 print함수로 표현 할 수 있다.

```python
name = input('이름을 입력하세요:')
print(name+'님 안녕하세요')
```
![스크린샷 2018-03-04 오후 10.24.12](https://i.imgur.com/r89OWce.png)

input은 모든 입력을 문자열로 받기 때문에 연산 시 주의해야한다.
```python
eng = input('영어점수:')
math = input('수학점수:')
total = eng+math
print(total)
```
![스크린샷 2018-03-04 오후 10.27.11](https://i.imgur.com/irWI3KK.png)

제대로 된 연산을 하기 위해서 int 함수를 사용해서 문자열을 숫자형으로 바꿔야 한다.
```python
eng = int(input('영어점수:'))
math = int(input('수학점수:'))
total = eng+math
print(total)
```
![스크린샷 2018-03-04 오후 10.29.04](https://i.imgur.com/8Ixl6kh.png)

## 5. 정리
이번 장에서는 변수에 대한 간단한 개념과 변수유형을 알아보고 간단한 실습을 진행하였다.  
sql을 다룰때도 문자열과 숫자형이 저장되는 차이가 궁금했었는데, 메모리에 저장되는 방법이 다르다는 것을 알게되어서 속이 후련하다.  
덕분에 인덱싱을 할때 왜 숫자형인지 그리고 문자열로 검색하는 것보다 숫자형으로 검색할때 더 빠른 이유를 알 것 같다.
