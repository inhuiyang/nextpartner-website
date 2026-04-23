# 넥스트파트너 웹사이트

> 50·60대 시니어를 위한 AI 맞춤 채용 플랫폼 — 프로토타입 (HTML/CSS/JS)

## 페이지 구조

| 파일 | 설명 |
|------|------|
| `index.html` | 메인 홈 — 이벤트 배너, AI 추천 공고, 공공 일자리, 콘텐츠 가이드, 소식 |
| `login.html` | 로그인 — 전화번호+비밀번호, 카카오/네이버 소셜 로그인 |
| `signup.html` | 회원가입 — 3단계 플로우 (ID/PW → 전화인증 → 약관동의) |
| `resume.html` | AI 이력서 만들기 — 5단계 체크리스트 + AI 생성 + 결과 확인 |
| `jobs.html` | 일자리 찾기 — AI추천 / 일반 / 공공 탭, 필터, 정렬 |
| `mypage.html` | 내 계정 — 이력서 관리, 지원현황, 면접현황, 구직활동확인서, 저장공고 |
| `styles.css` | 공통 디자인 시스템 (토큰 + 전체 컴포넌트) |

## 디자인 시스템

디자인 시스템 소스: `nextpartnerds` (별도 디렉토리)

### 주요 토큰

```css
--color-primary-500: #ff7f65   /* 메인 CTA 컬러 */
--color-neutral-900: #1a1a1a   /* 본문 텍스트 */
--font-base: 'Pretendard Variable'
```

### 시니어 UX 원칙
- 기본 폰트: **18px** (가독성 우선)
- 버튼 최소 높이: **48px** (터치 타겟)
- 모바일: 하단 바텀 내비게이션 (홈 / 공고찾기 / 이력서 / 내계정)
- 데스크탑: 상단 헤더 + 3탭 (AI추천 / 일반 / 공공)

### AI 관련 컴포넌트
- `match-badge` — AI 매칭 퍼센트 배지 (그라디언트)
- `reason-sentence` — 추천 이유 문장 (보라색 사이드바)
- `gradient-ai` — AI 강조 그라디언트 (`#ff7f65 → #a855f7 → #3b82f6`)

## 로컬 실행

별도 서버 불필요. `index.html`을 브라우저에서 바로 열면 됩니다.

```
nextpartner-website/
├── styles.css
├── index.html
├── login.html
├── signup.html
├── resume.html
├── jobs.html
└── mypage.html
```

## 기능명세서 매핑

| 명세 번호 | 기능 | 구현 파일 |
|-----------|------|-----------|
| 1. 회원가입 | 3단계 가입 플로우, 전화인증, 소셜 | `signup.html` |
| 2. AI 추천 공고 | 매칭 배지, 추천 이유, 피드백 | `jobs.html`, `index.html` |
| 3. 로그인 | 전화+PW, 소셜, 비밀번호 찾기 | `login.html` |
| 4. AI 이력서 | 체크리스트 플로우, OCR, AI 생성 | `resume.html` |
| 5. 메인 홈 | 배너, 추천공고, 공공, 가이드, 소식 | `index.html` |
| 6. 내 계정 | 이력서관리, 지원/면접현황, 확인서 | `mypage.html` |
