# Docker에 Mssql 세팅하기

1. 도커 설치하기
    - 구글에 "docker for Mac" 이라고 검색한다.
    - 검색하면 상단에 Install Docker DeskTop on Mac 눌러 들어간다.
        - [https://docs.docker.com/desktop/mac/install/](https://docs.docker.com/desktop/mac/install/)
    - 접속하여 나온 화면에서 Mac이 인텔인지 애플칩인 지 확인하여 맥환경에 맞는 걸로 선택하여 설치한다.
    - M1을 사용하는 나는 Mac with Apple chip을 설치했다.
    - 설치하여 도커에 계정을 만들어 접속한다 .
2. Mssql 설치하기 
    - 터미널 실행하기
    - 실행한 터미널에 "docker pull [mcr.microsoft.com/azure-sql-edge](http://mcr.microsoft.com/azure-sql-edge)" 라고 입력하여 도커 이미지를 다운로드한다.
    - 다운로드 후 "sudo docker run --cap-add SYS_PTRACE -e 'ACCEPT_EULA=1' -e 'MSSQL_SA_PASSWORD=사용자 비밀번호' -p 1433:1433 --name 사용자아이디 -d [mcr.microsoft.com/azure-sql-edge](http://mcr.microsoft.com/azure-sql-edge)" 입력한다.
    - 컨테이너 생성이 완료되었는 지 docker ps 를 이용해 확인한다.
3. Mssql 접속하기
    - 확인 후 [https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15](https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15) 접속하여 macOS.zip 설치한다.
    - 설치 후에 new connection 버튼 클릭 후 SqlServer 정상적으로 구동되는지 확인
    

참고 사이트 

[How to Install SQL Server on an M1 Mac (ARM64)](https://database.guide/how-to-install-sql-server-on-an-m1-mac-arm64/)

[How to Install Azure Data Studio on a Mac](https://database.guide/how-to-install-azure-data-studio-on-a-mac/)