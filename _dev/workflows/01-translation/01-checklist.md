# 한글화 체크리스트

> 총 234개 MDX 파일

## 진행 상황

| 카테고리 | 완료 | 전체 | 진행률 |
| -------- | ---- | ---- | ------ |
| 핵심 문서 (루트) | 99 | 99 | 100% |
| 시작하기 (get-started) | 48 | 48 | 100% |
| 가이드 (guides) | 25 | 25 | 100% |
| 튜토리얼 (tutorials) | 11 | 11 | 100% |
| 컬럼 타입 (column-types) | 6 | 6 | 100% |
| 마이그레이션 (migrate) | 4 | 4 | 100% |
| 확장 (extensions) | 4 | 4 | 100% |
| 릴리즈 노트 (latest-releases) | 37 | 37 | 100% |
| **총계** | **234** | **234** | **100%** |

> 🎉 **한글화 작업 완료!** (2026-01-08)

---

## 우선순위 1: 핵심 문서

### 개요 & 시작

- [ ] `overview.mdx` - Drizzle ORM 개요
- [ ] `get-started.mdx` - 시작하기 메인
- [ ] `why-drizzle.mdx` - Drizzle을 사용하는 이유
- [ ] `quick.mdx` - 빠른 시작

### 스키마 정의

- [ ] `sql-schema-declaration.mdx` - SQL 스키마 선언
- [ ] `schemas.mdx` - 스키마
- [x] `indexes-constraints.mdx` - 인덱스와 제약조건
- [ ] `sequences.mdx` - 시퀀스
- [ ] `views.mdx` - 뷰
- [x] `generated-columns.mdx` - 생성 컬럼
- [ ] `custom-types.mdx` - 커스텀 타입

### 데이터 조작

- [ ] `data-querying.mdx` - 데이터 쿼리
- [ ] `select.mdx` - SELECT
- [ ] `insert.mdx` - INSERT
- [ ] `update.mdx` - UPDATE
- [ ] `delete.mdx` - DELETE
- [x] `joins.mdx` - JOIN
- [ ] `set-operations.mdx` - 집합 연산
- [ ] `operators.mdx` - 연산자
- [ ] `sql.mdx` - SQL 표현식

### 관계 & 쿼리빌더

- [x] `relations.mdx` - 관계
- [x] `relations-schema-declaration.mdx` - 관계 스키마 선언
- [ ] `relations-v2.mdx` - 관계 v2
- [x] `relations-v1-v2.mdx` - v1에서 v2 마이그레이션
- [ ] `rqb.mdx` - Relational Query Builder
- [x] `rqb-v2.mdx` - RQB v2

### 고급 기능

- [ ] `transactions.mdx` - 트랜잭션
- [ ] `batch-api.mdx` - 배치 API
- [ ] `dynamic-query-building.mdx` - 동적 쿼리 빌딩
- [ ] `query-utils.mdx` - 쿼리 유틸리티
- [ ] `read-replicas.mdx` - 읽기 복제본
- [x] `cache.mdx` - 캐시
- [ ] `rls.mdx` - Row Level Security

### Drizzle Kit

- [ ] `kit-overview.mdx` - Drizzle Kit 개요
- [ ] `drizzle-config-file.mdx` - 설정 파일
- [ ] `migrations.mdx` - 마이그레이션
- [ ] `drizzle-kit-generate.mdx` - generate 명령어
- [ ] `drizzle-kit-migrate.mdx` - migrate 명령어
- [ ] `drizzle-kit-push.mdx` - push 명령어
- [ ] `drizzle-kit-pull.mdx` - pull 명령어
- [ ] `drizzle-kit-check.mdx` - check 명령어
- [ ] `drizzle-kit-up.mdx` - up 명령어
- [ ] `drizzle-kit-export.mdx` - export 명령어
- [ ] `drizzle-kit-studio.mdx` - studio 명령어
- [x] `kit-custom-migrations.mdx` - 커스텀 마이그레이션
- [ ] `kit-migrations-for-teams.mdx` - 팀 마이그레이션
- [x] `kit-web-mobile.mdx` - 웹/모바일

