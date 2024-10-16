# OsTicket-Post-Install-configuration

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial provides a overview of the post-installation configuration process for the open-source help desk ticketing system. In this phase, we will take the system from its initial setup to a fully operational help desk system by making artificial IT support staff along with different roles & departments, Customers. Along with SLA (Service level agreements) help topics, and users. Ready for handling real-world support tickets.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Cloud Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Roles(Roles assigned to different Agents such as Admins, Support staff to manage permissions & access)
- Departments(Ticket Visibility. Different departments based on the type of request on the ticket)
- Teams(Different teams to handle certain types of tickets based on serverity & type of request)
- Agents(workers)  Agents who will act as Support Staff employees 
- Users(Customers) End users who will act as people/employees needing help with their request.
- SLA (Policies that gauge severity of the request and time it needs to be resolved.
- Help Topics (Agents Gauge to type of request it is & Impact to the business. Business Critical Outage,
Personal Computer Issues,
Equipment Request,
Password Reset,
Other.


<h2>Configuration Steps</h2>

<p>

![Screenshot 2024-10-11 141706](https://github.com/user-attachments/assets/cf44e18d-1753-4a7e-b324-1a71061980cf)

</p>
<p>
Acknowledge the agent panel vs the admin panel. In the Admin Panel configure Roles for grouping permissions. Inspect all roles(name) & given checked & un-checked permissions under the permissions tab after clicking a role.
[Admin Panel > Agents > Roles]
</p>
<br />

<p>

![Screenshot 2024-10-11 143227](https://github.com/user-attachments/assets/c8f23b52-7386-49e3-90ed-fa0debe30bd3)

![Screenshot 2024-10-11 143853](https://github.com/user-attachments/assets/f1702bd8-db48-4c23-81ba-2ed0a4c574d1)

![Screenshot 2024-10-11 144033](https://github.com/user-attachments/assets/6ac9048c-31a1-45a4-835b-f8c2d34b5420)


</p>
<p>
Go back to roles tab. Click "add new role" on the right side & create a "Supreme Admin" role. Give all permissions to this role in the Permissions tab (Tickets, Task & Knowledge Base), then hit add role at the bottom. 
</p>
<br />

<p>

![Screenshot 2024-10-11 144326](https://github.com/user-attachments/assets/db6a08b6-0ae1-426e-9623-6decefdbcd5c)

![Screenshot 2024-10-11 145050](https://github.com/user-attachments/assets/678980c4-faf8-4b78-b90f-6f7091133d11)

![Screenshot 2024-10-11 145958](https://github.com/user-attachments/assets/1de69b8f-82ff-4566-a3e7-7c53ff75ea67)

</p>
<p>
Configure Departments (Ticket Visibilty, Help Desk vs SysAdmins, vs Networking).[Admin Panel > Agents > Departments] 
Add new department named "SYS ADMINS" with parent as Top Level Department. Hit Create Dept at the bottom.
</p>
<br />

<p>

![Screenshot 2024-10-11 150430](https://github.com/user-attachments/assets/2bcca3d1-2814-48bd-8566-0c9b09f9505c)

![Screenshot 2024-10-11 150450](https://github.com/user-attachments/assets/a8be33aa-056f-4688-bee7-7d7065fa67c2)

</p>
<p>

Configure Teams (Pull agents from different departments). Add new Team with the name "online banking" then hit create at the bottom.

</p>
<br />

<p>

![Screenshot 2024-10-11 151958](https://github.com/user-attachments/assets/1b33d0bb-7ed1-436f-b1f7-e88f7963d79b)

</p>
<br />

<p>

Allow anyone to create tickets
Admin Panel > Settings > User Settings (UNCHECK: unregistered users can create tickets)
Registration Required: Require registration and login to create tickets 

</p>
<br />

<p>

![Screenshot 2024-10-11 153309](https://github.com/user-attachments/assets/9ab338e6-2b51-4378-95f4-b0e1083bb4e2)

![Screenshot 2024-10-11 153401](https://github.com/user-attachments/assets/2eb21ecb-9009-41d5-ada5-891c66615554)

![Screenshot 2024-10-11 153423](https://github.com/user-attachments/assets/be1984e0-f87f-4c41-8270-60e60b464fe2)

Configure Agents (Support workers)
[Admin Panel > Agents > Add New]


JaneDoe (Dept: SysAdmins)(Role: Supreme admin) (Team: Online Banking) hit create

Create another Support Worker
JohnDoe (Dept: Support)(Role: View Only) hit create 

Set a password for both. (Uncheck "send the agent a password reset email")

</p>
<br />

<p>

![Screenshot 2024-10-11 155409](https://github.com/user-attachments/assets/e8e26831-53f7-4afb-b8bb-a925b958e602)


![Screenshot 2024-10-11 155547](https://github.com/user-attachments/assets/d7ef8243-ef25-4378-87fa-251e96c740a3)

Configure 2 Users in agent panel (customers)

[Agent Panel > Users > Add New]

Karen &
Ken

</p>
<br />

<p>

![Screenshot 2024-10-16 113445](https://github.com/user-attachments/assets/543525e6-64dd-4e94-a0fc-598be0278e30)

![Screenshot 2024-10-16 113643](https://github.com/user-attachments/assets/09492cd1-16b8-49f6-8a89-1469d1405bd2)

![Screenshot 2024-10-16 115727](https://github.com/user-attachments/assets/3ce80d3c-b41b-480c-96d8-ff05b7fad001)

Configure SLA's (Service Level Agreement)

Admin Panel -> Manage -> SLA

Sev-A (Grace Period: 1 hour, Schedule: 24/7)

Sev-B (Grace Period: 4 hours, Schedule: 24/7)

Sev-C (Grace Period: 8 hours, Business Hours)

![Screenshot 2024-10-16 120010](https://github.com/user-attachments/assets/7aec39c5-c5d8-4ffa-acd5-72f2923417a0)

![Screenshot 2024-10-16 120327](https://github.com/user-attachments/assets/240a2f6e-d052-4bed-9c5e-b549a0a48fcf)

Configure Help Topics (For when users create a ticket)

Admin Panel -> Manage -> Help Topics

Business Critical Outage

Personal Computer Issues

Equipment Request

Password Reset

Other








