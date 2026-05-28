# China Compliance Extension for Spec Kit

🛡️ Chinese advertising law, data compliance, and AI search visibility checks for Spec-Driven Development.

## Overview

This extension adds China-specific compliance checks to your Spec-Driven Development workflow. It helps you:

1. **Check content** for Chinese advertising law violations and platform-specific banned words
2. **Audit brand visibility** in Chinese AI search engines (DeepSeek, Kimi, 豆包, 通义千问, 文心一言)
3. **Assess cross-border data compliance** (PIPL, GDPR, CCPA) for applications handling Chinese user data

## Installation

```bash
specify extension add china-compliance
```

Or install from GitHub:

```bash
specify extension add china-compliance --from https://github.com/lm203688/spec-kit-china-compliance/archive/refs/tags/v1.0.0.zip
```

## Commands

### `/speckit.china-compliance.check`

Check content for Chinese advertising law violations, banned words, and platform-specific compliance.

```bash
# Check all platforms
/speckit.china-compliance.check "你的营销文案内容"

# Check specific platform
/speckit.china-compliance.check "文案内容" --platform douyin
```

Supported platforms: `baidu`, `douyin`, `xiaohongshu`, `taobao`, `wechat`

### `/speckit.china-compliance.geo-audit`

Audit brand visibility in Chinese AI search engines.

```bash
# Audit all Chinese AI engines
/speckit.china-compliance.geo-audit "你的品牌名"

# Audit specific engine
/speckit.china-compliance.geo-audit "品牌名" --engine deepseek
```

Supported engines: `deepseek`, `kimi`, `doubao`, `tongyi`, `ernie`

### `/speckit.china-compliance.data-export`

Assess cross-border data transfer compliance.

```bash
# Full compliance assessment
/speckit.china-compliance.data-export "电商应用，收集用户姓名、地址、支付信息，数据存储在AWS新加坡"

# Specific regulation
/speckit.china-compliance.data-export "应用描述" --scope pipl
```

## Workflow Integration

### After `/speckit.specify`

```bash
/speckit.specify          # Define your product spec
/speckit.china-compliance.check    # Verify content compliance
/speckit.china-compliance.geo-audit # Check AI search visibility
```

### During `/speckit.plan`

```bash
/speckit.plan             # Create implementation plan
/speckit.china-compliance.data-export  # Assess data compliance needs
```

### After `/speckit.implement`

```bash
/speckit.implement        # Implement the tasks
/speckit.china-compliance.check    # Final compliance verification
```

## Why This Extension?

- **广告法罚款可达20万元** — Chinese advertising law violations carry real financial penalties
- **AI搜索可见度** — If your brand isn't cited by DeepSeek/Kimi/豆包, you're invisible to 800M+ users
- **GDPR罚款可达€12亿** — Meta was fined €1.2B in 2023 for data transfer violations
- **数据出境评估** — Apps with >1M users must submit cross-border data transfer assessments

## API Backend

This extension uses a real API backend for compliance checks:

- **Compliance API**: `https://1341839497-2yuxt6z58d.ap-guangzhou.tencentscf.com`
- **GEO API**: `https://1341839497-2yuxt6z58d.ap-guangzhou.tencentscf.com`

No API key required for basic checks. Set `CN_COMPLIANCE_API_KEY` for extended usage.

## Related ClawHub Skills

This extension is powered by the same API backend as our ClawHub skills:

- [cn-seo-optimizer](https://clawhub.com/skills/cn-seo-optimizer) — 违禁词扫描+SEO合规检测
- [cn-geo-monitor](https://clawhub.com/skills/cn-geo-monitor) — AI搜索可见度+GEO审计
- [china-data-compliance](https://clawhub.com/skills/china-data-compliance) — PIPL/网络安全法合规

## License

MIT
