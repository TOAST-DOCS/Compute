## Infrastructure > Compute & Network > MySQL Guide
# MySQL 이미지 상품 가이드

## MySQL version

##### NHN ENT 토스트 클라우드 MySQL version 은 아래와 같이 2가지로 분류 되어 제공 됩니다.

* MySQL Community Server 5.6.38
    * mysql-community-server-5.6.38-2.el6.x86_64
* MySQL Community Server 5.7.20
    * mysql-community-server-5.7.20-1.el6.x86_64

## MYSQL 시작/정지 방법

```
#mysql 서비스 시작
shell> service mysqld start

#mysql 서비스 중지
shell> service mysqld stop

#mysql 서비스 재시작
shell> service mysqld restart
```

## MYSQL 접속

#### 이미지 생성 후 초기에는 아래와 같이 접속합니다.

```
shell> mysql -uroot
```

## MYSQL 이미지 생성 후 초기 설정

### 1\. 패스워드 변경

### 초기 설치 후 MYSQL ROOT 계정 패스워드는 지정 되어 있지 않습니다. 그러므로 설치 후 반드시 바로 패스워드 변경이 필요 합니다

* MYSQL 5.6 버전 패스워드 변경

```
SET PASSWORD [FOR user] = password_option

mysql> set password=password('패스워드');
```

* MYSQL 5.7 버전 패스워드 변경

```
ALTER USER USER() IDENTIFIED BY 'auth_string';

mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY '새로운비밀번호';
```

### MYSQL 기본 validate\_password\_policy 는 아래와 같습니다\.

* validate\_password\_policy=MEDIUM
* 기**본 8자 이상, 숫자,소문자,대문자,특수문자**를 포함해야 함.

### 2\. PORT 변경

#### 제공되는 이미지 PORT 는 Mysql 기본 포트인 3306 입니다. 보안상 포트 변경을 권장 합니다.

```
shell> vi /etc/my.cnf


#my.cnf 파일에 사용하고자 하는 포트를 명시해 줍니다. 

port =사용하고자하는포트명


#vi 편집기 저장


#mysql 서비스 재시작


shell> service mysqld restart


#변경된 포트로 아래와 같이 접속


shell> mysql -uroot -P[변경된포트번호]
```

## my.cnf 설명

my.cnf 의 기본 경로는 /etc/my.cnf 이며, ToastCloud 권장 variable 이 설정 되어 있으며, 내용은 아래와 같습니다.

| 이름 | 설명 |
| --- | --- |
| default\_storage\_engine | 기본 Stroage Engine 을 지정합니다.InnoDB 로 지정되며  Online-DDL 과 Transaction 사용이 가능합니다. |
| expire\_logs\_days | binlog 설정으로 쌓이는 로그 저장일을 설정합니다. 기본 3일로 지정되어 있습니다. |
| innodb\_log\_file\_size | transaction 의 redo log 를 저장하는 로그 파일의 사이즈를 지정합니다. <br><br>실제 운영 환경에서는 256MB 이상을 권장하며, 현재 512MB 로 설정되어 있습니다 .설정값 수정시 DB 재시작이 필요합니다. |
| innodb\_file\_per\_table | 테이블이 삭제되거나 Truncate 될때, 테이블 스페이스 공간이 OS 로 바로 반납됩니다. |
| innodb\_log\_files\_in\_group | innodb\_log\_file 파일의 갯수를 설정하며 순환적\(Circular\) 으로 사용 됩니다\. 최소 2개 이상으로 구성됩니다\. |
| log_timestamps | MYSQL 5.7 의 기본  log 시간은  UTC 로 표시 됩니다. 그러므로 로그 시간을 SYSTEM 로컬 시간으로 변경합니다. |
| slow\_query\_log | slow\_query log 옵션을 enable 합니다\. long\_query\_time 에 따른 기본 10초 이상의 쿼리는 slow\_query\_log 에 남게 됩니다\. |
| sysdate-is-now | sysdate 의 경우 replication 에서 sysdate()사용된 SQL 문은 복제시 Master 와 Slave 간데 시간이 다르게 되는 문제점이 있어 sysdate() 와 now() 의 함수를 동일하게 적용합니다. |

## MYSQL 디렉토리 설명

MYSQL 디렉토리 및 파일 설명은 아래와 같습니다.

| 이름 | 설명 |
| --- | --- |
| my.cnf | /etc/my.cnf |
| DATADIR | MYSQL 데이터 파일 경로  - /var/lib/mysql/ |
| ERROR_LOG | MYSQL error_log 파일 경로  - /var/log/mysqld.log |
| SLOW_LOG | MYSQL Slow Query 파일 경로 -  <span style="color:#333333">/var/lib/mysql/*slow.log</span> |
