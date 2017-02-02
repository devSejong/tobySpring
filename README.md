# 토비의 스프링 튜톨리얼

## 기존 예제코드에서 변경된 점

환경설정의 부담을 최대한으로 줄여 코드에만 집중할 수 있도록 만들었습니다.

* 메이븐을 사용한 환경구성
** 단순한 설정을 유지하기 위함
** 의존관계에 신경쓰지 않기 위함임
* mySql 대신 h2를 사용
** 별도의 DB없이 바로 실행할 수 있도록 하기 위함임

## 프로젝트 작동방법

### DB설정하기

* 동봉된 `h2.jar`파일을 실행합니다.
* `http://localhost:8082`를 이용하여 `h2-console`에 접근할 수 있습니다.
    * 이때 URL은 `jdbc:h2:tcp://localhost/~/test` id는 `sa` 패스워드는 빈값으로 설정하여 실행하시면 됩니다.
* `schema`가 만들어져있지 않은 경우 아래의 table create 구문을 생성하여주세요.
 
 ```sql
create table users (
  id varchar(10) primary key,	
  name varchar(20) not null,
  password varchar(10) not null
)
 ```
 
 ### 프로젝트 실행하기
 
 * `UserDao`파일의 `main`메서드를 실행합니다.
 

