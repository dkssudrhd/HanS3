
### 1.0.0 버전
![ERD 1.0.0](https://github.com/dkssudrhd/HanS3/blob/main/ERD/hanCloud.png)

> - 회원과 API 회원을 나눠 나중에 Member 회원만 따로 데이터베이스를 활용할 수 있도록 확장성을 예비한 설계
> - 그룹으로 저장소를 구분하도록 설정
> - 회원을 여러 그룹에 들어갈 수 있도록 구성
> - 저장소 마다 모든 이용자에게 어떤 권한을 줄지 설정 (읽기만, 모든 권한)

### 1.0.1 버전
![hanCloud](https://github.com/user-attachments/assets/0a2f7463-672d-4994-b163-5c93b7a0b998)

> - group을 team으로 table 이름 변경
> - team을 member와 연결시킴
> - api password를 암호화 시켜 넣음
> - member가 여러개의 api member를 얻을 수 있도록 관계를 1대 다로 변경
> - 필요한 칼럼들 추가
