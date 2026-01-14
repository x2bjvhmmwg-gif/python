
# Python 기초 총정리  
(환경 설정 → 자료형 → 연산 → 제어문 → 반복문 → 인덱싱/슬라이싱 → 함수 → 내장함수)

> Python을 사용하기 위한 진입 과정부터  
> 실제 많이 쓰는 문법과 개념을 학습 흐름에 맞게 정리

---

## 목차

- [Python 개요](#python-overview)
- [Python 실행과 인터프리터](#interpreter)
- [패키지 관리 (pip, uv)](#pip)
- [가상환경 (venv)](#venv)
- [Jupyter Notebook & Colab](#jupyter)
- [자료형(DataType)](#datatype)
- [자료형 비교](#type-compare)
- [문자열 상세](#string)
- [연산자](#operator)
- [조건문](#condition)
- [반복문](#loop)
- [인덱싱(Indexing)](#indexing)
- [슬라이싱(Slicing)](#slicing)
- [함수(Function)](#function)
- [자주 쓰는 내장 함수](#builtin)
- [입력과 형 변환](#input)
- [에러(Error) 기초](#error)
- [주석과 코드 스타일](#style)
- [GitHub 업로드 팁](#github)

---

<a id="python-overview"></a>

## 1. Python 개요

Python은 **인터프리터 언어**로, 코드를 한 줄씩 바로 실행한다.

- 실행 즉시 결과 확인 가능
- 문법이 간결하고 가독성이 좋음
- 들여쓰기(indent)가 문법의 일부

---

<a id="interpreter"></a>

## 2. Python 실행과 인터프리터

터미널에서 Python을 실행하면 **바로 입력 가능한 영역(REPL)** 이 열린다.

```bash
python
```

* 현재 설치된 Python 버전이 출력됨
  (예: Python 3.12.x)
* `exit()` 로 종료 가능

---

<a id="pip"></a>

## 3. 패키지 관리 (pip, uv)

```bash
pip list
```

* 현재 컴퓨터 또는 가상환경에 설치된 패키지 목록 확인

`pip`, `uv` 가 보이는 이유:

* Python 패키지를 설치/관리하기 위한 도구
* Python 설치 시 기본 포함되는 경우가 많음

---

<a id="venv"></a>

## 4. 가상환경 (venv)

가상환경은 **프로젝트별 독립된 Python 공간**이다.

```bash
python -m venv venv
```

### 활성화 / 비활성화

```bash
venv\Scripts\activate
deactivate
```

* 프로젝트마다 라이브러리 충돌 방지
* Jupyter도 가상환경 안에 설치하는 것이 좋음

---

<a id="jupyter"></a>

## 5. Jupyter Notebook & Colab

### Jupyter Notebook

```bash
pip install jupyter
jupyter notebook
```

* 셀 단위 실행
* 입력한 내용이 파일로 저장됨
* 종료: `Ctrl + C`

### Google Colab

* Jupyter와 UI 유사
* Google Drive에 저장
* 주소 공유가 편리
* 런타임 유형 변경 가능

GitHub:

* `.ipynb` 파일은 **실행 없이 결과 미리보기 가능**
* 코드 클릭 시 텍스트로 확인 가능

---

<a id="datatype"></a>

## 6. 자료형(DataType)

Python의 모든 값은 **자료형(Type)** 을 가진다.

### 숫자형

* `int` : 정수
* `float` : 실수

```python
a = 10
b = 3.14
```

---

### 문자열 (str)

```python
"hello"
'hello'
"""
여러 줄 문자열
"""
```

* `"` 와 `'` 는 동일한 문자열 타입
* 문자열은 **수정 불가 (immutable)**

특수 문자:

* `\n` : 줄 바꿈
* `\"` : 문자열 안에 큰따옴표 사용

---

### 불리언 (bool)

```python
True
False
```

* 반드시 대문자
* 조건 판단에 사용

---

### 리스트 (list)

```python
[1, 2, 3]
```

* 순서 있음
* 값 변경 가능

---

### 튜플 (tuple)

```python
(1, 2, 3)
```

* 순서 있음
* 값 변경 불가

---

### 딕셔너리 (dict)

```python
{"name": "Kim", "age": 20}
```

* key-value 구조

---

### None

```python
None
```

* 값이 없음을 의미
* JavaScript의 `null` 과 유사

---

<a id="type-compare"></a>

## 7. 자료형 비교

```python
10 == 10.0            # True
type(10) == type(10.0)  # False
```

```python
True == 1             # True
type(True) == type(1)  # False
```

```python
None is None          # True
```

* `==` : 값 비교
* `is` : 객체 비교 (주소)

---

<a id="string"></a>

## 8. 문자열 추가 설명

```python
print("문자" * 3)   # 문자문자문자
```

* `*` 는 문자열 반복
* `"문자" + 10` 은 타입 불일치로 오류 발생

---

<a id="operator"></a>

## 9. 연산자

### 산술 연산자

```python
+, -, *, /, %, **, //
```

* `/` : 나누기 (실수 결과)
* `//` : 몫
* `%` : 나머지
* `**` : 거듭제곱

---

### 비교 연산자

```python
==, !=, <, >, <=, >=
```

---

### 논리 연산자

```python
and, or, not
```

* `not` 은 뒤의 값을 반대로 판단

---

<a id="condition"></a>

## 10. 조건문

```python
if x > 0:
    print("양수")
elif x == 0:
    print("0")
else:
    print("음수")
```

한 줄 조건문도 가능:

```python
if x > 0: print("양수")
```

---

<a id="loop"></a>

## 11. 반복문

### for 문

```python
for i in [1, 2, 3, 4]:
    print(i)
```

* 리스트 안의 값이 하나씩 `i`에 들어감

```python
for i in range(5):
    print(i)
```

* Python에는 `of` 가 없음
* iterable을 `in` 으로 직접 순회

---

<a id="indexing"></a>

## 12. 인덱싱 (Indexing)

```python
text = "Python"
text[0]    # 'P'
text[-1]   # 'n'
```

* 하나의 값 접근
* 0부터 시작
* 범위 초과 시 오류

---

<a id="slicing"></a>

## 13. 슬라이싱 (Slicing)

```python
text[start:end:step]
```

```python
text = "Python"
text[0:3]     # 'Pyt'
text[2:]      # 'thon'
text[::-1]    # 'nohtyP'
```

* end는 포함되지 않음
* 원본은 변경되지 않음

---

<a id="function"></a>

## 14. 함수(Function)

```python
def add(a, b):
    return a + b
```

```python
def hello(name="World"):
    print(name)
```

* return이 없으면 `None` 반환

---

<a id="builtin"></a>

## 15. 자주 쓰는 내장 함수

```python
len(), type(), range()
print(), input()
sum(), max(), min(), sorted()
int(), float(), str(), bool()
```

---

<a id="input"></a>

## 16. 입력과 형 변환

```python
x = input("숫자 입력: ")
x = int(x)
```

* input 결과는 항상 문자열

---

<a id="error"></a>

## 17. 에러(Error) 기초

```python
"10" + 10      # TypeError
print(a)       # NameError
10 / 0         # ZeroDivisionError
```

* 에러 메시지를 읽는 습관 중요

---

<a id="style"></a>

## 18. 주석과 코드 스타일

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

## 19. GitHub 업로드 팁

```gitignore
venv/
__pycache__/
```


```



다음 뭐 할지 말해줘.
```
