# ECC 스킬 학습 진행 현황

> 마지막 업데이트: 2026-06-29 (connections-optimizer 완료)
> ✅ = 학습 완료 | ⬜ = 미학습

---

## ✅ 완료 (39개)

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [coding-standards](skills/coding-standards/SKILL.md) | 언어별 코딩 표준·컨벤션 정의<br>**패턴** 코드 스타일·네이밍·파일 구조 규칙화 → 일관된 코드베이스 유지 | ✅ |
| [hexagonal-architecture](skills/hexagonal-architecture/SKILL.md) | 도메인 로직을 DB·API·UI 등 외부 의존성으로부터 격리<br>**핵심** 포트(인터페이스)·어댑터(구현)로 경계 명시<br>**효과** 테스트가능성·교체가능성 확보 | ✅ |
| [git-workflow](skills/git-workflow/SKILL.md) | feature 브랜치·conventional commit·PR 리뷰 프로세스 정의<br>**목적** 팀 협업과 릴리스 이력 관리 | ✅ |
| [tdd-workflow](skills/tdd-workflow/SKILL.md) | RED → GREEN → REFACTOR 3단계 반복 개발 사이클<br>**효과** 설계 품질 향상·회귀 방지 | ✅ |
| [continuous-learning-v2](skills/continuous-learning-v2/SKILL.md) | 세션 종료 시 대화에서 패턴·결정·인사이트를 자동 추출<br>**저장** `~/.claude/memory`에 기록<br>**효과** 다음 세션에 컨텍스트 자동 제공 | ✅ |
| [e2e-testing](skills/e2e-testing/SKILL.md) | Playwright로 실제 브라우저 기반 E2E 테스트 작성<br>**패턴** Page Object Model로 유지보수성 확보<br>**연동** CI 파이프라인 | ✅ |
| [verification-loop](skills/verification-loop/SKILL.md) | 빌드·타입체크·린트·테스트·보안 스캔을 순서대로 실행<br>**목적** 코드 변경 후 종합 품질 게이트 통과 보장 | ✅ |
| [ai-regression-testing](skills/ai-regression-testing/SKILL.md) | LLM 출력 스냅샷 저장 → 모델 업데이트 시 비교<br>**목적** 예상치 못한 행동 변화 자동 감지 | ✅ |
| [eval-harness](skills/eval-harness/SKILL.md) | 테스트 케이스·채점 기준·기준선을 정의해 LLM 출력 정량 평가<br>**활용** 모델 비교·프롬프트 개선 | ✅ |
| [agent-eval](skills/agent-eval/SKILL.md) | 에이전트의 목표 달성·도구 사용·오류 복구 능력을 시나리오 기반으로 측정<br>**목적** 에이전트 신뢰도 정량화 | ✅ |
| [browser-qa](skills/browser-qa/SKILL.md) | 브라우저 자동화로 UI 요소 렌더링·인터랙션·접근성 자동 검증<br>**탐지** 시각적 회귀·기능 이상 | ✅ |
| [click-path-audit](skills/click-path-audit/SKILL.md) | 핵심 사용자 여정을 시뮬레이션해 클릭 경로의 단절·오류·UX 문제 감지<br>**목적** 사용자 흐름 무결성 검증 | ✅ |
| [benchmark](skills/benchmark/SKILL.md) | 코드 변경 전후 응답시간·처리량·메모리를 측정해 성능 회귀를 수치로 검증<br>**출력** 비교 리포트 생성 | ✅ |
| [workspace-surface-audit](skills/workspace-surface-audit/SKILL.md) | 설정파일·의존성·환경변수·CI 구성 등 개발환경 전반 점검<br>**목적** 문제 요소 식별 | ✅ |

---

## 🤖 에이전트/AI

