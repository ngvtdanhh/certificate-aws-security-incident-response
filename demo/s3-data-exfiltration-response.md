# 📦 S3 Data Exfiltration Response – AWS IR Playbook

How to detect and respond to a possible **S3 data exfiltration** using GuardDuty, CloudTrail, and automation.

---

## 🚨 Detection

- GuardDuty Findings:
  - `Policy:S3/BucketPermissions`
  - `S3:DataEvent/Exfiltration`
- S3 Access Logs show spikes in `GET` requests from unusual IPs

---

## 🕵️‍♀️ Investigation

- Identify affected bucket and object(s):
  ```bash
  aws s3api list-objects --bucket suspicious-bucket --query 'Contents[].Key'
  ```

  Check GetObject events:

   ```bash
  aws cloudtrail lookup-events \
  --lookup-attributes AttributeKey=EventName,AttributeValue=GetObject
  ```

## 🛡️ Containment

Change bucket policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Principal": "*",
      "Action": "s3:*",
      "Resource": ["arn:aws:s3:::suspicious-bucket/*"],
      "Condition": {"IpAddress": {"aws:SourceIp": "1.2.3.4"}}
    }
  ]
}
```

- Disable public access block if necessary

- Enable versioning to preserve historical copies

## 🔁 Remediation

- Review bucket ACLs and policies

- Enable S3 Object Lock

- Turn on Amazon Macie for future DLP scanning

## 💡 Pro Tip

- Automate detection + response using:

- CloudWatch Events + Lambda

- AWS Config Rule violation + remediation script





