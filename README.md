# NAWA 홈페이지

NAWA가 만드는 앱 **라클** 소개 페이지 (2026-11-23 NAWA 앱 → 라클로 문구·화면 교체). GitHub Pages로 배포한다.

- 주소: https://lacle.nawa.io.kr (가비아 CNAME `lacle` → kyungdh93.github.io). NAWA 대표 페이지 nawa.io.kr 는 `nawa-home` 저장소
- 빌드 도구 없음. `index.html`과 `assets/`만 수정하면 된다.

## 내용 기준

소개 문구는 앱 저장소의 정책서(`nawa/policy/`, 현재 기준 버전)와 맞춘다. 정책서가 바뀌면 기능·약속·로드맵 문구를 함께 확인한다.

## 구조

| 경로 | 내용 |
| --- | --- |
| `index.html` | 페이지 전체 |
| `assets/style.css` | 스타일. 색은 앱 디자인 토큰(`nawa/mobile/src/theme/tokens.ts`)과 같다. 화면 모드는 앱과 같이 시스템·라이트·다크 (고른 값은 `localStorage`의 `nawa-theme`, `<html data-theme>`) |
| `assets/img/` | 앱 화면 캡처(로컬 라클 웹 앱 390×802, 2배 — 홈·전체 기록·성장나무·성장스토리)와 라클 아이콘(`lacle/web/public`) |
| `robots.txt`, `sitemap.xml` | 검색 엔진용. 페이지를 추가하면 `sitemap.xml`에 주소와 `lastmod`를 넣는다 |
| `.nojekyll` | Jekyll 처리 끄기 |

## 로컬에서 보기

```bash
python3 -m http.server 8000   # http://localhost:8000
```

## 배포

`main` 브랜치에 push하면 1~2분 뒤 반영된다.
처음 한 번만: 저장소 Settings → Pages → Source `Deploy from a branch`, Branch `main` / `/ (root)`.

## 검색 노출

- `index.html` 머리에 대표 주소(canonical)·공유 정보(og)·구조화 데이터(JSON-LD, 사이트 이름 '라클' / 'Lacle')가 있다. 제목·설명을 바꾸면 og 값도 같이 바꾼다
- Google Search Console · 네이버 서치어드바이저에 사이트를 등록하고 `https://lacle.nawa.io.kr/sitemap.xml`을 제출한다 (소유 확인 메타 태그를 받으면 `index.html` 머리에 넣는다)
- GitHub Pages 설정에서 HTTPS 강제(Enforce HTTPS)를 켜 둔다
