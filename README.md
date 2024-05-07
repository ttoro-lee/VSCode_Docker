# VSCode_Docker
VSCode와 Docker 연결하는 방법 정리

### 1. vscode 설치

- vscode 설치
- https://code.visualstudio.com/download

### 2. vscode extension 설치

- Remote Development 설치
- Dev Containers가 위 package에 포함됨

### 3. Docker 설치

- Dev Containers가 설치되면서 자동으로 docker가 설치됨
- docker 설치 후 컴퓨터 재부팅

### 4. Remote 설정

- vscode -> F1 -> settings 검색 -> Open User Settings(JSON) 클릭
- 아래 코드 내용 추가
- ```
  "remote.SSH.remotePlatform" : { 
        "IP-ADDRESS" : "linux" 
    },
  ```
- vscode -> F1 -> Remote-SSH : Open SSH Configuration File -> "C:/Users/[user-name]/.ssh/config" 파일
- 아래 코드 내용 추가
- ```
  Host HOSTNAME@IP-ADDRESS:PORT
    HostName IP-ADDRESS
    Port PORT
    User [USER-NAME]
  ```

### 5. Remote 연결

- vscode -> F1 -> Remote-SSH: Connect to Host
- remote 주소 연결
- pw 입력
- 연결 성공

## Reference
---
- https://24hours-beginner.tistory.com/278
