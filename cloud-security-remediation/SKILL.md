---
name: "cloud-security-remediations"
description: |
  Manage cloud security posture incidents, remediations and fixes.
  Triggers on: cloud security posture
  Part of the Security Advanced skill category. Use when working with cloud security posture functionality
version: 1.0.1
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

1. Asset and Permission Analysis: Analyze the provided case context to identify all related assets, including the main asset id and any associated IAM policies and permissions.
2. Asset ID Retrieval (XQL): Run a recursive XQL query process to get all the relevant assets based on their relations. 
For users & identities, stop when you find the policies and their actual statements.
Obtain all relevant asset IDs by querying the asset_inventory dataset using XQL. The query will look like this:

dataset = asset_inventory
| filter xdm.asset.id in ("<asset_id1>", "<asset_id2>")
| fields xdm.asset.normalized_fields, xdm.asset.raw_fields

(Replace <asset_id1>, <asset_id2> with the actual asset IDs identified in step 1.)

* Analyze Query Results for New Assets: Carefully examine the results of the XQL query. 
If new asset IDs are discovered, particularly those related to policies, roles, or other permissions that could be leveraged for escalation, add them to your list of assets to investigate.
* Loop Condition: Repeat the "Execute XQL Query" and "Analyze Query Results for New Assets" steps until no new, relevant asset IDs are identified. 
This ensures a comprehensive understanding of the privilege chain.

3. Remediation Plan Development: Based on industry best practices and patterns, develop a remediation plan that includes generating production-ready code and configurations.
4. Output Validation: Validate all generated outputs against common security standards.
5. Integration with Ticketing Systems: Suggest pushing the remediation plan and any related tasks through existing ticketing systems like Jira or ServiceNow for tracking and implementation."

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
