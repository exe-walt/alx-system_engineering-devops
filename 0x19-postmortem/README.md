# 0x19-postmortem
==================================================

Issue Summary:
--------------------------------------------------
On March 27th, 2022, the web server of our online shopping platform experienced an outage that lasted for 2 hours and 30 minutes, from 3:30 pm to 6:00 pm GMT. During this period, users were unable to access the website, and those who managed to access it experienced slow loading times. Approximately 75% of the users were affected by the outage.


Root Cause:
--------------------------------------------------
The outage’s root cause was a misconfiguration in the Apache web server's configuration file. One of the developers had made changes to the file, and the changes were not properly implemented, causing the server to fail to handle incoming requests.


Timeline:
--------------------------------------------------
3:30 pm GMT: The issue was first detected when the monitoring system reported a sudden spike in server response time.

3:35 pm GMT: The on-call engineer received an alert and started investigating the issue.

3:45 pm GMT: The engineer discovered that the Apache web server was not responding to incoming requests.

4:00 pm GMT: The engineer tried restarting the Apache web server, but it did not resolve the issue.

4:15 pm GMT: The engineer assumed that the issue was with the database server and started investigating it.

4:30 pm GMT: Another engineer joined the investigation and discovered that the Apache web server's configuration file had been changed.

4:45 pm GMT: The team reverted the changes to the configuration file, and the Apache web server started responding to incoming requests.

5:00 pm GMT: The team tested the server and confirmed that it was fully operational.

5:15 pm GMT: The team escalated the incident to the DevOps team for further investigation and monitoring.

6:00 pm GMT: The incident was resolved, and the website was fully operational.


Misleading Investigation/Debugging Paths:
---------------------------------------------------
The team initially assumed that the issue was with the database server and wasted some time investigating it. This was a misleading path that delayed the resolution of the issue.


Incident Escalation:
---------------------------------------------------
The incident was escalated to the DevOps team for further investigation and monitoring.


Resolution:
---------------------------------------------------
The issue was resolved by reverting the changes to the Apache web server's configuration file.
Corrective and Preventative Measures:
To prevent similar incidents in the future, we will take the following corrective and preventative measures:
Ensure that changes to the configuration files are properly implemented and tested before being deployed to production.
Improve our monitoring system to quickly detect and alert us of any issues with the web server.
Train our engineers on best practices for debugging and troubleshooting server issues.
Implement a disaster recovery plan to minimize the impact of future incidents.


Tasks to Address the Issue:
----------------------------------------------------
Review and update our change management process to ensure that changes to production systems are properly tested and reviewed before being deployed.
Review and update our monitoring system to detect similar issues in the future.
Conduct a training session for all engineers on best practices for debugging and troubleshooting server issues.
Conduct a review of our disaster recovery plan and make improvements where necessary.
In conclusion, the outage was caused by a misconfiguration in the Apache web server's configuration file. The incident was resolved by reverting the changes to the file, and the website was fully operational within 2 hours and 30 minutes. We have identified corrective and preventative measures to prevent similar incidents in the future, and we will implement them to ensure the continued smooth operation of our online shopping platform.Review and update our change management process to ensure that changes to production systems are properly tested and reviewed before being deployed.
Review and update our monitoring system to detect similar issues in the future.
Conduct a training session for all engineers on best practices for debugging and troubleshooting server issues.
Conduct a review of our disaster recovery plan and make improvements where necessary.
In conclusion, the outage was caused by a misconfiguration in the Apache web server's configuration file. The incident was resolved by reverting the changes to the file, and the website was fully operational within 2 hours and 30 minutes. We have identified corrective and preventative measures to prevent similar incidents in the future, and we will implement them to ensure the continued smooth operation of our online shopping platform