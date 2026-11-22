# NAWA 홈페이지

NAWA가 만드는 앱 **라클** 소개 페이지 (2026-11-23 NAWA 앱 → 라클로 문구·화면 교체). GitHub Pages로 배포한다.

- 주소: https://kyungdh93.github.io/nawa-pages/
- 빌드 도구 없음. `index.html`과 `assets/`만 수정하면 된다.

## 내용 기준

소개 문구는 앱 저장소의 정책서(`nawa/policy/`, 현재 기준 버전)와 맞춘다. 정책서가 바뀌면 기능·약속·로드맵 문구를 함께 확인한다.

## 구조

| 경로 | 내용 |
| --- | --- |
| `index.html` | 페이지 전체 |
| `assets/style.css` | 스타일. 색은 앱 디자인 토큰(`nawa/mobile/src/theme/tokens.ts`)과 같다. 화면 모드는 앱과 같이 시스템·라이트·다크 (고른 값은 `localStorage`의 `nawa-theme`, `<html data-theme>`) |
| `assets/img/` | 앱 화면 캡처(로컬 라클 웹 앱 390×802, 2배 — 홈·전체 기록·성장나무·성장스토리)와 라클 아이콘(`lacle/web/public`) |
| `.nojekyll` | Jekyll 처리 끄기 |

## 로컬에서 보기

```bash
python3 -m http.server 8000   # http://localhost:8000
```

## 배포

`main` 브랜치에 push하면 1~2분 뒤 반영된다.
처음 한 번만: 저장소 Settings → Pages → Source `Deploy from a branch`, Branch `main` / `/ (root)`.
