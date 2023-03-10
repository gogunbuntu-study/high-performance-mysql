# high-performance-mysql
MySQL 성능 최적화 : 고성능 시스템 구축을 위한 전략과 최적화 기법

# 실습 환경 세팅
- Docker 를 활용한 MySQL 실습 환경 세팅
1. docker desktop 설치 ([Docker 문서 참고](https://docs.docker.com/desktop/))
2. MySQL 컨테이너 실행 `docker run --name 컨테이너명 -e MYSQL_ROOT_PASSWORD=root비밀번호 -dit -p 3306:3306 mysql:latest`
3. Docker 컨테이너 내로 이동 `docker exec -it 컨테이너명 bash`
4. MySQL 접속 `mysql -u root -p`

# Sakila 데이터베이스 설정
1. Sakila 데이터베이스 파일 tar/zip 다운로드 ([출처](https://dev.mysql.com/doc/index-other.html))
2. Docker 컨테이너 내로 파일 이동 `docker cp 다운로드_경로/sakila-db/ 컨테이너명:/root/data/`
3. Docker 컨테이너 내로 이동 `docker exec -it 컨테이너명 bash`
4. MySQL 접속 `mysql -u root -p`
5. 파일 실행 
    - `SOURCE /root/data/sakila-schema.sql;`
    - `SOURCE /root/data/sakila-data.sql;`
