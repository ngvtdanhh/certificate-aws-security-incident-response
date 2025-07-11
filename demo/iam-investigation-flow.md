# 🔍 IAM Investigation Flow – AWS Incident Response

This document outlines how to investigate IAM activity during a suspected security incident using AWS native tools.

---

## 📌 1. Identify Suspicious User or Role

- Check GuardDuty findings for unusual IAM behavior
  - Example: `UnauthorizedAccess:IAMUser/TorIPCaller`
- Validate against CloudTrail:
  ```bash
  aws cloudtrail lookup-events \
    --lookup-attributes AttributeKey=Username,AttributeValue=suspicious-user
  ```

## 📜 2. Review IAM Permissions

Check policy attachments:

```bash
aws iam list-attached-user-policies --user-name suspicious-user
aws iam list-user-policies --user-name suspicious-user
```

Use IAM Access Analyzer to detect unused permissions or overprovisioned access

## 🔒 3. Take Immediate Containment Action


Disable user:

```bash
aws iam update-login-profile --user-name suspicious-user --password-reset-required
```

Revoke session tokens:

```bash
aws sts revoke-session --access-key-id <AccessKeyID>
```

## 🧠 4. Investigate Root Cause

- Was the access key leaked?

- Was there credential reuse from another breached system?

- Check login history and IPs from CloudTrail logs

## 🧾 5. Remediation

- Rotate keys, audit MFA

- Implement least privilege & session logging


