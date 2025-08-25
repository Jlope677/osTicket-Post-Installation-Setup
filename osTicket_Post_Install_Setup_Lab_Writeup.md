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

**Admin Panel**
<img width="1273" height="1026" alt="admin panel" src="https://github.com/user-attachments/assets/d12904f1-07e1-48e7-be9f-4677602119f6" />

**Agent Panel**
<img width="1333" height="666" alt="agent panel" src="https://github.com/user-attachments/assets/40609f9e-c1f3-4529-8a54-599d807c1d24" />



**What I Learned:**  
I now understand how permission levels are separated in osTicket. Admins control structure, agents handle tickets.

---

### 🧑‍💼 Configure Roles

**Path:** `Admin Panel → Agents → Roles`  
I added a role called `Supreme Admin` to define top-level access.
<img width="1347" height="571" alt="add a new role" src="https://github.com/user-attachments/assets/6a09583a-dd73-473d-81ed-19afe1162bcd" />
<img width="1233" height="606" alt="add a new role1" src="https://github.com/user-attachments/assets/ed072df2-38c7-4d9a-b95b-a2772f3e5a1a" />
<img width="1245" height="734" alt="add a new role2" src="https://github.com/user-attachments/assets/99e5b2ab-b73f-450d-bafb-998e22eb7ad2" />
<img width="1315" height="585" alt="add a new role3" src="https://github.com/user-attachments/assets/04787261-9b17-441e-a858-438585f94077" />
<img width="1464" height="493" alt="add a new role4" src="https://github.com/user-attachments/assets/b63b8cef-b2d4-4540-b46b-b9262b9bd9bb" />
<img width="1370" height="535" alt="new role" src="https://github.com/user-attachments/assets/5e702de0-6442-439a-b680-55234aaafcd6" />







**What I Learned:**  
Roles let me define exactly what each level of user (Admin, Agent, Read-only) can see and do.

---

### 🏢 Configure Departments

**Path:** `Admin Panel → Agents → Departments`  
I created departments like:
- SysAdmins
- Networking
- Help Desk

<img width="1431" height="525" alt="departments" src="https://github.com/user-attachments/assets/036b4f79-1a1a-4d5b-b8ac-96ae96e9993e" />
<img width="1241" height="649" alt="departments2" src="https://github.com/user-attachments/assets/734b0d95-c362-40f5-8dea-e5b0309b7e45" />
<img width="1233" height="938" alt="departments3" src="https://github.com/user-attachments/assets/e353a3ff-30b4-4678-b39d-6bd58aa23de8" />
<img width="1265" height="590" alt="new department" src="https://github.com/user-attachments/assets/37ca6068-bd76-4326-af4f-918d1549c388" />





**What I Learned:**  
Departments are essential for organizing tickets and limiting visibility between teams.

---

### 👥 Configure Teams

**Path:** `Admin Panel → Agents → Teams`  
I made a team called `Online Banking` and added agents from different departments.

<img width="1389" height="475" alt="teams" src="https://github.com/user-attachments/assets/b3c872ff-5403-4557-a171-897c0debd849" />
<img width="1230" height="694" alt="teams2" src="https://github.com/user-attachments/assets/b68fc019-0940-4df3-a054-ddff0013eba9" />
<img width="1450" height="541" alt="new teams" src="https://github.com/user-attachments/assets/fa8108c0-1ad8-4a65-a383-18d12de5f276" />




**What I Learned:**  
Teams can pull agents from multiple departments, which is useful for cross-functional groups.

---

### 📩 Allow Anyone to Create Tickets

**Path:** `Admin Panel → Settings → User Settings`  
I **unchecked** “Unregistered users can create tickets” to require login.

<img width="1223" height="775" alt="allow ticketing from anyone" src="https://github.com/user-attachments/assets/fe35bbb5-695f-4584-9079-30ef148b19fa" />


**What I Learned:**  
Disabling guest tickets increases accountability and control over who interacts with the system.

---

### 👤 Configure Agents

**Path:** `Admin Panel → Agents → Add New`  
I created:
- Jane (Dept: SysAdmins)
- John (Dept: Support)

<img width="1233" height="493" alt="agents" src="https://github.com/user-attachments/assets/119ab3ba-d973-48bf-9863-2b9bc53e0082" />

**Jane**
<img width="1220" height="634" alt="agents2" src="https://github.com/user-attachments/assets/d234b9e3-5147-4d77-88ff-bbb923404a0f" />
<img width="1222" height="680" alt="Jane password" src="https://github.com/user-attachments/assets/624aadbc-3031-41e7-b5b3-0e6c696fecf7" />
<img width="1222" height="770" alt="agents3" src="https://github.com/user-attachments/assets/f60fc5c6-0df9-452e-8280-3083ad9368a4" />
<img width="1263" height="700" alt="agents4" src="https://github.com/user-attachments/assets/5e82ea71-abec-4a82-81ba-2fe12db86151" />
<img width="1302" height="452" alt="agents5" src="https://github.com/user-attachments/assets/6b7a96e2-7e7e-4c55-a6a3-68b10e6f3f88" />

