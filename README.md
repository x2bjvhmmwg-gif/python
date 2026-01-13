
---


---

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

* 인터프리터 언어 (한 줄씩 즉시 실행)
* 동적 타입 언어
* 들여쓰기(indent)가 문법

```bash
python
exit()
```

---

<a id="environment"></a>

## 2. 실행 환경과 가상환경

```bash
python -m venv venv
venv\Scripts\activate
deactivate
```

* 프로젝트별 패키지 독립 관리

---

<a id="jupyter"></a>

## 3. Jupyter Notebook

```bash
pip install jupyter
jupyter notebook
```

* 셀 단위 실행
* `.ipynb`는 GitHub에서 미리보기 가능
* 종료: `Ctrl + C`

---

<a id="datatype"></a>

## 4. 자료형(DataType)

### 숫자형

* int, float, complex

### 불리언

* True / False (대문자 필수)

### 시퀀스

* str, list, tuple

### 집합 / 딕셔너리

* set, dict

### None

* 값이 없음 (`NoneType`)

---

<a id="type-compare"></a>

## 5. 자료형 비교

```python
10 == 10.0                 # True
type(10) == type(10.0)     # False
```

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

<a id="condition"></a>

## 7. 조건문

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

<a id="loop"></a>

## 8. 반복문

```python
for i in [1, 2, 3, 4]:
    print(i)
```

```python
for i in range(5):
    print(i)
```

* Python에는 `of` 없음
* iterable을 직접 순회

---

<a id="function"></a>

## 9. 함수(Function)

```python
def add(a, b):
    return a + b
```

```python
def hello(name="World"):
    print(name)
```

* return이 없으면 `None`

---

<a id="builtin"></a>

## 10. 자주 쓰는 내장 함수

```python
len(), type(), range(), print(), input()
sum(), max(), min(), sorted()
```

---

<a id="methods"></a>

## 11. 자료형별 주요 메서드

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

<a id="input-casting"></a>

## 12. 입력과 형 변환

```python
x = input("숫자 입력: ")
x = int(x)
```

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

* 에러 메시지를 읽는 습관이 중요

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

---

<a id="github"></a>

## 15. GitHub 업로드 팁

```gitignore
venv/
__pycache__/
```

* `.md` + `.ipynb` 함께 업로드 추천

---



---


