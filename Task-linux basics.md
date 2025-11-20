# 🐧 **LINUX**

## **1. Basic Commands**

These are your day-1, must-know commands — the OGs of Linux.

### **📂 Navigation**

* `pwd` — shows where you’re standing.
* `ls` — list files.

  * `ls -la` → show all, including hidden stuff.
* `cd <folder>` — go inside a directory.
* `cd ..` — go back.

### **📁 File & Directory Handling**

* `mkdir <dir>` — create directory.
* `touch <file>` — create empty file.
* `cp source dest` — copy.
* `mv source dest` — move/rename.
* `rm <file>` — delete file.

  * `rm -r <dir>` → delete directory. Careful bro, this one bites.

### **📜 File Reading**

* `cat file` — print file.
* `more file` / `less file` — page by page.
* `head` / `tail` — show start/end of file.

### **🔍 Searching**

* `grep "text" file` — search text inside file.
* `find /path -name filename` — hunt something down in the system.

### **⚙ Permissions**

* `chmod 755 file` — change permissions.
* `chown user:group file` — change owner/group.

### **🛠 System**

* `top` — see running processes.
* `ps aux` — list all processes.
* `kill PID` — murder a process 💀
* `df -h` — disk usage.
* `free -m` — memory usage.

---

## **2. Linux Architecture**

Think of Linux like a 90s hero—simple, powerful, and still unbeatable.

### **🔹 1. Hardware Layer**

CPU, RAM, HDD — real physical stuff.

### **🔹 2. Kernel**

The boss.
Handles:

* Process management
* Memory management
* Device drivers
* System calls

### **🔹 3. System Libraries**

Middleware between apps and the kernel.
Example: glibc.

### **🔹 4. System Utilities**

Basic tools that run the system:

* `systemd`
* Shell (bash)
* Commands (`ls`, `ps`, etc.)

### **🔹 5. User Applications**

Your apps, scripts, browsers, tools.

**Flow:**
App → System Call → Kernel → Hardware

Straight, simple, powerful.

---

# ☁️ **AWS / CLOUD**

## **What is Cloud?**

Cloud = renting someone else's powerful computer instead of buying your own.

Instead of buying servers → you rent from AWS, Azure, GCP.
You pay only for what you use. Flexible, scalable, cheap (well… mostly 🤏).

---

## **Cloud Service Models**

Think of these as levels of responsibility.

### **1️⃣ IaaS (Infrastructure as a Service)**

You manage almost everything except the hardware.

* EC2
* VPC
* EBS

**Example:** Getting a raw VM and installing everything yourself.

### **2️⃣ PaaS (Platform as a Service)**

You focus on code, AWS manages infra.

* AWS Elastic Beanstalk
* AWS Lambda (sort-of)
* RDS (managed DB)

**Example:** Deploy your app, platform handles OS, runtime, scaling.

### **3️⃣ SaaS (Software as a Service)**

Ready-made apps delivered over internet.

* Gmail
* Zoom
* Salesforce

**Example:** You just use the service — no installation, no setup.

---

# 🛡 **IAM (Identity & Access Management)**

AWS ka security guard + entry manager.

IAM handles:

* **Users** — real people
* **Groups** — team of users
* **Roles** — temporary permission sets
* **Policies** — JSON permission documents

### **Core IAM Concepts**

* **Least privilege** → give minimum required access.
* **Policies** → Allow or Deny actions.
* **MFA** → extra security.
* **Root account** → God level. Never use casually.

### **Examples**

* Dev user → EC2FullAccess
* Tester → ReadOnlyAccess
* App running in EC2 → IAM Role attached