**John**
<img width="1305" height="799" alt="johnagent" src="https://github.com/user-attachments/assets/4e25fbba-8c37-453e-9756-ef8f8499b08f" />
<img width="1224" height="622" alt="john password" src="https://github.com/user-attachments/assets/a8d70fcc-b087-47cd-9bf0-389d49f6c91f" />
<img width="1222" height="735" alt="johnagent2" src="https://github.com/user-attachments/assets/89f23481-ea9a-4cd0-83e4-c0fc3e422ada" />
<img width="1231" height="724" alt="johnagent3" src="https://github.com/user-attachments/assets/bccc123e-785c-48c0-b1c4-92ca1f1aa986" />
<img width="1333" height="675" alt="johnagent4" src="https://github.com/user-attachments/assets/0e67ee6a-941a-4a3e-9f27-044242f7c0e0" />

**New agents**

<img width="1372" height="616" alt="new agent" src="https://github.com/user-attachments/assets/296d7950-b66b-4140-ba7b-2a72a64dae9c" />











**What I Learned:**  
Agents are staff members responsible for resolving tickets based on their department and team assignments.

---

### 👨‍👩‍👧 Configure Users (Customers)

**Path:** `Agent Panel → Users → Add New`  
I created users:
- Karen
- Ken

<img width="1307" height="535" alt="user1" src="https://github.com/user-attachments/assets/0d9acb53-52a3-44c6-80c0-bd7704d7f94d" />
<img width="841" height="506" alt="user2" src="https://github.com/user-attachments/assets/850a13eb-ae19-4a13-8934-e9e3ab950881" />
<img width="1312" height="536" alt="new user" src="https://github.com/user-attachments/assets/1f4db47b-3672-47bb-8c7f-4200a8dfdabf" />




**What I Learned:**  
Users are the ones submitting tickets. They don’t have access to the backend.

---

### ⏱️ Configure SLAs (Service Level Agreements)

**Path:** `Admin Panel → Manage → SLA`  
I added:
- Sev-A (1 hr, 24/7)
- Sev-B (4 hrs, 24/7)
- Sev-C (8 hrs, Business Hours)

<img width="1367" height="482" alt="sla1" src="https://github.com/user-attachments/assets/2d292935-69ca-4f7a-be30-4a14fdb6a762" />
<img width="1225" height="844" alt="sla2" src="https://github.com/user-attachments/assets/82c2b476-e881-4ce0-896c-648001d5f585" />
<img width="1241" height="853" alt="sla3" src="https://github.com/user-attachments/assets/e8c8b681-84f3-4443-8edf-531449d2215a" />
<img width="1209" height="816" alt="sla4" src="https://github.com/user-attachments/assets/064df79f-ea61-44bb-bbf0-9e564ebbfe0c" />
<img width="1258" height="614" alt="new sla" src="https://github.com/user-attachments/assets/9977953b-6350-4539-b396-34fac9efa973" />






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

<img width="1299" height="578" alt="helptopics" src="https://github.com/user-attachments/assets/3ce0796d-95b1-4958-b897-2891e0ac2586" />
<img width="1229" height="808" alt="helptopics2" src="https://github.com/user-attachments/assets/79b5bfbd-f3cc-40e7-a0c7-f44301d776ac" />
<img width="1226" height="796" alt="helptopics3" src="https://github.com/user-attachments/assets/c8db713b-b565-40e1-a5c7-49c9dcc0efb8" />
<img width="1214" height="847" alt="helptopics4" src="https://github.com/user-attachments/assets/d6dc9b7a-cf43-4655-893e-495296ab9bd4" />
<img width="1209" height="824" alt="helptopics5" src="https://github.com/user-attachments/assets/94511386-970f-4802-aa62-7dded558e50e" />
<img width="1272" height="808" alt="helptopics6" src="https://github.com/user-attachments/assets/55e9ba36-b548-456b-87ee-2357b1ea5f22" />
<img width="1227" height="798" alt="new helptopics" src="https://github.com/user-attachments/assets/0b431e1f-1d88-430d-a96f-f16c18060bd8" />








**What I Learned:**  
Help Topics guide the user in choosing the right issue category and help route the ticket appropriately.

---

## 📚 Summary

This lab helped me simulate a real-world help desk scenario using osTicket. From account creation to SLA management, I learned how to fully configure a ticketing system in a professional environment. I also better understand how teams, departments, and permissions work together to streamline support operations.
