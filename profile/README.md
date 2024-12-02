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

<img width="478" alt="image" src="https://github.com/user-attachments/assets/404b2569-2d02-4ed4-b9ae-7a0b502590a5"><img width="473" alt="image" src="https://github.com/user-attachments/assets/94fabc9c-c261-4716-b894-1022cffa0a00">


**[ System Configuration ]**
- **프론트엔드**: **React** 프레임워크로 JavaScript 기반의 반응형 웹 인터페이스를 구축하여, UI/UX를 구현하였습니다.
- **백엔드**: Java를 기반으로 한 **Spring Framework**와 **Spring Boot**로 견고하고 확장 가능한 서버 아키텍처를 설계했습니다.
- **데이터베이스**: DB 엔진은 **MySQL 8.4.0** 버전을 이용합니다.

> 1) 웹과 서버와 통신 시, **Jwt Token**을 이용하여 유저의 인증 및 인가가 진행됩니다.
>  2) 서버에서 데이터베이스 접근 시 JPA(ORM)을 구현한 **Hibernate**를 이용하며 MySQL과 연동하여 데이터를 저장 및 이용합니다.
> 3) **API**를 제공하는 사람인과 유튜브, 유데미는 OpenAPI를 통해 정보를 얻습니다.
> 4) API를 제공하지 않는 잡플래닛, 잡코리아, 인프런은 **Selenium**을 통해 플랫폼과 상호작용합니다.

**[ CI/CD ]**
1. GitHub에 Push 후 Merge가 되면 Github Actions의 CI/CD 파이프라인을 이용합니다.
2. Github에 파일을 통해 빌드 후, Docker 이미지를 빌드하고 Docker Hub에 이를 Push 합니다.
3. Github Actions는 서버가 배포된 EC2에 SSH 접속하여 Docker Hub로 부터 이미지를 Pull 후, 컨테이너를 실행합니다.

**[ AWS ]**
1. 서버는 EC2 컨테이너에서 작동되고, 클라이언트는 S3 기반의 CloudFront 서비스를 통해 작동됩니다.
2. 보안을 위한 HTTPS 적용을 위해 SSL은 ACM을 이용하고, Route 53을 통해 도메인과 연결 후, EC2와 S3에 각각 연결합니다.
3. 서버의 HTTPS 사용을 강제하기 위해 EC2는 로드밸런서를 통해 HTTP/80 접속 시, HTTPS/443으로 리다이렉트 되도록 지정합니다.
4. 클라이언트의 HTTPS 사용을 강제하기 위해 CloudFront의 설정을 HTTPS로 리다이렉트 되도록 지정합니다.







### Branch Strategy
깔끔한 개발 프로세스를 유지하기 위해 **GitHub Flow** 브랜치 전략을 사용합니다. 각 기능이나 수정 사항은 별도의 브랜치에서 개발되며, **Pull Request**를 통해 메인 브랜치에 병합됩니다. 일관성을 위해 **PR 템플릿**을 사용하여 주요 변경 사항을 명확히 하고, 팀원들이 효율적으로 **코드 리뷰**를 진행할 수 있도록 지원합니다. 이 방식은 코드 품질을 유지하고 협력적인 개발을 촉진합니다.

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
### Backend
1. 영상 추천 페이지에서 **영상이 보이지 않거나**, **개발환경의 더미 데이터가 함께 보이는 문제**를 해결.( [#117: 영상 추천을 보여주는 페이지의 오류 잡기](https://github.com/ICT-Dev-Route/Dev-Route-BE/issues/117))
   - **개발 및 운영 환경 분리**
       - 기존에는 `application.properties`에서 수동으로 프로파일을 설정하여 RDS에 데이터가 중복 저장되는 문제가 있었습니다.
       - 이를 해결하기 위해 `application-dev.properties`와 `application-prod.properties` 파일로 환경을 분리하여, 각 환경에 맞는 설정이 자동으로 적용되도록 개선했습니다.
2. CI/CD 시 **CPU 사용률 및 메모리 사용 문제**를 해결.([#125:CPU사용률 제어](https://github.com/ICT-Dev-Route/Dev-Route-BE/issues/115))
     - **CI/CD 개선을 통한 CPU 부하 완화**
       - Docker 빌드 시 캐싱을 적용해 빌드 시간을 단축하고, DockerHub에서 이미지를 Pull한 후 CPU 사용률 제어를 통해 CI/CD 과정에서의 부하를 줄였습니다.
     
    | 항목                | 기존 방식                                | 변경 후 설정                                      |
    |---------------------|------------------------------------------|---------------------------------------------------|
    | **CI/CD 시간 단축** | 캐싱 미적용, 긴 빌드 시간                | 캐싱 도입으로 CI/CD 시간 55.37% 개선               |
    | **CPU 사용률**      | 최대 97% 도달                            | 개선 후 약 53.6% 감소                              |
3. Selenium의 높은 대기 CPU 점유율을 **24%** 감소. ([크롤링 최적화](https://acoustic-rest-b1b.notion.site/11564b4a4ab48050ad58e0bb688d2e3e?pvs=4))
   - Prometheus를 통한 모니터링 지표를 통해 크롤링 진행 후 장기적으로 CPU 점유율이 상승하는 것을 발견
   - 초기 설정을 통해 Selenium Driver가 활성화된 상태에서 CPU를 지속적으로 점유
   - `Spring AOP`을 통해 크롤링이 진행된 로직 수행 후 자동으로 quit()을 수행하도록 설정

    | 항목                | 기존 방식                                | 변경 후 설정                                      |
    |---------------------|------------------------------------------|---------------------------------------------------|
    | **Live Thread Count** (현재 실행 중인 모든 스레드의 수) | 31 Threads             | 27 Threads (-4)              |
    | **Daemon Thread Count** (백그라운드 실행 중인 스레드의 수)      | 26 Threads                     | 22 Threads (-4)       |


## 9. Insights and Reflections

## 10. Presentation
[Google Slids](https://docs.google.com/presentation/d/1bHuITo0p8zitikeNWGA1nkG0hogWINJidQZ33G7mzbo/edit#slide=id.gd431007ba2_0_208)
