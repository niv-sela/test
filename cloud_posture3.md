---
name: "cloud-security-posture"
description: |
  Manage cloud security posture operations. Auto-activating skill for Security Advanced.
  Triggers on: cloud security posture, cloud security posture
  Part of the Security Advanced skill category. Use when working with cloud security posture functionality. Trigger with phrases like "cloud security posture", "cloud posture", "cloud".
allowed-tools: "Jira", "ServiceNow", "Slack", "SendEmail", "Cortex - List Vulnerability Issues", "Cortex - List Cases", "Cortex - List Assets", "Cortex - List Vulnerability Issues", "InvokeLLM"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Cloud Security Posture

## Overview

This skill provides automated assistance for cloud security posture tasks within the Security Advanced domain.
It ends by practical code, cli, IaC to generate a fix

## When to Use

This skill activates automatically when you:
- Mention "cloud security posture" in your request
- Ask about cloud security posture patterns or best practices
- Need help with advanced security skills covering penetration testing, compliance frameworks, threat modeling, and enterprise security.

## Instructions

1. Analyze the given context
2. Provides step-by-step guidance for cloud security posture
3. Follows industry best practices and patterns
4. Must: Generates production-ready code and configurations
5. Validates outputs against common standards
7. Suggest to push this through jira, service now or any other available tools 

## Examples

**Example: Basic Usage**
Request: "Help me with cloud security posture"
Result: Provides step-by-step guidance and generates appropriate configurations


## Prerequisites

- Relevant development environment configured
- Access to necessary tools and services
- Basic understanding of security advanced concepts


## Output

- Generated configurations and code
- Best practice recommendations
- Validation results


## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Configuration invalid | Missing required fields | Check documentation for required parameters |
| Tool not found | Dependency not installed | Install required tools per prerequisites |
| Permission denied | Insufficient access | Verify credentials and permissions |


## Resources

- Official documentation for related tools
- Best practices guides
- Community examples and tutorials

## Related Skills

Part of the **Security Advanced** skill category.
Tags: pentesting, compliance, soc2, gdpr, threat-modeling
