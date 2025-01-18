<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Creating ---> Ingesting---> Resolving</h1>
This tutorial outlines and simulates the lifecycle of a ticket from creation to ingestion to resolution within the open-source help desk ticketing system osTicket.<br />

<p>
 
  - NOTE: This project requires a working installation of the osTicket ticketing software and it is strongly recommended to perform the appropriate post-installation configurations.
    - For a step-by-step guide on how to perform both of these please take a look at two of my other github repositories linked below:
      - [osTicket Installation](https://github.com/CyberSecuriTim/osticket-installation)
      - [osTicket Post-installation Configuration](https://github.com/CyberSecuriTim/osticket-post-install-config)
  
</p>
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages Overview</h2>

- Creation
- Intake
- Assignment and Communication
- Working the Ticket
- Resolution

<h2>STAGE 1: Creating the Tickets</h2>

<p>

 - Access the osTicket end user portal within your Azure Windows 10 VM using this link (http://localhost/osTicket).
   - Select "Open a New Ticket"

![image](https://github.com/user-attachments/assets/a443bbe0-3b33-4ecf-bebc-acf6884ac87c)
  
   - Fill out the contact information for the user that is creating the ticket.
     - I used one of the users that was created during the previous lab [osTicket Post-Installation Configuration](https://github.com/CyberSecuriTim/osticket-post-install-config)
    
   - Select "Business Critical Outage" from the drop down menu of Help Topics.
   - Provide a brief statement that summarizes the current issue within the "Issue Summary" field
   - Lastly, feel free elaborate on the nature of the issue and exactly what seems to be wrong in the description box below the "Issue Summary" field. The more information that you 
     can provide to the Help Desk Agents the more accurately they can diagonse and resolve the issue for the user. 
   - Select "Create Ticket".


   ![image](https://github.com/user-attachments/assets/a715d51e-20d4-4b14-85d8-03b9cdcc0bd0)


  - Repeat the steps outlined above to create two more ticket as one of the created end users:
    - Help Topic: "Report a Problem"
    - Issue Summary: Accounting department needs adopbe upgrade.
      - NOTE: The issue description is intentionally ambiguous as in the real world, the end user will not always be able to provide the help desk agent with ample
        information initially and more investigation will be required. 
   ![image](https://github.com/user-attachments/assets/167e38f2-113a-424c-8cab-96ab3c0aa24a)
     - Help Topic: "Report a Problem / Personal Computer Issues"
     - Issue Summary: "The CFO states he is unable to use his laptop"
    ![image](https://github.com/user-attachments/assets/0b775085-680a-4e7f-a402-a1013e32beae)
</p>

<h2>
 STAGE 2: Intaking the Tickets
</h2>

<p>
 
 - Access the help desk agent login page using this link (http://localhost/osTicket/scp/login.php) within the Windows 10 VM hosted in Azure.
 - Login as one of your created  help desk agents (specifically one of them with access to the "System Adminstrators" Department so that you can view all 
  three of the tickets that we have created so far)
   - The "Business Critical Outage" Help Topic that was assigned to the "mobile/online banking portal outage" ticket was configured to automatically be 
     escalated to the Systems Administrator Department.

  - Then navigate to the Agent panel (if not brought there autmotically by the link)
    - From the Agent panel, select the "Tickets" tab.
    - Under the "Open" tab you should see all the unresolved tickets that have been created and automatically ingested into the ticketing system. 

 ![image](https://github.com/user-attachments/assets/b4e891d4-bd8c-44e5-b423-53af2a1ffa93)
</p>

<h2>
 MULTI-STAGE (STAGE 3 + 4): Working the Tickets through Assignment and Communication 
</h2>

<p>
 
 <h3> Gotta be quicker than that! </h3> 
 
  - You may notice that our first created ticket has been flagged as overdue by the system.
  - The SLA configured for the Help Topic that was 
    assigned to this ticket only allows a one hour grace period on a 24/7 schedule within which this ticket must be resolved.
      - In the real world as IT professionals we will not always be able to satisfy the SLA criteria but it is just as, if not more important to be transparent, honest 
        and communicate effectively to our end users as we work to resolve their tickets.
        ![image](https://github.com/user-attachments/assets/995f4123-eab3-4b86-ac8c-a09ffb3556fc)

 <h3> Now let's get these tickets resolved! </h3>

<h4> Ticket 1: Entire mobile/banking system is down</h4>

 - Start by Assigning this ticket to the "Online Banking" team, which was created during the [previous lab](https://github.com/CyberSecuriTim/osticket-post-install-config)
   - Click "Assigned to"
     - Assignee: "Online Banking"
     - Optionally, you can also provide a reason for this assignment.
   ![image](https://github.com/user-attachments/assets/c6bc0e4a-022e-4cf2-a9ad-729ae3025887)

 
 - Ensure to maintain regular communication to your end user(s) as you work the ticket.
![image](https://github.com/user-attachments/assets/595330b9-b989-4fe7-91b7-4f5d7fc2746e)

 - Let your end user(s) know that the ticket has been resolved.
   ![image](https://github.com/user-attachments/assets/6c990300-0c11-4308-98d0-3af86882d320)


  - Change the status of our ticket to "Resolved"
    - Another ticket bites the dust...man that feeling never gets old 😁
![image](https://github.com/user-attachments/assets/ee38ba09-f959-48d4-8aa1-01f85ef26c7d)

  - (From the Agent Panel) Return to the "Tickets" tab and under the "Open" tab we should see our two remaining unresolved tickets.
![image](https://github.com/user-attachments/assets/224bb27c-67b2-4dca-9b54-84feaed2ba58)



<h4> Ticket 2: Accounting department needs adobe upgrade. </h4>

- Start by changing the Department overseeing this ticket from "Maintenance" to "Support"
![image](https://github.com/user-attachments/assets/3d4f3f36-4176-45e9-b514-bf99c3d08198)

- Update the SLA plan from "Default SLA" to "Sev-C"
  - Optionally, you can also provide reason for this re-assigment of the SLA.
 ![image](https://github.com/user-attachments/assets/64a6e1af-1ef5-4d51-80d2-a89f2e330550)

- Repeat the ticket resolution best practices mentioned above regarding consistent and transparent communication with your end users and work this ticket to completion.
  - FYI: Cx means "customer"

![image](https://github.com/user-attachments/assets/14d0cb7b-03d9-4ef7-9297-3a42917ac4bc)


- Time to resolve our third and final ticket for the day!

  <h4> Ticket 3: The CFO states he is unable to use his laptop. </h4>
</p>
 
