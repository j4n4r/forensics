# Various forensics tools

## Collections
John Hammond collection: https://github.com/strandjs/IntroLabs/blob/master/IntroClassFiles/navigation.md

## Windows
AD Security https://adsecurity.org/
DeepBlueCli https://github.com/sans-blue-team/DeepBlueCLI

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

