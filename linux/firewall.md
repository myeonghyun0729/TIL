## 방화벽 상태
firewall-cmd --state

## 방화벽 reload
firewall-cmd --reload

## 방화벽 설정 목록 확인
firewall-cmd --list-all


## 서비스 추가
firewall-cmd --permanent --zone=public --add-service=서비스명

## 서비스 삭제
firewall-cmd --permanent --remove-service=서비스명


## 특정 포트 허용 설정
firewall-cmd --permanent --add-port=8080/tcp

## 등록된 포트 삭제
firewall-cmd --permanent --remove-port=8080/tcp

## 포트 구간 접근 허용 설정
firewall-cmd --permanent --add-port==8000-9000/tcp

## 포트 구간 접근 삭제
firewall-cmd --permanent --remove-port==8000-9000/tcp


## 특정 IP 허용 설정
firewall-cmd --permanent --add-source=192.111.1.1

## 특정 IP 차단 설정
### drop : 응답을 해주지않고 차단
firewall-cmd --add-rich-rule='rule family="ipv4" source address=192.111.0.1 drop'

### reject : 차단되었다고 응답
firewall-cmd --add-rich-rule='rule family="ipv4" source address=192.168.0.2 reject'

## 특정 IP 특정 포트 허용 설정
firewall-cmd --permanent --add-rich-rule='rule family="ipv4" source address=192.111.0.1 port port="80" protocol="tcp" accept'
firewall-cmd --permanent --add-rich-rule='rule family="ipv4" source address=192.111.0.1 port port="8080" protocol="tcp" accept'
