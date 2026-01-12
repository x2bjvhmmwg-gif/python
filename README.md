
```
Python_Basic_Study.md
```

---

## 내용 구조 (GitHub용 Markdown)

markdown
# 🐍 Python 기본 학습 정리

---

## 1️⃣ Python 시작과 환경 설정
- Python: **인터프리터 언어**
- 터미널 실행:
```bash
python  # 버전 확인
exit()  # 종료
````

* 가상 환경:

```bash
python -m venv 폴더명
venv\Scripts\activate  # 활성화
deactivate             # 비활성화
```

* Jupyter 설치 및 실행:

```bash
pip install jupyter
jupyter notebook
```

* Colab: 구글 드라이브 기반 → 공유, 런타임 변경 가능

---

## 2️⃣ 파일과 노트북 활용

* Python 코드는 `.py` 파일로 관리 가능
* Jupyter / Colab → 셀 단위 코드 실행 가능
* 변수 단독 작성 시 마지막 값 출력 가능
* Markdown 셀 활용 → 제목, 글, 목록, 코드 작성
* `.ipynb` 파일 그대로 GitHub 업로드 → 프리뷰 가능
* `.gitignore` 사용 → 업로드 제외 가능

---

## 3️⃣ Python 기본 자료형

| 자료형   | 예시                      | 설명   |
| ----- | ----------------------- | ---- |
| int   | `x = 10`                | 정수   |
| float | `y = 3.14`              | 실수   |
| str   | `'Hello'`, `"""여러 줄"""` | 문자열  |
| bool  | `flag = True`           | 참/거짓 |
| None  | `x = None`              | 값 없음 |

### 문자열 특성

* `' '`, `" "`, `''' '''`, `""" """` 모두 문자열
* 문자열 안에 따옴표 포함 시:

```python
"She said, \"Hello!\""
'It\'s sunny'
```

* 줄 바꿈: `\n` 또는 여러 줄 문자열 가능

---

## 4️⃣ 변수 규칙

* 첫 글자: 문자 또는 `_`
* 숫자로 시작 불가
* 예약어 사용 불가
* 언더스코어 사용 가능
* 권장 표기법:

  * 변수/함수: `snake_case`
  * 클래스: `PascalCase`
  * 상수: `UPPER_SNAKE_CASE`

---

## 5️⃣ 산술 연산

| 연산자 | 의미      | 예제       | 결과  |
| --- | ------- | -------- | --- |
| +   | 더하기     | `5 + 3`  | 8   |
| -   | 빼기      | `5 - 3`  | 2   |
| *   | 곱하기     | `5 * 3`  | 15  |
| /   | 나누기(실수) | `5 / 2`  | 2.5 |
| //  | 나누기(몫)  | `5 // 2` | 2   |
| %   | 나머지     | `5 % 2`  | 1   |
| **  | 제곱      | `2 ** 3` | 8   |

---

## 6️⃣ 비교 연산

| 연산자 | 의미     |
| --- | ------ |
| ==  | 값 같음   |
| !=  | 값 다름   |
| <   | 작음     |
| >   | 큼      |
| <=  | 작거나 같음 |
| >=  | 크거나 같음 |

---

## 7️⃣ 논리 연산

| 연산자 | 의미         |
| --- | ---------- |
| and | 모두 참 → 참   |
| or  | 하나라도 참 → 참 |
| not | 반대로 뒤집음    |

* 예제:

```python
True or False  # True
not True       # False
True and False # False
```

---

## 8️⃣ 조건문

```python
x = 10
if x > 0:
    print("양수")
elif x == 0:
    print("0입니다")
else:
    print("음수")
```

* 한 줄 조건문:

```python
print("양수") if x > 0 else print("0 또는 음수")
```

* 들여쓰기(indent) 중요

---

## 9️⃣ 반복문

* `for 변수 in iterable:` → 리스트, 튜플, 문자열 등 반복 가능
* `range()` 사용 → 숫자 범위 반복

```python
for i in range(5):  # 0~4
    print(i)
```

* 리스트 반복 예제:

```python
for i in [1, 2, 3, 4]:
    print(i)
```

---

## 💡 정리

* Python 기본 흐름:
  **환경 설정 → 변수/자료형 → 연산 → 조건문 → 반복문**
* Jupyter/Colab 활용 → **실습 + 시각적 확인**
* 자료형, 연산, 조건문, 반복문 기본 이해 후 **다른 기능 학습 수월**

```

---