### 에이전트 아키텍처 설계

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [santa-method](skills/santa-method/SKILL.md) | Implementer·Reviewer 에이전트를 별도 컨텍스트로 실행해 author bias 제거<br>**구조** 서로 상대방이 작성한 코드를 리뷰하는 적대적 교차검증 | ✅ |
| [ralphinho-rfc-pipeline](skills/ralphinho-rfc-pipeline/SKILL.md) | RFC를 의존성 DAG 유닛으로 분해<br>**파이프라인** 복잡도 티어별(trivial/small/medium/large) Research→Plan→Implement→Test→Review<br>**처리** 머지 큐에서 착지/evict, 최대 3패스 반복 | ✅ |
| [claude-devfleet](skills/claude-devfleet/SKILL.md) | MCP(localhost:18801)로 연결하는 외부 멀티에이전트 오케스트레이션 서버<br>**기능** `plan_project()`로 미션 DAG 생성, `dispatch_mission()`으로 에이전트를 격리된 worktree에 배포<br>**제한** 최대 3개 동시 실행 후 자동 머지 | ✅ |
| [agentic-engineering](skills/agentic-engineering/SKILL.md) | 에이전트 시스템을 체계적으로 운영하는 방법론<br>**핵심** eval-first 실행(기준선→구현→eval 비교), 15분 단위 작업 분해<br>**최적화** Haiku/Sonnet/Opus 모델 라우팅, 세션 전략·비용 추적 | ✅ |
| [ai-first-engineering](skills/ai-first-engineering/SKILL.md) | AI가 코딩을 담당하는 팀 운영 모델<br>**설계** 에이전트 친화적 아키텍처(명시적 경계·안정적 계약·결정론적 테스트)<br>**기준** eval 커버리지 중심 품질 관리 | ✅ |
| [council](skills/council/SKILL.md) | 정답 없는 트레이드오프 결정을 위한 다관점 검토 구조<br>**구성** Architect·Skeptic·Pragmatist·Critic 4개 관점을 별도 컨텍스트로 실행<br>**목적** anchoring 방지, 6단계 워크플로우로 구조적 의사결정 | ✅ |

### 에이전트 특수 기능

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [autonomous-loops](skills/autonomous-loops/SKILL.md) | 6가지 자율 루프 패턴 카탈로그<br>**패턴** Sequential Pipeline·NanoClaw REPL·Infinite Agentic Loop·Continuous Claude PR Loop·De-Sloppify·Ralphinho<br>**제공** 상황별 패턴 선택 기준과 조합 방법 | ✅ |
| [continuous-agent-loop](skills/continuous-agent-loop/SKILL.md) | autonomous-loops의 v1.8+ 정식 이름<br>**제공** 루프 선택 플로우 요약, 권장 프로덕션 스택(RFC분해·품질게이트·eval루프·세션지속성) 조합<br>**포함** 실패 모드·복구 절차 정의 | ✅ |
| [agent-introspection-debugging](skills/agent-introspection-debugging/SKILL.md) | 에이전트 실패 시 스스로 디버그하는 워크플로우<br>**단계** 포착→진단→최소복구→리포트 4단계<br>**특징** hidden runtime 아님, 명시적 절차 | ✅ |
| [context-budget](skills/context-budget/SKILL.md) | 세션 내 토큰 오버헤드 감사<br>**단계** 목록화→분류→문제감지→보고 4단계<br>**전략** MCP·에이전트·rules·CLAUDE.md 절감 방법 제시 | ✅ |
| [deep-research](skills/deep-research/SKILL.md) | firecrawl·exa MCP로 웹 검색·크롤링해 출처 명시 보고서 생성<br>**단계** 목표파악→계획→검색→심층읽기→종합→전달 6단계 워크플로우 | ✅ |

