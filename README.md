# Robonet Skills

Skills for building, testing, and deploying trading strategies using Robonet's MCP server.

## Overview

This repository provides **7 focused skills** for quantitative trading with Robonet, organized by development lifecycle:

```
1. browse-robonet-data        → Explore available resources (symbols, indicators, strategies)
2. design-trading-strategies   → AI-powered strategy ideation ($0.05-$1.00)
3. build-trading-strategies    → Generate complete strategy code ($1-$4.50)
4. improve-trading-strategies  → Refine, optimize, add ML predictions ($0.50-$4)
5. test-trading-strategies     → Backtest and validate performance ($0.001)
6. deploy-live-trading         → Deploy to live trading (⚠️ HIGH RISK, $0.50)
7. trade-prediction-markets    → Polymarket YES/NO token trading
```

## Natural Workflow Progressions

### Beginner Path
```
browse-robonet-data
  → design-trading-strategies (explore ideas cheaply)
  → build-trading-strategies (create code)
  → test-trading-strategies (validate)
```

### Developer Path
```
browse-robonet-data
  → build-trading-strategies (create code)
  → improve-trading-strategies (refine iteratively)
  → test-trading-strategies (validate each improvement)
  → deploy-live-trading (⚠️ only after thorough testing)
```

### Prediction Market Path
```
browse-robonet-data
  → trade-prediction-markets (self-contained Polymarket workflow)
```

## Skill Details

### 1. browse-robonet-data
**Purpose**: Fast, low-cost exploration of trading resources
**Tools**: 8 data tools (get_all_symbols, get_all_indicators, etc.)
**Cost**: Free to $0.001
**Risk**: None (read-only)
**Use when**: Starting any workflow, checking data availability

### 2. design-trading-strategies
**Purpose**: AI-powered strategy ideation
**Tools**: 1 tool (generate_ideas)
**Cost**: $0.05-$1.00 per generation
**Risk**: Low (ideas only, no execution)
**Use when**: Exploring concepts before expensive development

