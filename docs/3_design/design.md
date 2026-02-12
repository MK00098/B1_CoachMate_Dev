# CoachMate 디자인 시스템

## 컨셉

**직관적, 스마트, 간결** — Apple 스타일

슬로건: `Be Smarter, Be Better.`

## 색상

| 이름 | HEX | 용도 |
|------|-----|------|
| White | `#ffffff` | 배경, 라이트 섹션, 버튼 (다크 배경) |
| Black | `#000000` | 다크 섹션 배경, 버튼 (라이트 배경) |
| Light Gray | `#f5f5f7` | 카드, Nav, Footer 배경 |
| Space Black | `#1d1d1f` | 메인 텍스트 |
| Space Gray | `#86868b` | 보조 텍스트 |
| Border | `#d2d2d7` | 테두리, 구분선 |
| Accent | `#667eea → #764ba2` | CTA 그라데이션 (운동일지) |

## 폰트

```css
font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'SF Pro Text', sans-serif;
```

## 반응형 — 3단계 Breakpoint (Apple 방식)

`clamp()` 대신 `@media` 고정값으로 단계별 제어.

### Breakpoint
| 이름 | 조건 | 대상 |
|------|------|------|
| Desktop (Large) | > 1068px | 기본값 |
| Tablet (Medium) | ≤ 1068px | `@media (max-width: 1068px)` |
| Mobile (Small) | ≤ 734px | `@media (max-width: 734px)` |

### 타이포그래피 — 3단계

| 요소 | Desktop | Tablet | Mobile |
|------|---------|--------|--------|
| Hero h1 | 4.5rem | 3.5rem | 2.5rem |
| Hero h2 | 1.5rem | 1.3rem | 1.1rem |
| Section h2 | 3.5rem | 2.8rem | 2.2rem |
| Section h3 | 1.4rem | 1.2rem | 1rem |
| Hero slogan | 1.1rem | 1rem | 0.9rem |
| 본문 (p) | 1rem | 1rem | 1rem |
| Nav 링크 | 0.85rem | 0.85rem | 0.85rem |
| Footer | 0.8rem | 0.8rem | 0.8rem |

> 큰 제목만 반응형, 본문/UI 텍스트는 고정.

### 레이아웃 — 3단계

| 요소 | Desktop | Tablet | Mobile |
|------|---------|--------|--------|
| Section padding | 80px | 60px | 40px |
| Section min-height | 500px | 400px | 300px |
| Page header padding | 60px | 50px | 40px |
| Page header min-height | 200px | 175px | 150px |
| Card padding | 32px | 26px | 20px |
| Card border-radius | 18px | 16px | 12px |
| Input padding | 14px | 12px | 10px |
| Button padding | 14px 24px | 12px 20px | 10px 16px |
| Nav-links gap | 28px | 28px | 16px |

## 고정값 요소

| 요소 | 값 | 비고 |
|------|-----|------|
| Nav 높이 | 44px | Apple 기준, 모든 화면 동일 |
| Container max-width | 980px | |
| 좌우 패딩 | 22px | |
| Footer padding | 20px 0 | |
| Form max-width | 600px | 운동일지 폼 전용 |

## 버튼

### Hero 버튼
```
padding: 16px 32px (Desktop) → 14px 28px (Tablet) → 12px 24px (Mobile)
border-radius: 980px (완전 라운드)
font-size: 1.2rem → 1.1rem → 1rem
max-width: 320px / width: 100%
```

### 섹션 버튼
```
padding: 14px 28px → 12px 24px → 10px 20px
border-radius: 980px
font-size: 0.9rem (고정)
min-width: 140px
```

### 배경별 버튼 색상
- **블랙 배경** → 화이트 버튼
- **화이트 배경** → 블랙 버튼

## 인터랙션

| 요소 | Transition | Hover 효과 |
|------|-----------|------------|
| Nav 링크 | 0.2s | opacity 0.8 → 1.0 |
| 버튼 | 0.3s | scale(1.02) |
| Tool 카드 | 0.3s | scale(1.02) + box-shadow |

## 간격 시스템

```
제목 (h1/h2)
  ↓ 8px (타이트 — 정보 그룹)
설명 (h2/h3)
  ↓ 24px (넓게 — 행동 분리)
CTA 버튼
```

### 원칙
1. **관련 정보는 가깝게** — 제목과 설명은 8px
2. **행동 요소는 분리** — CTA 전 24px
3. **일관성 유지** — 모든 섹션 동일 규칙

## 페이지 구조

```
CoachMate
├── index.html          ← 홈 (Hero + 섹션)
├── smarter.html        ← Smarter (Tool 카드)
│   └── coaching-log.html  ← AI 운동일지 (폼)
├── better.html         ← Better (Tool 카드)
└── about.html          ← About (히어로)
```

## Nav 동작

| 페이지 | position | 이유 |
|--------|----------|------|
| index.html | `fixed` | 풀스크린 Hero 위에 떠야 함 |
| 서브 페이지 | `sticky` | 일반 스크롤 |
