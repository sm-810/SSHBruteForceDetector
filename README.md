# SSHBruteForceDetector
Python Scripts to attack from Ubuntu Server, as well as script to detect the brute force attack from RHEL10 Server.
Core Tools: 
  RHEL 10
  Ubuntu
  Python
  Bash
  Wireshark
Steps:
1. Attack through Ubuntu VM using custom Python SSH brute force script using libraries like ex: paramiko, Parallel-SSH, ssh2-python - I chose paramiko
2. Monitor SSH authentication logs (/var/log/secure or systemd journal) on RHEL 10 and generating test authentication failures
3. Keep count of any offending IP addresses in case it goes over the threshold
3. If it does, trigger a Python script to automatically ban any offending IP using firewalld
4. Use Wireshark to inspect the blocked connection
