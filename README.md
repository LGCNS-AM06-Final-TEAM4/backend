# 리테일 도메인 최종 프로젝트 backend

LG CNS AM Inspire Camp 6기 최종 프로젝트 4조의 백엔드 레포입니다. 도메인은 리테일이고 멘토는 이상헌 멘토님입니다.

주제는 아직 정하는 중입니다. 팀이 확정하면 이 문서에 프로젝트 소개와 주요 기능을 채웁니다.

## 레포 구성

프론트엔드와 백엔드는 레포를 나눕니다. 이 레포에는 MSA 서비스 전부를 Gradle 멀티 모듈로 두고, Config Server가 읽는 설정 파일은 별도 레포에 둡니다.

```
frontend   React + Vite                       (별도 레포)
backend    이 레포
├─ discovery   Eureka
├─ gateway     Spring Cloud Gateway, JWT 검증
├─ config      Config Server
├─ ai          Spring AI (ChatClient, 툴 호출)
├─ 업무 서비스  주제 확정 후 결정
├─ common      서비스가 같이 쓰는 코드
└─ infra       Dockerfile, docker-compose, 배포 설정
config     Config Server 설정 파일             (별도 레포)
```

모듈 골격은 주제와 서비스 분리가 정해진 뒤 만듭니다.

## 기술 스택

수업에서 직접 다룬 스택을 기준으로 정했습니다. 주제 확정 후 조정할 수 있습니다.

| 영역 | 기술 |
| --- | --- |
| 언어·프레임워크 | Java 21, Spring Boot 3.5.x, Spring Cloud 2025.0, Gradle 멀티 모듈 |
| MSA | Eureka, Spring Cloud Gateway, Config Server, OpenFeign, Kafka, Resilience4j |
| 데이터 | MariaDB, Spring Data JPA, Redis |
| AI | Spring AI |
| 관측 | Micrometer, Prometheus, Grafana, Zipkin |
| 배포 | Docker, GitHub Actions, AWS EC2 |

## 협업 규칙

브랜치, 커밋, PR, 리뷰 규칙은 [docs/협업규칙.md](docs/협업규칙.md)에 있습니다. 처음 합류하면 이 문서부터 읽어 주세요.

## 로컬 실행

서비스 코드가 올라오면 `infra/`의 docker-compose 기준으로 채웁니다.
