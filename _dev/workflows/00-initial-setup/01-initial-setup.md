# 초기 설정 워크플로우

프로젝트를 한글화 사이트에 맞게 설정하는 작업 목록

> 참고: [00-localization-checklist.md](./00-localization-checklist.md) - 범용 체크리스트

## 1. 도메인 & URL

### 필수 변경

| 파일 | 라인 | 현재 값 | 변경 값 |
| ---- | ---- | ------- | ------- |
| `astro.config.mjs` | 23 | `https://orm.drizzle.team` | `https://drizzle.docsforall.com` |
| `public/robots.txt` | 4 | `https://orm.drizzle.team/sitemap-index.xml` | `https://drizzle.docsforall.com/sitemap-index.xml` |

### 코드 내 도메인 참조 (변경 필요)

| 파일 | 라인 | 내용 |
| ---- | ---- | ---- |
| `src/utils.ts` | 5 | `orm\.drizzle\.team\|drizzle\.team` - nofollow 예외 도메인 |
| `tests/add-nofollow-to-external-links.test.ts` | 여러 | 테스트 케이스 내 도메인 |

### Tasks

- [x] `astro.config.mjs` site URL 변경
- [x] `public/robots.txt` sitemap URL 변경
- [x] `src/utils.ts` nofollow 예외 도메인 변경
- [x] 테스트 파일 도메인 업데이트

---

## 2. SEO & 메타 정보 ✅ 결정됨

### 기본 설명 → 한글화 (SEO 페널티 방지)

| 파일 | 라인 | 현재 값 | 변경 값 |
| ---- | ---- | ------- | ------- |
| `src/ui/BaseHead.astro` | 11 | `Drizzle ORM is a lightweight and performant TypeScript ORM with developer experience in mind.` | `Drizzle ORM은 개발자 경험을 중시하는 가볍고 빠른 TypeScript ORM입니다.` |

### 페이지 타이틀 → 한글화

| 파일 | 라인 | 현재 값 | 변경 값 |
| ---- | ---- | ---- | ---- |
| `src/ui/DocsLayout.astro` | 36 | `Drizzle ORM - ${...}` | `Drizzle ORM 한글 - ${...}` |
| `src/ui/CenteredLayout.astro` | 30 | `Drizzle ORM - ${...}` | `Drizzle ORM 한글 - ${...}` |
| `src/pages/index.astro` | 46 | `Drizzle ORM - next gen TypeScript ORM.` | `Drizzle ORM 한글 - 차세대 TypeScript ORM` |
| `src/pages/announcements.astro` | 33 | `Drizzle ORM - Announcements` | `Drizzle ORM 한글 - 공지사항` |
| `src/pages/404.astro` | 9 | `Drizzle ORM - next gen TypeScript ORM.` | `Drizzle ORM 한글 - 페이지를 찾을 수 없습니다` |

### SEO 작업

- [x] 기본 description 한글화
- [x] 페이지 타이틀 한글화

---

## 3. 애널리틱스 (제거 대상)

`src/ui/BaseHead.astro`에서 제거할 스크립트:

| 라인 | 서비스 | 용도 |
| ---- | ------ | ---- |
| 127-128 | Inkeep | AI 검색 위젯 |
| 131-133 | Plausible | 웹 애널리틱스 (`data-domain="orm.drizzle.team"`) |
| 142-146 | OneDollarStats | 웹 애널리틱스 (`data-site-id="orm.drizzle.team"`) |
| 147 | Cabin | 웹 애널리틱스 |
| 148-149 | Simple Analytics | 웹 애널리틱스 |

### Tasks

- [x] Plausible 스크립트 제거
- [x] OneDollarStats 스크립트 제거
- [x] Cabin 스크립트 제거
- [x] Simple Analytics 스크립트 제거
- [x] Inkeep 위젯 제거 (확정)

---

## 4. 외부 서비스 ✅ 결정됨

### Algolia DocSearch → 유지 (설정값만 변경 예정)

DocSearch 코드는 그대로 유지하고, 신규 신청 승인 후 설정값만 변경합니다.

| 파일 | 작업 |
| ---- | ---- |
| `src/ui/components/CenteredSearchWithAI.astro` | TODO 주석으로 설정값 변경 필요 표시 |
| `src/ui/components/landing/Header.astro` | TODO 주석으로 설정값 변경 필요 표시 |

> 배포 후 https://docsearch.algolia.com/apply 에서 신규 신청
> 승인 후 appId, apiKey, indexName 업데이트

### Inkeep AI 위젯 → 제거 확정

| 파일 | 작업 |
| ---- | ---- |
| `src/ui/BaseHead.astro:127-128` | Inkeep embed 스크립트 제거 |
| `src/ui/components/CenteredSearchWithAI.astro` | Inkeep 관련 코드 제거 |
| `src/ui/components/landing/Header.astro` | Inkeep 버튼/모달 제거 |
| `src/ui/components/ThemeScript.astro` | Inkeep 테마 연동 제거 |
| `src/ui/components/ThemeMobileScript.astro` | Inkeep 테마 연동 제거 |
| `src/types.ts:19` | Inkeep 타입 정의 제거 |
| `public/inkeep-styles.css` | 파일 삭제 |

### 스폰서 API → 유지 확정

원작자 존중을 위해 유지. 변경 없음.

### 외부 서비스 작업

- [x] Algolia DocSearch 설정값 TODO 주석 추가
- [x] Inkeep AI 위젯 제거

---

## 5. 소셜 링크 (유지 권장)

원본 프로젝트 커뮤니티 링크 - 변경 불필요

| 파일 | 서비스 | URL |
| ---- | ------ | --- |
| `src/ui/components/Footer.astro:22` | GitHub | `github.com/drizzle-team/drizzle-orm` |
| `src/ui/components/Footer.astro:35` | Discord | `discord.gg/yfjTbVXMW4` |
| `src/ui/components/Footer.astro:54` | Twitter | `twitter.com/DrizzleORM` |
| `src/ui/components/AsideSocials.astro` | 동일 | |

---

## 6. 기타 설정

### package.json (현재 상태 - 변경 불필요)

```json
{
  "name": "orm-drizzle-docs-astro",
  "version": "0.0.1"
}
```

### 브랜딩 (유지)

- `public/favicon.ico` - Drizzle 파비콘 유지
- 로고 이미지들 - 원본 유지

---

## 진행 체크리스트

### 1. 도메인 & URL

- [x] astro.config.mjs site URL 변경
- [x] robots.txt sitemap URL 변경
- [x] src/utils.ts nofollow 도메인 변경
- [x] 테스트 파일 도메인 업데이트

### 2. SEO & 메타 정보

- [x] 기본 description 한글화
- [x] 페이지 타이틀 한글화

### 3. 애널리틱스 제거

- [x] Plausible 제거
- [x] OneDollarStats 제거
- [x] Cabin 제거
- [x] Simple Analytics 제거

### 4. 외부 서비스

- [x] Algolia DocSearch 설정값 TODO 주석 추가 (신규 신청 후 업데이트)
- [x] Inkeep AI 위젯 제거
- [x] inkeep-styles.css 파일 삭제

---

## 변경 이력

| 날짜 | 작업 | 담당 |
| ---- | ---- | ---- |
| 2026-01-08 | 초기 설정 완료 - URL, SEO, 애널리틱스, Algolia, Inkeep 제거 | Claude |
