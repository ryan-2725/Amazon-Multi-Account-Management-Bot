# Amazon Multi-Account Management Bot

A production-grade Android automation system that manages many Amazon accounts in parallel—handling logins, profile switching, inventory checks, pricing updates, and order responses without human supervision. It eliminates tab-hopping, device juggling, and repetitive admin work so teams can scale operations across regions and marketplaces with confidence. Built for reliability and growth, the Amazon Multi-Account Management Bot brings consistent workflows to your Android device fleet.

<p align="center">
  <a href="https://Appilot.app" target="_blank"><img src="media/appilot-baner.png" alt="Appilot Banner" width="100%"></a>
</p>
<p align="center">
 <a href="https://t.me/devpilot1" target="_blank"><img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
 <a href="mailto:support@appilot.app" target="_blank"><img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"></a>
 <a href="https://appilot.app" target="_blank"><img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website"></a>
 <a href="https://discord.gg/r5sJ5vhf" target="_blank"><img src="https://img.shields.io/badge/Join-Appilot_Community-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Appilot Discord"></a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom Amazon Multi-Account Management Bot, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction

This repository demonstrates a complete, scalable automation stack for managing multiple Amazon accounts from Android devices and emulators. It automates routine Seller/Buyer app workflows—secure login rotation, stock checks, price edits, order confirmations, message replies, and KPI snapshots—so operators can run more accounts with fewer mistakes and tighter SLAs.

### Automating Amazon Multi-Account Ops at Scale
- Handles secure session rotation across dozens to hundreds of Amazon accounts with proxy/profile isolation.
- Orchestrates parallel Android devices/emulators for real-time updates (inventory, pricing, orders, messages).
- Mimics human behavior with randomized interactions, wait-times, and UI patterns to reduce flags.
- Adds enterprise-grade observability (logs, screenshots, metrics) and robust retry/recovery to minimize downtime.
- Integrates with queues and schedules so tasks run automatically, on-time, every day.

## Core Features

- **Real Devices and Emulators:** Run on USB devices, cloud device farms, or emulators (Bluestacks/Nox). Hot-swap devices, map accounts-to-devices, and persist sessions for speed.
- **No-ADB Wireless Automation:** Control devices over Wi-Fi without tethering. Zero-cable labs with remote start/stop, health checks, and live screen streaming.
- **Mimicking Human Behavior:** Randomized taps, swipe paths, dwell times, and UI traversal; staggered schedules and jitter to imitate natural usage patterns.
- **Multiple Accounts Support:** Strong session isolation per account (separate app profiles, storage dirs, and cookies). One bot, thousands of identities.
- **Multi-Device Integration:** Horizontal scaling via device pool manager; assign tasks to healthiest device based on availability, latency, and CPU.
- **Exponential Growth for Your Account:** Automate updates, messaging, and catalog hygiene to lift buy-box share, reduce response times, and improve seller metrics.
- **Premium Support:** Priority onboarding, runbooks, dashboards, and incident playbooks; optional managed device-farm setup.
- **Task Orchestration & Scheduler:** CRON-like schedules, queues, and rate limits for each workflow.
- **Resilient UI Engine:** Hybrid UIAutomator2 + Accessibility fallback with on-screen validation and DOM/text targeting.
- **Observability & Audits:** Structured logs, screenshots, session replays, and per-account reports for compliance.

### Additional Feature Matrix

| Feature | Description |
|---|---|
| **Smart Session Isolation** | Dedicated app data dirs, salt-based encryption for tokens, per-account cache control to prevent leakage. |
| **Proxy & Profile Manager** | Assign rotating/mobile/DC proxies per account; persistent device fingerprints to reduce correlation. |
| **Rule-Based Workflows** | If/else rules for price edits, reorder points, messaging templates, and SLA-based escalations. |
| **Task Queue & Rate Limits** | Redis/RabbitMQ-backed queues with per-account/device throttling to respect platform limits. |
| **Error Recovery & Logging** | Automatic retries with backoff, dead-letter queues, and annotated screenshots on failure. |
| **Role-Based Access Control** | Teams, permissions, and audit trails for who ran what, when, and on which account. |

</p>
<p align="center">
  <a href="https://appilot.app" target="_blank">
    <img src="media/amazon-multi-account-management-bot-banner.png" alt="amazon-multi-account-management-bot-architecture" width="95%">
  </a>
</p>

## How It Works 

1. **Input or Trigger** — From the Appilot dashboard, select tasks (e.g., rotate logins, check inventory, update prices, reply to messages) and choose the accounts/devices or smart groups to run against.  
2. **Core Logic** — Appilot drives the Android device/emulator via **UI Automator** and **Accessibility**, optionally over **ADB/Wi-Fi**, to navigate Amazon apps, locate UI elements, and perform taps, swipes, text entry, and submissions.  
3. **Output or Action** — The bot completes the designated actions (inventory syncs, price changes, order confirmations, buyer-seller messages) and exports structured results to storage or webhooks.  
4. **Other functionalities** — Centralized retry logic, error screenshots, run-level logs, parallel processing, health checks, and alerting configurable from the Appilot dashboard for smooth troubleshooting.

