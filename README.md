# 多吃鸭 eatmoreduck 🦆

Risk-control engineer in Shanghai — real-time risk systems in Java. AI-native on and off the clock: coding agents are my daily driver — I build tools with them and blog about what works.

🔗 [Website](https://www.eatmoreduck.com) · [Blog](https://blog.xiaohuangyu.space/en/) · [Daily Digest](https://digest.eatmoreduck.com)

## Highlights

- **[boss-zhipin-scraper](https://github.com/eatmoreduck/boss-zhipin-scraper)**&nbsp;<a href="https://github.com/eatmoreduck/boss-zhipin-scraper"><img src="https://img.shields.io/github/stars/eatmoreduck/boss-zhipin-scraper?style=flat&color=FE7D37" alt="stars" height="20" align="absmiddle"></a> — pulls real, unmasked salary data from BOSS Zhipin (China's largest job platform) by driving a real Chrome via CDP, no Selenium. I do risk control for a living — I know exactly what the anti-bot side checks.
- **[jev-chat](https://github.com/jev-chat)** — my WeChat AI assistant org: the jarvis engine (shared judge & evaluation layer, model routing) and its platform clients. I own the org and author the macOS client — screen reading, HUD, calibration, CI gates.
- **[Daily Digest](https://digest.eatmoreduck.com)** — AI agents, risk control, and interviews, digested daily and auto-built.

## Open-Source Contributions

**10 merged pull requests across 5 upstream projects, plus 13 open** (as of 27 October 2026) — the orca count is 4 solo merges plus 1 co-authored. Counts are public PRs authored by me in repositories I don't own or administer.

| Project | Merged | Open | What I work on there |
|---|---:|---:|---|
| [stablyai/orca](https://github.com/stablyai/orca)&nbsp;<a href="https://github.com/stablyai/orca"><img src="https://img.shields.io/github/stars/stablyai/orca?style=flat&color=FE7D37" alt="stars" height="16" align="absmiddle"></a> | 5 | 10 | Desktop agent workbench: scheduler correctness, telemetry privacy, sidebar data flow, test-ratchet CI |
| [anomalyco/opencode](https://github.com/anomalyco/opencode)&nbsp;<a href="https://github.com/anomalyco/opencode"><img src="https://img.shields.io/github/stars/anomalyco/opencode?style=flat&color=FE7D37" alt="stars" height="16" align="absmiddle"></a> | 0 | 3 | MIME sniffing, cache corruption recovery |
| [openclaw/openclaw](https://github.com/openclaw/openclaw)&nbsp;<a href="https://github.com/openclaw/openclaw"><img src="https://img.shields.io/github/stars/openclaw/openclaw?style=flat&color=FE7D37" alt="stars" height="16" align="absmiddle"></a> | 1 | 0 | Harness correctness |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)&nbsp;<a href="https://github.com/VoltAgent/awesome-agent-skills"><img src="https://img.shields.io/github/stars/VoltAgent/awesome-agent-skills?style=flat&color=FE7D37" alt="stars" height="16" align="absmiddle"></a> | 1 | 0 | Skill catalog entry — boss-zhipin tooling |
| [anomalyco/models.dev](https://github.com/anomalyco/models.dev)&nbsp;<a href="https://github.com/anomalyco/models.dev"><img src="https://img.shields.io/github/stars/anomalyco/models.dev?style=flat&color=FE7D37" alt="stars" height="16" align="absmiddle"></a> | 1 | 0 | Model-catalog cleanup, first-hand API verification |
| [fatwang2/awesome-jev](https://github.com/fatwang2/awesome-jev)&nbsp;<a href="https://github.com/fatwang2/awesome-jev"><img src="https://img.shields.io/github/stars/fatwang2/awesome-jev?style=flat&color=FE7D37" alt="stars" height="16" align="absmiddle"></a> | 2 | 0 | Directory entries for the Jev clients |


### What these changes actually fixed

- **A scheduled reminder could vanish for a whole day.** When the clock fell back for DST, orca's scheduler treated the repeated hour as already-done and skipped it. [#20179](https://github.com/stablyai/orca/pull/20179)
- **Computer-use agents broke on every fresh macOS machine.** SwiftPM resolved a different dependency ABI per machine; the build now pins one. [#21146](https://github.com/stablyai/orca/pull/21146)
- **Hook-install telemetry shipped raw error text.** It now reports error codes instead — the message never leaves the machine. [#26609](https://github.com/stablyai/orca/pull/26609)
- **A flaky-test ratchet could block unrelated PRs.** The ratchet now scopes to the merge base of the change under test. [#33782](https://github.com/stablyai/orca/pull/33782)
- **A model-catalog sync would have deleted a model that's still served.** Every entry I kept was verified against the live API by hand before the cleanup merged. [#7331](https://github.com/anomalyco/models.dev/pull/7331)

### 🧰 What I Build With

- **Real-time risk control**: the full chain — event streams (Kafka), real-time features (Flink), decision engines (Java / Spring Boot), hot-path caching (Redis), storage & analytics (MySQL, Elasticsearch, ClickHouse)
- **Tools & automation**: Python, Go, GitHub Actions
- **AI agents**: Claude Code, Codex — agent skills (SkillManager), auto-built digests (Daily Digest)
- **Frontend**: Vue, TypeScript, Hugo

![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Flink](https://img.shields.io/badge/Flink-E6526F?style=flat&logo=apacheflink&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat&logo=elasticsearch&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=flat&logo=clickhouse&logoColor=black)

