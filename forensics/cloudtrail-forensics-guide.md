# 🧪 CloudTrail Forensics – Incident Reconstruction Guide

This guide outlines how to perform **forensic analysis** in AWS using CloudTrail to trace the timeline and scope of an incident.

---

## 🔍 1. Scope Definition

- Determine the **timeframe** of the breach
- Identify **IAM entities** and **resources** involved
- Use GuardDuty findings or anomaly detection as reference points

---

## 🧰 2. Tools Required

- AWS CLI
- CloudTrail console
- jq (for JSON parsing)
- Optional: Amazon Athena or OpenSearch for large trail datasets

---

## 🧾 3. Timeline Reconstruction

- Pull all events for a given IAM user:

```bash
aws cloudtrail lookup-events \
  --lookup-attributes AttributeKey=Username,AttributeValue=attacker-user \
  --start-time 2025-07-01T00:00:00Z \
  --end-time 2025-07-02T00:00:00Z \
  --query 'Events[*].{Time:EventTime, Name:EventName, IP:SourceIPAddress}' \
  --output table
```

Look for:

- Console logins (ConsoleLogin)

- Key creation or deletion

- GetObject, PutObject, AssumeRole, UpdateFunctionCode, etc.

🧠 4. Indicators of Compromise (IoCs)
Unusual IPs or geolocations

Spikes in API usage (especially read/write/delete)

Accessing resources at abnormal times

🧹 5. Post-Incident Actions
Archive and encrypt logs

Tag and isolate compromised resources

Share findings with internal security teams or external authorities

## 💡 Pro Tips

- Use Athena + S3 for scalable log querying

- Redact sensitive fields before report sharing

- Always enable log file integrity validation in CloudTrail

## 🧩 References

- AWS CloudTrail Best Practices

- AWS IR Guidebook – Section 4: Log Analysis

- Digital Forensics on AWS (Black Hat Whitepaper)
