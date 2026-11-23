# XeoLab AI Search Optimization

주식회사 망고크리에이티브(MNGC)가 운영하는 XeoLab의 AI 검색 최적화 스킬입니다. 스킬 ID는 `xeolab-geo-optimizer`입니다. 한국어를 우선하며 필요하면 영어로 지원합니다. [English](README.md)

SEO, AEO, GEO, LLMO, Naver의 기술·콘텐츠 상태를 근거에 따라 진단하고, 우선순위와 개선안을 제안하며, 승인된 작업의 검증과 후속 측정을 지원합니다. 크롤러 관점의 HTML·색인 진단, 구조화 데이터와 llms.txt, 네이버 서치어드바이저, 질문 백로그·콘텐츠 발행 게이트·갱신, 측정 루프를 포함합니다.

고객 사이트·코드 변경, 배포, 콘텐츠 게시·수정·삭제, 외부 제출 및 계정 설정 변경은 구체적인 대상과 범위에 대한 **명시적 사용자 승인 후**에만 실행합니다. 진단 요청만으로 실행이 승인되지는 않습니다. AI 노출·인용, 검색 순위, 매출 증가는 보장하지 않습니다.

## 설치 및 실행

공개 저장소에서 직접 설치할 수 있습니다.

Claude Code 로컬 플러그인 설치:

```text
/plugin marketplace add alstlr0215-del/xeolab-geo-optimizer
/plugin install xeolab-geo-optimizer@xeolab-geo-optimizer
```

또는 저장소를 복제해 스킬 디렉터리로 설치합니다:

```bash
git clone https://github.com/alstlr0215-del/xeolab-geo-optimizer.git .agents/skills/xeolab-geo-optimizer
```

Claude Code 사용자는 스킬 디렉터리 전체를 프로젝트의 `.claude/skills/xeolab-geo-optimizer` 또는 `.agents/skills/xeolab-geo-optimizer`에 복사합니다. 개인 설치는 각각 `~/.claude/skills/xeolab-geo-optimizer`, `~/.agents/skills/xeolab-geo-optimizer`를 사용합니다. `SKILL.md`와 `references`가 함께 있어야 합니다. 설치 후 에이전트를 다시 시작하거나 스킬을 새로 불러옵니다.

```text
/xeolab-geo-optimizer https://example.com 을 진단하고 근거와 개선 우선순위를 보고해줘
```

사용 가능한 호출 방식은 사용하는 에이전트 환경에 따릅니다. 스킬을 선택해 같은 요청을 자연어로 전달할 수도 있습니다.

## 보고와 검증

각 발견 사항에 문제점, 근거와 확인 시점, 중요도, 개선 방안, 예상 작업 범위, 실행 승인 필요 여부와 상태, 후속 측정 지표·기준선·시점을 기록합니다. 실행 이후에는 변경 전후와 검증 결과를 추가합니다. 자세한 절차는 [XeoLab 표준 업무 절차](references/xeolab-workflow.md)를 참조하세요.

`references/`에는 각 영역 및 콘텐츠·측정 기준이 있으며, 한국어 문서가 정본이고 `references/en/`은 영문 미러입니다. 저장소 검증은 Python 3 표준 라이브러리만 필요합니다.

```bash
python3 tools/validate.py
python3 -m unittest discover -s tests -t .
```

## 원본 및 라이선스

[fire-your-seo-agency](https://github.com/leopard627/fire-your-seo-agency)를 기반으로 수정했습니다. 원본 작성자는 leopard627이며 XeoLab 또는 MNGC의 실적으로 표시하지 않습니다. 원본 저작권 고지와 MIT 라이선스 전문은 [LICENSE](LICENSE)에 보존되어 있습니다.
