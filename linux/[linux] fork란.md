# [linux] fork란?
> c로 간단한 서버를 제작하면서 다중 사용자의 접속을 구현하기 위해 필요해서 알아보게 되었다.

## 1. 문법
    #include <unistd.h>
    pid = fork();

## 2. fork는 언제 사용할까?
프로세스를 새로 생성할 때 사용한다.
원래 있던 프로세스(fork를 호출한)는 부모 프로세스, 새로 생겨난 프로세스는 자식 프로세스라 한다.

## 3. pid
모든 프로세스는 프로세스 아이디를 부여받는데,
생성한 순간 자식 프로세스의 pid는 0이 되며, 이것을 이용해 부모와 자식의 역할을 구분해서 지정헤 줄 수 있다.

## 4. wait
fork를 이용해 자식 프로세스를 생성했을 때, wait()를 사용하면 부모 프로세스가 자식 프로세스가 종료될 때까지 기다리게 된다.
자식 프로세스가 종료되기 전에 부모 프로세스가 먼저 종료되어 버리면 자식 프로세스가 고아 프로세스가 되어버린다.

    pid_t wait(int *status);


## 출처
<li> http://hunj.me/using_fork/
<li>https://www.joinc.co.kr/w/man/2/wait