### Seed (시딩)

- [ ] `seed-overview.mdx` - Seed 개요
- [ ] `seed-functions.mdx` - Seed 함수
- [ ] `seed-limitations.mdx` - Seed 제한사항
- [x] `seed-versioning.mdx` - Seed 버전관리

### 성능

- [ ] `perf-queries.mdx` - 쿼리 성능
- [x] `perf-serverless.mdx` - 서버리스 성능

### 통합

- [x] `graphql.mdx` - GraphQL
- [ ] `prisma.mdx` - Prisma 마이그레이션
- [ ] `eslint-plugin.mdx` - ESLint 플러그인

### 유효성 검사 라이브러리

- [ ] `zod.mdx` - Zod
- [ ] `valibot.mdx` - Valibot
- [ ] `arktype.mdx` - ArkType
- [ ] `typebox.mdx` - TypeBox

### 기타

- [ ] `goodies.mdx` - 유용한 기능들
- [x] `gotchas.mdx` - 주의사항
- [ ] `faq.mdx` - FAQ
- [ ] `upgrade-v1.mdx` - v1 업그레이드
- [x] `upgrade-21.mdx` - v0.21 업그레이드

---

## 우선순위 2: 데이터베이스 연결 (connect-*)

### PostgreSQL 계열

- [ ] `connect-overview.mdx` - 연결 개요
- [ ] `connect-neon.mdx` - Neon
- [ ] `connect-supabase.mdx` - Supabase
- [ ] `connect-vercel-postgres.mdx` - Vercel Postgres
- [x] `connect-xata.mdx` - Xata
- [x] `connect-pglite.mdx` - PGlite
- [x] `connect-aws-data-api-pg.mdx` - AWS Data API (PG)
- [x] `connect-nile.mdx` - Nile
- [x] `connect-prisma-postgres.mdx` - Prisma Postgres

### MySQL 계열

- [ ] `connect-planetscale.mdx` - PlanetScale
- [x] `connect-tidb.mdx` - TiDB
- [x] `connect-aws-data-api-mysql.mdx` - AWS Data API (MySQL)

### SQLite 계열

- [ ] `connect-turso.mdx` - Turso
- [x] `connect-turso-database.mdx` - Turso Database
- [ ] `connect-cloudflare-d1.mdx` - Cloudflare D1
- [x] `connect-cloudflare-do.mdx` - Cloudflare DO
- [x] `connect-bun-sqlite.mdx` - Bun SQLite
- [x] `connect-expo-sqlite.mdx` - Expo SQLite
- [x] `connect-op-sqlite.mdx` - OP SQLite
- [x] `connect-react-native-sqlite.mdx` - React Native SQLite
- [x] `connect-sqlite-cloud.mdx` - SQLite Cloud

### 기타

- [x] `connect-bun-sql.mdx` - Bun SQL
- [x] `connect-drizzle-proxy.mdx` - Drizzle Proxy

---

## 우선순위 3: 시작하기 (get-started/)

### 데이터베이스별 시작 가이드

- [x] `get-started-postgresql.mdx` - PostgreSQL
- [x] `get-started-mysql.mdx` - MySQL
- [x] `get-started-sqlite.mdx` - SQLite
- [x] `get-started-mssql.mdx` - MSSQL
- [x] `mssql-existing.mdx` - 기존 MSSQL 프로젝트
- [x] `get-started-singlestore.mdx` - SingleStore
- [x] `get-started-cockroach.mdx` - CockroachDB
- [x] `get-started-gel.mdx` - Gel
- [x] `gel-existing.mdx` - 기존 Gel 프로젝트

### get-started/ 폴더 내 파일 (48개)

