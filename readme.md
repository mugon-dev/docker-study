# build
### 현재폴더의 Dockerfile을 읽어 빌드
```
docker build ./
```

# run
```
docker run -it [빌드된 docker image 이름]
```

# -t 옵션으로 네이밍
## 규칙
```
-t 도커아이디/프로젝트이름:버전
```

# build, run with name
```
docker build -t mugon/hello:latest ./
docker run -it mugon/hello      
```