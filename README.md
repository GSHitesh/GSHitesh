<div align="right">
<sub>Document classification: <b>public</b> · last revised by author</sub>
</div>

# Incident Report &mdash; `INC-2026-001`

**Author:** Sai Hitesh Gorantla  &nbsp;·&nbsp;  **Severity:** S2 (mildly distracting)  &nbsp;·&nbsp;  **Status:** Ongoing

> A software engineer continues to operate in production. This document captures
> what happened, what's still happening, and what (if anything) can be done
> about it.

---

## 1. Summary

An individual matching the profile **`hitesh@prod`** has been observed
designing APIs, gluing CI/CD pipelines together, and quietly turning
2-hour manual ops into 30-second buttons. The behaviour is **expected**
and **non-recoverable**. No rollback is planned.

```text
ENVIRONMENT     production · staging · my own laptop at 1 AM
STACK           Python · Groovy · Java · Bash · a little Go
RUNS ON         coffee, mostly
UPTIME          high, see telemetry below
```

---

## 2. Timeline

<table>
<tr><th align="left">When</th><th align="left">What</th></tr>
<tr><td><code>T-1y</code></td><td>Repackaged a small mountain of open-source tooling into something the internal team could install without reading three wikis.</td></tr>
<tr><td><code>T-9m</code></td><td>Wired Slack into Jenkins so the engineers stopped tabbing between five UIs. Single hand, single pane of glass.</td></tr>
<tr><td><code>T-4m</code></td><td>Built a real-time dashboard for system health. Mostly green. Occasionally educational.</td></tr>
<tr><td><code>now</code></td><td>Writing a README in the form of a post-mortem because the regular kind felt dishonest.</td></tr>
</table>

---

## 3. Affected systems

The following components are known to be in scope:

```
┌─────────────────────────────────────────────────────────────────┐
│  language runtimes    Python · Groovy · Java · Bash · SQL       │
│  build & ship         Jenkins · GitHub Actions · JFrog · Docker │
│  configure            Ansible · shell glue · a lot of YAML      │
│  observe              Grafana · Prometheus · Loki · Zabbix      │
│  run on               RHEL · Rocky · SLES · bare metal · iLO    │
│  store                SQLite · PostgreSQL · the filesystem      │
└─────────────────────────────────────────────────────────────────┘
```

For the full topology, see the [live portfolio](https://gshitesh.github.io/hitesh.dev/).

---

## 4. What went well

- **Internal package mirror.** Took a heap of OSS, repackaged it, shipped it as one boring installable artefact. Boring is good. Boring means people stop filing tickets.
- **Slack &harr; Jenkins.** Build status, approvals, deploys &mdash; all in the channel where the work was already happening. Saved roughly one browser tab per engineer.
- **Real-time ops dashboard.** Single page, one glance, you know if production is happy. The grafana panels were the easy part; deciding what *not* to show was harder.

## 5. What went wrong

- Estimated everything would take "a couple of days". Some of it did.
- Tried to learn Kubernetes operators, OpenTelemetry, and Rust in the same week. Picked up one and a half.
- Has not yet automated the part where the coffee makes itself.

---

## 6. Telemetry

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=GSHitesh&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&title_color=22d3ee&icon_color=a78bfa&text_color=cbd5e1&bg_color=05070d" alt="GitHub stats" />
<img height="170" src="https://streak-stats.demolab.com?user=GSHitesh&hide_border=true&background=05070d&stroke=05070d&ring=22d3ee&fire=a78bfa&currStreakLabel=22d3ee&sideLabels=cbd5e1&dates=64748b&currStreakNum=f8fafc&sideNums=f8fafc" alt="Commit streak" />

<br />

<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=GSHitesh&layout=compact&hide_border=true&title_color=22d3ee&text_color=cbd5e1&bg_color=05070d&langs_count=8" alt="Top languages" />

<br /><br />

<img src="https://github-profile-trophy.vercel.app/?username=GSHitesh&theme=algolia&no-frame=true&no-bg=true&margin-w=8&row=1&column=7" alt="Trophies" />

<br /><br />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=GSHitesh&bg_color=05070d&color=22d3ee&line=a78bfa&point=f8fafc&hide_border=true&area=true&theme=react-dark" width="98%" alt="Contribution activity" />

</div>

<sub>If the dashboards above are blank, the upstream service is having a moment.
That's how observability works.</sub>

---

## 7. Action items

- [x] Ship the things that pay the bills.
- [x] Make production easier to look at than to ignore.
- [ ] Get genuinely good at Go.
- [ ] Read one paper a week. Currently behind.
- [ ] Decide if "automate the coffee" is a metaphor or a real project.

---

## 8. Contact

| | |
|---|---|
| Portfolio   | <https://gshitesh.github.io/hitesh.dev/> |
| LinkedIn    | [in/sai-hitesh-gorantla](https://www.linkedin.com/in/sai-hitesh-gorantla/) |
| Email       | gorantlahitesh01@gmail.com |
| Hours       | best between the first and third cup |

---

<sub><b>Appendix A &mdash; how to engage.</b> If you've got an interesting problem &mdash;
something with logs, latency, flaky deploys, or three engineers and four opinions
&mdash; open an issue against me. Replies typically arrive in the morning, after
caffeine has reached steady state.</sub>
