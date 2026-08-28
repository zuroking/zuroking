# PROTOCOL.md: 기술 기반 개발(Skill-Driven Development) 에코시스템

**Languages:** [English](PROTOCOL.md) · [Русский](PROTOCOL_ru.md) · [العربية](PROTOCOL_ar.md) · [中文](PROTOCOL_zh.md) · [Deutsch](PROTOCOL_de.md) · [Español](PROTOCOL_es.md) · [Français](PROTOCOL_fr.md) · [日本語](PROTOCOL_ja.md) · **한국어** · [Português](PROTOCOL_pt.md)

## 1. 개념 및 철학

이 문서는 하이브리드 에이전트 에코시스템에 맞게 조정된 포트폴리오 내의 개발 방법론을 설명합니다. 프로토콜은 초기 아키텍처 설계에서 최종 프레젠테이션 아티팩트 생성에 이르기까지 제품 라이프사이클의 전체 과정을 다룹니다.

핵심 원칙: **아키텍처 결정은 명시적이고, 재현 가능하며, 옹호할 수 있어야 합니다.** 우리는 단순히 코드를 작성하는 것에서 정기적인 작업, 디자인, 테스트 및 분석을 특정 에이전트의 전문 기술에 위임하는 **기술 기반 개발(Skill-Driven Development)**로 전환했습니다.

---

## 2. 역할 및 기술 분배

이 프로세스에는 세 가지 주요 엔티티와 통합 에이전트 환경이 참여합니다. 이들의 역할은 엄격하게 구분되며 서로 겹치지 않습니다.

### 2.1. 개발자 (인간)
제품 소유자. 모든 아키텍처 결정 시점에 대한 최종 결정권을 가지며, 범위를 승인하고, 개발 방향을 설정하며, 에이전트의 결과물을 수락합니다.

### 2.2. OpenCode (자율 실행자)
최대 1M 토큰의 컨텍스트 창을 갖고 터미널에서 작동하는 실행 에이전트. 코드 작성, 인터페이스 구축, 문서 및 미디어 아티팩트 생성을 담당합니다.
다음과 같은 기술 무기고를 보유하고 있습니다:
*   **엔지니어링 및 코드:** `code-review-skill`, `webapp-testing`, `mcp-builder`, `skill-creator`, `claude-api`.
*   **디자인 및 프론트엔드:** `frontend-design`, `web-artifacts-builder`, `theme-factory`, `canvas-design`, `algorithmic-art`, `brand-guidelines`.
*   **문서 및 오피스:** `build-project-docs`, `doc-coauthoring`, `docx`, `pdf`, `pptx`, `xlsx`.
*   **커뮤니케이션 및 교육:** `academy-guide`, `internal-comms`, `slack-gif-creator`, `discernment-nudge`.

### 2.3. Claude Desktop (아키텍트 및 분석가)
데이터 센터 및 아키텍처 검토자 역할을 합니다. 프로덕션 코드를 직접 작성하지는 않지만 로직을 검증하고 데이터베이스 데이터를 분석하며 OpenCode를 위한 작업을 공식화합니다.
기술 무기고:
*   **컨텍스트 관리:** `morning`, `Import-memory`, `skill-creator`, `doc-coauthoring`.
*   **분석 및 검증:** `analyze`, `data-context-extractor`, `explore-data`, `validate-data`, `statistical-analysis`.
*   **DB 및 데이터 시각화:** `sql-queries`, `write-query`, `build-dashboard`, `create-viz`, `data-visualization`.

### 2.4. Antigravity (통합 에이전트 환경)
33개의 모든 기술이 통합된 완전히 자율적인 환경.
*   **핵심 규칙:** 앞으로 모든 프로젝트 문서는 기술에 대한 제한 없는 접근 권한을 가진 최고의 문서화 도구로서 Gemini 및 Claude 모델을 활용하여 Antigravity를 통해서만 생성되고 유지되어야 합니다.

---

## 3. 프로토콜 단계 (프로젝트 라이프사이클)

### 단계 1: 초기화 및 ARCHITECTURE.md
단 한 줄의 코드가 작성되기 전에 아키텍처가 공식화됩니다.
1.  **Claude Desktop**은 `morning` 및 `Import-memory` 기술을 활성화하여 컨텍스트와 이전 작업을 로드합니다. 그런 다음 `analyze`를 적용하여 요구 사항을 분해합니다.
2.  **OpenCode**는 `build-project-docs`를 사용하여 `ARCHITECTURE.md` 초안을 만듭니다.
3.  문서가 구체화됩니다: 데이터 구조, 저장 형식, 기술 스택 및 모듈 분류.

### 단계 2: Grill-me (아키텍처 스트레스 테스트)
아키텍처는 신념만으로 받아들여지지 않습니다. 반드시 분석되고 도전받아야 합니다.
1.  **Claude Desktop**은 데이터의 '맹점'을 식별하기 위해 `data-context-extractor`를 적용하고 까다로운 질문을 생성하기 위해 `doc-coauthoring`을 적용합니다.
2.  **OpenCode**는 제안된 기술 솔루션에 대한 비판적인 자기 평가를 위해 `discernment-nudge`를 사용할 수 있습니다.
3.  논쟁의 여지가 있는 모든 결정 시점은 **선택한 솔루션 -> 대안을 거부한 이유 -> 범위에서의 제외 사항**의 삼각 구조로 마무리됩니다.

