# VO 만들때 
1. 기본 생성자
2. ex) this.  =
  자기 자신의 데이터로 접근을 허용
3. 빈 생성자
4. setter / geteer
5. toString
   toString()메소드는 해당 인스턴스에 대한 정보를 문자열로 반환
   @Override
   override == 재정의
   하위클래스가 상위 클래스의 메서드를 구현하는 것을 의미
   상속관계에서 사용
   ex)부모 객체에 printerA라는 메서드가 있고 상속을 받은 객체에서 printerA를 재정의해서 쓰고 싶을때
      만약 printterAA라고 오타를 입력할경우 @Override가 붙어있다면 부모객체엔 이런 메서드가 없다고 에러가 남
      근데 만약 @Override 가 붙어있지 않다면 상속받은게 아니고 새로운 메서드를 만들어 쓴것이 때문에 에러가 나지 않음
   