### 3. build-trading-strategies
**Purpose**: Generate complete strategy code
**Tools**: 2 tools (create_strategy, create_prediction_market_strategy)
**Cost**: $1.00-$4.50 per strategy (MOST EXPENSIVE)
**Risk**: Low (generates code but doesn't execute)
**Use when**: Ready to commit to development with clear requirements

### 4. improve-trading-strategies
**Purpose**: Refine, optimize, and enhance existing strategies
**Tools**: 3 tools (refine_strategy, optimize_strategy, enhance_with_allora)
**Cost**: $0.50-$4.00 per operation
**Risk**: Low (modifies code but doesn't execute)
**Use when**: Have existing strategy that needs improvement

### 5. test-trading-strategies
**Purpose**: Validate strategy performance on historical data
**Tools**: 3 tools (run_backtest, run_prediction_market_backtest, get_latest_backtest_results)
**Cost**: $0.001 per backtest
**Risk**: None (simulation only)
**Use when**: After building or improving strategies (ALWAYS before deployment)

### 6. deploy-live-trading
**Purpose**: Deploy strategies to live trading on Hyperliquid
**Tools**: 5 tools (deployment_create, list, start, stop, account management)
**Cost**: $0.50 to create deployment
**Risk**: ⚠️ **HIGH** (real capital at risk)
**Use when**: After thorough testing (6+ months, Sharpe >1.0, drawdown <20%)

**CRITICAL WARNING**: NEVER deploy without extensive backtesting. You can lose ALL deployed capital.

### 7. trade-prediction-markets
**Purpose**: Build and test Polymarket prediction market strategies
**Tools**: 6 tools (event browsing, data analysis, strategy creation, backtesting)
**Cost**: $0.001 for data, $1-$4.50 for strategy creation
**Risk**: Medium (specialized domain)
**Use when**: Trading on real-world events (politics, economics, sports, crypto)

## Installation

Add skills using the Agent Skills CLI:

```sh
# Install specific skills
npx skills add https://github.com/robonet-tech/skills --skill browse-robonet-data
npx skills add https://github.com/robonet-tech/skills --skill build-trading-strategies
npx skills add https://github.com/robonet-tech/skills --skill test-trading-strategies

# Or install all skills
npx skills add https://github.com/robonet-tech/skills --skill browse-robonet-data
npx skills add https://github.com/robonet-tech/skills --skill design-trading-strategies
npx skills add https://github.com/robonet-tech/skills --skill build-trading-strategies
npx skills add https://github.com/robonet-tech/skills --skill improve-trading-strategies
npx skills add https://github.com/robonet-tech/skills --skill test-trading-strategies
npx skills add https://github.com/robonet-tech/skills --skill deploy-live-trading
npx skills add https://github.com/robonet-tech/skills --skill trade-prediction-markets
```

## Design Philosophy

### Progressive Disclosure by Risk Level
- **None**: browse-robonet-data, test-trading-strategies (read-only/simulation)
- **Low**: design-trading-strategies, build-trading-strategies, improve-trading-strategies (code generation)
- **Medium**: trade-prediction-markets (specialized domain)
- **HIGH**: deploy-live-trading (real capital at risk)

### Cost Transparency
- **Free/$0.001**: Browse data, backtest (use liberally)
- **$0.05-$1.00**: Generate ideas (cheap exploration)
- **$0.50-$4.50**: Build/improve strategies (expensive AI operations)
- **$0.50**: Deploy to live trading (setup fee)

### Persona Alignment
- **Data Analyst**: browse-robonet-data
- **Strategy Researcher**: browse-robonet-data, design-trading-strategies
- **Strategy Developer**: build-trading-strategies, improve-trading-strategies, test-trading-strategies
- **Live Trader**: test-trading-strategies, deploy-live-trading
- **Prediction Market Trader**: trade-prediction-markets

## What Makes These Skills Useful

Each skill provides contextual information beyond tool definitions:

- **Purpose & Context**: WHY the skill exists, what problems it solves
- **Decision Logic**: WHEN to use specific tools (explicit guidance)
- **Workflows**: HOW to sequence tools for complex goals (step-by-step)
- **Domain Knowledge**: WHAT "good" looks like (metrics, best practices, trading expertise)
- **Safety Guardrails**: Risk management, constraints, troubleshooting patterns
- **Cost/Time Awareness**: Help LLM make intelligent trade-offs

This transforms the LLM from "a tool caller" into "a domain expert who uses tools effectively."

## Tool Distribution

| Skill | Tools | Execution Time | Cost | Risk |
|-------|-------|---------------|------|------|
| browse-robonet-data | 8 | <1s | Free-$0.001 | None |
| design-trading-strategies | 1 | 20-40s | $0.05-$1.00 | Low |
| build-trading-strategies | 2 | 30-60s | $1.00-$4.50 | Low |
| improve-trading-strategies | 3 | 20-60s | $0.50-$4.00 | Low |
| test-trading-strategies | 3 | 20-60s | $0.001 | None |
| deploy-live-trading | 5 | <5s | $0.50 setup | HIGH |
| trade-prediction-markets | 6 | Variable | $0.001-$4.50 | Medium |

**Total**: 28 tool references across 7 skills (some tools shared between skills)

## Shared References

Common documentation for all skills:
- **tool-catalog.md**: Complete reference for all 24 MCP tools
- Additional shared references to be added for performance metrics, risk management, etc.

## Contributing

To contribute new skills or improve existing ones, please follow the [Agent Skills](https://agentskills.io/) format.

## Support

- **Issues**: https://github.com/robonet-tech/skills/issues
- **Robonet Dashboard**: https://robonet.tech
- **Documentation**: See individual skill SKILL.md files

## License

[License information to be added]

## Disclaimer

⚠️ **Trading Risk Warning**: Trading crypto perpetuals and prediction markets involves substantial risk of loss. Only trade with capital you can afford to lose. Past performance does not guarantee future results. This software is provided for educational purposes and is not financial advice.
