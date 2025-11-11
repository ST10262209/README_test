# **Municipal Services Application**

## 📌 **Overview**

The **Municipal Services Application** is a **WPF application** built with **.NET 9.0** in Visual Studio.
It streamlines reporting municipal issues such as **road damage, water leaks, power outages, and waste management concerns**.

The application also supports **file attachments**, **gamification features**, and allows users to view all submitted issues.
Additionally, it introduces a **Local Events & Announcements system** using **custom data structures** including a **dictionary, stack, and set** for optimized event management and user recommendations.

The latest update (Task 3) further expands the system with a **Service Request Status module** built using advanced data structures such as a **Binary Search Tree, Min-Heap, Graphs**, and **Breadth-First Search (BFS)** traversal. A new Submit Service Request page allows users to create service requests that feed directly into these data structures.

---

## 📺 **YouTube Video**


---

## 🔒 **Admin Login Details**
* Username: **admin**
* Password: **EB10#**

---
## 📝 **Changelog**

###  **Changelog according to Part 1 Feedback**
* Improved the UI of buttons on the home page (MainWindow) and on the submit report page (ReportIssuesWindow).
* Added more lines on the location input so that it can be captured more accurately (As per feedback).
* Added a helper class (IssueReportHelper.cs) for my custom linked list (As per feedback).

###  **Changelog according to Part 2 Feedback**
* Seperated the Recommended Events section which was previously underneath the Events list in the card, but now it is inside its own card in-between the Events card and the Announcments card. This makes it easier for users to find (As per feedback).
* Improved the UI of buttons on the home page (MainWindow), enabled the service request status tab and gave it an icon.

###  **Changelog for new part 3**
* Added a Submit Service Request page (modern UI, rounded design, icons).
* Service Requests now include Location, Category, Description, Status, and DateSubmitted.
* Submitted requests feed into:

  * BST (sorted storage)
  * Min-Heap (urgency sorting)
  * Graph (department routing)
* Updated Service Request Status page with:

  * Two-column design
  * Urgent request card
  * Department routing card
  * “Add Service Request” button
*Improved UI consistency with rounded buttons and modern styling.

  
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

### **Service Request Status System (New – Part 3)**

The final part of the POE introduces a **service request tracking system**, built using advanced data structures to optimise storage, searching, and routing of municipal service requests.

#### **Key Features**

* **View All Service Requests**  
  Displayed using a **Binary Search Tree (BST)** sorted by Request ID.

* **Search Requests by ID**  
  Powered by efficient BST lookup (O(log n)).

* **Most Urgent Request Panel**  
  Uses a **Min-Heap** ordered by *oldest DateSubmitted* to highlight the most urgent request.

* **Dynamic Department Processing Route**  
  Built using a **Graph** based on the request category.  
  A **Breadth-First Search (BFS)** generates a step-by-step route showing how the request moves through departments.

* **Two-Column Optimised Layout**  
  The DataGrid appears on the left, while the **Urgent Request card** and **Department Route card** are displayed on the right for improved visibility.

* **Submit New Service Request**
  A dedicated Submit Service Request page allows users to create new requests by entering Location, Category, and Description.

#### **Data Structures Used**

**Binary Search Tree (BST)**  
Used for sorted storage of service requests and fast searching.

**Min-Heap**  
Used to prioritise the oldest request and display it as the “Most Urgent Request”.

**Graph**  
Represents department flows such as:  
* Customer Service → Water Department → Engineering  
* Customer Service → Roads Department  
* Customer Service → Electrical Department  

**Breadth-First Search (BFS)**  
Used to calculate and visualise the department route a request takes.

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
git clone https://github.com/VCWVL/prog7312-poe-ST10262209.git
cd prog7312-poe-ST10262209.git
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

### **Service Request Status**

* Access via the main screen
* View all service requests in sorted order (BST)
* Search for a request using its ID
* See the most urgent pending request by showing the user oldest as the most urgent.
* View a visual department processing route generated by Graph + BFS
* Understand request routing based on category

### **Submit Service Request**

* Access this page by clicking the “+ Submit Service Request” button in the top-right corner of the Service Request Status screen.
* Users can enter Location, Category, and Description when submitting a new request.
* A unique ID, status, and timestamp are automatically assigned to the request.
* The new request is added to:

  * The BST (sorted request storage)
  * The Min-Heap (urgent request prioritisation)
  * The Graph routing system (to generate the BFS department route)
* The page uses a clean, modern card layout matching the Event Submission UI.
* After submitting, the user is returned to the Service Request Status page where the new request appears immediately.

---

## 👨‍💻 **Author**

Developed by **Cade Gamble**