### 단계 3: 의도적인 일탈 (Deliberate Deviations)
`ARCHITECTURE.md` 내에 우리가 **의식적으로 빌드하지 않기로 선택한** 모든 기능과 능력을 기록하는 섹션입니다. 프로젝트 능력의 경계는 아키텍처의 완전한 일부입니다. 개발 중에 결정이 변경되면 이전 결정은 이유와 함께 이 섹션으로 이동합니다.

### 단계 4: 모듈별 구현
개발은 종속성 그래프를 따라 상향식으로 진행됩니다.
1.  **OpenCode**는 프로젝트 코어를 구현합니다. 통합 및 프로토콜의 경우 `mcp-builder` 및 `claude-api`가 활용됩니다.
2.  비주얼 관련 작업을 할 때, **OpenCode**는 `brand-guidelines` -> `theme-factory` -> `frontend-design` -> `web-artifacts-builder` 체인을 활성화합니다.
3.  절차적 그래픽 생성 또는 복잡한 캔버스의 경우 `algorithmic-art` 및 `canvas-design`이 적용됩니다.

### 단계 5: 코드 검토 및 테스트
검증은 항상 코드 작성과 분리됩니다.
1.  **OpenCode**는 `code-review-skill`을 사용하여 별도의 패스를 수행하여 버그와 타협점을 식별합니다.
2.  UI 및 통합 테스트는 `webapp-testing` 기술을 통해 수행됩니다. 테스트 출력(stdout/stderr)은 수정 없이 저장됩니다.
3.  **Claude Desktop**이 데이터 처리 검증에 개입합니다: 데이터베이스 무결성을 확인하기 위해 `sql-queries` 및 `write-query`를 사용하고, 비즈니스 로직을 검증하기 위해 `validate-data` 및 `statistical-analysis`를 사용합니다.

### 단계 6: 아티팩트 및 분석 생성
프로젝트가 사용자 또는 이해관계자에게 제시되어야 합니다.
1.  **Claude Desktop**은 `build-dashboard`, `create-viz`, `data-visualization`을 사용하여 애플리케이션 결과 또는 메트릭을 기반으로 보고서를 작성합니다.
2.  **OpenCode**는 이 데이터를 즉시 사용 가능한 비즈니스 아티팩트로 패키징합니다:
    *   보고서 및 사양: `pdf`, `docx`, `xlsx` 기술.
    *   아키텍처 프레젠테이션: `pptx` 기술.
    *   교육 및 내부 자료: `academy-guide`, `internal-comms`.
    *   공고용 동적 콘텐츠: `slack-gif-creator`.

### 단계 7: 최종 체크리스트
출시 전 다음 사항이 검증됩니다:
*   최종 코드와 `ARCHITECTURE.md`의 동기화.
*   실제 테스트 로그의 존재.
*   임시 파일, 캐시 및 비밀 키의 부재.

---

## 4. 모델 선택 정책 (Model Selection Policy)

OpenCode는 무료 모델에서 실행되며, 선택은 작업에 따라 결정됩니다:

| 모델 | 역할 | 목적 | 개인정보 보호 상태 |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.2 Free** | 자율 에이전트 (코어) | 메인 기술 매트릭스 실행, 1M 토큰 컨텍스트, 터미널에서의 다단계 로직. | 영구 무료 등급 |
| **Nemotron 3 Ultra Free** | 심층 분석가 | 무거운 수학, 복잡한 알고리즘, 대규모 시스템 리팩토링. | **NVIDIA 체험판** — 제품 개선을 위해 데이터가 로깅됩니다. |
| **Nemotron 3.5 Lightning Free** | 백그라운드 실행자 | 빠른 검증, 유틸리티 함수 호출, 대량 파이프라인 처리. | **NVIDIA 체험판** — Ultra와 동일. |
| **MiMo V2.5 Free** | UI/UX 도우미 | 스크린샷 디버깅, 즉석 `frontend-design`. | 임시 무료 기간. |

**Antigravity**의 경우, 제한/할당량 소모를 최소화하고 작업 및 문서화 작업을 지속할 수 있도록 **Gemini 3.5 Flash (Medium)**가 기본 엔진으로 사용됩니다.

**보안 제한:** 체험판 엔드포인트(Nemotron, MiMo)로 개인 키, 토큰, 실제 데이터베이스 및 비공개 저장소를 전달하는 것은 **엄격히 금지**됩니다. 민감한 데이터에는 로컬 또는 신뢰할 수 있는 환경만 사용됩니다.

---

## 5. 핵심 에코시스템 원칙

1. **명시적인 결정이 편리한 기본값보다 낫습니다.** 에이전트가 갈림길에 서면 추측하지 않고 옵션을 공식화하고 승인을 기다립니다(또는 타협점을 기록합니다).
2. **기술은 의도된 목적으로 사용됩니다.** Excel 보고서가 필요한 경우 Markdown 테이블을 생성할 필요가 없습니다(`xlsx` 사용). 대시보드를 텍스트로 설명할 필요가 없습니다(`build-dashboard` + `create-viz` 사용).
3. **검토 중 발견된 버그는 정상 작동하는 시스템을 의미합니다.** `code-review-skill`을 통해 검토 단계에서 발견된 문제점은 2단계 필터가 작동한다는 증거입니다.
4. **프로젝트 경계는 침해할 수 없습니다.** 불완전한 만능 도구보다 의도적인 일탈(Deliberate Deviations) 섹션이 명확히 문서화된 고도로 전문화된 도구가 더 낫습니다.
