# 스프링 JDBC로 데이터베이스와의 연동 설정하기
JDBC(Java Database Connectivity)는 대부분의 개발자가 쉽게 이해할 수 있는 데이터 액세스 기술. 스프링에서 제공하는 JDBC는 기존 JDBC의 장점과 단순함을 유지하면서 단점을 보완. 간결한 API뿐만 아니라 확장된 JDBC의 기능도 제공.

한개의 XML 파일에서 모든 빈을 설정하면 복잡해서 관리하기 어려움. 빈의 종류에 따라 XML 파일에 나누어 설정.
```
// 여러 설정 파일을 읽어 들이기 위해 스프링의 ContextLoaderListener를 설정
<listener>
  <listener-class>
    org.springframework.web.context.ContextLoaderListener
  </listener-class>
</listener>
```

# JdbcTemplate 클래스 이용해 회원 정보 조회
|기능|메서드|
|:--:|:--:|
|insert, update, delete관련 메서드|int update(String query), int update(String query, Object[] args), int update(String query, Object[] args, int[] argTypes)|
|select 기능 메서드|int queryForInt(String query), int queryForInt(String query, Object[] args), long queryForLong(String query), long queryForLong(String query, Object[] args), Object queryForObject(String query, Class requiredType), List queryForList(String query), List queryForList(String query, Object[] args)|

