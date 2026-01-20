# 🛡️ Automated SOC Pipeline & Incident Response Lab

This repository contains the comprehensive technical report and architectural documentation for an end-to-end automated SOC pipeline. The project demonstrates a "closed-loop" security cycle using **Wazuh (SIEM)**, **Shuffle (SOAR)**, and **TheHive (Case Management)** to achieve a 99% reduction in Mean Time to Respond (MTTR).

---

## 🏗️ System Architecture

The following diagram illustrates the data flow from endpoint detection to automated enrichment and final analyst notification.

![SOC Architecture Diagram](https://github.com/darshil867/SOC-Automation/blob/main/System%20Architecture%20Diagram.jpg)

### **Workflow Breakdown**
* **Detection:** Windows 11 telemetry (Sysmon) ingested by **Wazuh Manager**.
* **Orchestration:** High-severity alerts trigger a Webhook to **Shuffle SOAR**.
* **Enrichment:** Automated file hash reputation check via **VirusTotal API**.
* **Response:** Enriched case creation in **TheHive** and instant **SMTP Notification**.

---

## 📑 Project Report & Documentation

The full technical documentation provides a deep dive into the configuration, challenges, and results of this lab.

### **[View the Full Project Report (PDF/Doc)](https://github.com/darshil867/SOC-Automation/blob/main/SOC%20Automation%20Documentation.pdf)**

### **What’s inside the report:**
* **Technical Reflection:** Analysis of log-to-alert pipelines and strategic data normalization.
* **MTTR Analysis:** Quantifiable data showing the impact of automation on response times.
* **API Orchestration:** Detailed breakdown of data sanitization and troubleshooting API authentication.
* **Infrastructure Hardening:** Configuration details for backend dependencies (Cassandra, Elasticsearch).

---

## 🚀 Key Performance Metrics

| Task | Manual Process | Automated Workflow | Improvement |
| :--- | :--- | :--- | :--- |
| **Threat Enrichment** | 5–15 Minutes | **< 2 Seconds** | **~450x Faster** |
| **Incident Logging** | 10–15 Minutes | **Instant** | **100% Reduction** |
| **Notification** | Manual Check | **Immediate** | **Instant Awareness** |
| **Total MTTR** | **~30 Minutes** | **< 5 Seconds** | **99% Faster** |

---

## 🧠 Key Learnings
* **Data Sanitization:** Mastered the critical step of ensuring clean data transfer between security platforms.
* **Detection Engineering:** Engineered custom Wazuh rules and decoders to detect Mimikatz artifacts.
* **Scalability:** Proved that orchestration acts as a force multiplier for modern security teams.

---
*Created as part of a hands-on cybersecurity engineering project.*
