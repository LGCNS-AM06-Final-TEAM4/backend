# 리테일 도메인 최종 프로젝트

LG CNS AM Inspire Camp 6기 최종 프로젝트 4조 레포입니다. 도메인은 리테일이고 멘토는 이상헌 멘토님입니다.

주제는 아직 정하는 중입니다. 1회차 멘토링(11.14)에서 가안을 검토한 뒤 팀이 확정하면 이 문서에 프로젝트 소개와 주요 기능을 채웁니다.

## 기술 스택 (멘토 계획서 기준, 주제 확정 시 조정)

| 영역 | 기술 |
| --- | --- |
| Frontend | React, TypeScript |
| Backend | Spring Boot |
| AI | FastAPI, LLM API, RAG |
| DB | PostgreSQL |
| Infra | AWS (ECS, RDS, S3), Docker, GitHub Actions |

## 폴더 구조

```
frontend/   웹 화면
backend/    업무 API
ai/         AI 서비스
infra/      docker-compose, 배포 설정
data/       정답셋, 전처리 스크립트 (원본 데이터는 커밋하지 않음)
docs/       협업 규칙, 설계 문서
```

서비스를 한 레포에서 관리합니다. API 규격이 바뀔 때 FE·BE·AI를 한 PR에서 같이 고칠 수 있고, 이슈와 Projects 보드가 한곳에 모이기 때문입니다.

## 협업 규칙

브랜치, 커밋, PR, 리뷰 규칙은 [docs/협업규칙.md](docs/협업규칙.md)에 있습니다. 처음 합류하면 이 문서부터 읽어 주세요.

## 로컬 실행

서비스 코드가 올라오면 `infra/`의 docker-compose 기준으로 채웁니다.
