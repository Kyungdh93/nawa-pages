# NAWA 홈페이지

NAWA 회사·서비스 소개 페이지. GitHub Pages로 배포한다.

- 주소: https://kyungdh93.github.io/nawa-pages/
- 빌드 도구 없음. `index.html`과 `assets/`만 수정하면 된다.

## 구조

| 경로 | 내용 |
| --- | --- |
| `index.html` | 페이지 전체 |
| `assets/style.css` | 스타일. 색은 앱 디자인 토큰(`nawa/mobile/src/theme/tokens.ts`)과 같다 |
| `assets/img/` | 앱 화면 캡처(`nawa/prototype/screenshots`)와 파비콘 |
| `.nojekyll` | Jekyll 처리 끄기 |

## 로컬에서 보기

```bash
python3 -m http.server 8000   # http://localhost:8000
```

## 배포

`main` 브랜치에 push하면 1~2분 뒤 반영된다.
처음 한 번만: 저장소 Settings → Pages → Source `Deploy from a branch`, Branch `main` / `/ (root)`.
