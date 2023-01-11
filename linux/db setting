## 테이블 생성
```sql
CREATE DATABASE '테이블명'
```

## 사용자명 생성
```sql
-- 내부 접근만 허용
CREATE USER '사용자명'@'localhost' IDENTIFIED BY '비밀번호';
-- 외부 접근을 허용
CREATE USER '사용자명'@'%' IDENTIFIED BY '비밀번호';
```

## 테이블 권한 부여
```sql
-- 모든 데이터베이스의 모든 테이블 모든 권한 부여
GRANT ALL PRIVILEGES ON DB명.* TO '유저명'@'%';
-- 특정 데이터베이스의 모든 테이블 모든 권한 부여
GRANT ALL PRIVILEGES ON DB명.* TO '유저명'@'%';
-- 특정 데이터베이스의 특정 테이블에 모든 권한 부여
GRANT ALL PRIVILEGES ON DB명.테이블명 TO '유저명'@'%';
```

## 사용자 삭제
```sql
DROP USER '사용자명'@'%';
```

## 권한 설정 reload
```sql
FLUSH PRIVILEGES;
```
