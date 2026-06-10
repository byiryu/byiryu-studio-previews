# byiryu-studio-previews

byiryu studio 프로젝트 미리보기 · 디자인 시스템 · 검증 자료 저장소.

**랜딩:** https://byiryu.github.io/byiryu-studio-previews/

## 구조

```
byiryu-studio-previews/
├── index.html                       # 스튜디오 랜딩 (프로젝트 목록 + 도구)
├── studio/
│   └── logo-concepts.html           # 스튜디오 로고 컨셉 보드 (SVG 6안)
├── tools/
│   └── color-palette-viewer.html    # 컬러 팔레트 뷰어 (필터 기반)
│
├── weather-outfit/                  # PALETI (v1.x 출시)
│   ├── index.html                   # 프로젝트 인덱스 (sanity + design)
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
