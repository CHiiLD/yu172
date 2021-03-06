# 테스팅

## 테스팅 기초와 원리

### 테스팅 기초

- 소프트웨어의 **신뢰성을** 확증하는 과정

- 좋은 테스트란 숨어있는 **오류를** 잘 발견하는 것

### 테스팅 용어

- 오류 - 프로그램 실행 결과가 **예상한** 결과와 다른 경우
- 결함 - 버그
- 고장 - 명세에서 작성된 요구와 기능을 제대로 수행할 수 없는 경우

### 테스팅의 원리

- 테스팅은 오류를 발견하려고 프로그램을 실행시키는 것
- 구현과 관계없는 독립된 팀에서 수행되어야 함.

## 블랙박스 테스팅

### 블랙박스 테스팅

- 프로그램의 구조를 고려치 아니함
- 테스트 케이스는 프로그램의 모듈의 **요구나** **명세를** 기초로 결정
- **입력과** **출력에** 대해 알아야 함
- 기능 테스트
- 가능한 모든 기능을 테스트하는 것이 좋음

### 동치 클래스

- 프로그램에서 같은 부분을 구동시키고 결과를 확인하는 값들의 **대푯값**
- 모든 대푯값을 찾아내어 각 클래스에서 하나의 값으로 실행시킨다면 전수 테스트와 같음
- min < value < mac

### 경계값 분석

- 동치 클래스의 경계에서 문제를 발생하는 특수한 값이 존재
- 동치 클래스의 경계값은 높은 효율을 가짐

### 원인과 결과 그래프

- 입력조건의 조합을 체계적으로 선택하는 테스트 기법
- 노드와 기호로 표시
- 각 결과들에 대해서 조건의 조합을 나열

## 화이트박스 테스팅

### 화이트 박스 테스팅

- 모듈의 논리적인 구조를 체계적으로 점검하는 테스팅
- 논리 흐름도(logic-flow diagram)를 이용

### 기본 경로 테스팅

- 독립적인 논리 흐름을 검사하는 테스트 케이스
- 시작노드에서 종료노드까지 **서로 다른** 경로로써 싸이클은 최대 한번만 지나가야함

### 싸이클로매틱 복잡도

- 기본경로의 수를 결정하는 이론
- 계산 3가지 방법
  - 폐쇄경로의 수 + 1 : 논리 흐름 그래프는 이차원 평면으로 여러 영역으로 나뉘며, 이 중 폐쇄경로의 수에 1을 더한 값
  - 노드와 간선의 수 : 간선의 수에서 노드의 수를 빼고 2를 더한 값 **E - N + 2**
  - 단일 조건의 수 + 1 : 참과 거짓으로 판별되는 원자적 조건의 수에 1을 더한 값
- 위 3가지 방법의 값이 같아야함

### 테스트 커버리지

### 반복문의 테스팅

## 객체지향 테스팅

### 사용 사례 기반 테스팅

- 사용사례로부터 테스트 케이스 추출
- **사용자의** 입력과 액션을 파악
- 입력값을 정상/비정상/예외 값으로 분류
- 테스트 케이스 생성
  - 테스트 조합이 오류를 발견할 가능성이 있다면 선택
  - 테스트 조합이 프로그램의 기능과 동작의 정확성을 가진다면 선택
  - 중복 제거

### 상태 기반 테스팅

- 같은 입력에 대해 같은 동작을 보이며 동일한 결과를 생성하는 시스템을 대상
  - 배치 처리 시스템
  - 계산 중심 시스템
  - 하드웨어로 구성된 회로
- 시스템의 동작은 시스템의 상태에 의해 좌우됨
  - 상태 - 과거 입력에 대한 영향을 표시
  - 트랜지션 - 이벤트에 대한 반응으로 시스템의 하나의 상태에서 다른 상태로 변화하는 과정을 나타냄
  - ____ - 시스템에 대한 입력
  - 액션 - 이벤트에 대한 출력


## 통합 테스팅

### 통합 테스팅

- 모듈의 결합을 테스트
  - 여러 개발팀에서 개발한 각각의 단위 모듈을 대상
  - 모듈-모듈 간의 결합을 테스트
- 결합 순서
  - 빅뱅
  - 하향식
  - 상향식
  - 연쇄식
- 용어
  - 드라이버 - 모듈이 호출하는 간이 소프트웨어
  - 3rd party - 모듈이 호출하는 또 다른 모듈

### 빅뱅 통합

한 번에 모든 모듈을 모아 통합

### 하향식 통합

- 시스템 구조상 **상위** 모듈부터 통합
- 장점
  - 중요한 모듈의 인터페이스를 조기에 테스트
  - 인터페이스를 이용하여 시스템의 모습을 일찍 구현
  - 개발자 입장에서 용이함
- 단점
  - 입출력 모듈이 상대적으로 하위에 있음 -> 테스트 케이스 작성 및 실행이 어려움
  - 중요 기능이 마지막에 구현됨

### 상향식 통합

- 시스템의 구조상 하위 모듈부터 통합
- 장점
  - 점증식 통합 방식 - 오류 발견이 쉬움, 하드웨어 사용 분산
  - 하위층 모듈을 하위층보다 더 단위 테스트
- 단점
  - 초기에 시스템의 뼈대가 그려지지 않음
  - 상위층의 중요 인터페이스를 마지막에 구현

### 연쇄식 통합

## 시스템 및 인수 테스팅

- 컴포넌트를 통합 후 수행하는 테스트 기법

### 기능 테스트

### 성능 테스트

### 보안 테스트

### 사용성 테스트

### 인수 테스트

### 설치 테스트

## 테스트 자동화 도구