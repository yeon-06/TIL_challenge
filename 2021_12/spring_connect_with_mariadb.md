### โ org/mariadb/jdbc/Driver : Unsupported major.minor version 52.0 
๐ Java์ MariaDB ๋ฒ์  ๋ง์ถ๊ธฐ (๋ฒ์  ํ์ธํ๋ ๊ณณ)

### โ Driver com.mysql.cj.jdbc.Driver claims to not accept jdbcUrl
๐ ํด๊ฒฐ1) application.properties์์ ์ค์ ํ url์ ์คํ ์๋์ง ํ์ธ  
๐ ํด๊ฒฐ2) localhost์ ๊ฒฝ์ฐ ์๋์ ๊ฐ์ด ์ค์ ํด์ผ ํจ  

```
spring.datasource.url=jdbc:mysql://localhost.com:3306/DB๋ช
```

### โ No session repository could be auto-configured, check your configuration (session store type is 'jdbc')
๐ application.properties์์ 'spring.session.store-type' ์ ๊ฑฐ

### โ java.sql.SQLNonTransientConnectionException: Could not connect to address=(host=XXXXXXX)(port=3306)(type=master) : Socket fail to connect to host:XXXXXXX, port:3306.
#### ์์ ์์ธ1
: DB ์๋น์ค๊ฐ ์ข๋ฃ๋์ด ์์ ๋๋ ์ ์ํ  DB์ ์ฃผ์๋ฅผ ์๋ชป ์๋ ฅ    
๐ DB๊ฐ ์ ์์ ์ผ๋ก ๊ตฌ๋์ค์ธ์ง ํ์ธ

#### ์์ ์์ธ2
: ๊ณ์ ์ ๋ํด ์ ๊ทผ ๊ถํ์ด ์์  
๐ application.properties์ ์ ์ ๊ณ์ ์ ๊ถํ ํ์ธ

#### ์์ ์์ธ3
: MariaDB์ ์ธ๋ถ IP ์ ์์ด ๋ถ๊ฐ๋ฅ ๐ 50-server.conf ํ์ผ์์ bind-address๋ฅผ 0.0.0.0(์ ์ฒด ๊ณต๊ฐ)๋ก ๋ณ๊ฒฝ  

***
### ์ถ์ฒ
1. https://stackoverflow.com/questions/62797182/driver-com-mysql-cj-jdbc-driver-claims-to-not-accept-jdbcurl
2. https://stackoverflow.com/questions/50941891/spring-session-boot-error-no-session-repository-could-be-auto-configured-chec
3. https://tyrannocoding.tistory.com/42
4. https://www.lesstif.com/dbms/mysql-client-port-113347417.html
5. https://serverfault.com/questions/844103/why-is-mysql-connecting-through-socket-even-though-im-specifying-host-and-port
