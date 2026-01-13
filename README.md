
---

# 🐍 Python 기초 정리 (입문 ~ 핵심 문법)

> Python을 사용하기 위한 진입 과정부터
> 자료형, 비교, 연산, 제어문, 반복문, 함수까지 정리

---

## 1️⃣ Python 실행 환경 이해

### 🔹 Python은 인터프리터 언어

* 코드를 **한 줄씩 즉시 실행**
* 터미널에서 바로 실행 가능

```bash
python
```

```bash
exit()
```

* Python 버전 확인

```bash
python --version
```

---

## 2️⃣ 가상 환경 (venv)

### 가상 환경 생성

```bash
python -m venv 폴더명
```

### 가상 환경 활성화 (Windows)

```bash
venv\Scripts\activate
```

### 비활성화

```bash
deactivate
```

📌 프로젝트별 패키지 관리 목적

---

## 3️⃣ pip / uv

* `pip` : Python 패키지 관리자
* `pip list` : 설치된 패키지 확인
* `uv` : pip 대체용 최신 패키지 관리 도구

```bash
pip install 패키지명
```

---

## 4️⃣ Jupyter Notebook

### 설치

```bash
pip install jupyter
```

### 실행

```bash
jupyter notebook
```

* 웹 기반 실행
* 셀 단위 실행
* `.ipynb` 파일은 GitHub에서 **미리보기 가능**
* 실행은 안 되지만 코드 확인 가능

📌 종료: 터미널에서 `Ctrl + C`

---

## 5️⃣ Python 기본 자료형 (DataType)

### 🔹 숫자형 (Numeric)

* `int` : 정수
* `float` : 실수
* `complex` : 복소수

```python
a = 10
b = 3.14
c = 3 + 4j
```

---

### 🔹 불리언 (Boolean)

```python
True
False
```

⚠️ 반드시 대문자

---

### 🔹 시퀀스 타입 (Sequence)

#### 문자열 (str)

```python
"hello"
'hello'
"""여러 줄
문자열"""
```

* `\n` : 줄바꿈
* `\"` : 큰따옴표 출력

```python
print("Hi" * 3)  # 반복
```

---

#### 리스트 (list)

```python
lst = [1, 2, 3]
lst.append(4)
lst[0] = 100
```

---

#### 튜플 (tuple)

```python
t = (1, 2, 3)
```

* 값 변경 불가

---

### 🔹 집합 (set)

```python
s = {1, 2, 3, 3}
```

* 중복 제거
* 순서 없음

---

### 🔹 딕셔너리 (dict)

```python
person = {"name": "Alice", "age": 25}
```

---

### 🔹 None

```python
x = None
```

* 값이 없음
* JS의 `null`과 유사

---

## 6️⃣ 자료형 비교

### 값 비교 vs 타입 비교

```python
10 == 10.0        # True
type(10) == type(10.0)  # False
```

```python
True == 1         # True
type(True) == type(1)   # False
```

### is vs ==

```python
a = None
a is None   # True
```

📌 `is` → 객체 비교
📌 `==` → 값 비교

---

## 7️⃣ 연산자

### 산술 연산

```python
+, -, *, /, %, **
```

### 비교 연산

```python
==, !=, <, >, <=, >=
```

### 논리 연산

```python
and, or, not
```

```python
True or False   # True
not True        # False
```

---

## 8️⃣ 조건문 (if)

```python
if x > 0:
    print("양수")
elif x == 0:
    print("0")
else:
    print("음수")
```

📌 들여쓰기(indent)가 문법

### 한 줄 조건문

```python
if x > 0: print("양수")
```

---

## 9️⃣ 반복문

### for 문

```python
for i in [1, 2, 3, 4]:
    print(i)
```

📌 Python에는 `of` 없음
→ iterable 자체를 `in`으로 순회

---

### range()

```python
for i in range(5):
    print(i)
```

---

## 10️⃣ 함수 (Function)

```python
def add(a, b):
    return a + b
```

```python
result = add(3, 4)
print(result)
```

📌 `return`이 없으면 `None` 반환

---

## 11️⃣ 출력 (print)

```python
print("Hello")
print(10)
```

* Jupyter에서는 변수만 써도 출력 가능

```python
x = 10
x
```

---

## 12️⃣ GitHub 관리 팁

* `.ipynb` 파일 그대로 업로드 가능
* `.gitignore`에 파일명 작성 시 제외 가능

```gitignore
venv/
__pycache__/
```

---

## 📌 전체 핵심 요약

* Python은 인터프리터 언어
* 가상환경으로 프로젝트 관리
* 자료형은 동적 타입
* `==` vs `is` 차이 중요
* 들여쓰기가 문법
* Jupyter는 연습·시각화에 최적

---

---
