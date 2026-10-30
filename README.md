<div align="center">

# ⚡ coralstay

**Autonomous Software Factory · Systems & eBPF Observability · Reference-Driven Engineering Katas**

[![Platform](https://img.shields.io/badge/platform-macOS%20arm64-000000?logo=apple&logoColor=white)](https://github.com/coralstay/dev-toolchain)
[![Toolchain](https://img.shields.io/badge/toolchain-asdf%20%2B%20git--bundle-F16436)](https://github.com/coralstay/dev-toolchain)
[![Foundry](https://img.shields.io/badge/architecture-Sigkill%20Foundry-6E56CF)](https://github.com/coralstay/coralstay-software-factory)
[![Languages](https://img.shields.io/badge/stack-C%2FC%2B%2B17%20%C2%B7%20Rust%20%C2%B7%20Go%20%C2%B7%20Java%2025%20%C2%B7%20Python%203.12%20%C2%B7%20POSIX%20sh-2EA44F)](https://github.com/coralstay/dev-toolchain)

</div>

---

## 🏛️ 4-Domain Engineering Architecture

전체 워크스페이스(`~/githubs`)와 GitHub 저장소(`github.com/coralstay`)는 역할과 책임에 따라 **4개의 도메인**과 **불변 오픈소스 컨테이너(`opensource/`)**로 엄격하게 분리·운영됩니다.

```text
~/githubs/
├── bin/                         # 통합 실행 명령어 (53종)
├── coralstay-software-factory/  # [1] 자율형 에이전트 소프트웨어 팩토리
├── dev-tools/                   # [2] 개발 인프라·관측·생산성 도구
├── freeride/                    # [3] 234권 원서 해부·실습(Kata) 연합체
├── toy-project/                 # [4] 풀스택·클라우드 통합 레퍼런스
└── opensource/                  # [5] 48종 오픈소스 버전 컨테이너 (.bundle)
```

---

### 1. 🏭 `coralstay-software-factory` — *Sigkill Foundry*
> **"처리량이 아니라 판단의 독립성이다."**  
> 태스크를 `backlog.md` 계층(마일스톤 · 태스크 · AC)으로 분해하고, 역할형 에이전트(`Implementer` · `Reviewer` · `Verifier` · `Logger`)를 독립 프로세스로 스폰한 뒤 작업 종료 즉시 `kill -9`로 회수하여 컨텍스트 오염을 원천 차단하는 소프트웨어 공장 아키텍처입니다.

| 저장소 | 공개 | 핵심 역할 | CLI 명령어 |
| :--- | :---: | :--- | :--- |
| **[coralstay-software-factory](https://github.com/coralstay/coralstay-software-factory)** | `Public` | Sigkill Foundry SDD(제안서·요구사항·아키텍처·구현계획) 설계 저장소 | `build-diagrams --help` |
| **[claude-code-agile-hooks](https://github.com/coralstay/claude-code-agile-hooks)** | `Public` | Claude Code 규율 레이어 (TDD/테스트 게이트, 상태 전이, 위상 정렬 작업 순서) | `agile-hooks-install --help`<br>`work-order --help` |
| **[coding-agent-git-commit-tool](https://github.com/coralstay/coding-agent-git-commit-tool)** | `Public` | 코딩 에이전트 커밋 메시지 규격 검증 및 모델·태스크 트레일러 자동 기록 훅 | `git-commit-tool --help` |
| **[agent-orchestrator](https://github.com/coralstay/agent-orchestrator)** | `Private` | 역할형 에이전트 독립 프로세스 스폰·회수 JVM 오케스트레이터 (Java 25 + Gradle) | `agent-orchestrator --help` |

---

### 2. 🧰 `dev-tools` — *Developer Tooling & Kernel Observability*
> macOS 개발 환경 부트스트랩, 2계층 `.tool-versions` 기반 언어·오픈소스(`@oss`) 버전 고정, L2~L7 커널 패킷/코드 추적, 에디터·문서 자동화를 담당하는 자체 제작 도구군입니다.

| 저장소 | 공개 | 핵심 역할 | CLI 명령어 |
| :--- | :---: | :--- | :--- |
| **[dev-toolchain](https://github.com/coralstay/dev-toolchain)** | `Public` | macOS 언어 런타임(`asdf` 8종) & 오픈소스(`@oss` 48종 `.bundle`) 통합 버전 매니저 | `dev-toolchain --help`<br>`dev-toolchain-uninstall --help` |
| **[ebpf-wire-to-code-tracer](https://github.com/coralstay/ebpf-wire-to-code-tracer)** | `Private` | eBPF(`libbpf` · `bpftool` · `bcc`) 기반 L2~L7 Pre-Compute 전 계층 가시성 트레이서 | — |
| **[omnivim](https://github.com/coralstay/omnivim)** | `Private` | Neovim · Vim · IdeaVim · VS Code 키바인딩 단일화 및 144개 인터랙티브 실습 드릴 | `omnivim --help` · `practice --help`<br>`check --help` · `reset --help` |
| **[central-docs-collector](https://github.com/coralstay/central-docs-collector)** | `Private` | 워크스페이스 내 설계·보안·운영 문서 및 AI 에이전트 지침/프롬프트 중앙 수집기 | `central-docs --help` |

---

### 3. 🥋 `freeride` — *F.R.E.E.-R.I.D.E.*
> **Federated Repositories for Extracting Every Reference Into Developer-Executed Katas**  
> *"이름은 무임승차(freeride)지만, 실체는 234권의 원서를 페이지마다 해부해 직접 손으로 코딩하고 테스트를 통과해야만 내릴 수 있는 수련 열차다."*

| 저장소 | 공개 | 핵심 도메인 및 수련 내용 | CLI / 실행기 |
| :--- | :---: | :--- | :--- |
| **[freeride](https://github.com/coralstay/freeride)** | `Private` | 8개 수련 트랙 마스터 연합 워크스페이스 및 `layout.yaml` 토폴로지 | — |
| **[doctree](https://github.com/coralstay/doctree)** | `Private` | Google Drive PDF 대장 · 3-Way SHA-256 동기화 · Apple Vision + Graphviz DOT 파서 | `doctree --help` |
| **[handcrafted-cpp](https://github.com/coralstay/handcrafted-cpp)** | `Private` | C/C++17, STL, 알고리즘(TAOCP·종만북), Linux 시스템 프로그래밍(TLPI·eBPF) 실습장 | `./scripts/run.sh`<br>`./scripts/test.sh` |
| **[handcrafted-java](https://github.com/coralstay/handcrafted-java)** | `Private` | Java 25 LTS 언어 명세(JLS), JVM 내부 구조 및 Spring 7 실습장 | `./gradlew test` |
| **[databases](https://github.com/coralstay/databases)** | `Private` | 데이터베이스 18권 기반 SQL · 스토리지 엔진 · 실행계획 튜닝 실습장 | `./scripts/test.sh` |
| **[devOps-LifeCycle](https://github.com/coralstay/devOps-LifeCycle)** | `Private` | 30개 AWS 클라우드 아키텍처 시나리오 및 Terraform · DevSecOps 검증 파이프라인 | `./scripts/test.sh` |
| **[coding-style-refactoring-principles](https://github.com/coralstay/coding-style-refactoring-principles)** | `Private` | 소프트웨어 공학 9대 명저 기반 클린 코드 · 리팩터링 · 단위 테스트 다국어 실습장 | `./scripts/test.sh` |

---

### 4. 🚀 `toy-project` — *End-to-End Production Reference*

| 저장소 | 공개 | 기술 스택 및 아키텍처 |
| :--- | :---: | :--- |
| **[react-next-spring-postgresql-terraform-aws](https://github.com/coralstay/react-next-spring-postgresql-terraform-aws)** | `Private` | **Next.js (React) · Spring Boot (Java 25) · PostgreSQL · Terraform · AWS · k3d** 기반 풀스택 및 클라우드 IaC 통합 레퍼런스 |

---

## 📦 2-Tier `.tool-versions` & Git Bundle 오픈소스 아키텍처

외부 오픈소스(48종)는 포크(Fork)로 계정을 오염시키지 않고 **원본(Upstream) 클론 + 버전별 불변 Git Bundle(`bundles/<tag>.bundle`) + 버전별 워크트리(`<tag>/`)** 구조로 로컬에서 직접 격리 관리합니다.

```text
opensource/in-use/<오픈소스명>/
├── upstream/               # 원본 upstream git clone
├── bundles/
│   └── <버전태그>.bundle   # git bundle create로 박제한 단일 파일 아카이브
├── <버전태그>/             # 프로젝트(.opensource/<이름>)가 심링크하는 버전 폴더
└── current -> <버전태그>   # 전역 기본 버전 심링크
```

- **1계층 (Global SSOT)**: [`dev-tools/dev-toolchain/.tool-versions`](https://github.com/coralstay/dev-toolchain/blob/main/.tool-versions) (`~/.tool-versions` 심볼릭 링크) — 8종 언어 런타임(`nodejs`, `pnpm`, `java`, `gradle`, `python`, `uv`, `rust`, `golang`) + 48종 오픈소스(`# @oss`) 기본 릴리스 태그 정의
- **2계층 (Project Local Override)**: `<project>/.tool-versions` — 프로젝트마다 필요한 언어 버전과 오픈소스 버전을 핀 고정하면 `dev-toolchain sync`가 `<project>/.opensource/<이름> -> ~/githubs/opensource/in-use/<이름>/<버전태그>` 심볼릭 링크를 자동 연결합니다.

```zsh
dev-toolchain status          # 글로벌 언어 8종 + 오픈소스 48종 번들 상태 + 프로젝트별 오버라이드 조회
dev-toolchain current         # 현재 작업 디렉토리($PWD)에 적용된 로컬 .tool-versions 확인
dev-toolchain project <이름>  # 특정 프로젝트의 언어 및 @oss 오픈소스 버전 조회
dev-toolchain sync            # 모든 @oss 버전 태그의 .bundle + <태그>/ 생성 및 심링크 동기화
```
