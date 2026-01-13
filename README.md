
---



---


---

# Python 기초 총정리 (입문 ~ 핵심 문법)

> Python 실행 환경부터
> 자료형, 비교, 연산, 제어문, 반복문, 함수, 자주 쓰는 코드까지 정리

---

## 📑 목차

1. [Python 개요](#1-python-개요)
2. [실행 환경 & 가상환경](#2-실행-환경--가상환경)
3. [Jupyter Notebook](#3-jupyter-notebook)
4. [자료형(DataType)](#4-자료형datatype)
5. [자료형 비교](#5-자료형-비교)
6. [연산자](#6-연산자)
7. [조건문](#7-조건문)
8. [반복문](#8-반복문)
9. [함수(Function)](#9-함수function)
10. [자주 쓰는 내장 함수](#10-자주-쓰는-내장-함수)
11. [자료형별 주요 메서드](#11-자료형별-주요-메서드)
12. [입력과 형 변환](#12-입력과-형-변환)
13. [에러와 예외 기초](#13-에러와-예외-기초)
14. [주석과 코드 스타일](#14-주석과-코드-스타일)
15. [GitHub 업로드 팁](#15-github-업로드-팁)

---

## 1️⃣ Python 개요

* 인터프리터 언어 (한 줄씩 실행)
* 동적 타입 언어
* 들여쓰기(indent)가 문법

```bash
python
exit()
```

---

## 2️⃣ 실행 환경 & 가상환경

```bash
python -m venv venv
venv\Scripts\activate
deactivate
```

* 프로젝트별 독립 환경 관리

---

## 3️⃣ Jupyter Notebook

```bash
pip install jupyter
jupyter notebook
```

* 셀 단위 실행
* `.ipynb` → GitHub 미리보기 가능
* 종료: `Ctrl + C`

---

## 4️⃣ 자료형(DataType)

### 숫자형

```python
int, float, complex
```

### 불리언

```python
True, False
```

### 시퀀스

```python
str, list, tuple
```

### 집합 / 딕셔너리

```python
set, dict
```

### None

```python
None
```

---

## 5️⃣ 자료형 비교

```python
10 == 10.0          # True
type(10) == type(10.0)  # False
```

```python
True == 1           # True
type(True) == type(1)   # False
```

```python
None is None        # True
```

* `==` : 값 비교
* `is` : 객체 비교

---

## 6️⃣ 연산자

### 산술

```python
+, -, *, /, %, **
```

### 비교

```python
==, !=, <, >, <=, >=
```

### 논리

```python
and, or, not
```

---

## 7️⃣ 조건문

```python
if x > 0:
    print("양수")
elif x == 0:
    print("0")
else:
    print("음수")
```

```python
if x > 0: print("양수")
```

---

## 8️⃣ 반복문

```python
for i in [1, 2, 3]:
    print(i)
```

```python
for i in range(5):
    print(i)
```

* Python에는 `of` 없음
* iterable을 직접 순회

---

## 9️⃣ 함수(Function)

```python
def add(a, b):
    return a + b
```

```python
def hello(name="World"):
    print(name)
```

* return 없으면 `None`

---

## 10️⃣ 자주 쓰는 내장 함수

```python
len()
type()
range()
print()
input()
sum()
max()
min()
sorted()
```

```python
len([1,2,3])      # 3
sorted([3,1,2])   # [1,2,3]
```

---

## 11️⃣ 자료형별 주요 메서드

### 문자열

```python
upper(), lower(), split(), replace()
```

### 리스트

```python
append(), remove(), pop(), sort()
```

### 딕셔너리

```python
keys(), values(), items(), get()
```

---

## 12️⃣ 입력과 형 변환

```python
x = input("숫자 입력: ")
x = int(x)
```

```python
str(), int(), float(), bool()
```

---

## 13️⃣ 에러와 예외 기초

```python
# TypeError
"10" + 10
```

```python
# NameError
print(a)
```

```python
# ZeroDivisionError
10 / 0
```

에러 메시지를 **읽는 습관**이 중요

---

## 14️⃣ 주석과 코드 스타일

```python
# 한 줄 주석
"""
여러 줄 주석
"""
```

* 변수명: snake_case
* 들여쓰기: 4칸

---

## 15️⃣ GitHub 업로드 팁

```gitignore
venv/
__pycache__/
```

* `.md` + `.ipynb` 함께 업로드 추천

---


---


