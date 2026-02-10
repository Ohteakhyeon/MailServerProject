# MailServerProject
메일서버 구축 프로젝트: Rocky9 + Postfix/Dovecot/Roundcube, SES 릴레이로 Gmail/네이버 발송 검증(SPF/DKIM/DMARC PASS)

## 프로젝트 목표
- Rocky 9 기반 메일서버 구축
- 외부(Gmail/Naver) 수신/발송 + 첨부파일
- 발송은 Amazon SES SMTP 릴레이로 전달률 확보

## 아키텍처(다이어그램 링크 널거임)

## 주요 기능 체크리스트
- SMTP 수신(25), Submission(587), IMAPS(993), Webmail(443)
- SPF/DKIM/DMARC PASS
- Bounce/Complaint 처리(선택)

## 빠른 재현 가이드(최소 단계 링크)
- Route53 DNS -> EC2 -> Postfix -> Dovecot -> Roundcube -> TLS -> SES relay -> 테스트

## 테스트 결과(스크린샷/ 증거 링크?)
- Gmail "원본 보기" 에서 SPF/DKIM/DMARC PASS 캡처

## 보안/운영
- fail2ban, 로그 위치, 백업/복구 개요