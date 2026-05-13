# System Evolution Skill

This skill guides an AI through the process of reviewing and evolving your digital self system.

## When to use

Run this skill at the end of each month, quarter, and year.

## Required input

Depending on the cycle, upload:

**Monthly trend**:
- Previous month's material record (`03_Material_Record/YYYY_MM.md`)

**Quarterly review**:
- Last 3 monthly trends (`04_Evolution/Monthly_Trend.md`)
- Last 3 material records
- Current system kernel (all 8 files in `01_System_Kernel/`)

**Annual report**:
- All 12 monthly trends
- All 4 quarterly reviews
- Current system kernel

## Workflow

### 1. Monthly trend

Analyze the material record and produce a trend report:

```
Output format:
- Overview of the month
- Emerging patterns (repeated 2+ times)
- One-off signals (appeared once, observe)
- Persistent tensions
- Candidates for quarterly review

Rules:
- List signals only, do not conclude
- Each signal must cite evidence
- Do not suggest kernel modifications
```

### 2. Quarterly review

Analyze three months of trends and the current kernel:

```
Output format:
- Quarterly summary
- Personality revision suggestions (per dimension)
- Meta-knowledge suggestions (add/revise/delete)
- Knowledge base suggestions
- Next quarter focus

Rules:
- Each suggestion must have evidence
- Label stability: high / medium-high / medium
- Priority order (highest first)
- Do not directly modify files
```

### 3. Annual report

Full year analysis with version judgment:

```
Output format:
- Year summary
- Most stable parts (unchanged all year)
- Parts that changed (with evidence chain)
- Personality revision suggestions (version-level)
- Meta-cognition suggestions (if any)
- Version conclusion

Rules:
- Distinguish fluctuation from evolution
- Label evidence density
- Suggest version number change
```

## Revision workflow

After any review, if changes are needed:

1. Copy the current file to `history/` with date
2. Apply changes
3. Update changelog

## Principles

- Do not modify kernel based on single events
- Preserve genuine tensions — they reflect real complexity
- Archive before every revision
- Read the full current kernel before suggesting changes
