# [Asp.Net] 클라이언트 IP 주소 얻는 방법

**1. 일반적인 클라이언트 IP 주소 얻는 법**

```
Request.ServerVariables["REMOTE_ADDR"];
```

**2. 프록시 서버를 통해 전달 된 클라이언트 IP 주소 얻는 법**

```
Request.ServerVariables["HTTP_X_FORWARDED_FOR"];
```