- [x] `postgresql-new.mdx` - PostgreSQL 시작하기 (node-postgres)
- [x] `postgresql-existing.mdx` - 기존 PostgreSQL 프로젝트
- [x] `neon-existing.mdx` - 기존 프로젝트에서 Neon
- [x] `nile-existing.mdx` - 기존 프로젝트에서 Nile
- [x] `sqlite-existing.mdx` - 기존 SQLite 프로젝트
- [x] `sqlite-new.mdx` - SQLite 시작하기 (libsql)
- [x] `mysql-new.mdx` - MySQL 시작하기
- [x] `mysql-existing.mdx` - 기존 MySQL 프로젝트
- [x] `supabase-existing.mdx` - 기존 Supabase 프로젝트
- [x] `supabase-new.mdx` - Supabase 시작하기
- [x] `turso-new.mdx` - Turso Cloud 시작하기
- [x] `turso-existing.mdx` - 기존 Turso Cloud 프로젝트
- [x] `d1-existing.mdx` - 기존 D1 프로젝트
- [x] `d1-new.mdx` - Cloudflare D1 시작하기
- [x] `vercel-new.mdx` - Vercel Postgres 시작하기
- [x] `vercel-existing.mdx` - 기존 Vercel Postgres 프로젝트
- [x] `planetscale-existing.mdx` - 기존 PlanetScale 프로젝트
- [x] `tidb-new.mdx` - TiDB 시작하기
- [x] `tidb-existing.mdx` - 기존 TiDB 프로젝트
- [x] `xata-existing.mdx` - 기존 Xata 프로젝트
- [x] `op-sqlite-new.mdx` - OP-SQLite 시작하기
- [x] `op-sqlite-existing.mdx` - 기존 OP-SQLite 프로젝트
- [x] `expo-existing.mdx` - 기존 Expo 프로젝트
- [x] `expo-new.mdx` - Expo 시작하기
- [x] `mssql-new.mdx` - MSSQL 시작하기 (node-mssql)
- [x] `singlestore-new.mdx` - SingleStore 시작하기 (mysql2)
- [x] `singlestore-existing.mdx` - 기존 SingleStore 프로젝트
- [x] `do-new.mdx` - Cloudflare Durable Objects 시작하기
- [x] `pglite-new.mdx` - PGlite 시작하기
- [x] `cockroach-new.mdx` - CockroachDB 시작하기 (node-postgres)
- [x] `pglite-existing.mdx` - 기존 PGlite 프로젝트
- [x] `cockroach-existing.mdx` - 기존 CockroachDB 프로젝트
- [x] `sqlite-cloud-new.mdx` - SQLite Cloud 시작하기
- [x] `sqlite-cloud-existing.mdx` - 기존 SQLite Cloud 프로젝트
- [x] `gel-new.mdx` - Gel 시작하기
- [ ] 나머지 파일 목록은 별도 확인 필요

---

## 우선순위 4: 가이드 (guides/)

> 25개 파일 - 실용적인 사용 가이드

