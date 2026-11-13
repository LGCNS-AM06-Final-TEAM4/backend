# infra

서비스 이미지를 만드는 Dockerfile, 로컬에서 전체를 띄우는 docker-compose, GitHub Actions 배포에 쓰는 설정을 둡니다.

AWS 자격 증명과 DB 비밀번호는 GitHub Secrets와 `.env`로만 관리하고 커밋하지 않습니다.
