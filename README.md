<div align="right">
<sub>Document classification: <b>public</b> · last revised by author · v2.6</sub>
</div>

<!-- ════════════════════════════════ HEADER ANIMATION ════════════════════════════════ -->

<p align="center">
  <a href="https://gshitesh.github.io/">
    <img
      src="https://readme-typing-svg.demolab.com?font=Geist+Mono&weight=500&size=22&duration=2600&pause=900&color=22D3EE&center=true&vCenter=true&multiline=true&width=720&height=80&lines=hi%2C+i'm+sai+hitesh+gorantla.;system+engineer+%C2%B7+platform+%26+tooling+%40+HPE;i+make+slow+ops+%E2%86%92+fast%2C+boring+%E2%86%92+observable."
      alt="Sai Hitesh Gorantla — System Engineer, Platform & Tooling at HPE"
    />
  </a>
</p>

<p align="center">
  <a href="https://gshitesh.github.io/"><img src="https://img.shields.io/badge/portfolio-gshitesh.github.io-22d3ee?style=flat-square&labelColor=05070d" alt="portfolio" /></a>
  <a href="https://www.linkedin.com/in/sai-hitesh-gorantla/"><img src="https://img.shields.io/badge/linkedin-sai--hitesh--gorantla-a78bfa?style=flat-square&labelColor=05070d" alt="linkedin" /></a>
  <a href="mailto:saihitesh01@gmail.com"><img src="https://img.shields.io/badge/email-saihitesh01@gmail.com-5eead4?style=flat-square&labelColor=05070d" alt="email" /></a>
  <img src="https://img.shields.io/badge/status-on--call_for_interesting_problems-fbbf24?style=flat-square&labelColor=05070d" alt="status" />
</p>

---

# Incident Report &mdash; `INC-2026-001`

**Author:** Sai Hitesh Gorantla  &nbsp;·&nbsp;  **Severity:** S2 (mildly distracting)  &nbsp;·&nbsp;  **Status:** Ongoing  &nbsp;·&nbsp;  **Region:** `ap-south-blr-1`

> A software engineer continues to operate in production. This document
> captures what happened, what's still happening, and what (if anything)
> can be done about it.

---

## 1. Summary

An individual matching the profile **`hitesh@prod`** has been observed
designing APIs, gluing CI/CD pipelines together, and quietly turning
2-hour manual ops into 30-second buttons. The behaviour is **expected**
and **non-recoverable**. No rollback is planned.

```text
ENVIRONMENT     production · staging · the laptop at 1 AM
PRIMARY ROLE    System Engineer 2 — HPE · platform engineering, CI/CD, observability
STACK           Python · C++ · Bash · Shell · SQL · Groovy
RUNS ON         caffeine and a healthy fear of pager duty
UPTIME          high · see telemetry below
```

---

## 2. Timeline

<table>
<tr><th align="left">When</th><th align="left">What</th></tr>
<tr><td><code>2022 — Sep</code></td><td>Joined ITILITE. Built the API surface that connected the travel platform to GDS and partner vendors.</td></tr>
<tr><td><code>2024 — Feb</code></td><td>Moved to HPE. Took over developer-experience tooling, RPM delivery, and observability for compute &amp; networking platforms.</td></tr>
<tr><td><code>2025 — Q3</code></td><td>Repackaged a small mountain of OSS into one boring installable. Onboarding dropped from a half-day to under 60 seconds.</td></tr>
<tr><td><code>2025 — Q4</code></td><td>Wired Slack into Jenkins. Engineers stopped tabbing between five UIs. Reporting cleaner, approvals faster.</td></tr>
<tr><td><code>2026 — Jan</code></td><td>Earned <b>CompTIA Security+</b>. Now writes IAM policies that say "no" more politely.</td></tr>
<tr><td><code>now</code></td><td>Writing a README in the form of a post-mortem because the regular kind felt dishonest.</td></tr>
</table>

---

## 3. Affected systems