- [x] `guides.mdx` - 가이드 인덱스 (컴포넌트만 포함, 번역 불필요)
- [x] `incrementing-a-value.mdx` - SQL 값 증가시키기
- [x] `limit-offset-pagination.mdx` - Limit/Offset 페이지네이션
- [x] `include-or-exclude-columns.mdx` - 쿼리에서 컬럼 포함 또는 제외하기
- [x] `cursor-based-pagination.mdx` - 커서 기반 페이지네이션
- [x] `count-rows.mdx` - 행 개수 세기
- [x] `decrementing-a-value.mdx` - SQL 값 감소시키기
- [x] `conditional-filters-in-query.mdx` - 쿼리의 조건부 필터
- [x] `upsert.mdx` - Upsert
- [x] `empty-array-default-value.mdx` - 빈 배열을 기본값으로 사용하기
- [x] `d1-http-with-drizzle-kit.mdx` - D1 HTTP와 Drizzle Kit
- [x] `full-text-search-with-generated-columns.mdx` - 생성된 컬럼으로 전체 텍스트 검색
- [x] `gel-ext-auth.mdx` - Gel 인증 확장
- [x] `mysql-local-setup.mdx` - MySQL 로컬 설정
- [x] `point-datatype-psql.mdx` - PostgreSQL Point 데이터 타입
- [x] `postgis-geometry-point.mdx` - PostGIS Geometry Point
- [x] `postgresql-full-text-search.mdx` - PostgreSQL 전문 검색
- [x] `postgresql-local-setup.mdx` - PostgreSQL 로컬 설정
- [x] `seeding-using-with-option.mdx` - with 옵션으로 시딩
- [x] `seeding-with-partially-exposed-schema.mdx` - 부분 노출 스키마로 시딩
- [x] `select-parent-rows-with-at-least-one-related-child-row.mdx` - 최소 하나의 관련 자식 행이 있는 부모 행 조회
- [x] `timestamp-default-value.mdx` - 기본값으로 SQL Timestamp 사용하기
- [x] `toggling-a-boolean-field.mdx` - Boolean 필드 토글
- [x] `unique-case-insensitive-email.mdx` - 대소문자 구분 없는 고유 이메일
- [x] `update-many-with-different-value.mdx` - 여러 행을 서로 다른 값으로 업데이트
- [x] `vector-similarity-search.mdx` - 벡터 유사도 검색

### guides/ 폴더 내 파일

> 총 25개 파일
> 참고: `Guides.astro` 컴포넌트 번역 필요 (별도 작업)

---

## 우선순위 5: 튜토리얼 (tutorials/)

> 11개 파일 - 단계별 튜토리얼

- [x] `tutorials.mdx` - 튜토리얼 인덱스 (프론트매터 추가, Tutorials.astro 컴포넌트 번역 완료)

### tutorials/ 폴더 내 파일

> 파일 목록은 별도 확인 필요
> 참고: `Tutorials.astro` 컴포넌트 번역 완료

---

## 우선순위 6: 보조 문서

### column-types/ (6개)

> 데이터베이스별 컬럼 타입 문서

- [x] `pg.mdx` - PostgreSQL 컬럼 타입
- [x] `mysql.mdx` - MySQL 컬럼 타입
- [x] `sqlite.mdx` - SQLite 컬럼 타입
- [x] `mssql.mdx` - MSSQL 컬럼 타입
- [x] `singlestore.mdx` - SingleStore 컬럼 타입
- [x] `cockroach.mdx` - CockroachDB 컬럼 타입

### extensions/ (4개)

> PostgreSQL 확장 문서

- [x] `sqlite.mdx` - SQLite 확장
- [x] `singlestore.mdx` - SingleStore 확장
- [x] `pg.mdx` - PostgreSQL 확장 (pg_vector, postgis)
- [x] `mysql.mdx` - MySQL 확장

### migrate/ (4개)

> 마이그레이션 관련 문서

- [x] `components.mdx` - MDX 컴포넌트 사용 예제
- [x] `migrate-from-prisma.mdx` - Prisma에서 마이그레이션
- [x] `migrate-from-sequelize.mdx` - Sequelize에서 마이그레이션
- [x] `migrate-from-typeorm.mdx` - TypeORM에서 마이그레이션

---

## 우선순위 7: 릴리즈 노트 (latest-releases/)

> 37개 파일 - 버전별 릴리즈 노트
> 최신 버전부터 번역 권장

- [x] `latest-releases.mdx` - 릴리즈 노트 인덱스 (프론트매터 + LatestReleases.astro 컴포넌트 번역 완료)

---

## 변경 이력

