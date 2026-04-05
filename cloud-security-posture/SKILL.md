---
name: "cloud-security-posture"
description: |
  Manage cloud security posture operations.
  Triggers on: cloud security posture
  Part of the Security Advanced skill category. Use when working with cloud security posture functionality
version: 1.0.0
---

# Cloud Security Posture

## Overview

This skill provides automated assistance for cloud security posture tasks within the Security Advanced domain.
It ends by practical code, cli, IaC to generate a fix

## When to Use

This skill activates automatically when you:
- Mention "cloud security posture" in your request
- Ask about cloud security posture patterns or best practices
- Ask about cloud security remediations and fixes

## Instructions

1. Analyze the given context
2. Provides step-by-step guidance for cloud security posture
3. Follows industry best practices and patterns
4. Must: Generates production-ready code and configurations
5. Validates outputs against common standards
7. Suggest to push this through jira, service now or any other available tools 

## Examples

**Example: create a remediation plan and provide a fix**
Request: "create a remediation plan and provide a fix"
Result: Provides step-by-step fix through commandline fixes, IaC code, suggested Agentix tools, or python code

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
