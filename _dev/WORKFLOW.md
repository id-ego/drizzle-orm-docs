# Drizzle ORM Docs 한글화 프로젝트 워크플로우

## 개요

이 문서는 [drizzle-team/drizzle-orm-docs](https://github.com/drizzle-team/drizzle-orm-docs) 원본 저장소를 Fork하여 한글화 문서 사이트를 운영하는 워크플로우를 설명합니다.

## 저장소 구조

```text
drizzle-team/drizzle-orm-docs (upstream)   ← 원본 저장소
         │
         │ Fork
         ▼
id-ego/drizzle-orm-docs (origin)           ← 내 저장소 (한글화)
         │
         │ Clone
         ▼
로컬 PC                                     ← 작업 환경
```

## 브랜치 전략

| 브랜치 | 용도 |
|--------|------|
| `main` | 한글화 버전 (배포 대상) |
| `upstream/main` | 원본 참조용 (동기화 소스) |

## 초기 설정

### 1. GitHub에서 Fork

1. [drizzle-team/drizzle-orm-docs](https://github.com/drizzle-team/drizzle-orm-docs) 접속
2. **Fork** 버튼 클릭
3. 설정:
   - Repository name: `drizzle-orm-docs`
   - Description: `Drizzle ORM 한글 문서`

### 2. 로컬 Clone

```bash
git clone https://github.com/id-ego/drizzle-orm-docs.git
cd drizzle-orm-docs
```

### 3. Upstream 원격 저장소 추가

```bash
git remote add upstream https://github.com/drizzle-team/drizzle-orm-docs.git
```

### 4. 확인

```bash
git remote -v
# origin    https://github.com/id-ego/drizzle-orm-docs.git (fetch)
# origin    https://github.com/id-ego/drizzle-orm-docs.git (push)
# upstream  https://github.com/drizzle-team/drizzle-orm-docs.git (fetch)
# upstream  https://github.com/drizzle-team/drizzle-orm-docs.git (push)
```

## Git 동기화 워크플로우

### 원본 업데이트 확인 및 반영

```bash
# 1. 원본 변경사항 다운로드 (내 코드에 영향 없음)
git fetch upstream

# 2. 새 커밋 있는지 확인
git log main..upstream/main --oneline

# 3. 새 커밋이 있으면 병합
git merge upstream/main

# 4. 내 저장소에 push
git push origin main
```

### Git 명령어 설명

| 명령어 | 역할 |
|--------|------|
| `git fetch upstream` | 원본 변경사항 다운로드 (내 코드 안 건드림) |
| `git log main..upstream/main` | upstream에만 있는 새 커밋 확인 |
| `git log upstream/main..main` | 내가 추가한 커밋 확인 |
| `git merge upstream/main` | 원본 변경사항을 내 코드에 합침 |

### Merge 동작 방식

Git은 **변경된 부분만 자동으로 합칩니다**:

| 파일 상태 | upstream | 나 | 결과 |
|-----------|----------|-----|------|
| LICENSE.md | 안 건드림 | 수정함 | **내 버전 유지** |
| README.md | 안 건드림 | 안 건드림 | 그대로 |
| docs/intro.mdx | 수정함 | 안 건드림 | **upstream 반영** |
| docs/guide.mdx | 수정함 | 수정함 (번역) | **충돌 발생** |

### 충돌 해결

같은 파일의 같은 부분을 둘 다 수정했을 때 충돌 발생:

```markdown
<<<<<<< HEAD
내 버전 (한글 번역)
=======
원본 버전 (새 내용)
>>>>>>> upstream/main
```

해결 방법:

1. 파일을 직접 편집하여 원하는 형태로 수정
2. `<<<`, `===`, `>>>` 마커 삭제
3. 저장 후:

```bash
git add <충돌파일>
git commit -m "merge: upstream 동기화, 충돌 해결"
```

## 라이선스

Apache 2.0 라이선스

**조건**: LICENSE 파일에 원저작자 표시 유지

## 프로젝트 구조

```text
src/
├── content/docs/     # MDX 문서 파일 (번역 대상)
├── pages/            # Astro 페이지
├── ui/components/    # UI 컴포넌트
└── data/             # 설정 데이터

_dev/                 # 개발 문서 (이 파일 포함)
```

## 한글화 작업 체크리스트

### Phase 1: 저장소 정리

- [x] Fork 및 Clone
- [x] Upstream 원격 저장소 설정
- [ ] README.md 한글화 프로젝트 설명 추가
- [ ] CLAUDE.md 생성

### Phase 2: 배포 설정 ✅ 완료

- [x] 배포 플랫폼 선택 (Vercel / Cloudflare Pages)
- [x] 도메인 연결: https://drizzle.docsforall.com

### Phase 3: 한글화 작업

- [ ] src/content/docs/ 문서 번역
- [ ] UI 텍스트 번역 (있다면)

### Phase 4: 자동화

- [ ] 원본 동기화 워크플로우 추가 (GitHub Actions)
- [ ] 자동 배포 확인

---

## 개발 명령어

```bash
pnpm install          # 의존성 설치
pnpm run dev          # 개발 서버 (localhost:4321)
pnpm run build        # 프로덕션 빌드
pnpm run preview      # 빌드 미리보기
pnpm run test         # 테스트 실행
```
