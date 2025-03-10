**Description -**

The Data Enablement Emailer is an automation for the weekly requirement of sending emails informing the availability
of a zip file on an sFTP server. The email is sent on a weekly basis at the conclusion of an automatic data license
run from the previous week. The automation is scheduled to run via an ActiveBatch trigger launched via a text-file
drop into a designated folder located at /zfs1/Operations_limited/Data_Enablement/Data_License_Turn/Trigger/.
The automation begins by conducting a JIRA search for sub-task (child) tickets that are created from parent TURN
Tickets. The found tickets are mined for information required for the email generation.  There is also an excel file
located on ZFS1 that is accessed for email data and all information is copied into an email template that is then
transmitted in text form. An email text-file is added to the Jira ticket as an attachment and a comment is also posted
in the ticket alerting 'Revenue Recognition' that the attachment now exists. Finally the 'labels' field is updated to
indicate that this ticket has been processed to avoid duplicate runs. Automation now includes an ability to post zip 
files to the customer's ftp sight. An option of running without the ftp posting is set in the config file under the 
'Project Details' section as 'running mode', set as follows: 
1 -> sftp only, 2 -> email only, 3 -> both sftp and email.

**Application Information -**

Required modules: <ul>
                  <li>main.py,
                  <li>data_enablement_email_manager.py,
                  <li>jira_manager.py,
                  <li>sftp_manager.py,
                  <li>excel_manager.py,
                  <li>email_manager.py,
                  <li>config.ini
                  </ul>
                  
Location:         <ul>
                  <li>Scheduled on ActiveBatch: 
                  <li>Deployed:  
                  </ul>

Source Code:      <ul>
                  <li>https:
                  </ul>

LogFile Location: <ul>
                  <li>
                  </ul>
                  
ExcelFile Location:<ul>
                   <li>
                   </ul>

**Contact Information -**

Primary Users:    <ul>
                  <li>
                  </ul>

Lead Customer:    <ul>
                  <li>
                  </ul>

Lead Developer:   <ul>
                  <li>Bradley Ruck
                  </ul>

Date Launched:    <ul>
                  <li>February, 2018
                  </ul>
                  
Date Updated:     <ul>
                  <li>August, 2018
                  </ul>
                  