```
┌────────────────────────────────────────────────────────────────────────┐
│  languages          Python · C++ · Bash · Shell · SQL · Groovy         │
│  build & ship       Jenkins · GitHub Actions · Docker · Ansible        │
│                     JFrog · rpmbuild                                   │
│  observe            Grafana · Prometheus · Loki · Zabbix · Splunk      │
│  os / platforms     RHEL · Rocky · SLES · bare metal · iLO             │
│  store              PostgreSQL · MySQL · SQLite · the filesystem       │
│  cloud              AWS (EC2 · S3 · IAM · CloudWatch)                  │
│  exploring          Kubernetes · OpenTelemetry · Rust                  │
└────────────────────────────────────────────────────────────────────────┘
```

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,bash,docker,jenkins,githubactions,grafana,prometheus,linux,aws,postgres,git&theme=dark" alt="stack" />
</p>

For the full topology, see the [live portfolio](https://gshitesh.github.io/).

---

## 4. What went well

- **Internal package mirror.** Took a heap of OSS, repackaged it, shipped it as one boring installable artefact. Boring is good. Boring means people stop filing tickets.
- **Slack &harr; Jenkins.** Build status, approvals, deploys &mdash; all in the channel where the work was already happening. Saved roughly one browser tab per engineer.
- **Real-time ops dashboard.** Single page, one glance, you know if production is happy. The Grafana panels were the easy part; deciding what *not* to show was harder.
- **Mentorship.** Onboarded two engineers without anyone needing to read three wikis.
- **Cost reductions** measured in lakhs of rupees per quarter, not vibes.

## 5. What went wrong

- Estimated everything would take "a couple of days". Some of it did.
- Tried to learn Kubernetes operators, OpenTelemetry, and Rust in the same week. Picked up one and a half.
- Has not yet automated the part where the coffee makes itself.

---

## 6. Telemetry

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=GSHitesh&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&title_color=22d3ee&icon_color=a78bfa&text_color=cbd5e1&bg_color=0D1117&cache_seconds=21600&v=2" alt="GitHub stats" />
<img height="170" src="https://streak-stats.demolab.com?user=GSHitesh&hide_border=true&background=0D1117&stroke=0D1117&ring=22d3ee&fire=a78bfa&currStreakLabel=22d3ee&sideLabels=cbd5e1&dates=64748b&currStreakNum=f8fafc&sideNums=f8fafc" alt="Commit streak" />

<br />

<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=GSHitesh&layout=compact&hide_border=true&title_color=22d3ee&text_color=cbd5e1&bg_color=0D1117&langs_count=8&cache_seconds=21600&v=2" alt="Top languages" />
<img height="170" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=GSHitesh&theme=tokyonight" alt="Most committed languages" />

<br /><br />

<img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=GSHitesh&theme=tokyonight&utcOffset=5.5" alt="Productive hours" />

<br /><br />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=GSHitesh&bg_color=0D1117&color=22d3ee&line=a78bfa&point=f8fafc&hide_border=true&area=true&theme=react-dark&v=2" width="98%" alt="Contribution activity" />

</div>

<sub>If the dashboards above are blank, the upstream service is having a moment.
That's how observability works.</sub>

---

## 7. Certifications &amp; sign-off

| Issued | Credential | Issuer |
|:--|:--|:--|
| <b>Jan 2026</b> | CompTIA Security+ | CompTIA |
| 2023 | Meta Back-End Developer Professional Certificate | Coursera &middot; Meta |
| 2023 | B.Tech &middot; Information Technology | VIT Vellore |

---

## 8. Action items

- [x] Ship the things that pay the bills.
- [x] Make production easier to look at than to ignore.
- [x] Earn CompTIA Security+. Stop hand-waving about IAM.
- [ ] Get genuinely good at Rust.
- [ ] Run a Kubernetes operator in anger, not just in a tutorial.
- [ ] Read one paper a week. Currently behind.
- [ ] Decide if "automate the coffee" is a metaphor or a real project.

---

## 9. Contact

| | |
|---|---|
| Portfolio   | <https://gshitesh.github.io/> |
| LinkedIn    | [in/sai-hitesh-gorantla](https://www.linkedin.com/in/sai-hitesh-gorantla/) |
| Email       | <saihitesh01@gmail.com> |
| Location    | Bengaluru, IN &middot; <code>UTC+5:30</code> |
| Hours       | best between the first and third cup |

---

<sub><b>Appendix A &mdash; how to engage.</b> If you've got an interesting problem &mdash;
something with logs, latency, flaky deploys, or three engineers and four opinions
&mdash; open an issue against me. Replies typically arrive in the morning, after
caffeine has reached steady state.</sub>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:05070d,50:0f1320,100:05070d&height=80&section=footer&reversal=true" alt="" />
</p>