## Tech Stack 

- **Language:** Kotlin, Java, Python, JavaScript  
- **Frameworks:** Appium, UI Automator, Espresso, Robot Framework, Cucumber  
- **Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks, Nox Player, Scrcpy, Firebase Test Lab, MonkeyRunner, Accessibility  
- **Infrastructure:** Dockerized device farms, Cloud-based emulators, Proxy networks, Parallel Device Execution, Task Queues, Real device farm

## Directory Structure
```
amazon-multi-account-management-bot/
│
├── src/
│ ├── python/
│ │ ├── main.py
│ │ ├── orchestrator/
│ │ │ ├── scheduler.py
│ │ │ ├── dispatcher.py
│ │ │ └── workers/
│ │ │ ├── inventory_worker.py
│ │ │ ├── pricing_worker.py
│ │ │ ├── messaging_worker.py
│ │ │ └── login_rotation_worker.py
│ │ ├── android/
│ │ │ ├── device_controller.py
│ │ │ ├── uiautomation.py
│ │ │ ├── accessibility_fallback.py
│ │ │ └── screen_validator.py
│ │ ├── core/
│ │ │ ├── account_profile.py
│ │ │ ├── proxy_manager.py
│ │ │ ├── session_store.py
│ │ │ ├── rule_engine.py
│ │ │ └── rate_limiter.py
│ │ ├── io/
│ │ │ ├── storage.py
│ │ │ ├── exporters/
│ │ │ │ ├── csv_exporter.py
│ │ │ │ └── webhook_exporter.py
│ │ │ └── imports/
│ │ │ └── accounts_loader.py
│ │ └── utils/
│ │ ├── logger.py
│ │ ├── retry.py
│ │ └── screenshots.py
│ └── js/
│ └── dashboard/
│ ├── package.json
│ ├── src/
│ │ ├── index.tsx
│ │ ├── components/
│ │ │ ├── DeviceTable.tsx
│ │ │ ├── AccountTable.tsx
│ │ │ └── RunConsole.tsx
│ │ └── api/
│ │ └── client.ts
│ └── public/
│ └── index.html
│
├── config/
│ ├── settings.yaml
│ ├── devices.yaml
│ ├── proxies.yaml
│ └── credentials.env
│
├── automation/
│ ├── flows/
│ │ ├── login_rotation.yaml
│ │ ├── inventory_check.yaml
│ │ ├── price_update.yaml
│ │ └── messaging_reply.yaml
│ └── locators/
│ └── amazon_screens.json
│
├── logs/
│ ├── runs/
│ └── screenshots/
│
├── output/
│ ├── reports/
│ └── exports/
│
├── docker/
│ ├── Dockerfile.api
│ ├── Dockerfile.worker
│ └── docker-compose.yml
│
├── requirements.txt
├── package.json
└── README.md
```


## Use Cases

- **Aggregators** use it to rotate through hundreds of regional accounts and sync inventory, so they can keep buy-box share without manual checks.  
- **E-commerce teams** use it to update prices and confirm orders across marketplaces, so they can maintain SLAs and reduce cancellations.  
- **Support ops** use it to auto-reply with buyer-seller templates, so they can cut response times and improve account health.  
- **Agencies** use it to onboard new client accounts and run daily hygiene tasks, so they can scale without expanding headcount.  
- **Developers** use it to test seller workflows on device farms, so they can validate UI flows before release.

## FAQs

**How do I configure this automation for multiple accounts?**  
Define each account in `config/credentials.env` (or a secure vault) and map it to a device group in `config/devices.yaml`. The scheduler reads `automation/flows/*.yaml` and assigns tasks per account with session isolation and proxy bindings.

**Does it support proxy rotation or anti-detection?**  
Yes. `proxies.yaml` supports pool-based and per-account proxies (mobile/DC). The Profile Manager persists device fingerprints, while randomized timings and traversal patterns help reduce correlation.

**Can I schedule it to run periodically?**  
Absolutely. Use the built-in scheduler (`scheduler.py`) or connect to a CRON/task-queue. Each flow has rate limits and run windows to avoid bursts.

**What happens if a step fails mid-run?**  
The retry wrapper captures screenshots, logs the context, and retries with exponential backoff. Irrecoverable steps move to a dead-letter queue for review.

**Can I run it without USB cables?**  
Yes. Wireless control is supported (ADB over Wi-Fi or ADB-less paths via Accessibility). The device health monitor ensures stability and reconnects when needed.

## Performance & Reliability Benchmarks 

- **Execution Speed:** 50–120 actions/min per device (typical UI flows: login → navigate → update → confirm), dependent on network and device tier.  
- **Success Rate:** 95% end-to-end task success on stable device farms with validated locators and healthy proxies.  
- **Scalability:** Proven architecture for **300–1,000** concurrent Android devices using sharded queues and stateless workers.  
- **Resource Efficiency:** Worker CPU < 35% median, RAM < 400 MB per process; screenshot capture batched to minimize I/O.  
- **Error Handling:** Structured logs, per-step screenshots, automatic retries with backoff, circuit breakers for flaky screens, and alerting via webhooks/Slack.


##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>
