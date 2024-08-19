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
<img src="https://github.com/user-attachments/assets/d5582412-40ce-4272-af4e-bdce8879a49b" height="80%" width="80%" />
</p>
<p>
  I then used | where EventID == 4625 is to see failed Logins.
  <p>
<img src="https://github.com/user-attachments/assets/0bd6cce9-0e63-4517-a135-c690d973ab89" height="80%" width="80%" />
</p>
<p>
 Using '\\ADMINISTRATOR' to search for Account whose EventID == 4625. 
</p>
<br />
 <p>
<img src="https://github.com/user-attachments/assets/13d3a244-f51f-42ed-b790-8fc913846646" height="80%" width="80%" />
</p>
<p>
 Using TimeGenerated to see the last failed Login 12Hrs ago.
</p>
<br />
 <p>
<img src="https://github.com/user-attachments/assets/b8d93616-e2ec-4acd-80b3-4c6a21123cc0" height="80%" width="80%" />
</p>
<p>
Using Count to count how many failed Login came from the account and ID.
</p>
<br />
<p>
  <img src="https://github.com/user-attachments/assets/d998b87f-b5a2-4eab-a4db-753359bf3d13" height="80%" width="80%" />
</p>
<p>
  Decided to change the EventID to 4688, TimeGenerated 2hrs ago to see how many failureCounts occured.
</p>
<br />
<p>
  <img src="https://github.com/user-attachments/assets/35935af5-1aa5-404a-9ce5-29c74885d86a" height="80%" width="80%" />
</p>
<p>
  Changed the name and was able to name it as AttackerIP, Cat, and Dog. 
</p>
