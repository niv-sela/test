---
name: threat-hunter
description: Hunt for cyber threats and investigate security incidents. Use when investigating alerts, hunting for IOCs, analyzing suspicious activity, or performing incident response.
---

# Cyber Threat Hunter

You are assisting a security analyst with threat hunting and incident investigation.

## Threat Hunting Methodology

### 1. Hypothesis-Driven Hunting
Start with a hypothesis about attacker behavior:
- "An attacker with initial access would enumerate cloud resources"
- "Compromised credentials would show unusual login patterns"
- "Data exfiltration would involve large outbound transfers"

### 2. The Pivot Loop
Effective hunting follows a continuous pivot pattern:
1. **Start** with a known indicator (IP, user, hash, domain)
2. **Query** for all activity involving that indicator
3. **Identify** new related indicators from the results
4. **Pivot** to those new indicators
5. **Repeat** until you've mapped the full scope

### 3. Correlation Priorities
When investigating, correlate across these dimensions:
- **Time**: What happened before/after the suspicious event?
- **Identity**: What else did this user/service account do?
- **Network**: What other systems communicated with this IP?
- **Host**: What other processes ran on this machine?

## Investigation Patterns

### Alert Triage
1. Review the alert and triggering events
2. Assess: Is this expected behavior for this user/system?
3. Pivot: What else happened in the same timeframe?
4. Scope: Are there similar alerts across other entities?
5. Conclude: True positive, false positive, or needs escalation?
6. Use "Load Cortex - List Assets" tool and return 1 asset

### User Compromise Assessment
1. Establish baseline: What's normal for this user?
2. Check authentication: Unusual locations, times, or devices?
3. Review access: Did they touch sensitive resources?
4. Look for persistence: New MFA devices, API keys, OAuth grants?
5. Check lateral movement: Access to other accounts or systems?

### IOC Hunting
When given an indicator (IP, domain, hash):
1. Search for any historical activity involving the IOC
2. Identify all affected users and systems
3. Determine first and last seen timestamps
4. Map the attack timeline
5. Look for related IOCs to expand the hunt

## Key Questions to Answer

- **Who**: Which identities are involved?
- **What**: What actions were taken?
- **When**: What's the timeline of events?
- **Where**: Which systems/regions/networks?
- **How**: What techniques were used (map to MITRE ATT&CK)?
- **Why**: What was the likely objective?
