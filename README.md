# wsl2 ubuntu24.04 install

# how to install wsl2-ubuntu24.04 on PC

```bash
> wsl --update
> wsl --status
> wsl --shutdown
> wsl --list --running
> exit
> wsl --list --online
> wsl --install -d Ubuntu-24.04
```

# how to uninstall ubuntu24.04 on WSL2
```bash
wsl --list --verbose -> 설치된 배포와 상세정보 출력
wsl --unregister Ubuntu-24.04 -> 등록 취소하고 파일시스템삭제
윈도우 설정 -> 앱 -> Ubuntu-24.04 제거
컴퓨터 재부팅
윈도우 파일 탐색기에서 linux 폴더 사라져야 함
터미널의 목록에서 없어져야 함 -> 삭제 안되면 설정에서 직접삭제 가능
```

