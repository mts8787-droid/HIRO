# 🐈‍⬛ HIRO

**Harness for Interactive Reporting Optimization**

> Built for beginners. Engineered for repetition.

HIRO optimizes how you build interactive dashboards with Claude Code. Instead of crafting data parsers, chart components, and newsletter templates from scratch every time, HIRO ships a reusable harness — **skills, rules, hooks, and scenario-based bootstraps** — that turns the manual workflow into a standardized, repeatable pipeline.

HIRO 는 Claude Code 로 인터랙티브 대시보드를 만드는 작업을 최적화합니다. 데이터 파서, 차트 컴포넌트, 뉴스레터 템플릿을 매번 처음부터 짜는 대신, HIRO 는 재사용 가능한 하네스 — **스킬·룰·훅·시나리오 기반 부트스트랩** — 를 제공해 수작업 워크플로우를 표준화된 반복 가능한 파이프라인으로 바꿉니다.

---

## 본 리포

본 리포는 [`my-geo-newsletter`](https://github.com/mts8787-droid/my-geo-newsletter) 의 **sanitized mirror** — `scripts/publish-hiro.mjs` 가 화이트리스트 파일만 복사해서 자동 동기화. 본 리포는 직접 수정하지 말고 원본 저장소에서 수정.

## 적용 (다른 프로젝트에 도입)

```bash
# 1) 본 리포 통째로 clone
git clone https://github.com/mts8787-droid/HIRO.git

# 2) 대상 프로젝트 루트에 복사
cp -r HIRO/.claude HIRO/CLAUDE.md HIRO/AGENTS.md HIRO/docs <your-project>/

# 3) Hook 실행 권한
cd <your-project>
chmod +x .claude/hooks/*.sh

# 4) Claude Code 실행 → CLAUDE.md / .claude/* 자동 로드
```

## 구조

| 파일/폴더 | 역할 |
|---|---|
| `CLAUDE.md` | Claude Code 프로젝트 헌법 (자동 로드) |
| `AGENTS.md` | OpenAI Codex / Antigravity 자동 로드 표준 |
| `.claude/settings.json` | Hook 등록 (JSON 강제 — 100% 시스템 차단) |
| `.claude/hooks/*.sh` | 자동 검사 스크립트 (syntax-check, block-dist, newsletter-guard) |
| `.claude/rules/*.md` | Rule 매뉴얼 (data / design / ai / newsletter) + BOOTSTRAP 시나리오 |
| `.claude/skills/<name>/SKILL.md` | 작업 매뉴얼 (data-add / design-chart / newsletter-make 등) |
| `.claude/agents/*.md` | Sub-Agent (read-only 진단 전담 등) |
| `docs/agents/**` | 사람용 미러 (HARNESS.html, CHART_LIBRARY.html, HUMAN_GUIDE.md) |

## 라이브 뷰

본 저장소 운영 인스턴스의 `/hiro` 페이지에서 인증 없이 열람 가능 (외부 게시).

---

🐈‍⬛ *히로 — 본 하네스의 마스코트 검은 고양이. 부트스트랩 시나리오 같은 대화형 작업에서 친근한 안내자로 말을 건넵니다.*
