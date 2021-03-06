# 파이썬 기초 스터디

## 스터디 개요
- 기간 : 2016.12.27일 부터 약 5~6주
- 스터디 리더 : 한영빈(소프16)
- 스터디 방식 : 교재로 먼저 공부 후 모임 때 질의응답 + 모임때마다 알고리즘 풀이 하기([작성한 소스코드는 저장소에 올리기](https://github.com/s-owl/python-basics-study))
- 교재 : [점프 투 파이썬](https://wikidocs.net/book/1) + 추가적인 서적이나 인터넷 자료
- 구성원 : 한영빈(소프16), ~~김지연(소프16)~~, 송지은(소프15), 배다슬(소프12), 김재경(소프12), ~~한나라(정통16)~~
- 스터디 모임 시각 : 매주 화요일 오후 2시~4시 - 3주차 모임은 목요일
- 모임 장소 : SSS 랩실

## 계획중인 스터디 커리큘럼
- 시작 전 : 스터디 방식 등 수립
- 1주차 : 0~3장
- 2주차 : 4장
- 3주차 : 5장
- 4주차 : 6장
- 5주차 : 7장

## 1주차 모임
- 2016.12.27
- 참석자 : 한영빈, 김재경, 송지은, 배다슬
- 진도 : 0~3장

### Python 설치
- 이 스터디에서는 Python 3 를 사용합니다. 장그러므로, Python 3 를 설치합시다. Python 2 는 오래 된 것도 있고, 새로 나오는 라이브러리나 프레임워크, 자료 등이 Python 3 을 기반으로 하기 때문입니다.

#### Windows
[Python 홈페이지](https://www.python.org) 에서 설치 마법사를 내려받아, 설치 마법사의 안내에 따라 설치합니다.
[여기](https://www.python.org/downloads/windows/) 를 눌러 설치 마법사 다운로드 페이지로 이동합니다.

`chocolatey` 패키지 관리자를 사용하시는 경우, 명령 프롬포트나 Windows PowerShell 를 관리자 권한으로 켜고, 다음을 실행하여 설치할 수도 있습니다.

```posh
choco install python
```

#### Linux
보통 리눅스에는 Python 이 설치되어 있습니다. 그러나 설치되지 않는 경우도 있고, Python 2 가 설치된 경우도 있습니다.

Arch Linux 의 경우, `pacman`을 사용하여 `python` 패키지를 설치하면, 최신 버전의 Python 3 가 설치됩니다.

```bash
sudo pacman -S python
```

Ubuntu 의 경우 배포판 버전에 따라 제공되는 패키지 이름에 차이가 있습니다. Ubuntu 16.04 에서는 `python3` 패키지를 `apt` 로 설치합니다.

```bash
sudo apt install python3
```

#### macOS
Windows 와 마찬가지로 설치마법사를 이용하여 설치할 수 있습니다. [여기를 클릭하여 설치마법사 다운로드 페이지로 이동합니다.](https://www.python.org/downloads/mac-osx/)

또는, [Homebrew](http://brew.sh/) 를 사용 하시는 경우, 다음을 실행하여 설치하실 수 있습니다.

```bash
brew install python3
```

---

- for 반복문
  - Python 에서는 `for(i=0; i<10; i++)` 형식의 반복문을 사용하는 대신 `for i in range(0,10)` 형식의 반복문을 사용함. (for 변수 in 리스트 형식에 맞춰, 리스트 자리에 숫자 리스트를 만드는 `range()` 함수 활용)
- tuple 을 사용하는 이유 - 리스트보다 동작속도가 더 빠름.
- 딕셔너리에서 튜플을 키로 사용 할 수 있으나, 리스트는 키로 사용 불가. - 값이 변할 수 없는 것만 키로 사용 가능.
- `range()` 함수
  - `range(시작값, 끝값)` / `range(시작값, 끝값, 증가값)`
- `help()` 함수
  - 인터프리터에서 사용 가능.
  - 인수를 비우면, 파이썬에 대한 간단한 안내가 나옴.
  - 인수로 함수나 변수, 자료형을 넘기면 해당 함수나 변수, 자료형에 대한 설명이 나옴.
  - 예시 : `help(sum)` - `sum()` 함수에 대한 설명이 나옴
- `id(객체)` - 해당 객체의 고유값을 반환함
- 딕셔너리 : 자료구조의 해시테이블 작동원리와 비슷함.
- 컴파일러 : 한꺼번에 기계어로 번역 후 실행시 번역된 것을 실행 / 인터프리터 : 실행할 때 한 줄씩 번역하여 실행 / JIT(Just In Time) : 실행 시 번역 한 것을 저장 해뒀다가 같은 코드 실행시 앞서 번역하여 저장했던 것을 실행
- Python 에는 `switch` 와 증감 연산자가 없음
- 레퍼런스 카운트 - 파이썬의 쓰레기 수집기가 메모리를 해체하는 기준 중 하나로 사용함.

## 2주차 모임
- 2017.01.03
- 참석자 : 한영빈, 김재경, 배다슬
- 결석 : 송지은(병결)
- 진도 : 4장

- 파일 읽기 모드 유형
  - 첫 번째 글자
   - r : 파일 읽기
   - w : 파일 쓰기(없으면 만들고, 있으면 덮어씀)
   - x : 파일 쓰기(없을 경우에만.)
   - a : 파일 추가하기(파일이 있으면 파일 끝에서부터 쓰기)
  - 두 번째 글자
   - t(또는 생략) : 텍스트
   - b : 바이너리

## 3주차 모임
- 2017.01.12
- 참석자 : 한영빈, 송지은, 김재경
- 결석 : 배다슬(공결)

- 파이썬 모듈 : C언어로 치면 헤더 파일, Java로 치면 클래스와 메소드가 정의된 `*.java` 파일
- 연산자 오버로딩 : 객체 사이에 연산자를 사용할 수 있게 해줌
- `if __name__=="__main__":` : 인터프리터로 실행한 경우 `True`, 대화형 인터프리터에서 실행하는 경우 `False`
- 파이썬 생성자 함수 : `__init__(...):`
- 패키지 : Java 의 패키지와 거의 동일 (디렉터리를 `.` 으로 구분 - 예 : a/b/c -> a.b.c)
- 파이썬의 `raise` 는 Java 의 `throw` 와 거의 동일
- 파이썬의 `filter` 는 자바스크립트의 `filter` 와 거의 동일함.

- 스레드 사용 생성하여 실행하기

```python
# 스레딩 모듈 로드
import threading
# 스레드 생성
t = threading.Thread(target=<실행할 함수>, args=(<함수에 넘길 매개변수>))
# daemon 플래그를 설정하여, 주 프로그램이 종료될 때, 스레드도 같이 종료되도록 설정.
t.daemon = True
# 스레드 시작
t.start()
```

## 4주차 모임
- 2017.01.17
- 참석자 : 배다슬, 한영빈
- 결석 : 김재경(공결), 송지은(?)

## 5주차 모임
- 2017.01.31
- 참석자 : 한영빈, 배다슬
- 결석 :

- RegExr - 정규 표현식 테스트 사이트 : http://regexr.com/
- Python re 모듈 참조문서 : https://docs.python.org/2/library/re.html
