# Various forensics tools

## Collections
- John Hammond collection: https://github.com/strandjs/IntroLabs/blob/master/IntroClassFiles/navigation.md

## Forensics
- https://github.com/VirusTotal/yara


## Windows
- AD Security https://adsecurity.org/
- DeepBlueCli https://github.com/sans-blue-team/DeepBlueCLI
- MichaelHaag https://asrgen.streamlit.app/

## COMPROMISED WINDOWS MACHINE PLAYBOOK:
### Event log analysis and monitoring

#### High Priority (Critical Monitoring)
Purpose: Detect and alert on critical security, stability, and unauthorized changes.  
Event IDs: 4625, 4672, 4720, 4740, 4688, 4697, 1102, 41, 7036, 7045  

Details:  
4625: Failed logon attempts (detect brute force or unauthorized access).  
4672: Special privileges assigned to new logon (privileged account activity).  
4720: User account created (potential unauthorized account creation).  
4740: Account locked out (indicates failed login attempts or suspicious activity).  
4688: A new process has been created (track execution of suspicious processes).  
4697: A service was installed in the system (monitor for unauthorized changes).  
1102: Audit log cleared (indicates potential attacker activity).  
41: Kernel power failure (unexpected shutdown or crash).  
7036: Service state changes (e.g., start or stop of critical services).  
7045: A new service was installed (potential malware activity).  

#### Medium Priority (Proactive Monitoring)  
Purpose: Monitor for system reliability, account changes, and network activity.  
Event IDs: 4624, 4768, 4769, 4776, 5136, 5156, 5145, 6008  

Details:  
4624: Successful logon (monitor for unusual logon activity).  
4768: Kerberos authentication ticket requested (track legitimate and illegitimate ticket requests).  
4769: Kerberos service ticket requested (monitor service ticket activity).  
4776: NTLM authentication attempted (detect failed attempts).  
5136: A directory service object was modified (track critical AD changes).  
5156: Windows Filtering Platform allowed a connection (monitor for unusual traffic).  
5145: A file was accessed over the network (track unauthorized file access).  
6008: Unexpected shutdown (monitor for system reliability).  

#### Low Priority (Routine Monitoring)  
Purpose: Monitor application performance and routine updates.  
Event IDs: 1000, 1001, 1002, 1026, 19, 20, 21  

Details:  
1000: Application crash (monitor failing applications).  
1001: BugCheck (logs BSOD details for troubleshooting).  
1002: Application hang (detect prolonged application inactivity).  
1026: .NET Runtime error (monitor issues with .NET-based applications).  
19: Windows Update installed successfully (track successful updates).  
20: Windows Update failed to install (monitor failed updates).  
21: Windows Update restarted the system (check for scheduled vs unscheduled updates).  

Comma-Separated Lists  
High Priority  
4625, 4672, 4720, 4740, 4688, 4697, 1102, 41, 7036, 7045  

Medium Priority  
4624, 4768, 4769, 4776, 5136, 5156, 5145, 6008  

Low Priority  
1000, 1001, 1002, 1026, 19, 20, 21  


Top 25 Windows Event IDs for SOC Analyst 
1. 4624 – Successful Logon
2. 4625 – Failed Logon
3. 4648 – Logon Attempt Using Explicit Credentials
4. 4672 – Special Privileges Assigned to New Logon
5. 4634 – Logoff
6. 4688 – A New Process Has Been Created
7. 4689 – A Process Has Ended
8. 5156 – Windows Filtering Platform Connection Allowed
9. 5158 – Windows Filtering Platform Connection Blocked 
10. 1102 – Audit Log Cleared 
11. 4720 – User Account Created 
12. 4726 – User Account Deleted 
13. 4732 – Member Added to Security-Enabled Local Group 
14. 4738 – User Account Changed 
15. 4740 – User Account Locked Out 
16. 4756 – Member Added to Security-Enabled Global Group 
17. 4768 – Kerberos TGT Requested 
18. 4769 – Kerberos Service Ticket Requested 
19. 4776 – Credentials Validation Attempted 
20. 4798 – User’s Local Group Membership Enumerated 
21. 5140 – Network Share Accessed 
22. 5152 – Connection Blocked by WFP 
23. 5058 – KDC Service Stopped 
24. 4703 – User Right Assigned 
25. Event ID 4743 – Computer Account Moved 
