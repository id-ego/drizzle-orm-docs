# 오픈소스 한글화 프로젝트 초기 설정 체크리스트

오픈소스 문서를 Fork하여 한글화할 때 확인해야 할 모든 설정 항목

## 1. 도메인 & URL

검색 패턴: `site:`, `url`, `domain`, `host`, `baseUrl`, `siteUrl`

- [ ] 프레임워크 설정 파일의 사이트 URL
  - Astro: `astro.config.mjs` → `site`
  - Next.js: `next.config.js` → `basePath`, `assetPrefix`
  - Vite: `vite.config.ts` → `base`
  - Docusaurus: `docusaurus.config.js` → `url`, `baseUrl`
- [ ] `robots.txt` - Sitemap URL
- [ ] `sitemap.xml` 또는 sitemap 생성 설정
- [ ] Canonical URL 설정
- [ ] 내부 절대 경로 링크들

## 2. SEO & 메타 정보

검색 패턴: `<title>`, `<meta`, `og:`, `twitter:`, `description`

- [ ] 기본 사이트 제목
- [ ] 기본 설명 (description)
- [ ] Open Graph 태그 (og:title, og:description, og:image, og:url)
- [ ] Twitter Card 태그
- [ ] 페이지별 타이틀 템플릿 (예: `{page} | Site Name`)
- [ ] 404/500 에러 페이지 타이틀

## 3. 애널리틱스 & 추적 (제거 대상)

검색 패턴: `analytics`, `gtag`, `GA-`, `plausible`, `data-domain`, `tracker`

- [ ] Google Analytics (gtag, GA4)
- [ ] Google Tag Manager
- [ ] Plausible Analytics
- [ ] Fathom Analytics
- [ ] Simple Analytics
- [ ] Cabin Analytics
- [ ] Umami
- [ ] Mixpanel
- [ ] Hotjar / FullStory
- [ ] 에러 추적 (Sentry, LogRocket, Bugsnag)

## 4. 외부 서비스 & API

검색 패턴: `api.`, `cdn.`, `fetch(`, `axios`, `.com/`, `.io/`

- [ ] 검색 서비스 (Algolia DocSearch, Typesense, Meilisearch)
- [ ] 댓글 서비스 (Disqus, Giscus, Utterances)
- [ ] 채팅/AI 위젯 (Intercom, Crisp, Inkeep)
- [ ] 뉴스레터 (Mailchimp, ConvertKit, Buttondown)
- [ ] 스폰서/후원 API
- [ ] 인증 서비스 (Auth0, Clerk)
- [ ] 폼 서비스 (Formspree, Netlify Forms)

## 5. 소셜 링크

검색 패턴: `discord`, `twitter`, `github.com`, `x.com`, `linkedin`

- [ ] Discord 초대 링크
- [ ] Twitter/X 링크
- [ ] GitHub 저장소 링크 (원본 유지 vs 변경)
- [ ] YouTube 채널
- [ ] 블로그/뉴스 링크
- [ ] 기타 소셜 미디어

## 6. 브랜딩 & 에셋

검색 패턴: `logo`, `favicon`, `icon`, `brand`

- [ ] 파비콘 (favicon.ico, favicon.svg)
- [ ] 로고 이미지
- [ ] Apple Touch Icon
- [ ] PWA 아이콘 (manifest.json)
- [ ] Open Graph 기본 이미지
- [ ] 이메일 템플릿 로고

## 7. 법적 정보

검색 패턴: `LICENSE`, `copyright`, `©`, `privacy`, `terms`

- [ ] LICENSE 파일 (저작권 표시 추가)
- [ ] 코드 내 저작권 주석
- [ ] 푸터 저작권 문구
- [ ] 개인정보처리방침 (필요시)
- [ ] 이용약관 (필요시)

## 8. 패키지 & 프로젝트 정보

파일: `package.json`

- [ ] `name` - 프로젝트 이름
- [ ] `description` - 프로젝트 설명
- [ ] `author` - 작성자 정보
- [ ] `repository` - 저장소 URL
- [ ] `homepage` - 홈페이지 URL
- [ ] `bugs` - 이슈 트래커 URL
- [ ] `license` - 라이선스

## 9. 배포 & CI/CD

검색 위치: `.github/workflows/`, `vercel.json`, `netlify.toml`, `wrangler.toml`

- [ ] GitHub Actions 워크플로우
- [ ] 배포 플랫폼 설정 (Vercel, Netlify, Cloudflare Pages)
- [ ] 환경 변수 설정
- [ ] 도메인/DNS 설정
- [ ] Preview 배포 설정

## 10. 콘텐츠 & UI 텍스트

검색 패턴: 하드코딩된 영문 텍스트

- [ ] 네비게이션 메뉴 레이블
- [ ] 푸터 텍스트
- [ ] 버튼 텍스트 (Search, Menu, Copy, etc.)
- [ ] 에러 메시지
- [ ] 빈 상태 메시지
- [ ] 날짜/시간 포맷

## 11. README & 문서

- [ ] `README.md` - 프로젝트 설명 추가
- [ ] `CONTRIBUTING.md` - 기여 가이드 (필요시)
- [ ] `CHANGELOG.md` - 변경 이력 (필요시)

---

## 빠른 검색 명령어

```bash
# URL/도메인 찾기
grep -rn "https://" --include="*.{ts,js,mjs,astro,tsx,jsx,json,md}" | grep -v node_modules | grep -v ".lock"

# 애널리틱스 찾기
grep -rn "analytics\|gtag\|plausible\|data-domain" --include="*.{ts,js,astro,tsx}" | grep -v node_modules

# API 엔드포인트 찾기
grep -rn "api\." --include="*.{ts,js,tsx}" | grep -v node_modules

# 소셜 링크 찾기
grep -rn "discord\|twitter\|github\.com" --include="*.{astro,tsx,ts}" | grep -v node_modules
```

---

## 결정 필요 항목

각 프로젝트마다 결정이 필요한 사항:

| 항목 | 옵션 | 권장 |
|------|------|------|
| GitHub 링크 | 원본 유지 / Fork로 변경 | 원본 유지 |
| 커뮤니티 링크 (Discord 등) | 원본 유지 / 제거 / 새로 생성 | 원본 유지 |
| 스폰서 표시 | 유지 / 제거 | 유지 (원작자 존중) |
| 검색 기능 | 유지 / 제거 / 자체 구축 | 검토 필요 |
| 댓글 기능 | 유지 / 제거 / 자체 구축 | 검토 필요 |
