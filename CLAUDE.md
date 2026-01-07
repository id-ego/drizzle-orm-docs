# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Drizzle ORM 문서 한글화 프로젝트. [drizzle-team/drizzle-orm-docs](https://github.com/drizzle-team/drizzle-orm-docs)를 Fork하여 한글 번역 문서 사이트를 운영.

- **원본**: https://github.com/drizzle-team/drizzle-orm-docs
- **배포**: https://drizzle.docsforall.com
- **기술 스택**: Astro + MDX + React
- **라이선스**: Apache-2.0

## Commands

```bash
pnpm run dev      # 개발 서버 (localhost:4321)
pnpm run build    # 타입 체크 및 빌드 (./dist/)
pnpm run preview  # 빌드 결과 미리보기
pnpm run test     # Vitest 테스트 실행
```

Package manager: pnpm (preinstall 스크립트로 강제)

## Architecture

### Content Layer

- **Documentation**: `src/content/docs/` MDX 파일 (번역 대상), `_meta.json`으로 네비게이션 구조 정의
- **Announcements**: `src/content/announcements/` 마크다운 파일
- **Roadmap**: `src/data/roadmap.md`
- **Shipping/Releases**: `src/data/shipping.yaml`

### Routing

- Landing page: `src/pages/index.astro`
- Dynamic doc routing: `src/pages/[...slug].astro`
- LLM context endpoints: `/llms.txt`, `/llms-full.txt` (`src/pages/llms.txt.ts`)

### Layout System

- `DocsLayout.astro`: 문서 페이지 (사이드바, 우측 네비게이션, dialect 탭)
- `Layout.astro`: 일반 페이지
- `BaseHead.astro`: 공통 HTML head

### Component Types

- **Astro Components** (`src/ui/components/`): 서버 렌더링 구조 컴포넌트
- **React Components** (`src/ui/components/landing/benchmark/`): 클라이언트 인터랙티브 컴포넌트

### Path Aliases

- `@/` → `src/`
- `@components/` → `src/ui/components/`
- `@mdx/` → `src/mdx/`

## Key Files

- `astro.config.mjs`: Astro 설정 (MDX, sitemap, Shiki)
- `src/content/docs/_meta.json`: 사이드바 네비게이션 구조
- `src/transformers.ts`: 코드 블록 변환 (복사 버튼, 접기/펼치기)
- `_dev/WORKFLOW.md`: 한글화 워크플로우 및 upstream 동기화 방법