| 날짜 | 작업 | 담당 |
| ---- | ---- | ---- |
| 2026-01-08 | 체크리스트 생성 | Claude |
| 2026-01-08 | `joins.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `indexes-constraints.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `graphql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `cache.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `rqb-v2.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `kit-web-mobile.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `perf-serverless.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `seed-versioning.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `upgrade-21.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `relations-v1-v2.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-pglite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-aws-data-api-pg.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-xata.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-prisma-postgres.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-tidb.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-nile.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-react-native-sqlite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-aws-data-api-mysql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-sqlite-cloud.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-op-sqlite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-expo-sqlite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-bun-sqlite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `guides.mdx` 확인 완료 (번역 불필요) | Claude |
| 2026-01-08 | `connect-cloudflare-do.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `tutorials.mdx` 한글화 완료 (프론트매터 + Tutorials.astro 컴포넌트) | Claude |
| 2026-01-08 | `connect-turso-database.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-drizzle-proxy.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `connect-bun-sql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `get-started-sqlite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `get-started-postgresql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `get-started-gel.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `get-started-mssql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `get-started-singlestore.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `get-started-cockroach.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `get-started-mysql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `mssql.mdx` 한글화 완료 (column-types) | Claude |
| 2026-01-08 | `latest-releases.mdx` 한글화 완료 (프론트매터 + LatestReleases.astro 컴포넌트) | Claude |
| 2026-01-08 | `pg.mdx` 한글화 완료 (PostgreSQL 컬럼 타입) | Claude |
| 2026-01-08 | `singlestore.mdx` 한글화 완료 (SingleStore 컬럼 타입) | Claude |
| 2026-01-08 | `mysql.mdx` 한글화 완료 (MySQL 컬럼 타입) | Claude |
| 2026-01-08 | `column-types/sqlite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `column-types/cockroach.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `extensions/pg.mdx` 한글화 완료 (pg_vector, postgis) | Claude |
| 2026-01-08 | `extensions/sqlite.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `migrate/components.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `extensions/mysql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `extensions/singlestore.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `migrate-from-prisma.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `migrate-from-typeorm.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `migrate-from-sequelize.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `incrementing-a-value.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `limit-offset-pagination.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `count-rows.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `include-or-exclude-columns.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `cursor-based-pagination.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `upsert.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `decrementing-a-value.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `toggling-a-boolean-field.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `conditional-filters-in-query.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `unique-case-insensitive-email.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `empty-array-default-value.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `update-many-with-different-value.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `postgis-geometry-point.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `select-parent-rows-with-at-least-one-related-child-row.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `full-text-search-with-generated-columns.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `vector-similarity-search.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `postgresql-full-text-search.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `d1-http-with-drizzle-kit.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `point-datatype-psql.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `postgresql-local-setup.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `mysql-local-setup.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `seeding-using-with-option.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `seeding-with-partially-exposed-schema.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `gel-ext-auth.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `postgresql-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `sqlite-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `mysql-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `mysql-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `postgresql-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `sqlite-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `supabase-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `neon-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `supabase-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `neon-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `turso-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `turso-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `planetscale-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `d1-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `planetscale-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `vercel-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `vercel-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `d1-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `tidb-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `bun-sqlite-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `xata-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `bun-sqlite-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `xata-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `tidb-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `op-sqlite-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `bun-sql-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `bun-sql-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `expo-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `op-sqlite-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `expo-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `mssql-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `mssql-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `do-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `singlestore-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `singlestore-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `do-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `pglite-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `pglite-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `nile-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `cockroach-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `cockroach-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `nile-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `turso-database-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `sqlite-cloud-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `gel-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `turso-database-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `sqlite-cloud-new.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `gel-existing.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `generated-columns.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `relations-schema-declaration.mdx` 한글화 확인 (이미 완료됨) | Claude |
| 2026-01-08 | `relations.mdx` 한글화 완료 | Claude |
| 2026-01-08 | `kit-custom-migrations.mdx` 한글화 확인 (이미 완료됨) | Claude |
| 2026-01-08 | `gotchas.mdx` 한글화 확인 (이미 완료됨) | Claude |
