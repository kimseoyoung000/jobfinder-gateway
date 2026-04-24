# JobFinder — API Gateway (Spring Cloud Gateway)

> JobFinder 구인구직 플랫폼의 API Gateway 서비스  
> 단일 진입점으로 JWT 검증 및 서비스 라우팅 담당

## 역할

- 클라이언트의 모든 요청을 단일 진입점(포트 8000)으로 수신
- Eureka Discovery를 통해 서비스 조회 후 URL 기반 라우팅
- `/user-service/**` → Main Service (8001)
- `/board-service/**` → Board Service (8002)

## 관련 레포지토리

| 서비스 | 레포 | 포트 | 역할 |
|--------|------|------|------|
| Main Service | [jobfinder-main](https://github.com/kimseoyoung000/jobfinder-main) | 8001 | 회원/채용/이력서/지원 |
| Board Service | [jobfinder-board](https://github.com/kimseoyoung000/jobfinder-board) | 8002 | 게시판/커뮤니티 |
| API Gateway | [jobfinder-gateway](https://github.com/kimseoyoung000/jobfinder-gateway) | 8000 | 라우팅/JWT 검증 |
| Discovery | [jobfinder-discovery](https://github.com/kimseoyoung000/jobfinder-discovery) | 8761 | 서비스 등록/조회 |

## 기술 스택

| 구분 | 기술 |
|------|------|
| Framework | Spring Cloud Gateway |
| Discovery | Eureka Client |
| Port | 8000 |
