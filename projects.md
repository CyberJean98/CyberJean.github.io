---
layout: page
title: Projects
permalink: /projects/
---

## 🛠️ Cybersecurity Labs & Builds

### [Home SOC Lab (Wazuh)](https://github.com/Retroflowing/SOC-Lab)
*Built on a Lenovo ThinkCentre M700*
* **The Mission:** Deploy a functional SIEM to monitor home network traffic.
* **Status:** Active. Currently ingesting logs from Ubuntu and Windows endpoints.

### [Pwnagotchi Build](https://github.com/Retroflowing/Pwnagotchi)
*Built on a Raspberry Pi Zero 2 W*
* **The Mission:** Learn the mechanics of WPA handshakes and deauthentication.
* **Tools:** Waveshare e-Paper, UPS Lite Battery, AI-powered "brain."

---
*Documenting my journey from Worcester's kitchens to the SOC.*
---

## Engineering a Serverless Threat Intelligence Pipeline

**Objective:**
To build a fully automated, zero-touch pipeline that aggregates, summarizes, and publishes daily cybersecurity threat intelligence using AI and continuous integration.

**Tools & Technologies Used:**
* **Infrastructure:** GitHub Actions (CI/CD), GitHub Pages
* **Languages:** Python, Bash, YAML, Markdown, CSS/SCSS
* **APIs & Data:** Google Gemini 2.5 Flash API, JSON Parsing
* **Framework:** Jekyll (Static Site Generation)

**Architecture & Workflow:**
1. **Automated Trigger:** A GitHub Actions cron job triggers the pipeline automatically.
2. **API Integration:** A `curl` command queries the Gemini API with highly specific prompts, utilizing bypass parameters for strict formatting control.
3. **Data Parsing:** A custom Python script parses the raw JSON response, extracts the payload, and dynamically formats it into a Jekyll-compliant Markdown file.
4. **Version Control & Deployment:** Git automatically stages, commits, and pushes the new file to the repository. The pipeline is hardened with `-X ours` merge conflict resolution to prevent CI/CD traffic jams.
5. **Static UI:** The data is pushed to a custom-styled, dark-mode static website mimicking a SOC Analyst dashboard.

**Challenges Overcome:**
* **Data Normalization:** Overcame AI formatting hallucinations by engineering strict prompt boundaries and utilizing Python to sanitize the JSON-to-Markdown pipeline.
* **Git Automation:** Resolved `add/add` merge conflicts within a headless runner environment by implementing forced-update branch logic.
* **Security Posture:** Ensured the pipeline operates on the Principle of Least Privilege. API keys are strictly secured via GitHub Secrets, and the resulting static site presents zero server-side attack surface.

**Outcome:**
A highly resilient, automated threat intelligence feed that runs indefinitely at zero cost, demonstrating practical knowledge of API integration, CI/CD automation, and secure development practices.
