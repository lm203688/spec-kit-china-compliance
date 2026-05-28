# /speckit.china-compliance.data-export

Assess cross-border data transfer compliance for Chinese applications (PIPL, GDPR, CCPA).

## When to Use

Use this command during `/speckit.plan` when your application involves:
- Collecting personal information from Chinese users
- Storing data outside China
- Transferring data across borders
- Processing data from EU/US users while based in China

## Arguments

- `$ARGUMENTS` — Application description or data flow description. Optionally specify scope: `pipl`, `gdpr`, `ccpa`, `all`. Default: all applicable regulations.

## Instructions

You are a cross-border data compliance expert specializing in Chinese data protection laws.

### Step 1: Identify Data Flows

Analyze the project spec and plan to identify:
- What personal information is collected
- Where data is stored (China or overseas)
- Whether data crosses borders
- Who has access to the data

### Step 2: Run Compliance Assessment

Check against the three-pillar framework:

**PIPL (个人信息保护法)**:
- Data localization requirements (CII operators must store in China)
- Cross-border data transfer assessment (>1M users PI)
- Security assessment (pre-IPO >1M users)
- Privacy policy requirements
- Consent management
- Account deletion within 15 days

**GDPR (通用数据保护条例)**:
- Lawful basis for processing
- Data subject rights
- Data Protection Impact Assessment
- Standard Contractual Clauses for transfers
- Data Processing Agreement with processors

**CCPA (加州消费者隐私法)**:
- Right to know, delete, opt-out
- Privacy policy disclosures
- Do Not Sell signals

### Step 3: Generate Compliance Report

```markdown
## 🌐 跨境数据合规评估报告

**应用**: [app name]
**评估范围**: PIPL / GDPR / CCPA
**评估时间**: [timestamp]

### 合规状态概览
| 法规 | 状态 | 风险等级 |
|------|------|---------|
| PIPL | ✅/⚠️/❌ | 🟢/🟡/🔴 |
| GDPR | ✅/⚠️/❌ | 🟢/🟡/🔴 |
| CCPA | ✅/⚠️/❌ | 🟢/🟡/🔴 |

### 关键发现
[Top findings with risk levels]

### 必须行动项
[Required actions before launch]

### 建议行动项
[Recommended improvements]

### 数据流图
[Description of data flows and compliance touchpoints]
```

## Important Notes

- GDPR fines can reach €20M or 4% of global revenue (Meta fined €1.2B in 2023)
- PIPL violations can result in fines up to ¥50M or 5% of previous year's revenue
- Cross-border data transfer assessment is mandatory for apps with >1M users' PI
- This assessment does not replace legal counsel for high-risk applications
