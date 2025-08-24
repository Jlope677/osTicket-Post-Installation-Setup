# 📌 osTicket Post-Installation Setup

**Lab Goal:**  
After installing osTicket on my Azure VM, I logged in as an Admin and configured roles, departments, teams, SLAs, and more to simulate a working help desk environment. This helped me understand how tickets flow from user creation all the way to team routing and SLA management.

---

## 🧠 Overview

- **VM**: osticket-vm on Azure  
- **OS**: Windows 10  
- **Tool**: osTicket Help Desk System  
- **Access**:  
  - **Admin/Analyst Login Page**: `http://localhost/osTicket/scp/login.php`  
  - **End User Ticket Page**: `http://localhost/osTicket`

---

## 🛠️ Step-by-Step Configuration

### 🔐 Acknowledge Admin Panel vs Agent Panel

I explored the difference between the Admin Panel (full system control) and the Agent Panel (ticket handling only).

![Admin vs Agent Panel](images/admin-vs-agent-panel.png)

**What I Learned:**  
I now understand how permission levels are separated in osTicket. Admins control structure, agents handle tickets.

---

### 🧑‍💼 Configure Roles

**Path:** `Admin Panel → Agents → Roles`  
I added a role called `Supreme Admin` to define top-level access.

![Roles](images/create-role.png)

**What I Learned:**  
Roles let me define exactly what each level of user (Admin, Agent, Read-only) can see and do.

---

### 🏢 Configure Departments

**Path:** `Admin Panel → Agents → Departments`  
I created departments like:
- SysAdmins
- Networking
- Help Desk

![Departments](images/departments.png)

**What I Learned:**  
Departments are essential for organizing tickets and limiting visibility between teams.

---

### 👥 Configure Teams

**Path:** `Admin Panel → Agents → Teams`  
I made a team called `Online Banking` and added agents from different departments.

![Teams](images/teams.png)

**What I Learned:**  
Teams can pull agents from multiple departments, which is useful for cross-functional groups.

---

### 📩 Allow Anyone to Create Tickets

**Path:** `Admin Panel → Settings → User Settings`  
I **unchecked** “Unregistered users can create tickets” to require login.

![User settings](images/user-settings.png)

**What I Learned:**  
Disabling guest tickets increases accountability and control over who interacts with the system.

---

### 👤 Configure Agents

**Path:** `Admin Panel → Agents → Add New`  
I created:
- Jane (Dept: SysAdmins)
- John (Dept: Support)

![Agents](images/agents.png)

**What I Learned:**  
Agents are staff members responsible for resolving tickets based on their department and team assignments.

---

### 👨‍👩‍👧 Configure Users (Customers)

**Path:** `Agent Panel → Users → Add New`  
I created users:
- Karen
- Ken

![Users](images/users.png)

**What I Learned:**  
Users are the ones submitting tickets. They don’t have access to the backend.

---

### ⏱️ Configure SLAs (Service Level Agreements)

**Path:** `Admin Panel → Manage → SLA`  
I added:
- Sev-A (1 hr, 24/7)
- Sev-B (4 hrs, 24/7)
- Sev-C (8 hrs, Business Hours)

![SLA](images/sla.png)

**What I Learned:**  
SLAs ensure that tickets are addressed within time limits based on severity.

---

### 🆘 Configure Help Topics

**Path:** `Admin Panel → Manage → Help Topics`  
I created topics like:
- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset
- Other

![Help Topics](images/help-topics.png)

**What I Learned:**  
Help Topics guide the user in choosing the right issue category and help route the ticket appropriately.

---

## 📚 Summary

This lab helped me simulate a real-world help desk scenario using osTicket. From account creation to SLA management, I learned how to fully configure a ticketing system in a professional environment. I also better understand how teams, departments, and permissions work together to streamline support operations.
