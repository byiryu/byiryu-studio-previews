# weather-outfit (PALETI) — 디자인 프리뷰 (공개)

✅ **PALETI 출시(v1.1.x)에 따라 공개됨.** 이 디렉토리는 GitHub Pages 로 배포되는 출시 디자인 프리뷰입니다.
공개 URL: https://byiryu.github.io/byiryu-studio-previews/weather-outfit/design/

> 이전 이름은 `design-preview-current/`. 출시 후 정책(`{project}/design/` = 출시 시 공개)에 따라 `design/` 으로 승격됨 (2026-06-10).

워크플로우 마스터: `ApplicationProject/_docs/workflow.md` 섹션 8 (시각화 자료 정책)

---

## 포함 파일

### Canonical 디자인
| 파일 | 내용 |
|------|------|
| `index.html` | 디자인 프리뷰 허브 (canonical 4종 + 버전별 이력) |
| `design-system.html` | 토큰 시각화 — 컬러·타이포·스페이싱·라디우스·elevation·시스템 컬러 |
| `components.html` | 컴포넌트 카탈로그 — 버튼·카드·칩·input·태그 (Light/Dark) |
| `prototype.html` | 인터랙티브 프로토타입 — 8 화면 클릭 전환 |
| `widgets.html` | 위젯 시각화 — iOS Lock/Home(소·중) + Android Glance(소·중) |

### 버전별 프로토타입 이력 (의사결정 흔적)
| 파일 | 내용 |
|------|------|
| `prototype-v1.1.1-ia.html` | v1.1.1 설정 IA — 추천·코디 분리 + 진입점 리네임 |
| `prototype-v1.1.1-meta-chip.html` | v1.1.1 메타칩 재설계 — 성별·무드·계절 Before/After |
| `prototype-v1.2-occasion.html` | v1.2 상황(occasion) 입력 — '오늘의 상황' 섹션 + 메타칩 합류 |
| `prototype-v1.2-main-density.html` | v1.2 메인 헤더 압축 — AS-IS vs TO-BE |
| `prototype-v1.2-feedback.html` | v1.2 좋아요/싫어요 — 1탭 + OS 리뷰 시트 트리거 |
| `prototype-v1.2-share-card.html` | v1.2 오늘의 룩 공유 카드 — 미니멀/아이콘-리치/에디토리얼 |

## 로컬 보기 방법

```bash
cd weather-outfit/design && python3 -m http.server 8000
# → http://localhost:8000
```
또는 VSCode Live Server 확장, 또는 `open index.html` (file:// 일부 제약).

---

## 토큰 출처

`_docs/design-briefs/weather-outfit/design-system.md` 의 토큰을 그대로 적용.
컬러는 **Y1 (Warm Minimal 인디고)**.

---

## 변경 이력

| 일자 | 변경 |
|------|------|
| 2026-05-11 | 초안 — 4 HTML 빌드, Y1(인디고) 토큰 적용 |
| 2026-06-10 | `design-preview-current/` → `design/` 승격 (출시 후 공개). v1.1.1 / v1.2 프로토타입 이력 인덱스 합류 |
