# balancewave-site

발란스웨이브 — 병원·의원 AI 검색(GEO) 마케팅 홈페이지의 **미리보기** 빌드입니다.

- 미리보기 주소: https://jpstudio5252-eng.github.io/balancewave-site/
- 정식 도메인: `balancewave.co.kr` (아직 이 저장소와 연결되지 않음)

## 이 저장소에 들어 있는 것

`gh-pages` 브랜치(= 이 브랜치) 루트가 GitHub Pages로 그대로 서비스되는 정적 빌드 결과물입니다.

| 경로 | 내용 |
|---|---|
| `/` | 홈 (한국어) |
| `/diagnosis/` | AI 검색 6항목 자체 진단 |
| `/services/` | 서비스 4단계·진행 순서 |
| `/cases/` | 실제 진단 사례 3건 |
| `/about/` | 대표 소개 |
| `/contact/` | 상담 문의 |
| `/en/` | English |
| `robots.txt` · `sitemap.xml` · `llms.txt` · `404.html` | 크롤러·AI 안내 파일 |

## 고치는 방법

원본 소스와 빌드 스크립트는 앱 워크스페이스의 `handoffs/🏥-발란스웨이브-병원-geo-사이트-제작/`에 있습니다.

1. `site.config.json`에서 값 변경 (상호·연락처·가격 공개 여부·사례 실명 여부·`site.base_url`)
2. `python3 build.py && python3 validate.py`
3. `site/` 내용을 이 저장소 루트에 복사 → `main`과 `gh-pages` 두 브랜치에 푸시

## 주의

- 이 빌드는 **미리보기**입니다. `site.base_url`이 미리보기 주소로 되어 있어 canonical·sitemap·JSON-LD가 미리보기 주소를 가리킵니다. 정식 게시 시 `site.base_url`을 `https://balancewave.co.kr`로, `site.preview`를 `false`로 바꿔 다시 빌드합니다.
- 가격(`pricing.public: false`)과 익명 사례 실명(`cases[].show_real_name: false`)은 공개 결정 전이라 화면에 나오지 않습니다.
