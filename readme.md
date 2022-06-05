# build, run
```
docker build --progress=plain -t mugon/nodejs ./
docker run -p 5000:8080 mugon/nodejs 
```

# dockerfile

## source 파일 복사
copy로 컨테이너에 현재 폴더의 파일들을 카피해줘야함

## 컨테이너안의 네트워크에 접근하는 방법
컨테이너 외부에서 내부의 포트에 접근하기 위해서 포트 매핑(-p 외부포트:내부포트)이 필요함

## working directory
이미지안에 소스코드를 가지고 있을 디렉터리 생성

## 어플리케이션 소스 변경으로 재빌드 시 효율적으로 하는 법

### package.json 먼저 카피 후 npm install
-> cache 된 파일이 있기 때문에 package.json이 변경되지 않으면 패키지를 다시 받지 않음

## volume
copy는 복사해서 컨테이너에 넣지만 volume는 컨테이너가 로컬 파일을 참조(매핑)함