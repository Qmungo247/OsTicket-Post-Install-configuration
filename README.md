# OsTicket-Post-Install-configuration

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial provides a overview of the post-installation configuration process for the open-source help desk ticketing system. In this phase, we will take the system from its initial setup to a fully operational help desk system, ready for handling real-world support tickets.<br />

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
</p>
<p>
Configure Departments (Ticket Visibilty, Help Desk vs SysAdmins, vs Networking).[Admin Panel > Agents > Departments] 
Add new department named "SYS ADMINS" with parent as Top Level Department. Hit Create Dept at the bottom.
</p>
<br />
