# byiryu-studio-previews

byiryu studio 프로젝트 미리보기 · 디자인 시스템 · 검증 자료 저장소.

**랜딩:** https://byiryu.github.io/byiryu-studio-previews/

## 구조

```
byiryu-studio-previews/
├── index.html                       # 스튜디오 랜딩 (프로젝트 목록 + 스튜디오)
├── studio/
│   └── logo-concepts.html           # 스튜디오 로고 컨셉 보드 (SVG 6안)
│
├── weather-outfit/                  # PALETI (v1.x 출시)
│   ├── index.html                   # 프로젝트 인덱스 (sanity + design + 도구)
│   ├── color-palette-viewer.html    # 컬러 팔레트 뷰어 (날씨/계절/역할 필터)
│   ├── design/                      # 출시 디자인 프리뷰 (공개) — 구 design-preview-current/
│   │   ├── index.html               #   canonical 4종 + 버전별 프로토타입 이력
│   │   ├── design-system.html · components.html · prototype.html · widgets.html
│   │   └── prototype-v1.1.1-*.html · prototype-v1.2-*.html   # 버전별 이력
│   └── sanity/                      # 검증 자료 (의사결정 흔적)
│       ├── color-matrix.html · matrix-fallback.html · themes.html
│       ├── recommendation-samples.html · anchor-color-palette.html
│       ├── anchor-ux-walkthrough.html · settings-ia-prototype.html
│       ├── occasion-quality-board.html
│       └── _archive/                # 폐기·구버전 자료 (옛 알고리즘·디자인 탐색·구 스키마)
│
└── weaver/                          # 미니멀 회피 아케이드 (Unity, 기획·프로토타입)
    ├── index.html
    └── sanity/prototype-v1.html · prototype-v2.html
```

> `travel-illust` / `lego-builder` 는 설계 단계 — 디렉토리는 `/new` 착수 시 생성.

## ★ 인덱스 연결 의무 — 고아 페이지 금지 (필수 규칙, 2026-06-11)

**페이지를 추가·이동·삭제하는 모든 세션 (리드·마케팅·플랫폼) 동일 적용:**

1. 모든 페이지는 **루트 `index.html` → `{project}/index.html` → 페이지** 3단 체인으로 도달 가능해야 한다. `_archive/` 같은 하위 묶음도 자체 index + 부모 인덱스에서의 링크 필수
2. **페이지 추가와 인덱스 갱신은 같은 커밋** — 고아 페이지를 push 하지 않는다
3. **죽은 placeholder 링크 금지** — 페이지가 생기면 즉시 활성 링크, 없으면 링크를 두지 않는다
4. 인덱스 링크 라벨 = **한글 제목 + 날짜·1줄 설명 메타** (파일명 노출 X). superseded 자료는 흐림 처리 + 상태 라벨
5. push 전 `./check_orphans.sh` 실행 → `OK` 확인
6. **★ 비공개 진행 (unlisted) 상태** — 출시 전 자료를 공개 인덱스에서 숨기되 URL 직접 접근은 유지하고 싶을 때: (a) 루트 `.unlisted` 에 경로 prefix 등록 (예: `weaver/`) (b) 해당 페이지 전부 `<meta name="robots" content="noindex, nofollow">` 의무 (검색 노출 차단 — 스크립트가 검사) (c) 루트 index 카드 = "비공개 진행" 상태 표기, 링크 없음 (d) `{project}/index.html` 은 유지 — URL 아는 사람의 허브. **"잊힌 고아"와 "의도적 비공개"의 구분 = `.unlisted` 등록 여부**

상세 = `ApplicationProject/_docs/workflow.md` §8.7

## 공개 정책

**디자인 작업물 (`{project}/design/`)** — 프로젝트 출시 후 공개. 출시 전엔 로컬 보관.

**검증 자료 (`{project}/sanity/`)** — 의사결정 흔적, 출시 전 작업물이지만 추적 가능성을 위해 공개 유지.

상세 규칙은 워크플로우 마스터 문서 참조: `ApplicationProject/_docs/workflow.md`

## 호스팅

GitHub Pages — 푸시하면 자동 배포.

## 이력

| 일자 | 변경 |
|------|------|
| 2026-05-08 | `color-palette-viewer` 이름으로 V4-1 컬러 팔레트 뷰어 생성 |
| 2026-05-10~11 | weather-outfit 검증 자료 8건 추가 |
| 2026-05-11 | **`byiryu-studio-previews` 로 이름 변경.** 스튜디오 단위 표준 구조 (`{project}/design/` + `{project}/sanity/`) 도입 |
| 2026-06-10 | PALETI 출시 후 정리 — `weather-outfit/design-preview-current/` → `design/` 승격(공개), 고아 sanity 보드·로고 컨셉·버전 프로토타입 인덱스 연결, README 구조 정합 |
| 2026-06-10 | `tools/color-palette-viewer` → `weather-outfit/` 이동(PALETI 전용 도구), PALETI 카드 Google Play 링크 추가, weaver 카드 비활성화, 미리보기 카드 네이밍 간소화 |
| 2026-06-11 | **★ 인덱스 연결 의무 규칙 신설** (고아 페이지·죽은 링크 금지, workflow §8.7) + `check_orphans.sh` 추가 + weaver 카드 활성화 회수 (disabled placeholder → 실 링크) |
