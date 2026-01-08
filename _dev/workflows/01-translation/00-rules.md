# 한글화 작업 규칙

## 기본 설정

- **작업 대상 폴더**: `src/content/docs/`
- **커밋 전 반드시 사용자 확인 필요**
- **ko 에이전트를 통해 작업 진행**
- **체크리스트 업데이트 필수**

---

## 제외 대상

### 폴더 제외

| 경로 | 사유 |
| ---- | ---- |
| `node_modules/` | 의존성 패키지 |
| `dist/` | 빌드 출력 |
| `.astro/` | Astro 캐시 |
| `public/` | 정적 파일 (이미지, 폰트) |
| `src/assets/` | 에셋 파일 |
| `src/mdx/get-started/` | 데이터베이스별 코드 스니펫 (코드 위주) |
| `src/ui/components/landing/` | 랜딩 페이지 컴포넌트 (별도 관리) |
| `tests/` | 테스트 파일 |

### 파일 제외

| 패턴 | 사유 |
| ---- | ---- |
| `*.config.js`, `*.config.ts`, `*.config.mjs` | 설정 파일 |
| `*.json` | 데이터/설정 파일 |
| `*.yaml`, `*.yml` | 데이터 파일 |
| `*.d.ts` | 타입 정의 |
| `src/utils.ts` | 유틸리티 함수 |
| `src/types.ts` | 타입 정의 |
| `src/env.d.ts` | 환경 타입 |

---

## 한글화 대상

### 번역 O (우선순위순)

| 경로 | 설명 | 우선순위 |
| ---- | ---- | -------- |
| `src/content/docs/` | MDX 문서 (본문, 제목, 설명) | 1 |
| `src/content/announcements/` | 공지사항 | 2 |
| `src/data/roadmap.md` | 로드맵 | 3 |
| `src/ui/components/` | UI 컴포넌트 (표시 텍스트) | 4 |
| `src/pages/` | 페이지 컴포넌트 (UI 텍스트) | 4 |

### 번역 X (원본 유지)

- API 명세 (props, types, methods)
- 파일명, 폴더명
- import 문, 변수명
- CLI 명령어
- URL, 경로
- SQL 쿼리문
- 코드 블록 내 코드
- 브랜드명 (Drizzle, PostgreSQL, MySQL, SQLite 등)
- 패키지명 (drizzle-orm, drizzle-kit 등)

---

## 코드 예제 번역 규칙

### 번역 O

| 구분 | 예시 |
| ---- | ---- |
| 코드 블록 외부 설명 | 본문 텍스트 |
| 주석 (선택적) | `// 사용자 테이블 생성` |

### 번역 X

| 구분 | 예시 |
| ---- | ---- |
| SQL 쿼리 | `SELECT * FROM users` |
| 코드 | `const db = drizzle(...)` |
| 테이블/컬럼명 | `users`, `email`, `id` |
| 타입명 | `string`, `number`, `boolean` |
| 함수명 | `createTable`, `insert` |

### 예시

```mdx
// 원본
To create a table, use the `pgTable` function:

\`\`\`ts
const users = pgTable('users', {
  id: serial('id').primaryKey(),
  name: text('name'),
});
\`\`\`

// 번역
테이블을 생성하려면 `pgTable` 함수를 사용합니다:

\`\`\`ts
const users = pgTable('users', {
  id: serial('id').primaryKey(),
  name: text('name'),
});
\`\`\`
```

---

## MDX 프론트매터 번역 규칙

| 필드 | 번역 | 예시 |
| ---- | ---- | ---- |
| `title` | ✅ 번역 | `title: "시작하기"` |
| `description` | ✅ 번역 | `description: "Drizzle ORM 시작 방법"` |
| `slug` | ❌ 유지 | `slug: "get-started"` |

---

## 용어집

### 일반 용어

| 영어 | 한글 |
| ---- | ---- |
| Getting Started | 시작하기 |
| Overview | 개요 |
| Installation | 설치 |
| Configuration | 설정 |
| Documentation | 문서 |
| Usage | 사용법 |
| Example | 예제 |
| API Reference | API 레퍼런스 |
| Migration | 마이그레이션 |
| Tutorial | 튜토리얼 |
| Guide | 가이드 |
| Note | 참고 |
| Warning | 주의 |
| Tip | 팁 |
| Important | 중요 |
| Deprecated | 지원 중단 |

### Drizzle 관련 용어

| 영어 | 한글 |
| ---- | ---- |
| Schema | 스키마 |
| Table | 테이블 |
| Column | 컬럼 |
| Query | 쿼리 |
| Insert | 삽입 |
| Update | 업데이트 |
| Delete | 삭제 |
| Select | 조회 |
| Join | 조인 |
| Relation | 관계 |
| Transaction | 트랜잭션 |
| Index | 인덱스 |
| Constraint | 제약조건 |
| Primary Key | 기본 키 |
| Foreign Key | 외래 키 |
| Introspection | 인트로스펙션 |
| Push | 푸시 |
| Pull | 풀 |
| Generate | 생성 |
| Drizzle Kit | Drizzle Kit (원문 유지) |
| Drizzle ORM | Drizzle ORM (원문 유지) |
| Drizzle Studio | Drizzle Studio (원문 유지) |

### 데이터베이스 관련 용어

| 영어 | 한글 유지 사유 |
| ---- | -------------- |
| PostgreSQL | 브랜드명 |
| MySQL | 브랜드명 |
| SQLite | 브랜드명 |
| Neon | 브랜드명 |
| Turso | 브랜드명 |
| PlanetScale | 브랜드명 |
| Supabase | 브랜드명 |
| Vercel | 브랜드명 |
| Cloudflare | 브랜드명 |

---

## 작업 순서

1. 체크리스트에서 미완료 항목 확인
2. ko 에이전트로 작업 지시
3. 작업 완료 후 체크리스트 업데이트
4. **사용자에게 커밋 여부 확인**
5. 승인 후 커밋 진행

---

## 에이전트 사용법

```bash
Task tool 호출:
- subagent_type: "ko"
- prompt: 파일 경로와 번역 대상 명시
- 체크리스트 업데이트 지시 포함
```

---

## 주의사항

- 문장은 자연스러운 한국어로 번역
- 기술 용어는 용어집 참조
- 코드 블록 내 코드는 번역하지 않음
- 병렬 작업 시 파일 충돌 주의
- MDX 컴포넌트 문법 유지 (`<Callout>`, `<Tab>` 등)
- 링크 URL은 변경하지 않음
- 이미지 alt 텍스트는 번역

---

## 품질 체크리스트

번역 완료 후 확인:

- [ ] 코드 블록이 정상 렌더링되는가
- [ ] MDX 컴포넌트가 깨지지 않았는가
- [ ] 링크가 정상 작동하는가
- [ ] 용어가 일관되게 사용되었는가
- [ ] 문장이 자연스러운가
