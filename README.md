# kill 명령어

## kill 명령어의 특징
+ 프로세스에 signal을 보내는 명령어이다.
+ 기본 signal이 SIGTERM인데, 이 시그널의 기본 동작이 프로그램 종료이다.
+ 일반적으로 종료 시그널과 함께 사용된다.

## Signal
![스크린샷(28)](https://user-images.githubusercontent.com/50985536/171604765-f24b50c3-89a6-46b1-965a-5e662a760949.png)
+ kill -l 를 입력하면 위와 같이 signal 번호와 이름이 나타난다.
+ 아무런 signal이 지정되지 않을시 kill PID를 입력하고 SIGTERM이 전달된다.
+ kill -(보낼 시그널) PID의 형식으로 시그널을 전달한다.
+ signal은 숫자나 SIG를 뺀 이름으로도 가능하다.

## kill를 이용한 종료

1. kill -TERM {PID}
+ kill {PID}, kill -15 {PID}과 같은 명령어이다.
+ 작업했던 파일과 설정를 모두 저장후 종료시킨다.
+ 기본값인 TERM(SIGTERM)은 kill 명령어의 15번 시그널이다.

2. kill -9 {PID}
+ kill -KILL {PID}와 같은 명령어이다.
+ kill 명령어 자체는 프로세스 종료 명령어가 아니다.
+ kill 명령어의 기본 실행동작이 프로세스 종료일 뿐이다.
+ 시그널로 KILL을 보내게 되면 프로세스를 강제종료 시키기 때문에 저장되지 않은 데이터 등을 잃을 수 있으므로 단순히 프로세스 종료 목적으로 쓰는 것은 위험하다.
+ KILL(SIGKILL)은 kill 명령어의 9번 시그널이다.
