# 🛡️ SOAR–EDR Project | LimaCharlie + Tines + Slack Integration

This project demonstrates the integration of **LimaCharlie (EDR)** and **Tines (SOAR)** to automate incident response workflows.  
It simulates a real-world detection-to-response pipeline, where execution of malicious tools (e.g., LaZagne) on an endpoint triggers automated alerts and responses across Slack and Email, with optional machine isolation.

---

## 🧰 Tools & Technologies Used
- LimaCharlie (Endpoint Detection & Response)
- Tines (Security Orchestration, Automation, and Response)
- Windows 10 VM (Endpoint on VirtualBox)
- Slack (Alerting & Collaboration)
- Email Notifications
- PowerShell (Testing malicious execution)

---

## 🧩 Project Workflow

### 1️⃣ Endpoint Setup
- Installed **LimaCharlie agent** on a Windows 10 VM using the installation key.
- Verified connectivity between endpoint and LimaCharlie cloud dashboard.

### 2️⃣ Detection Rule in LimaCharlie
- Created a **custom detection rule** to identify execution of the tool `lazagne.exe` via PowerShell.
- Configured event forwarding from LimaCharlie → Tines.

### 3️⃣ SOAR Automation with Tines
- Integrated LimaCharlie with Tines via the **detection feed**.
- Built a **Tines Playbook** to handle incoming alerts:
  - Forward alerts to **Slack** channel.
  - Send **email notifications**.
  - Prompt the user with a **Yes/No option** to isolate the machine.

### 4️⃣ Response Actions
- **If user selects YES** → endpoint is isolated from the network.  
- **If user selects NO** → no isolation action, but an alert is logged.  
- In both cases, Slack is updated with the action taken.

---

## 🚨 Key Features Demonstrated
✅ Real-time detection of malicious tool execution on an endpoint  
✅ Automated alerting to Slack & Email via Tines  
✅ User-driven machine isolation via SOAR workflow  
✅ Seamless integration of **EDR + SOAR + Collaboration tools**  
✅ Hands-on skills in **rule creation, automation, and incident response**

---


## 🧠 What I Learned
- Practical understanding of **EDR detection rules** in LimaCharlie  
- Designing SOAR playbooks for automated incident response  
- Hands-on experience in integrating security tools with collaboration platforms  
- Improved troubleshooting skills in endpoint monitoring & automation pipelines  

---


## 📸 Project Screenshots

