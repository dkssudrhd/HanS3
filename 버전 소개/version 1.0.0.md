## version 1.0.0 진행 과정

1. 서버에 파일 저장 구현
2. 서버에 파일 삭제 구현
3. url을 통해 파일 읽기 구현
4. url을 통해 파일 다운로드 구현
5. jenkins를 사용하여 ci/cd 구현

## 과정 중 문제점 및 해결과정

### 문제
- 같은 폴더 안에 파일을 저장하면 이전에 있던 파일을 덮어서 저장해버림
  - 만약 a.jpg란 파일이 있으면 a.jpg란 다른 파일을 저장시 기존 파일이 없어짐
    
![저장방법1](https://github.com/user-attachments/assets/1c385d5f-21a5-4e26-98ee-a87f6d4d344c)

### 해결방법
- 폴더 저장시 미리 이름이 중복인지 확인하는 과정을 추가함
  - 중복일 시 예외처리

![저장방법2](https://github.com/user-attachments/assets/296733b1-10d7-4d65-98f4-722970c7d2da)
