# spec-kit Extension 提交指南

## 方式1：通过Issue模板提交（推荐）

1. 打开 https://github.com/github/spec-kit/issues/new?template=extension_submission.yml
2. 填写以下内容：

### Extension ID
china-compliance

### Extension Name
China Compliance Extension

### Version
1.0.0

### Description
Chinese advertising law compliance checker, AI search visibility auditor, and cross-border data compliance assessor for Spec-Driven Development. Covers 200+ banned words across 5 Chinese platforms, AI citation monitoring for 5 Chinese AI engines, and PIPL/GDPR/CCPA cross-border data transfer assessment.

### Author
lm203688

### Repository URL
https://github.com/lm203688/spec-kit-china-compliance

### Download URL
https://github.com/lm203688/spec-kit-china-compliance/archive/refs/tags/v1.0.0.zip

### License
MIT

### Required Spec Kit Version
>=0.1.0

### Number of Commands
3

### Commands
1. speckit.china-compliance.check — Check content for Chinese advertising law violations, banned words, and platform-specific compliance
2. speckit.china-compliance.geo-audit — Audit brand visibility in Chinese AI search engines
3. speckit.china-compliance.data-export — Assess cross-border data compliance (PIPL/GDPR/CCPA)

### Number of Hooks
0

### Tags
compliance, chinese, geo, legal

### Key Features
- Real API backend for compliance checks (no API key required for basic usage)
- 200+ banned words across 5 Chinese platforms with safe replacement suggestions
- AI search visibility scoring across 5 Chinese AI engines (DeepSeek, Kimi, 豆包, 通义千问, 文心一言)
- Cross-border data transfer assessment (PIPL + GDPR + CCPA)
- Risk-level classification (high/medium/low) with actionable fix suggestions
- Battle-tested: caught 23 violations in a single Douyin script that 3 human reviewers missed

### Testing
- [x] Extension tested on real projects
- [x] All commands work as expected
- [x] extension.yml manifest is valid
- [x] README.md with installation and usage instructions included
- [x] Compatible with Claude Code, Cursor, Windsurf, Codex CLI, Gemini CLI, OpenClaw

---

## 方式2：直接在浏览器打开

https://github.com/github/spec-kit/issues/new?template=extension_submission.yml&title=[Extension]:+Add+china-compliance

然后复制上面的内容填入对应字段。
