# wsl2 ubuntu24.04 install

# how to install wsl2-ubuntu24.04 on PC

```bash
> wsl --update
> wsl --status
> wsl --shutdown
> wsl --list --running
> exit # 터미널 종료후 다시실행
> wsl --list --online 
> wsl --install -d Ubuntu-24.04
```

# how to uninstall ubuntu24.04 on WSL2
```bash
1. wsl --list --verbose -> 설치된 배포와 상세정보 출력
2. wsl --unregister Ubuntu-24.04 -> 등록 취소하고 파일시스템삭제
3. 윈도우 설정 -> 앱 -> Ubuntu-24.04 제거
4. 컴퓨터 재부팅
5. 윈도우 파일 탐색기에서 linux->Ubuntu-24.04 폴더 사라져야 함
6. 터미널의 목록에서 없어져야 함 -> 삭제 안되면 설정에서 프로필 직접삭제
```

# how to install SSH
```bash
1. SSH server 설치
$ sudo apt update
$ sudo apt install openssh-server

2. SSH 설정파일(/etc/ssh/sshd_config)에서 아래처럼 수정 
- PasswordAuthentication no -> PasswordAuthentication yes
$ sudo vi /etc/ssh/sshd_config

3. openSSH 재가동/상시가동/가동확인
$ sudo systemctl restart ssh -> 설정 변경 후 재시동
$ sudo systemctl enable ssh -> 부팅시 자동실행
$ sudo systemctl status ssh -> active(running) 확인할 것

4. openSSH 동작확인
$ sudo apt install net-tools -> net-tools 설치
$ netstat -ant -> 로컬 컴퓨터의 모든 IP주소(0.0.0.0)의 22번포트가 열려 있어야 함(LISTEN 상태)
```
