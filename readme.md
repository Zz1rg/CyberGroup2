# CRON Event Meaning

**CRON job added by attacker**

This means the attacker manually added a scheduled task to the system's crontab file (e.g., /etc/crontab, or user-specific crontabs like crontab -e). The job likely points to a script or command they want to run repeatedly or at boot.

Why it's bad: It's a classic persistence method — if the system reboots, the attack re-executes automatically.

---------------------------------------------------------------------------------------------------------------------

**CRON executed reverse_shell.py**

This tells us that the system executed a Python script designed to establish a reverse shell.

A reverse shell connects from the compromised server back to the attacker's machine, giving them remote control. It bypasses inbound firewall restrictions.

Why it's bad: It's live remote control. If you see this, the attacker probably has (or had) an interactive shell session on the machine.

---------------------------------------------------------------------------------------------------------------------

**CRON job started: wget malicious.sh**

This indicates the attacker used wget (a Linux command-line tool to download files from the web) to pull a malicious script (malicious.sh) from an external server.

Why it's bad: This shows tool deployment — attackers are downloading additional payloads (could be backdoors, keyloggers, miners, etc.)

---------------------------------------------------------------------------------------------------------------------

**Payload staging: downloading additional tools via wget**
