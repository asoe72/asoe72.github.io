---
title: "MongoDB 설치와 데이터베이스 생성"
date: 2019-09-28 09:54:00 -0400
categories: MongoDB
---

MongoDB를 설치한다. 운영체계와 설치한 MongoDB 버전은 각기 아래와 같다.

    Windows 10 Home 64bit

    MongoDB Server
    Version 3.6.13

윈도우의 `환경변수 - 시스템 변수`에 아래를 추가한다.

```dos
C:\Program Files\MongoDB\Server\3.6\bin
```

데이터베이스들을 보관할 폴더 `mongo_db/`를 생성한다. 서브 폴더로 `mongo_db/local/`을 만든다.

이제 `mongo_db/`에 아래와 같이 daemon(서버)을 실행할 배치파일 `mongodb_start.bat`을 만든다.

```dos
mongod --auth --dbpath e:/mongo_db/local
```

`mongodb_start.bat`을 실행하면, port 27017에서 connection을 대기한다는 메시지가 나온다.

이제, 명령 프롬프트를 열고 mongoDB shell을 실행한다.

```dos
mongo
```

- 참고자료 : Do it! Node.js 프로그래밍
