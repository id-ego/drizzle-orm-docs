# Drizzle ORM 한글 문서

[Drizzle ORM](https://orm.drizzle.team) 공식 문서의 한글 번역 프로젝트입니다.

- **배포 사이트**: https://drizzle.docsforall.com
- **원본 저장소**: https://github.com/drizzle-team/drizzle-orm-docs

## 기여하기

번역에 참여하고 싶으시다면 언제든 환영합니다!

1. 이 저장소를 Fork 합니다
2. 번역할 문서를 선택합니다 (`src/content/docs/` 내 MDX 파일)
3. 번역 후 Pull Request를 생성합니다

### 번역 가이드라인

- 기술 용어는 원문 그대로 유지하거나 괄호 안에 원문 병기
- 코드 블록 내 주석은 번역 가능
- 일관된 어투 사용 (경어체)

---

## 프로젝트 구조

MDX 문서 파일:

```text
├── src/
│   ├── content/
│   │   └── docs/          # 문서 MDX 파일
```

공지사항 마크다운 파일:

```text
├── src/
│   ├── data/
│   │   └── announcements/ # 공지사항
```

로드맵 마크다운 파일:

```text
├── src/
│   ├── data/
│   │   └── roadmap.md     # 로드맵
```

Shipping 섹션 YAML 파일:

```text
├── src/
│   ├── data/
│   │   └── shipping.yaml  # 배포 현황
```

```yaml
progress: number
weeks:
  - date:
      start: "YYYY-MM-DD"
    details:
      - string
```

---

## 명령어

모든 명령어는 프로젝트 루트에서 실행합니다:

| 명령어                     | 설명                                             |
| :------------------------ | :----------------------------------------------- |
| `pnpm install`            | 의존성 설치                                       |
| `pnpm run dev`            | 개발 서버 시작 (`localhost:4321`)                 |
| `pnpm run build`          | 프로덕션 빌드 (`./dist/`)                         |
| `pnpm run preview`        | 빌드 결과 로컬 미리보기                           |
| `pnpm run astro ...`      | Astro CLI 명령어 실행                             |
| `pnpm run astro -- --help`| Astro CLI 도움말                                  |

---

## 라이선스

이 프로젝트는 [Apache License 2.0](LICENSE) 라이선스를 따릅니다.

- 원본 Drizzle ORM 문서: Copyright 2024 Drizzle Team
- 한글 번역: Copyright 2026 id-ego
