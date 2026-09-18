# namdo-trip-2026

## 이 저장소가 하는 일
노션 페이지 "남도 여행 일정표"(2026.11.20~22, 8명, 순천-여수-보성/구례-하동)를 모바일 친화적인 단일 HTML 페이지로 만들어 GitHub Pages로 게시한 것. 지인들에게 링크로만 공유하는 용도.

- 게시 URL: https://line20061114-crypto.github.io/namdo-trip-2026/
- GitHub Pages 설정: Settings → Pages → Deploy from a branch → `main` / `(root)`

## 파일 구성
- `index.html` — 페이지 본체 (단일 파일, 인라인 CSS만 사용, 외부 라이브러리/폰트 의존 없음)
- `robots.txt` — 전체 크롤링 차단 (`Disallow: /`)
- (선택) `.nojekyll` — Jekyll 처리 방지용, 없어도 현재는 문제 없음

## 필수 요건 (수정 시 반드시 유지)
1. **검색엔진 노출 차단**: `robots.txt`의 `Disallow: /`와 `index.html` `<head>`의
   `<meta name="robots" content="noindex, nofollow, noarchive, nosnippet">` 두 가지를 절대 제거하지 말 것.
   링크를 아는 사람만 접근 가능해야 하고, 검색/색인에는 노출되면 안 됨.
2. GitHub Pages 무료 플랜은 완전 비공개(로그인 필요)를 지원하지 않음 — URL을 아는 사람은 누구나 접근 가능한 상태가 최선임을 사용자도 인지하고 있음.
3. 외부 이미지(S3 서명 URL 등 만료되는 링크)는 넣지 않음 — 노션 원본에 있던 사진들은 서명 URL이 금방 만료되어 의도적으로 제외함.

## 디자인 방향
- 모바일 퍼스트, 카드형 레이아웃, 라이트/다크모드 모두 대응(`prefers-color-scheme`)
- 일자별 일정은 `<details>` 아코디언(타임라인 스타일)으로 구성, JS 없이 순수 HTML/CSS
- 웜톤 뉴트럴 팔레트(테라코타/그린 accent) — 특허법인 C&S 업무용 네이비/코랄 디자인 시스템과는 무관한 별도 개인 프로젝트임

## 수정 워크플로우
- 사소한 텍스트 수정: GitHub 웹에서 `index.html` 직접 편집(연필 아이콘) → Commit
- 구조적 수정: 로컬에서 `index.html` 수정 후 커밋 → Pages 반영까지 약 30초~1분

## 원본 데이터 출처
노션 페이지 "남도 여행 일정표" (참여자: 김영민, 김희경, 민윤희, 백무현, 안은숙, 유혜진, 임은진, 정희석).
일정이 노션에서 바뀌면 이 페이지도 수동으로 동기화해야 함 (자동 연동 없음).
