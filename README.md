🛡️ SOC Home Lab - Wazuh SIEM
مختبر SOC كامل على VirtualBox، هجومات حقيقية من Kali، وكشف في Wazuh.
Lab Architecture
الجهاز IP الدور
Wazuh Server 192.168.56.106 SIEM / Detection
Windows Server 2016 192.168.56.105 Victim / DC
Kali Linux 192.168.56.104 Attacker
Network: Host-Only 192.168.56.0/24
Agent: Wazuh Agent + Sysmon on Windows
Incidents Detected
ID الهجوم النتيجة
INC-001 SMB Brute Force - 6 محاولات تم الكشف - فشل الهجوم
Tools Used
Wazuh 4.14.7 - SIEM
Sysmon - Windows Logging
Nmap - Scanning
smbclient / Hydra - Brute Force
VirtualBox
What I Learned
الفرق بين wazuh-alerts و wazuh-events
كيف Wazuh يكشف حدث 4625 ويحوله لـ Rule 60122
كيف أكتب تقرير تحقيق SOC كامل مع MITRE ATT&CK
