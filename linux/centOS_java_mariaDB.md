## 최신 업데이트 적용
```
$ yum update
```
## 설치된 JDK 확인
```
$ yum list installed *jdk-devel
```
## 설치가능한 JDK 확인
```
$ yum list *jdk-devel
```
## Java 설치
```
$ yum -y install java-1.8.0-openjdk-devel.x86_64
```

## javac 위치 확인
```
$ which javac
```

## 해당 링크에서 원본 파일 위치 확인
```
$ readlink -f /usr/bin/javac
```
## 3. 환경변수 잡아주기
```
$ vim /etc/profile
```

## 파일 맨 아래에 아래 내용 추가
```
$ export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.345.b01-1.el7_9.x86_64
$ export PATH=$JAVA_HOME/bin:$PATH
```

## 적용
```
$ source /etc/profile
```

## mariaDB 설치
```
$ yum install mariadb mariadb-server
```

## 서비스 시작
```
$ systemctl start mariadb
```

## 확인
```
$ netstat -tnlp
```

## 미설치 시 설치
```
$ yum install net-tools
```
