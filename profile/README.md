# 초보 개발자를 위한 플랫폼, DevRoute📚</h1>
## 1.Introduction
### Goal
> **DevRoute**는 초보 개발자들을 위해 직무별 로드맵과 기술 스택을 시각화해주는 플랫폼입니다. 이 프로젝트는 **초보 개발자**들이 목표를 명확하게 세우고 필요한 기술을 단계별로 익힐 수 있도록 돕기 위해 시작되었습니다.

### Feature
🚀**개발 로드맵 제공**<br>
처음 시작하는 개발자들을 위한 단계별 로드맵 제공, 쉽게 따라할 수 있는 가이드!

💼**채용공고 통합**<br>
여러 채용공고를 한눈에! 이해하기 쉬운 형태로 정리된 정보 제공.

🔍**기술 스택 분석**<br>
현재 시장에서 인기 있는 기술 스택을 한눈에 파악, 초보자도 쉽게 이해할 수 있게 구성.

🎓**학습 자료 추천**<br>
필요한 기술을 학습할 수 있는 유튜브 영상과 온라인 강의 추천.

## 2.Team

| **Front** | **Back** | **Back** | **Back** |
| :------: |  :------: | :------: | :------: |
| [<img src="https://avatars.githubusercontent.com/u/65596779?v=4" height=150 width=150> <br/> @heewon1104](https://github.com/heewon1104) | [<img src="https://avatars.githubusercontent.com/u/113831848?v=4" height=150 width=150> <br/> @Munhangyeol](https://github.com/Munhangyeol) | [<img src="https://avatars.githubusercontent.com/u/63222221?v=4" height=150 width=150> <br/> @mete0rfish](https://github.com/mete0rfish) | [<img src="https://avatars.githubusercontent.com/u/121409074?v=4" height=150 width=150> <br/> @maark1106](https://github.com/maark1106) |

## 3.Delopment Enviroment
- **Operating Systems**: Windows 11, macOS
- **IDEs**: IntelliJ, Visual Studio, AWS
- **Frameworks & Libraries**: Spring Framework, React
- **Languages**: Java, SQL, JavaScript
- **Version Control**: GitHub
- **Collaboration Tools**: Notion, Discord, Google Meet
- **Server & Database**: AWS EC2, RDS, Docker
- **CI/CD Pipeline**: GitHub Actions
- **Monitoring Tools**: Prometheus, Grafana

## 4. Technologies and Branch Strategy
### Technologies

### Branch Strategy

## 5.Main Logic

<h4>로그인 및 회원가입</h4>
<img src="https://github.com/user-attachments/assets/a4310ef9-d160-4924-9c7e-c430aac1a8f0" width="500"/>
<img src="https://github.com/user-attachments/assets/a4310ef9-d160-4924-9c7e-c430aac1a8f0" width="500"/>

<h4>메인 페이지</h4>
<img src="https://github.com/user-attachments/assets/02531176-4aa0-4a9b-b490-0869cede8b4f" width="500"/>

<h4>직군별 개발자 설명</h4>
<img src="https://github.com/user-attachments/assets/7713ba9a-b7a5-47b5-9792-392dcfc8f344" width="500"/>

<h4>개발자 로드맵</h4>
<img src="https://github.com/user-attachments/assets/dff83337-9e60-47c0-a132-e9c3ff4c5543" width="500"/>

<h4>기업 정보 검색</h4>
<img src="https://github.com/user-attachments/assets/904391a1-373f-41c9-913a-715091381993" width="500"/>

<img src="https://github.com/user-attachments/assets/5b98ce14-1bda-42f6-8890-fa68a3c3bf57" width="500"/>

<h4>채용 공고</h4>
<img src="https://github.com/user-attachments/assets/29fb4dfa-2d0d-42d4-9da8-856bde80f4ec" width="500"/>

<h4>개발 관련 추천 영상</h4>
<img src="https://github.com/user-attachments/assets/ea17fc0e-fcb7-46ac-811c-d99c5ff5d5d8" width="500"/>

<h4>문의사항</h4>
<img src="https://github.com/user-attachments/assets/879d556e-8066-45e0-a2cc-db1fd9848722" width="500"/>


## 6. Directory Structure
### Backend
```
.
└── devroute
    ├── api
    │   ├── suggestion
    │   └── visitorcount
    ├── bookmark
    │   ├── domain
    │   ├── exception
    │   └── json
    ├── company
    │   ├── controller
    │   ├── domain
    │   ├── dto
    │   ├── repository
    │   └── service
    ├── crawling
    │   └── dto
    ├── dataloader
    ├── global
    │   ├── aop
    │   │   ├── crawl
    │   │   └── timetrace
    │   ├── auth
    │   │   ├── filter
    │   │   └── jwt
    │   ├── config
    │   └── exception
    ├── recruitment
    │   ├── controller
    │   ├── domain
    │   ├── dto
    │   ├── enums
    │   ├── repository
    │   ├── service
    │   └── utils
    ├── roadmap
    │   ├── description
    │   ├── domain
    │   ├── dto
    │   ├── enums
    │   └── repository
    ├── user
    │   ├── domain
    │   ├── dto
    │   ├── enums
    │   └── service
    └── video
        ├── Repository
        ├── constans
        ├── domain
        ├── dto
        │   ├── infrean
        │   ├── udemy
        │   └── youtube
        ├── enums
        ├── exception
        ├── fetcher
        └── service
```

## 8. Trouble Shooting

## 9. Insights and Reflections