### LLM 비용/성능 최적화

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [token-budget-advisor](skills/token-budget-advisor/SKILL.md) | 답변 전 1–4 깊이 레벨 제시로 사용자가 응답 길이를 선택<br>**흐름** 입력 토큰 휴리스틱 추정→복잡도 분류→레벨별 응답 | ✅ |
| [prompt-optimizer](skills/prompt-optimizer/SKILL.md) | 거친 프롬프트를 분석해 최적화된 프롬프트로 변환<br>**파이프라인** 프로젝트 감지→의도→범위→ECC매핑→누락감지→모델권장 6단계<br>**역할** 자문만 수행, 직접 실행 안 함 | ✅ |

---

## 🔒 보안

### 코드/앱 보안 분석

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [security-review](skills/security-review/SKILL.md) | 배포 전 보안 취약점 점검<br>**체크리스트** Secrets·Input·SQLi·Auth·XSS·CSRF·RateLimit·SensitiveData·Blockchain·Deps 10개 항목<br>**패턴** httpOnly 쿠키·RLS·CSP·Double-Submit Cookie 제공 | ✅ |
| [security-scan](skills/security-scan/SKILL.md) | AgentShield로 `.claude/` 설정 전체 스캔<br>**대상** CLAUDE.md·settings.json·mcp.json·hooks·agents<br>**기능** 등급(A~F) 산출, 자동 수정, Opus 3-에이전트 심층 분석, GitHub Action CI 연동 | ✅ |
| [security-bounty-hunter](skills/security-bounty-hunter/SKILL.md) | 버그바운티 제출 기준으로 실제 악용 가능한 취약점만 탐색<br>**In-Scope** SSRF·Auth Bypass·RCE·SQLi·CMDi·Path Traversal·XSS 7가지 패턴<br>**방법** Source→Sink 흐름 추적, Quality Gate 6단계 | ✅ |

---

## ⚙️ 개발 워크플로우

### 설계/아키텍처

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [blueprint](skills/blueprint/SKILL.md) | 한 줄 목표를 멀티 세션/멀티 에이전트 구성 계획으로 변환<br>**파이프라인** Research→Design→Draft→Review→Register 5단계<br>**특징** Cold-start 실행, Dependency edge 기반 병렬 감지, 적대적 검토 게이트(Opus), Plan mutation protocol | ✅ |
| [api-design](skills/api-design/SKILL.md) | 프로덕션 REST API 설계 패턴<br>**규칙** URL 명명(복수 명사·케밥 케이스), HTTP 메서드·상태 코드 의미 체계<br>**패턴** 응답 봉투, 오프셋/커서 페이지네이션, 필터링/정렬, 인증/인가, 요율 제한(Retry-After)<br>**버전** URL 경로 버전 관리(Sunset 헤더 RFC 8594) | ✅ |
| [architecture-decision-records](skills/architecture-decision-records/SKILL.md) | 코딩 세션 중 아키텍처 결정을 구조화된 문서로 캡처<br>**구조** Context·Decision·Alternatives·Consequences 4섹션<br>**생명주기** proposed→accepted→deprecated/superseded<br>**원칙** Mitigation 명시, 트레이드오프 명시, "why 중심" 기록 | ✅ |
| [backend-patterns](skills/backend-patterns/SKILL.md) | 확장 가능한 서버 사이드를 위한 백엔드 패턴 모음<br>**구조** Repository·Service Layer·Middleware(HOF)<br>**성능** N+1 방지(배치 조회), Cache-Aside(Redis)<br>**운영** 중앙화 오류 핸들러, Exponential Backoff, RBAC, 구조화 로깅 | ✅ |
| [mcp-server-patterns](skills/mcp-server-patterns/SKILL.md) | MCP 서버 구축·통합 패턴<br>**구성요소** Tool(액션)·Resource(URI 기반 읽기전용)·Prompt(템플릿) 3종<br>**트랜스포트** stdio(로컬) vs Streamable HTTP(원격)<br>**주의** SDK API는 버전마다 달라 공식 문서 필수 확인 | ✅ |
| [codebase-onboarding](skills/codebase-onboarding/SKILL.md) | 새 코드베이스 온보딩·파악 전략<br>**단계** 정찰→아키텍처 매핑→컨벤션 감지→결과물 생성 4단계<br>**출력** 온보딩 가이드 + CLAUDE.md 생성<br>**원칙** Glob/Grep으로만 정찰, 기존 CLAUDE.md 보완(교체 금지), 추측 금지 | ✅ |
| [claude-api](skills/claude-api/SKILL.md) | Python/TypeScript SDK로 Claude API 호출<br>**기능** Messages API, Streaming, Tool Use(3메시지 루프), Vision(base64), Extended Thinking<br>**비용 절감** Prompt Caching(최대 90%), Batches API(50%)<br>**모델** Opus·Sonnet·Haiku 선택 기준 | ✅ |

