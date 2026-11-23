# XeoLab AI Search Optimization

XeoLab AI Search Optimization is operated by Mango Creative Co., Ltd. (MNGC). The skill ID is `xeolab-geo-optimizer`. Korean is the primary language; English is supported when needed. [한국어](README.ko.md)

It audits SEO, AEO, GEO, LLMO and Naver using evidence, proposes prioritized improvements, and supports verification and measurement of approved work. The inherited playbook covers crawler-facing HTML and indexing, structured data and llms.txt, Naver Search Advisor, content backlog and publishing gates, refresh and measurement.

Changes to a customer's site or code, deployment, publishing or editing content, external submissions and account settings require the user's **explicit approval of the specific target and scope**. An audit request alone does not authorize execution. AI visibility or citations, search rankings and revenue increases are never guaranteed.

## Install and use

Install directly from the public repository.

Local plugin installation in Claude Code:

```text
/plugin marketplace add alstlr0215-del/xeolab-geo-optimizer
/plugin install xeolab-geo-optimizer@xeolab-geo-optimizer
```

Alternatively clone the repository as a project skill:

```bash
git clone https://github.com/alstlr0215-del/xeolab-geo-optimizer.git .agents/skills/xeolab-geo-optimizer
```

Claude Code users can copy the complete skill directory to `.claude/skills/xeolab-geo-optimizer` or `.agents/skills/xeolab-geo-optimizer` in your project. For personal installation use `~/.claude/skills/xeolab-geo-optimizer` or `~/.agents/skills/xeolab-geo-optimizer`. Keep `SKILL.md` and `references` together. Restart the agent or reload skills after installation.

```text
/xeolab-geo-optimizer Audit https://example.com and report evidence and priorities
```

Invocation depends on the agent environment; selecting the skill and requesting the audit in natural language is also an option.

## Reports and checks

For each finding, report the problem, evidence and observation date, severity, recommendation, estimated scope, whether approval is required and its status, and follow-up metrics, baseline and timing. After implementation add changes and verification. See the [XeoLab workflow](references/en/xeolab-workflow.md).

The Korean references are canonical and `references/en/` mirrors them. Repository checks require only Python 3's standard library:

```bash
python3 tools/validate.py
python3 -m unittest discover -s tests -t .
```

## Origin and license

This project is adapted from [fire-your-seo-agency](https://github.com/leopard627/fire-your-seo-agency), originally authored by leopard627. Upstream work is not represented as an XeoLab or MNGC achievement. The original copyright notice and full MIT license remain in [LICENSE](LICENSE).
