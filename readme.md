# 개발환경
```
docker compose up --build
```

# 운영환경 with nginx
```
docker build -t mugon/docker-react-app .
docker run -p 8080:80 mugon/docker-react-app
```