### 자동화/운영

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [automation-audit-ops](skills/automation-audit-ops/SKILL.md) | 자동화 현황을 증거 기반으로 전수조사<br>**대상** 훅·GitHub Actions·MCP·커넥터<br>**분류** configured/stale/broken/missing → keep/merge/cut/fix-next 판단<br>**원칙** 수정 전 감사 먼저 | ✅ |
| [github-ops](skills/github-ops/SKILL.md) | gh CLI로 GitHub 저장소 운영<br>**이슈** 유형·우선순위 레이블, good-first-issue 분류<br>**PR** 5일 이상 flag·stale policy, CI/CD 실패 분석(flaky test 구분)<br>**릴리즈** changelog 생성, Dependabot 보안 모니터링 | ✅ |
| [terminal-ops](skills/terminal-ops/SKILL.md) | 증거 우선(evidence-first) 터미널 실행 워크플로우<br>**단계** surface 파악→실패 먼저 읽기→좁은 수정→정확한 상태 보고<br>**상태** inspected/changed locally/verified locally/committed/pushed/blocked<br>**원칙** 증명 명령 재실행 전 "수정됐다" 금지 | ✅ |

### 멀티에이전트 패턴

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [nanoclaw-repl](skills/nanoclaw-repl/SKILL.md) | `claude -p` 래핑 세션 인식 REPL<br>**저장** `~/.claude/claw/<name>.md`에 대화 영속 저장<br>**명령** `/branch` 분기·`/compact` 압축·`/search` 세션 간 검색<br>**원칙** 핸들러는 결정론적·로컬 유지 | ✅ |

---

## ☕ Java/Spring

### 코딩 표준

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [java-coding-standards](skills/java-coding-standards/SKILL.md) | Java 17+ 코딩 표준·컨벤션 가이드<br>**네이밍** PascalCase/camelCase<br>**불변성** `record`·`final`, Optional 체인, sealed class + pattern matching<br>**검증** Bean Validation(`@NotBlank`·`@NotNull`), 도메인별 커스텀 예외<br>**테스트** JUnit5+AssertJ | ✅ |

### Spring Boot

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [springboot-patterns](skills/springboot-patterns/SKILL.md) | Spring Boot 아키텍처·API 패턴<br>**계층** Controller→Service→Repository, `@Transactional`/`readOnly`<br>**예외** `@ControllerAdvice` 중앙 처리, RFC 7807 에러 표준<br>**성능** `@Cacheable`/`@Async`, `OncePerRequestFilter`(Rate Limiting)<br>**보안** X-Forwarded-For는 getRemoteAddr 사용, Micrometer+Prometheus 관찰 가능성 | ✅ |
| [springboot-tdd](skills/springboot-tdd/SKILL.md) | Spring Boot TDD 개발 사이클<br>**4계층** 단위(@Mock)·웹(@WebMvcTest)·통합(@SpringBootTest)·영속성(@DataJpaTest)<br>**DB** Testcontainers+@DynamicPropertySource<br>**커버리지** JaCoCo(prepare-agent→jacoco.exec→report), Maven phase/goal 관계 | ✅ |
| [springboot-security](skills/springboot-security/SKILL.md) | Spring Boot 보안 구성 패턴<br>**인증** JWT(단기)+Refresh Token, @PreAuthorize 인가, BCrypt/Argon2<br>**방어** Bean Validation, SQL 인젝션 방지, CSRF(세션=활성/Bearer=비활성)<br>**운영** 시크릿 외부화, CSP·frameOptions·CORS, Bucket4j 속도 제한<br>**스캔** OWASP/Snyk 의존성 스캔, JSON 구조화 로깅 | ✅ |
| [springboot-verification](skills/springboot-verification/SKILL.md) | Spring Boot 6단계 검증 루프<br>**단계** 빌드(-T 병렬)→정적분석(SpotBugs/PMD/Checkstyle)→테스트+JaCoCo 80%+→보안스캔(OWASP+grep 시크릿)→Spotless 포맷→Diff 검토<br>**판정** Output Template으로 READY/NOT READY 결정 | ✅ |

