<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Creating ---> Ingesting---> Resolving</h1>
This tutorial outlines the lifecycle of a ticket from creation to ingestion to resolution within the open-source help desk ticketing system osTicket.<br />

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
   - Select "Create Ticket"


   ![image](https://github.com/user-attachments/assets/a715d51e-20d4-4b14-85d8-03b9cdcc0bd0)

</p>

