# 🧰 Core AWS Security Services for Incident Response

AWS provides various native tools to support detection, investigation, and response in the cloud.

---

## 📡 GuardDuty

- Threat detection service
- Detects port scans, unusual login patterns, malware communication
- Event types: EC2 behavior, IAM anomalies, S3 data events

## 📜 AWS CloudTrail

- Records all API calls in your AWS account
- Useful for tracing attacker actions or privilege misuse

## ⚙️ AWS Config

- Captures resource configurations and changes
- Enables compliance audits and rollback analysis

## 🧠 AWS Security Hub

- Central view of findings from GuardDuty, Inspector, Macie, etc.
- Uses the AWS Foundational Security Best Practices standard

## 🧪 Amazon Detective

- Visualizes and investigates AWS resources over time
- Helps correlate activity using graphs

---

## 🔐 IAM & Logging Tools

- IAM Access Analyzer for role trust relationships
- CloudWatch Logs for system/application behavior
- AWS CloudTrail Lake (advanced log analytics)
