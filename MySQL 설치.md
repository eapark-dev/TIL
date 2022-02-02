# MySQL 설치

1) homebrew로 MySql 설치 하기 

→ mysql 설치 명령어 

```bash
$ brew install mysql
```

2) homebrew에서 MySql 설치 되었는 지 확인 하는 방법 

```bash
$ brew list
```

3) homebrew에서 설치된 MySql 실행하기

```bash
$ mysql.server start
```

4) MySql 암호 설정 하기

```bash
$ mysql_secure_installation
```

5)MySql 접속 하기 

```bash
#명령어 입력 후 설정한 비밀번호 입력
$ mysql -uroot -p
```