---

## 🗄️ DB

### 데이터베이스 마이그레이션

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [database-migrations](skills/database-migrations/SKILL.md) | 안전한 DB 스키마 마이그레이션 전략·롤백 계획<br>**5대 원칙** 불변·순방향·분리·규모테스트·파일화<br>**PostgreSQL** CONCURRENTLY·expand-contract·배치+SKIP LOCKED<br>**툴** Prisma/Drizzle/Kysely/Django/golang-migrate<br>**무중단** EXPAND→MIGRATE→CONTRACT 3단계 | ✅ |

---

## 🐳 인프라/배포

### 컨테이너/배포

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [docker-patterns](skills/docker-patterns/SKILL.md) | Docker·Compose 컨테이너화 모범 사례<br>**Dockerfile** 멀티 스테이지(deps→dev→build→production)<br>**볼륨** named·bind·anonymous 3종, Override 파일, 서비스 이름 DNS 네트워킹<br>**보안** non-root·cap_drop·read_only·no-new-privileges, 안티패턴 | ✅ |
| [deployment-patterns](skills/deployment-patterns/SKILL.md) | 프로덕션 배포 전략·CI/CD 파이프라인 패턴<br>**전략** 롤링·블루-그린·카나리<br>**인프라** Kubernetes 프로브(liveness·readiness·startup), 12-Factor 환경 설정(zod 검증)<br>**운영** GitHub Actions 파이프라인, 롤백 전략<br>**체크리스트** 애플리케이션·인프라·모니터링·보안·운영 | ✅ |

### 릴리스/모니터링

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [dashboard-builder](skills/dashboard-builder/SKILL.md) | 운영자 질문 중심 모니터링 대시보드 구축 방법론<br>**원칙** Vanity board 금지·Guardrail 4원칙<br>**5대 운영 질문** 헬스·지연·처리량·Saturation·Upstream health<br>**보드** overview→performance→resources→서비스별<br>**품질** 제목·단위·임계값 필수 | ✅ |
| [canary-watch](skills/canary-watch/SKILL.md) | 배포 후 URL 회귀 모니터링<br>**감시 항목** HTTP Status·Console Errors·Network Failures·LCP/CLS/INP·Content·API Health 6종<br>**모드** Quick check·Sustained watch·Diff mode(카나리 vs 프로덕션 비교)<br>**알림** critical→warning→info 3단계 임계값 | ✅ |

---

## 🖥️ 프론트엔드 + Python

### 프론트엔드 패턴

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [frontend-patterns](skills/frontend-patterns/SKILL.md) | React/Next.js 프론트엔드 패턴 모음<br>**컴포넌트** Composition·Compound Components·Render Props<br>**훅** useToggle·useQuery·useDebounce<br>**상태** Context+useReducer<br>**성능** useMemo·useCallback·lazy+Suspense·Virtualization<br>**UX** Controlled Form·ErrorBoundary·Framer Motion·키보드 내비게이션 | ✅ |

