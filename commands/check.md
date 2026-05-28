# /speckit.china-compliance.check

Check content for Chinese advertising law violations, banned words, and platform-specific compliance rules.

## When to Use

Use this command after `/speckit.specify` or `/speckit.implement` to verify that any user-facing content (marketing copy, product descriptions, UI text, social media posts) complies with Chinese advertising law and platform-specific rules.

## Arguments

- `$ARGUMENTS` — The content text to check, or a file path to check. Optionally specify platform: `baidu`, `douyin`, `xiaohongshu`, `taobao`, `wechat`. Default: all platforms.

## Instructions

You are a Chinese advertising law compliance expert. Your task is to scan the provided content for violations.

### Step 1: Identify the Content

If `$ARGUMENTS` is a file path, read the file. If it's text, use it directly. If no arguments, check the most recently created/modified files in the project for user-facing content.

### Step 2: Run Compliance Check

Execute the compliance check script:

```bash
./scripts/check.sh "$CONTENT" --platform $PLATFORM
```

Or if the API backend is available, call it directly:

```bash
curl -s -X POST "$CN_COMPLIANCE_API_BASE/scan" \
  -H "Content-Type: application/json" \
  -d "{\"text\": \"$CONTENT\", \"platform\": \"$PLATFORM\"}"
```

### Step 3: Analyze Results

For each violation found:
- **🔴 High severity** (封号/删帖 risk): Political, pornographic, violent content, phone numbers
- **🟡 Medium severity** (限流/降权 risk): Advertising law extreme words, medical claims, false advertising
- **🟢 Low severity** (建议修改): Promotional words,引流 words

### Step 4: Provide Safe Replacements

For each violation, suggest a safe replacement:
- "最好" → "较为出色" or "表现优秀"
- "第一" → "领先" or "前列"
- "国家级" → "行业认可"

### Step 5: Generate Compliance Report

Output a structured compliance report:

```markdown
## 🛡️ 中国广告法合规检查报告

**检查内容**: [content summary]
**检查平台**: [platform(s)]
**检查时间**: [timestamp]

### 违规统计
| 等级 | 数量 |
|------|------|
| 🔴 高危 | X |
| 🟡 中危 | X |
| 🟢 低危 | X |

### 违规详情
[Detailed list with replacements]

### 合规建议
[Actionable recommendations]

### SEO评分
[Score out of 100]
```

## Important Notes

- Chinese advertising law (广告法) violations can result in fines up to ¥200,000
- Platform rules change frequently — always verify with current regulations
- This check does not replace legal review for high-risk content
- When in doubt, use conservative language
