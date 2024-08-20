<h4>Log Analytics Workspace</h4>
<p>I am running a Windows Security Event in my workspace to collect, analyze query log data from various sources. I'm able to gain insight into my cloud and on-premises environments.</p>

<p>
<img src="https://github.com/user-attachments/assets/2f4fea15-1830-496d-bcf2-e331f907cdf6" height="80%" width="80%" />
<img src="ttps://github.com/user-attachments/assets/89443fd9-b104-4425-9cc4-67aafda5f0d4" height="80%" width="80%" />
</p>
<p>
  <h6> I was able to run a SecurityEvent in the last 30mins on event ID '4688' on the Remote Desktop and Server Msg Block in the last 30mins, which generated 96 failed authentications.
 SecurityEvent captures and stores security-related logs, such as logins and authentication attempts. It's used to monitor and analyze security activities and helping detect 
  potential threats.</h6> SMB is used for sharing files, printers, and other resources between computers on a network.
<br />
<p>
<img src="https://github.com/user-attachments/assets/6ad40ccc-11e1-4b54-b3d8-d194bb6f0434" height="80%" width="80%" />
</p>
<p>
Detecting a brute-force attack attempt by failed login events (EventID '4625') in the last 60mins. As you can see, I grouped the failures by source IP address and counts the number 
  of the failed attempt. If any IP address has more than 10 failed login attempts within 60mins, it's now flagged as a brute-force attack.
  <p>
<img src="https://github.com/user-attachments/assets/09bc6d1d-8f25-4638-9054-9845c262386e" height="80%" width="80%" />
    <img src="https://github.com/user-attachments/assets/ccfaa535-5777-45a0-a772-9e4a4ef7dfc1" height="80%" width="80%" />
</p>
<p>
There are other ways you can troubleshoot this and getting the same results. Using EventID '4625' to filter the SecurityEvent logs for failed login attempts in the last 60mins. 
  Using LogonType3 to focus on network logons like RDP and SMB. Summarizing the IP Address and counting the number of failed attempts by each IP Address and destination host.
  Any IP Address with over 5 login attempts is a potential brute-force attack.
</p>
<br />
 <p>
<img src="https://github.com/user-attachments/assets/1ece3198-752c-43f8-abb9-0a59091e794a" height="80%" width="80%" />
   <img src="https://github.com/user-attachments/assets/81734efd-eb22-4506-a73a-55a73d158945" height="80%" width="80%" />

</p>
<p>
I wanted to detect Malware on Microsoft Window's EventLog either on the ID '1151' or '1150', which detects scanning or malware events on the Windows Defender actions. Since the
  Eventlevel is a 4, it's nothing too concerning, it means information. Which provides informational msgs about system or application operations.
</p>
<br />
