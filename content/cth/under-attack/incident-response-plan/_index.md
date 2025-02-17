---
title: Incident Response Plan
toc: false
---

Purpose: This document outlines the steps to take when an incident occurs affecting company security, services, or infrastructure.

{{% steps %}}

### Step 1: Identify the Incident

- Monitor alerts and logs for unusual activities
- Check security tools, logs, or user reports
- Classify the incident severity:
    - 🟢 Low: Minor issue, no impact
    - 🟡 Medium: Some users affected, partial system impact
    - 🔴 High: Full outage, security breach, data compromise

📌 Tools to use:
- Firewall logs
- Cloud monitoring (AWS, GCP, Azure)
- SIEM (Security Information and Event Management)

### 📌 Step 2: Activate the Incident Response Team (IRT)

✅ Notify the right team immediately
✅ Assign an Incident Manager to take control
✅ Communicate the issue to leadership & key stakeholders
✅ Set up a dedicated incident Slack/Teams/War Room

📌 Key Contacts:
- Security Team: (Email, Phone)
- IT Operations: (Email, Phone)
- Legal & Compliance: (Email, Phone)
- Public Relations (PR) Team: (If external communication is needed)

### Step 3: Contain the Threat

✅ Block malicious traffic, isolate affected systems
✅ Reset compromised accounts and enforce MFA
✅ Disable access to vulnerable endpoints
✅ Apply temporary patches or firewall rules

📌 Emergency actions:
- Stop affected services (systemctl stop <service>)
- Lock compromised user accounts (passwd -l <user>)
- Network segmentation: block traffic from affected IPs

### Step 4: Investigate the Root Cause

✅ Gather logs from affected systems:
```
journalctl -u <service> --since "1 hour ago"
```
✅ Review security logs (SIEM, IDS/IPS, WAF)
✅ Check for unauthorized access or file changes
✅ Analyze compromised accounts, leaked credentials

{{% /steps %}}