### Python 패턴

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [python-patterns](skills/python-patterns/SKILL.md) | Python 핵심 설계 패턴·코드 품질 가이드<br>**3대 원칙** EAFP·Readability·Explicit<br>**타입** Union·TypeVar·Protocol, DataClass·NamedTuple<br>**고급** 데코레이터(functools.wraps·클래스 기반), 동시성(Threading/Multiprocessing/Async-Await)<br>**최적화** `__slots__` 메모리 절감, pyproject.toml 패키지 관리 | ✅ |
| [python-testing](skills/python-testing/SKILL.md) | pytest 기반 Python 테스트 전략·픽스처<br>**사이클** TDD RED→GREEN→REFACTOR, 커버리지 80%+<br>**픽스처** 스코프·autouse·conftest·픽스처 간 의존<br>**파라미터화** parametrize·ids·params, 마커(-m·strict-markers)<br>**모킹** @patch·return_value·side_effect·mock_open·autospec<br>**기타** pytest-asyncio, pytest.raises, tmp_path | ✅ |

---

## 🎛️ ECC 도구

### 설정/감사

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [ck](skills/ck/SKILL.md) | 프로젝트 컨텍스트 저장·자동 주입 도구<br>**등록** projects.json으로 프로젝트 관리<br>**저장** `/ck:save`로 세션 상태(summary·leftOff·nextSteps·decisions·blockers) 기록<br>**주입** SessionStart 훅이 cwd 매칭으로 ~100 토큰 자동 제공 | ✅ |
| [configure-ecc](skills/configure-ecc/SKILL.md) | `AskUserQuestion` 기반 6단계 ECC 설치 마법사<br>**선택** Core/Niche, 45개 스킬, 8개 카테고리<br>**검증** 경로 참조 검증, 최적화 수행<br>**레벨** user-level vs project-level 설치 선택 가능 | ✅ |

### 스킬 관리

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [skill-comply](skills/skill-comply/SKILL.md) | 스킬·룰·에이전트 정의의 실제 준수율 자동 측정<br>**시나리오** supportive→neutral→competing 3단계 엄격도 자동 생성<br>**측정** `claude -p` 실행 후 툴 호출 트레이스를 LLM으로 분류·순서 검증<br>**출력** self-contained 보고서 | ✅ |
| [skill-stocktake](skills/skill-stocktake/SKILL.md) | Claude 스킬/커맨드 품질 자동 감사(audit)<br>**모드** Quick Scan(변경분만, 5–10분)·Full Stocktake(전체, 20–30분)<br>**흐름** Inventory→Quality Evaluation→Summary→Consolidation 4단계<br>**판정** Keep/Improve/Update/Retire/Merge 5종 verdict<br>**기준** Actionability·Scope fit·Uniqueness·Currency 4차원 | ✅ |
| [hookify-rules](skills/hookify-rules/SKILL.md) | 로컬 전용 패턴 감시 규칙 파일 생성<br>**형식** `.claude/hookify.{name}.local.md` 마크다운 파일<br>**이벤트** bash·file·stop·prompt 4가지<br>**액션** warn(기본)/block, 단순 `pattern` 또는 다중 `conditions`(AND)<br>**특징** Claude가 파일을 읽고 자율 준수하는 방식 (런타임 강제 아님) | ✅ |

### 외부 연결 빌더

| 스킬 이름 | 목적/요약설명 | 완료 |
|-----------|--------------|------|
| [connections-optimizer](skills/connections-optimizer/SKILL.md) | X·LinkedIn 네트워크를 검토 우선 방식으로 정리·확장·아웃리치<br>**모드** light-pass/default/aggressive 3종<br>**점수화** reciprocity·브리지 가치·최근 활동 기반<br>**초안** `brand-voice`로 사용자 목소리 그대로 작성<br>**원칙** 자동 발송 금지, 항상 검토 팩 먼저 제시 | ✅ |

---

> **진행 현황**: 60 / 60 완료 🎉
