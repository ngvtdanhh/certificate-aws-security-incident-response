# 🚨 Detection and Escalation in AWS

Understanding how to detect and escalate security events is critical to effective response in cloud environments.

---

## 🧭 Detection Sources

| Source        | Purpose                                     |
|---------------|---------------------------------------------|
| GuardDuty     | Anomaly detection for AWS resources         |
| CloudTrail    | Records API calls and account activity      |
| VPC Flow Logs | Traffic patterns and IP-level visibility    |
| AWS Config    | Resource drift or unauthorized changes      |
| Security Hub  | Centralized alert management                |

---

## 📈 Severity Classification

AWS recommends classifying incidents by:

- Impact (data loss, unauthorized access)
- Scope (single instance vs. entire VPC/account)
- Exposure time
- Compliance requirements (PCI, HIPAA, etc.)

---

## 📞 Escalation Paths

- Use CloudWatch Alarms to trigger SNS notifications
- Incident automation via Lambda + Step Functions
- Notify stakeholders via AWS Chatbot, email, or ticketing tools

---

## 🧠 Best Practices

- Define escalation tiers (SOC analyst → SecOps → CISO)
- Periodically review alert thresholds and false positives
- Use runbooks for response consistency
