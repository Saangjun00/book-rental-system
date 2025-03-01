# 도서 대여 시스템(도서관)

## 👥 팀원 소개
| 이름 | Github |
| --- | --- |
| 김상준 | https://github.com/Saangjun00 |
| 김민석 | https://github.com/MinSeuk00 |
| 백민철 | https://github.com/baekmincheol |

---

## 기술 스택

| 분류 | 활용 기술 및 프레임워크 |
| ----- | ---- |
| **Programing** | Java |
| **Frontend** | HTML, CSS, JavaScript, Bootstrap |
| **Backend** | Spring, Spring Security, Spring Data JPA, Hibernate |
| **Database** | MariaDB |
| **Collaboration** | GitHub |

---

## 주요 기능

- **회원가입**:
  - Spring Security를 사용한 암호화 기능

- **로그인**:
  - 사용자 인증 정보를 통해 로그인

- **프로필 기능**:
  - 회원 정보 및 패널티 포인트, 패널티 해제일 조회 기능

- **관리자 기능**:
  - 관리자 페이지
  - 도서 관리(등록 및 삭제)
  - 회원 관리(회원 전체 목록 조회, 검색)
  - 대여 관리(전체 대여 목록 조회, 전체 연체 목록 조회, 전체 과거 대여목록 조회) 

- **도서 대여**:
  - 도서 목록 조회
  - 도서 대여 기능(조건에 따른 대여 가능 여부 체크 - 대여, 대여중, 대여 불가)

- **대여 목록**:
  - 도서 반납
  - 사용자 대여 목록 조회
  - 사용자 과거 대여 목록 조회

- **인기 도서 목록**:
  - 빌린 도서 횟수에 따른 책 순위 목록
 
- **패널티 적용**
  - 반납 예정일이 지나가면 매일 패널티 포인트 1P씩 부과되며 3일차부터는 등차수열을 적용하여 패널티 점수 부과
  - 패널티 점수가 1P 이상 있을시 연체자로 구분하여 도서 대여 불가
  - 반납 완료 시 매일 패널티 포인트 1P씩 차감하여 0P 도달시 연체자 해제
 
---

## 화면 구성
| 메인 페이지 | 도서대여 페이지 |
| ----- | ----- |
| ![image](https://github.com/user-attachments/assets/08774e5b-3fb9-47cc-a9c6-611dfafc7dc0) | ![image](https://github.com/user-attachments/assets/6c3169dc-ec95-49d3-bba8-bfac6eebc028) |
| **대여 기록 페이지** | **관리자 페이지** |
| ![image](https://github.com/user-attachments/assets/b4a0515a-574b-42ac-9c60-428a2692f263) | ![image](https://github.com/user-attachments/assets/d74c2c32-a916-4169-b9cc-9651d3d9a6fd) |
| **회원 관리 페이지(관리자)** | **도서 관리 페이지(관리자)** |
| ![image](https://github.com/user-attachments/assets/f92ed058-d98a-4bc1-bd3a-60ed22cb421c) | ![image](https://github.com/user-attachments/assets/7fc3b3eb-4228-44fc-a13d-f39482da9253) |
| **대여 관리 페이지(관리자)** | |
| ![image](https://github.com/user-attachments/assets/9bf57f96-94c2-4b6c-890d-4f337621f14b) | |

## 디렉토리 구조
```bash
│  .gitattributes
│  .gitignore
│  build.gradle
│  gradlew
│  gradlew.bat
│  HELP.md
│  settings.gradle
│          
└─src
    ├─main
    │  ├─java
    │  │  └─com
    │  │      └─example
    │  │          └─bookrentalsystem
    │  │              │  BookRentalSystemApplication.java
    │  │              │  
    │  │              ├─config
    │  │              │      PasswordConfig.java
    │  │              │      SecurityConfig.java
    │  │              │      
    │  │              ├─controller
    │  │              │      AdminController.java
    │  │              │      AuthController.java
    │  │              │      HomeController.java
    │  │              │      MemberController.java
    │  │              │      RentalController.java
    │  │              │      
    │  │              ├─dto
    │  │              │      BookRentalDto.java
    │  │              │      BookRequestDto.java
    │  │              │      MemberDto.java
    │  │              │      SignupRequestDto.java
    │  │              │      
    │  │              ├─entity
    │  │              │      Book.java
    │  │              │      Member.java
    │  │              │      Rental.java
    │  │              │      RentState.java
    │  │              │      Role.java
    │  │              │      
    │  │              ├─repository
    │  │              │      BookRepository.java
    │  │              │      MemberRepository.java
    │  │              │      RentalRepository.java
    │  │              │      
    │  │              └─service
    │  │                      BookService.java
    │  │                      MemberDetailsService.java
    │  │                      MemberService.java
    │  │                      RentalService.java
    │  │                      
    │  └─resources
    │      │  application-test.properties
    │      │  application.properties
    │      │  
    │      ├─static
    │      └─templates
    │          │  home.html
    │          │  
    │          ├─admin
    │          │      bookList.html
    │          │      home.html
    │          │      memberList.html
    │          │      rentalList.html
    │          │      
    │          ├─fragments
    │          │      footer.html
    │          │      header.html
    │          │      
    │          ├─member
    │          │      login.html
    │          │      profile.html
    │          │      signup.html
    │          │      
    │          └─rental
    │                  history.html
    │                  rentalBook.html
```
                            




