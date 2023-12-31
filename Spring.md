# Spring 혼자 공부한 것 


1. **프로젝트 생성**
   - `new -> spring legacy project -> 서버체크 -> 실행 -> home world!`
   - `pom.xml`: 의존성 관리, 라이브러리 등...

2. **MyBatis 설정**
   - `mapper` -> `xml`
   - DB 쿼리와 SQL 매핑, 동적 SQL

3. **Web 설정**
   - `web.xml` -> `servlet-context` -> `root-context`
   - CSS 관련 매핑, DB 접속 URL

4. **DAO 생성**
   - 인터페이스: 데이터베이스와의 통신을 처리
   - Mapper: 데이터베이스와 연결 및 데이터베이스 엑세스를 전담하는 클래스

5. **VO 생성**
   - 데이터의 구조를 나타내는 객체
   - 접근 권한 설정(private)
   - 빈 생성자, getter, setter

6. **Service 생성**
   - `@Autowired`로 DAO 의존성 주입
   - 예외 처리 고려
   - 인터페이스와 구현체(ServiceImpl) 모두 작성

7. **Controller 생성**
   - Service 의존성 주입
   - URL mapping
   - 요청 처리, 모델 데이터
   - `@RequestMapping`, `@PostMapping`, `@ResponseBody`

8. **기타**
   - `log4j` 파일은 로그 기록에 사용
   - Controller에서는 사용자 입력 처리와 응답에만 집중하고, Service에서는 실제 기능 제공
   - XML 파일에 오라클 DB 쿼리 작성

9. **Service 인터페이스 및 구현체 작성 규칙**
   - Service 인터페이스에는 메서드 선언만
   - Service 구현체(ServiceImpl)에는 실제 코드 작성
   - 인터페이스와 구현체에 동일한 메서드 선언 필요

   ```java
   // 예시
   // ServiceImpl
   public void freeWrite(FreeBoardVO freeboard) throws Exception {
       int result = dao.freeWrite(freeboard);
       if(result == 0) {
           throw new Exception();
       }
   }

   // Service 인터페이스
   public void freeWrite(FreeBoardVO freeboard) throws Exception;
