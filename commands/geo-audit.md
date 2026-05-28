# /speckit.china-compliance.geo-audit

Audit brand visibility in Chinese AI search engines (DeepSeek, Kimi, 豆包, 通义千问, 文心一言).

## When to Use

Use this command after `/speckit.specify` to understand how your brand or product appears in Chinese AI search results, or after `/speckit.implement` to verify that your content is optimized for AI citation.

## Arguments

- `$ARGUMENTS` — Brand name or product name to audit. Optionally specify engine: `deepseek`, `kimi`, `doubao`, `tongyi`, `ernie`. Default: all Chinese AI engines.

## Instructions

You are a Chinese AI search engine optimization expert. Your task is to audit brand visibility across Chinese AI search engines.

### Step 1: Identify the Brand

Use `$ARGUMENTS` as the brand name. If no arguments, look for brand/product names in the project's spec files.

### Step 2: Run Visibility Check

Execute the visibility check script:

```bash
./scripts/check-visibility.sh "$BRAND" --all-engines
```

Or call the API directly:

```bash
curl -s -X POST "$CN_GEO_API_BASE/visibility" \
  -H "Content-Type: application/json" \
  -d "{\"brand\": \"$BRAND\", \"engines\": [\"deepseek\",\"kimi\",\"doubao\",\"tongyi\",\"ernie\"]}"
```

### Step 3: Analyze Per-Engine Results

For each Chinese AI engine:

| Engine | Key Characteristic | Optimization Strategy |
|--------|-------------------|----------------------|
| DeepSeek | Reasoning model, rewards structured logic | Use clear headings, numbered lists, citations |
| Kimi | 2M token window, processes full documents | Provide comprehensive, detailed content |
| 豆包 | ByteDance ecosystem, #1 AI assistant | Optimize for short-form, conversational answers |
| 通义千问 | Alibaba search integration | E-commerce and business context |
| 文心一言 | Baidu search integration | SEO-friendly, structured data |

### Step 4: Generate GEO Audit Report

```markdown
## 🔍 中国AI搜索可见度审计报告

**品牌**: [brand name]
**审计时间**: [timestamp]

### 各引擎可见度
| 引擎 | 引用率 | 趋势 | 建议 |
|------|--------|------|------|
| DeepSeek | X% | ↑/↓/→ | [suggestion] |
| Kimi | X% | ↑/↓/→ | [suggestion] |
| 豆包 | X% | ↑/↓/→ | [suggestion] |
| 通义千问 | X% | ↑/↓/→ | [suggestion] |
| 文心一言 | X% | ↑/↓/→ | [suggestion] |

### 5维评分
| 维度 | 评分 | 说明 |
|------|------|------|
| 合规风险 | X/100 | [note] |
| 互动潜力 | X/100 | [note] |
| 品牌安全 | X/100 | [note] |
| SEO可见度 | X/100 | [note] |
| AI引用概率 | X/100 | [note] |

### 优化建议
[Prioritized action items]
```

## Important Notes

- AI search visibility is different from traditional SEO — it measures how often AI engines cite your brand
- Chinese AI engines have different citation logic than Western ones (ChatGPT/Perplexity)
- If your brand isn't cited, it's invisible to 800M+ Chinese AI search users
- Predictions are probabilistic — always verify with actual engine results
