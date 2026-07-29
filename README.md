# eks-rbac-audit

Kubernetes RBAC escalation auditor for EKS — **in design, not yet runnable**.

## Goal

Analyze RBAC roles and bindings in EKS clusters for privilege-escalation
paths and risky grants:

- Wildcard verbs and resources
- Escalation primitives: `pods/exec`, `impersonate`, `bind`, `escalate`
- Cluster-wide secrets access
- Orphaned and unused permissions

Output will be a severity-ranked report (table and JSON) suitable for CI.

## Status

Design phase. No code has been published yet; this repo currently holds the
project scaffold and license. For the AWS IAM side of the same least-privilege
story, see [`secure-iam-lint`](https://github.com/rivassec/secure-iam-lint).
