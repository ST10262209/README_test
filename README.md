# **Municipal Services Application**

## 📌 **Overview**

The **Municipal Services Application** is a **WPF application** built with **.NET 9.0** in Visual Studio.
It streamlines reporting municipal issues such as **road damage, water leaks, power outages, and waste management concerns**.

The application also supports **file attachments**, **gamification features**, and allows users to view all submitted issues.
Additionally, it introduces a **Local Events & Announcements system** using **custom data structures** including a **dictionary, stack, and set** for optimized event management and user recommendations.

---

## 📺 **YouTube Video**
https://youtu.be/2r2U4O1GJDo

---

## 📺 **Admin Login Details**
* Username: **admin**
* Password: **EB10#**

---

## 🚀 **Features**

### **Issue Reporting & Management**

* **Submit Issues** → Enter **location**, **category**, **description**, and optional file attachments.
* **File Attachments** → Upload and remove files/images as evidence.
* **Progress & Achievements** → **Progress Bar** shows report completion; **badges** unlock after 1, 5, and 10 submissions.
* **View Issues** → View all submitted issues with full details, including attachment paths.
* **Custom LinkedList** → Manages reported issues efficiently.

### **Local Events & Announcements**

* **View Events** → Events are displayed from a **custom dictionary**.
* **Search & Filter** → Users can search by **keywords** and filter events by **category** or **date**. Filters use a **custom set**.
* **Submit New Event** → Users can submit events which are added to a **custom stack** pending **admin approval**.
* **Admin Login & Approval** → Admin logs in from the home page, opens the **Admin Event Approval Window**, and approves or rejects submitted events.

  * Approved events are removed from the **stack** and added to the **custom dictionary**, making them visible in the **event list**.
* **Event Recommendation Algorithm** → Tracks each user's **most searched keywords** and **most filtered categories** using the **custom dictionary**. Recommended events are displayed under the main events list.

### **UI & Data Management**

* **Modern & Consistent UI** → Clean, scrollable forms with a consistent color palette.
* **Custom Data Structures** → **LinkedList** for issues, **Dictionary** for events, **Stack** for pending submissions, and **Set** for filters.

---

## 🛠️ **Requirements**

* **IDE:** Visual Studio 2022 (17.10 or newer, with .NET 9.0 support)
* **Framework:** .NET 9.0 (WPF Desktop)
* **OS:** Windows 10 or later
* **Dependencies:** None (everything included with .NET)

---

## ⚙️ **Installation & Setup**

### **Clone the repository**

```bash
git clone https://github.com/VCWVL/prog7312-part-2-ST10262209.git
cd prog7312-part-2-ST10262209
```

### **Open the solution**

1. Launch **Visual Studio 2022** (or newer)
2. Open the `.sln` file

### **Check target framework**

1. Right-click the project → **Properties**
2. Under **Target Framework**, select **.NET 9.0 (Windows)**

### **Build the solution**

* Press **Ctrl + Shift + B** or via **Build → Build Solution**

---

## ▶️ **Running the Application**

* Press **F5** (Debug) or **Ctrl + F5** (Run without debugging)

* The **Main Dashboard** opens, allowing you to:

  * Report new issues
  * View all submitted issues
  * Track achievements & progress
  * Access **Local Events & Announcements**
  * Submit new events to be approved

---

## 📖 **Usage Guide**

### **Main/Home Screen**

* Launch screen displays the **dashboard**, navigation tabs for reporting issues and achievements, and a summary of submitted issues.

### **Reporting an Issue**

1. Select **Report Issue** from the navigation tab
2. Enter **Location**
3. Select **Category** → Roads, Water, Electricity, Waste Management, Other
4. Enter **Description**
5. Attach a file (optional)
6. Watch the **Progress Bar** fill as fields are completed
7. Click **Submit** to save the issue

### **Viewing Issues**

* Navigate back to the main page to see all reported issues in a structured table.
* Each record shows **Location**, **Category**, **Description**, **Date reported**, and **Attachment path**

### **Viewing Achievements (Gamification)**

* Select **Achievements** from the home screen
* Achievements unlock as users report more issues:

  * Submit 1 issue → 🎉 **Helping Hand**
  * Submit 5 issues → 💪 **Neighborhood Guardian**
  * Submit 10 issues → 🌟 **Community Hero**

### **Local Events & Announcements**

* Access via the main screen
* **Event List** shows all approved events from the **custom dictionary**
* **Search** → Enter keywords to filter events
* **Filters** → Filter by **Category** or **Date** using the **custom set**
* **Submit Event** → Users can submit events to a **stack** pending **admin approval**
* **Admin Login** → Admin logs in from the home page, opens **Admin Event Approval Window**, and can approve or reject events
* **Approved Events** → Moved from **stack** to **custom dictionary** and displayed in the events list
* **Recommended Events** → Suggested events based on user’s **previous search keywords** and **filtered categories**, displayed under the main events list

---

## 👨‍💻 **Author**

Developed by **Cade Gamble**
