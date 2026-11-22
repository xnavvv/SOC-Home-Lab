INC-001: SMB Brute Force
الحالة: مغلق - تم الكشف
الخطورة: متوسطة
التاريخ: 22 نوفمبر 2026 - 01:50:52
المصدر: Wazuh SIEM
الملخص
تم رصد 6 محاولات فشل دخول متتالية على سيرفر ويندوز، من جهاز واحد، على حساب Administrator، باستخدام SMB. تم الكشف بواسطة Wazuh Rule 60122. لم ينجح المهاجم.
الأصول
الضحية: Windows Server 2016 - 192.168.56.105
المهاجم: Kali Linux - 192.168.56.104
الكشف: Wazuh Server - 192.168.56.106
Agent ID: 007
Timeline
01:49 - سكان Nmap، بورتات مفتوحة: 53, 88, 135, 139, 445, 389, 5985
01:49 - فشل Hydra، تم التبديل لـ smbclient
01:50:52 - 6 محاولات LOGON_FAILURE
01:50:52 - Wazuh سجل 6 أحداث 4625
الأدلة
MITRE ATT&CK
Tactic: Credential Access - TA0006
Technique: T1110.002 - Brute Force: Password Guessing
Technique: T1021.002 - Remote Services: SMB
IoCs
Attacker IP: 192.168.56.104
Victim IP: 192.168.56.105
Port: 445/SMB
Account: Administrator
Tool: smbclient / Hydra
التوصيات
قفل الحساب بعد 5 محاولات فاشلة
تعطيل حساب Administrator الافتراضي
تفعيل SMB Signing
قاعدة Wazuh: 10 محاولات في 5 دقائق = تنبيه مستوى 12
تفعيل MFA على حسابات الأدمن
