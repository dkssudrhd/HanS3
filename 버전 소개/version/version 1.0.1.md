## version 1.0.1 진행 과정

1. API 명세서 구현
2. ERD 구현

## 과정 중 문제점 및 해결과정

### 문제
- API 명세서 도입 요망
  - 내가 만든 Rest API를 잘 정리 해줄 것들이 필요
- ERD의 관계문제
  - API Member가 한개라서 만약 비밀번호를 잊었을 경우 다시 사용할 수 가 없음(API member의 Password가 암호화 되어 들어가서)

### 해결방법
- API 명세서 도입
  - Swagger와 Rest Docs를 함께 사용한 API 명세서 도입
    - 서로의 장점과 단점을 생각하여 도입
    - [내용 정리 블로그]([https://github.com/user-attachments/assets/296733b1-10d7-4d65-98f4-722970c7d2da](https://velog.io/@dkssudrhd/API-%EB%AA%85%EC%84%B8%EC%84%9C%EB%8A%94-%EB%AD%90%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%B4%EC%95%BC-%ED%95%98%EC%A7%80))
- ERD의 관계문제
    - API Member의 Password를 암호화 하여 DB에 저장 -> 다시 확인할 방법이 없음
      - 해결법은 2가지인데 새로운 Password로 변경 -> 그럼 이전에 돌아가던 것들이 안돌아감...
      - 그럼 관계를 변경 -> 이걸로 선택
    - Member API 가 이전에는 1:1 관계 였음 하지만 -> 1:n으로 변경
      - 추가적으로 team과 연결된 관계를 ApiMember에서 Member로 변경 
