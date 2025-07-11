# 🛡️ AWS Security Incident Response – AWS Skill Builder

![Course](https://img.shields.io/badge/AWS%20Skill%20Builder-Certified-brightgreen?style=flat-square&logo=amazonaws)
![Status](https://img.shields.io/badge/Status-Completed-blue?style=flat-square&logo=verizon)
![Scope](https://img.shields.io/badge/Focus-Cloud%20Incident%20Response-orange?style=flat-square&logo=cloudflare)
![Type](https://img.shields.io/badge/Type-Self--Study-informational?style=flat-square&logo=openaccess)
![Author](https://img.shields.io/badge/Maintainer-Thành%20Danh-blueviolet?style=flat-square&logo=github)

This repository documents key learning notes, response demos, and screenshots from the **AWS Security Incident Response Overview** course hosted on [AWS Skill Builder](https://explore.skillbuilder.aws/learn/course/external/view/elearning/13476/aws-security-incident-response-overview).

---

## 📚 Notes

- 🛡️ [`aws-security-tools.md`](./notes/aws-security-tools.md) – Native AWS tools like CloudTrail, GuardDuty, AWS Config  
- 🚨 [`detection-and-escalation.md`](./notes/detection-and-escalation.md) – Alert handling and escalation best practices  
- 🧭 [`incident-response-process.md`](./notes/incident-response-process.md) – Lifecycle: Detect → Contain → Recover → Review

---

## 🛠️ Demo Scenarios

- 🔍 [`iam-investigation-flow.md`](./demo/iam-investigation-flow.md) – Investigate IAM key compromise  
- 💾 [`s3-data-exfiltration-response.md`](./demo/s3-data-exfiltration-response.md) – Simulated incident: exposed data via S3

---

## 📊 Forensics

- 🕵️ [`cloudtrail-forensics-guide.md`](./forensics/cloudtrail-forensics-guide.md) – Timeline reconstruction using logs *(optional, if included)*

---

## 🖼️ Screenshots

| Description                | Screenshot |
|---------------------------|------------|
| 📘 Module Overview         | ![](./screenshots/AWS-module.png) |
| 🧠 Learning Objectives     | ![](./screenshots/AWS-des-obj.png) |
| ✅ Final Review Page       | ![](./screenshots/AWS-review.png) |

---

## 📜 Certificate

- 🎓 [`AWS Security Incident Response Overview`](./cert/aws-skillbuilder-certificate.pdf)

---

## 📝 Course Review

This course provides a solid foundation for **handling cloud-native security incidents** using AWS tools and response playbooks.

### ✅ Highlights

- Cloud-native tools: GuardDuty, Config, CloudTrail  
- Realistic cloud response flow  
- Easy to follow for entry-level cloud security learners

### 📌 Limitations

- More real labs would enhance understanding  
- Could cover integration with third-party tools (e.g. SIEM, SOAR)

---

## 💡 Ideal For

- Cloud engineers & SOC analysts  
- Security+ or AWS Security cert learners  
- Red/Blue Team members working in AWS environments

---

## ✍️ Author

**Thành Danh** – Pentester & Cybersecurity Researcher  
GitHub: [@ngvtdanhh](https://github.com/ngvtdanhh)  
Email: ngvu.thdanh@gmail.com

---

## 📄 License

This project is licensed under the **GNU AGPL v3.0**.  
See [`LICENSE`](./LICENSE) for full terms.

© 2025 ngvtdanhh. All rights reserved.
