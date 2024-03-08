# be-chess
## 구현 목록
**Piece (값 객체)**
- 체스 게임에 필요한 말들을 담당하는 클래스
- private 생성자를 가지고, 인스턴스 생성한 이후에는 인스턴스의 상태 값을 변경할 수 없다.
- 색과 이름을 받아 말(Piece 객체)들을 생성하는 팩토리 메소드들을 가진다. 

**PieceTest**
- 의도한 대로 말들이 잘 생성되는지 확인한다 

**Board**
- 체스판을 담당하는 Board 클래스
- 보드를 초기 설정한다
- 현재의 보드 상태 반환한다

**BoardTest**
- 32개의 말이 잘 세팅 됐는지
- 의도한 대로 체스 판이 출력되는지 확인한다 

**StringUtils**
- 줄바꿈 추가하는 유틸리티 메서드 

**Play**
- 사용자에게 게임의 시작과 종료 여부를 입력받는다

## 배운점 기록
**assertJ 라이브러리 추가**
- assertThat 사용하고 싶다면 assertJ 라이브러리 사용해야 함
- (JUnit5에서 직접 제공하지 않기 때문)
- assertJ.jar 파일 -> 라이브러리 추가해서 해결했다가 패키지를 분리하면 에러가 나는 것을 확인하고, gradle 에 추가

**github fork**
- fork 할 때, main은 디폴트로 따라오기 때문에 main 에 있는 commit 내역들은 그대로 딸려온다...
- 그냥 새로운 브랜치를 파서 작업해야함 
- 만약 원치 않는 commit 내역들을 감추는 효과(?)를 주고 싶다면 reset --hard 돌아가길원하는commit의 해시 로 돌아가서 작업한다...

**@BeforeEach**
- 이 어노테이션이 붙으면 테스트 메소드보다 먼저 실행 됨 

**팩토리 메서드**

## 더 알아봐야 할 점
- 머지 되길 기다리며 새로운 브랜치를 파서 작업하다가 머지가 된다면? 내역을 문제 없이 가져온 후 이어서 작업하는 방법은...? rebase --onto 가 답일깡...?
- .gitignore 파일에 대하여 