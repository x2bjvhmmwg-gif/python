
# Python 기초 총정리 (입문 ~ 핵심 문법)

> Python 실행 환경부터  
> 자료형, 비교, 연산, 제어문, 반복문, 함수, 자주 쓰는 코드까지 정리

---

## 목차

* [Python 개요](#python-overview)
* [실행 환경과 가상환경](#environment)
* [Jupyter Notebook](#jupyter)
* [자료형(DataType)](#datatype)
* [자료형 비교](#type-compare)
* [연산자](#operator)
* [조건문](#condition)
* [반복문](#loop)
* [함수(Function)](#function)
* [자주 쓰는 내장 함수](#builtin)
* [자료형별 주요 메서드](#methods)
* [입력과 형 변환](#input-casting)
* [에러와 예외 기초](#error)
* [주석과 코드 스타일](#style)
* [GitHub 업로드 팁](#github)

---

<a id="python-overview"></a>

## 1. Python 개요

Python은 **사람이 읽기 쉬운 문법**을 목표로 만들어진 언어이다.

* 인터프리터 언어  
  → 코드를 한 줄씩 바로 실행한다.
* 동적 타입 언어  
  → 변수 선언 시 자료형을 미리 정하지 않는다.
* 들여쓰기(indent)가 문법  
  → 중괄호 `{}` 대신 들여쓰기로 코드 블록을 구분한다.

```bash
python
exit()
````

---

<a id="environment"></a>

## 2. 실행 환경과 가상환경

가상환경은 **프로젝트마다 패키지를 독립적으로 관리**하기 위해 사용한다.

```bash
python -m venv venv
venv\Scripts\activate
deactivate
```

* `venv` 폴더 안에 해당 프로젝트 전용 Python 환경 생성
* 다른 프로젝트와 라이브러리 충돌 방지

---

<a id="jupyter"></a>

## 3. Jupyter Notebook

Jupyter Notebook은 **학습과 실습에 최적화된 환경**이다.

```bash
pip install jupyter
jupyter notebook
```

* 셀 단위로 코드 실행 가능
* 결과를 바로 확인 가능
* `.ipynb` 파일은 GitHub에서 바로 미리보기 가능

---

<a id="datatype"></a>

## 4. 자료형(DataType)

Python의 모든 값은 **자료형(Type)** 을 가진다.

### 숫자형

* `int` : 정수
* `float` : 실수
* `complex` : 복소수

```python
a = 10
b = 3.14
```

### 불리언(Boolean)

```python
True
False
```

* 반드시 대문자로 작성
* 조건문의 판단 기준으로 사용

### 시퀀스 타입

* `str` : 문자열
* `list` : 리스트 (변경 가능)
* `tuple` : 튜플 (변경 불가)

```python
text = "Hello"
arr = [1, 2, 3]
```

### 집합 / 딕셔너리

* `set` : 중복 없는 집합
* `dict` : key-value 구조

```python
user = {"name": "Kim", "age": 20}
```

### None

```python
a = None
```

* 값이 없음을 의미
* JavaScript의 `null` 과 유사

---

<a id="type-compare"></a>

## 5. 자료형 비교

```python
10 == 10.0                 # True
type(10) == type(10.0)     # False
```

* 값은 같지만 자료형은 다르다

```python
True == 1                  # True
type(True) == type(1)      # False
```

```python
None is None               # True
```

* `==` : 값 비교
* `is` : 객체(주소) 비교

---

<a id="operator"></a>

## 6. 연산자

### 산술 연산자

```python
+, -, *, /, %, **
```

* `/` : 나누기 (결과는 실수)
* `//` : 몫
* `%` : 나머지
* `**` : 거듭제곱

```python
5 ** 2   # 25
```

### 비교 연산자

```python
==, !=, <, >, <=, >=
```

### 논리 연산자

```python
and, or, not
```

```python
True or False   # True
not True        # False
```

---

<a id="condition"></a>

## 7. 조건문

조건에 따라 **실행 흐름을 나눈다**.

```python
if x > 0:
    print("양수")
elif x == 0:
    print("0")
else:
    print("음수")
```

### 한 줄 조건문

```python
if x > 0: print("양수")
```

* 코드가 짧을 때만 사용 권장

---

<a id="loop"></a>

## 8. 반복문

### for 문

```python
for i in [1, 2, 3, 4]:
    print(i)
```

* 리스트 안의 값이 하나씩 `i`에 들어간다

### range()

```python
for i in range(5):
    print(i)
```

* `range(시작, 끝, 증가)`

### Python에 `of`가 없는 이유

* Python은 `in` 하나로 모든 반복을 표현
* iterable(순회 가능한 객체)을 직접 순회

---

<a id="function"></a>

## 9. 함수(Function)

함수는 **코드를 묶어서 재사용**하기 위한 문법이다.

```python
def add(a, b):
    return a + b
```

```python
def hello(name="World"):
    print(name)
```

* `return`이 없으면 자동으로 `None` 반환

---

<a id="builtin"></a>

## 10. 자주 쓰는 내장 함수

```python
len()      # 길이
type()     # 자료형 확인
range()    # 반복 범위
print()    # 출력
input()    # 입력
```

```python
sum(), max(), min(), sorted()
```

---

<a id="methods"></a>

## 11. 자료형별 주요 메서드

### 문자열

```python
upper(), lower()
split(), replace()
```

### 리스트

```python
append(), remove()
pop(), sort()
```

### 딕셔너리

```python
keys(), values()
items(), get()
```

---

<a id="input-casting"></a>

## 12. 입력과 형 변환

```python
x = input("숫자 입력: ")
x = int(x)
```

* `input()`의 결과는 항상 문자열

```python
str(), int(), float(), bool()
```

---

<a id="error"></a>

## 13. 에러와 예외 기초

```python
"10" + 10        # TypeError
print(a)         # NameError
10 / 0           # ZeroDivisionError
```

* 에러 메시지를 읽는 습관이 매우 중요

---

<a id="style"></a>

## 14. 주석과 코드 스타일

```python
# 한 줄 주석
"""
여러 줄 주석
"""
```

* 변수명: snake_case
* 들여쓰기: 4칸
* 가독성을 최우선으로 작성

---

<a id="github"></a>

## 15. GitHub 업로드 팁

```gitignore
venv/
__pycache__/
```

* `.md` + `.ipynb` 함께 업로드 추천
* 학습 과정 커밋도 충분히 가치 있음




```
