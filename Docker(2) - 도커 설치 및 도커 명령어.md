# Docker(2) - 도커 설치 및 도커 설명

1. chrome창에 docker for Mac 입력하여 최상단 사이트 접속
2. 사용하는 맥 칩에 따라 Intel chip 또는 Mac with Apple chip 다운로드 
3. 다운로드 한 dmg파일을 실행시켜 도커를 어플리케이션 폴더로 옮긴다.
4. 어플리케이션에 있는 도커를 실행한다.
5. 도커를 설치한다.
6. 만약 도커 계정이 없다면 회원가입 한다.

## 도커 엔진

- 도커는 서버와 클라이언트 구조로 이루어져 있다.
- 도커 커맨드는 일종의 클라이언트라고 이해하면 된다.

## 도커 이미지

- 도커 이미지는 컨테이너를 사용하기 위해 사용한다.
- 도커 이미지는 스크립트의 집합이다.

## 도커 컨테이너

- 도커 이미지가 리눅스 컨테이너 형태로 실행한 상태를 의미함
- 도커 컨테이너는 분리된 공간이다.

→ 컨테이너와 이미지를 다뤄서 도커를 작업한다.

---

- 명령어 사용법

```bash
docker image 명령 # 도커 이미지 명령 옵션
docker container 명령 옵션 # 도커 컨테이너 명령 옵션
```

- Docker Hub 접속
    - [https://hub.docker.com/](https://hub.docker.com/) 접속
    - 해당 사이트 회원 가입

    ## 도커 명령어
    
    - 터미널에서 docker hub 로그인 하기
    
    ```bash
    docker login #도커 로그인 명령어
    docker logout #도커 로그아웃
    docker search 다운로드 받을 이미지 검색어 #ex) docker search ubuntu
    ```
    - /앞단이 docker hub의 사용자명이다.
    - 공식 일경우는 OFFICIAL [OK]로 표시된다.
    
    ```bash
    # 너무 많은 이미지 검색 시에는 --limit 옵션을 넣을 수 있다.
    ```
    
    - 선택한 이미지를 다운 받는 명령어
    
    ```bash
    docker pull 이미지 이름 #docker pull ubuntu
    docker images #다운로드 받은 이미지 확인 명령어
    docker image ls -q #도커 이미지 아이디만 조회하는 명령어
    ```
