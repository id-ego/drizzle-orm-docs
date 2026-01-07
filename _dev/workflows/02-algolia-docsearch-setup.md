# Algolia DocSearch 설정 가이드

Drizzle ORM 한글 문서 사이트에 검색 기능을 활성화하기 위한 Algolia DocSearch 설정 방법입니다.

## 1. DocSearch 신청

### 신청 조건

DocSearch는 무료로 제공되지만 다음 조건을 충족해야 합니다:

- 오픈소스 프로젝트 또는 기술 문서 사이트
- 공개적으로 접근 가능한 사이트
- 프로덕션 환경에 배포된 상태

### 신청 방법

1. https://docsearch.algolia.com/apply 접속
2. 신청 양식 작성:
   - **Website URL**: `https://drizzle.docsforall.com`
   - **Email**: 관리자 이메일
   - **Repository URL**: `https://github.com/id-ego/drizzle-orm-docs`
3. 제출 후 승인 대기 (보통 1-2주 소요)

### 승인 후 받게 되는 정보

승인되면 이메일로 다음 정보를 받습니다:

```
appId: "YOUR_APP_ID"
apiKey: "YOUR_SEARCH_API_KEY"
indexName: "YOUR_INDEX_NAME"
```

---

## 2. 설정값 업데이트

승인 후 아래 3개 파일의 설정값을 업데이트합니다.

### 2.1 CenteredSearchWithAI.astro

**파일 경로**: `src/ui/components/CenteredSearchWithAI.astro`

```javascript
docsearch({
  container: '#docsearch',
  appId: "YOUR_APP_ID",           // 새 appId로 교체
  apiKey: "YOUR_SEARCH_API_KEY",  // 새 apiKey로 교체
  indexName: "YOUR_INDEX_NAME",   // 새 indexName으로 교체
  placeholder: "문서 검색...",
});
```

### 2.2 landing/Header.astro

**파일 경로**: `src/ui/components/landing/Header.astro`

```javascript
docsearch({
  container: "#docsearch",
  appId: "YOUR_APP_ID",           // 새 appId로 교체
  apiKey: "YOUR_SEARCH_API_KEY",  // 새 apiKey로 교체
  indexName: "YOUR_INDEX_NAME",   // 새 indexName으로 교체
  placeholder: "문서 검색...",
});
```

### 2.3 BaseHead.astro (선택사항)

**파일 경로**: `src/ui/BaseHead.astro`

preconnect URL의 appId도 업데이트하면 성능이 향상됩니다:

```html
<link
  rel="preconnect"
  href="https://YOUR_APP_ID-dsn.algolia.net"
  crossorigin
/>
```

---

## 3. 검색어 찾기

모든 파일에서 변경이 필요한 위치를 찾으려면:

```bash
grep -rn "MXZNUT59HV" src/
```

현재 사용 중인 임시 값:
- `appId`: `MXZNUT59HV`
- `apiKey`: `7c390e262ac8858df0b6624d01d9dfef`
- `indexName`: `orm-drizzle`

---

## 4. 테스트

설정 후 다음을 확인합니다:

1. 로컬에서 개발 서버 실행: `npm run dev`
2. 검색 버튼 클릭 또는 `/` 키 입력
3. 검색어 입력 시 결과가 표시되는지 확인

---

## 5. 크롤링 주기

DocSearch는 보통 일주일에 한 번 사이트를 크롤링합니다. 새 콘텐츠가 검색에 반영되기까지 시간이 걸릴 수 있습니다.

크롤링을 수동으로 트리거하려면 Algolia 대시보드에서 가능합니다.

---

## 참고 자료

- [DocSearch 공식 문서](https://docsearch.algolia.com/docs/what-is-docsearch)
- [DocSearch 신청](https://docsearch.algolia.com/apply)
- [Algolia 대시보드](https://www.algolia.com/dashboard)
