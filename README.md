# CoachMate

운동전문가를 위한 AI 플랫폼

**업무는 AI에게, 본질에 집중**

## 서비스 구조

```
CoachMate
├── Smarter (더 스마트한 업무)
│   ├── 운동일지 AI
│   └── 식단관리 AI (준비 중)
└── Better (더 확실한 성장)
    ├── 교육 (준비 중)
    ├── 자격증 (준비 중)
    └── 채용 (준비 중)
```

## 프로젝트 구조

```
B1_CoachMate_Dev/
├── src/                    ← 프론트엔드 (배포되는 코드)
│   ├── index.html
│   ├── smarter.html
│   ├── coaching-log.html
│   ├── better.html
│   └── about.html
├── functions/              ← 백엔드 - Cloudflare Functions (추후)
├── docs/                   ← 내부 문서
│   ├── 1_business/         ← 사업 (비전, 시장, 페르소나)
│   ├── 2_product/          ← 제품 (PRD, 기능 정의)
│   ├── 3_design/           ← 디자인 (UI/UX)
│   ├── 4_engineering/      ← 개발 (기술 설계)
│   ├── 5_ai/               ← AI/데이터 (모델, 프롬프트)
│   ├── 6_marketing/        ← 마케팅 (GTM, 콘텐츠)
│   └── 7_legal/            ← 법률/윤리 (개인정보, 약관)
├── .gitignore
└── README.md
```

## 기술 스택

- 순수 HTML/CSS 정적 페이지 (JavaScript 없음)
- 서버/백엔드/DB 없음

## 배포

```
로컬 개발 (VSCode + Claude Code) → GitHub → Cloudflare Pages
```

- **GitHub** — 소스코드 버전 관리
- **Cloudflare Pages** — GitHub 연동, push 시 자동 배포 (빌드 출력: `src/`)
- **HTTPS** — Cloudflare SSL 인증서 자동 제공
- **CDN** — Cloudflare 글로벌 엣지 서버에서 서빙

배포 URL: https://coachmate.pages.dev/
