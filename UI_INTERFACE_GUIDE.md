# SRC Management System - UI Interface Guide

## Complete Visual Interface Specifications

---

## 1. LOGIN SCREEN
**File Path:** `Views/LoginWindow.xaml`

### Layout & Design:
```
┌─────────────────────────────────────────┐
│                                         │
│         SRC MANAGEMENT SYSTEM           │
│                                         │
│         [Login Icon]                    │
│                                         │
│    Username: [________________]         │
│                                         │
│    Password: [________________]         │
│                                         │
│    [ Remember Me ☐ ]                   │
│                                         │
│    [     LOGIN BUTTON     ]             │
│                                         │
│    [ Forgot Password? ]                 │
│                                         │
└─────────────────────────────────────────┘
```

### Features:
- Centered login form (500px width × 400px height)
- Blue gradient background
- Logo at top
- Username text input
- Password text input (masked)
- "Remember Me" checkbox
- Login button (blue, bold font)
- "Forgot Password?" link
- Error message display area
- Loading spinner during authentication

### Color Scheme:
- Background: Dark blue gradient (#1a3a52 to #2c5aa0)
- Text: White (#FFFFFF)
- Input fields: Light gray (#F5F5F5)
- Button: Bright blue (#0066CC)
- Accent: Orange (#FF9500)

---

## 2. MAIN DASHBOARD
**File Path:** `Views/MainWindow.xaml`

### Layout & Design:
```
┌─────────────────────────────────────────────────────────────────────────┐
│ [Menu Icon]  SRC MANAGEMENT SYSTEM                          [👤] [⚙️]  │
├──────────────┬────────────────────────────────���───────────────────────┤
│              │                                                        │
│ MENU         │              WELCOME, [USERNAME]!                    │
│              │                                                        │
│ • Dashboard  │  ┌──────────────┬──────────────┬──────────────┐       │
│ • Members    │  │  Members     │    Events    │   Budget     │       │
│ • Events     │  │     125      │      8       │   $15,000    │       │
│ • Finance    │  └──────────────┴──────────────┴──────────────┘       │
│ • Reports    │                                                        │
│ • Settings   │  RECENT ACTIVITIES              UPCOMING EVENTS       │
│              │  ┌─────────────────┐          ┌──────────────────┐    │
│ [Logout]     │  │ • New member    │          │ • Meeting - Dec 5│    │
│              │  │   joined SRC    │          │ • Event - Dec 10 │    │
│              │  │                 │          │ • Fund - Dec 15  │    │
│              │  └─────────────────┘          └──────────────────┘    │
│              │                                                        │
│              │  STATISTICS                    ANNOUNCEMENTS           │
│              │  ┌─────────────────┐          ┌──────────────────┐    │
│              │  │ Total Budget    │          │ New SRC Policy   │    │
│              │  │ $15,000         │          │ approved!        │    │
│              │  │ ━━━━━━━━━ 60%   │          │                  │    │
│              │  └─────────────────┘          └──────────────────┘    │
│              │                                                        │
└──────────────┴────────────────────────────────────────────────────────┘
```

### Key Components:
- **Top Navigation Bar:**
  - Menu toggle button (hamburger icon)
  - App title and logo
  - User profile icon
  - Settings icon
  - Logout button

- **Sidebar Menu:**
  - Dashboard (active by default)
  - Members
  - Events
  - Finance
  - Reports
  - Settings
  - Logout

- **Main Content Area:**
  - Welcome greeting with username
  - Key metrics cards (Members, Events, Budget)
  - Recent activities list
  - Upcoming events section
  - Budget statistics chart
  - Announcements section

### Color Scheme:
- Sidebar: Dark blue (#1a3a52)
- Background: Light gray (#F8F9FA)
- Cards: White (#FFFFFF)
- Text: Dark gray (#333333)
- Accent: Blue (#0066CC)
- Secondary accent: Orange (#FF9500)

---

## 3. MEMBERS MANAGEMENT
**File Path:** `Views/MembersWindow.xaml`

### Layout & Design:
```
┌─────────────────────────────────────────────────────────────┐
│ Members Management                                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ [+ Add Member] [Edit] [Delete] | Search: [___________]    │
│                                                             │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ Name        │ Position      │ Email      │ Contact   │  │
│ ├──────────────────────────────────────────────────────┤  │
│ │ John Smith  │ President     │ john@...   │ 055-1234  │  │
│ │ Sarah Lee   │ VP            │ sarah@...  │ 055-5678  │  │
│ │ Mike Chen   │ Treasurer     │ mike@...   │ 055-9012  │  │
│ │ Emma Davis  │ Secretary     │ emma@...   │ 055-3456  │  │
│ │ David Wilson│ Member        │ david@...  │ 055-7890  │  │
│ │ Lisa Brown  │ Member        │ lisa@...   │ 055-2345  │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                             │
│ Showing 1-6 of 125 members          [< Prev] [Next >]      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Features:
- **Toolbar:**
  - Add Member button (green)
  - Edit button (blue)
  - Delete button (red)
  - Refresh button
  - Export to Excel button

- **Search & Filter:**
  - Search box (real-time filtering)
  - Filter by position dropdown
  - Filter by department

- **Data Grid:**
  - Sortable columns: Name, Position, Email, Contact, Join Date
  - Alternating row colors for readability
  - Row selection checkbox
  - Click to view full member details

- **Pagination:**
  - Previous/Next buttons
  - Current page indicator
  - Items per page selector

---

## 4. ADD/EDIT MEMBER DIALOG
**File Path:** `Views/Dialogs/MemberDialog.xaml`

### Layout & Design:
```
┌──────────────────────────────────────────┐
│  Add New Member                      [X] │
├──────────────────────────────────────────┤
│                                          │
│ First Name:    [____________________]   │
│                                          │
│ Last Name:     [____________________]   │
│                                          │
│ Email:         [____________________]   │
│                                          │
│ Phone:         [____________________]   │
│                                          │
│ Position:      [Dropdown ▼]             │
│                 • President              │
│                 • Vice President         │
│                 • Treasurer              │
│                 • Secretary              │
│                 • Member                 │
│                                          │
│ Department:    [Dropdown ▼]             │
│                                          │
│ Date Joined:   [Calendar Picker]        │
│                                          │
│ Bio:           [____________________]   │
│                [____________________]   │
│                                          │
│ [ Save ]  [ Cancel ]                    │
│                                          │
└──────────────────────────────────────────┘
```

### Features:
- Modal dialog (600px × 500px)
- Form validation with error messages
- Required field indicators (*)
- Dropdown menus for Position and Department
- Calendar picker for Date Joined
- Multi-line text area for Bio
- Save and Cancel buttons
- Close button (X)

---

## 5. EVENTS MANAGEMENT
**File Path:** `Views/EventsWindow.xaml`

### Layout & Design:
```
┌────────────────────────────────────────────────────────────┐
│ Events Management                                          │
├────────────────────────────────────────────────────────────┤
│                                                            │
│ [+ Add Event] [Edit] [Delete] | Filter: [Status ▼]       │
│                                                            │
│ View: [Calendar] [List] [Timeline]                        │
│                                                            │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ Event Name    │ Date       │ Time    │ Location    │  │
│ ├──────────────────────────────────────────────────────┤  │
│ │ General Mtg   │ Dec 5, 2024│ 2:00 PM │ Hall A      │  │
│ │ Orientation   │ Dec 10,2024│ 9:00 AM │ Campus      │  │
│ │ Fundraiser    │ Dec 15,2024│ 6:00 PM │ Auditorium  │  │
│ │ Year-End Gala │ Dec 22,2024│ 7:00 PM │ Ballroom    │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
│ [< Prev Month] December 2024 [Next Month >]              │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Features:
- **Toolbar:**
  - Add Event button
  - Edit button
  - Delete button
  - View toggle (Calendar/List/Timeline)
  - Filter by status

- **Calendar View:**
  - Month calendar
  - Events highlighted on dates
  - Click to view/edit event
  - Drag to reschedule

- **List View:**
  - Sortable columns: Event Name, Date, Time, Location, Status
  - Status badges (Upcoming, Ongoing, Completed, Cancelled)
  - Attendance count

- **Timeline View:**
  - Chronological event display
  - Event duration visualization

---

## 6. ADD/EDIT EVENT DIALOG
**File Path:** `Views/Dialogs/EventDialog.xaml`

### Layout & Design:
```
┌──────────────────────────────────────────┐
│  Add New Event                       [X] │
├──────────────────────────────────────────┤
│                                          │
│ Event Name:    [____________________]   │
│                                          │
│ Description:   [____________________]   │
│                [____________________]   │
│                                          │
│ Date:          [Calendar Picker]        │
│                                          │
│ Start Time:    [Time Picker]            │
│                                          │
│ End Time:      [Time Picker]            │
│                                          │
│ Location:      [____________________]   │
│                                          │
│ Organizer:     [____________________]   │
│                                          │
│ Expected Attendance: [____]             │
│                                          │
│ Status:        [Dropdown ▼]             │
│                 • Planned                │
│                 • Confirmed              │
│                 • Ongoing                │
│                 • Completed              │
│                                          │
│ Attachments:   [+ Add File]             │
│                                          │
│ [ Save ]  [ Cancel ]                    │
│                                          │
└──────────────────────────────────────────┘
```

### Features:
- Modal dialog (600px × 550px)
- Event details form
- Date and time pickers
- Status dropdown
- Attendance capacity field
- File upload for event materials
- Form validation
- Save and Cancel buttons

---

## 7. FINANCE MANAGEMENT
**File Path:** `Views/FinanceWindow.xaml`

### Layout & Design:
```
┌────────────────────────────────────────────────────────────┐
│ Finance Management                                         │
├────────────────────────────────────────────────────────────┤
│                                                            │
│ ┌─────────────┬─────────────┬─────────────┐               │
│ │  INCOME     │  EXPENSES   │  BALANCE    │               │
│ │  $5,000     │  $2,500     │  $2,500     │               │
│ └─────────────┴─────────────┴─────────────┘               │
│                                                            │
│ [+ Add Transaction] [Edit] [Delete] | Period: [2024 ▼]  │
│                                                            │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ Date       │ Description    │ Category │ Amount │ Type│  │
│ ├─────────────────���────────────────────────────────────┤  │
│ │ Dec 1      │ Student fees   │ Income   │ $1,500 │ ✓  │  │
│ │ Dec 2      │ Decoration     │ Expense  │ $800   │ ✗  │  │
│ │ Dec 3      │ Catering       │ Expense  │ $1,200 │ ✗  │  │
│ │ Dec 5      │ Donation       │ Income   │ $500   │ ✓  │  │
│ │ Dec 7      │ Transport      │ Expense  │ $500   │ ✗  │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
│ BUDGET BREAKDOWN                                           │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ Events      ████████░░░ 60%  ($3,000/$5,000)        │  │
│ │ Operations  ████░░░░░░░ 20%  ($1,000/$5,000)        │  │
│ │ Marketing   ██░░░░░░░░░ 10%  ($500/$5,000)          │  │
│ │ Other       ░░░░░░░░░░░ 10%  ($500/$5,000)          │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Features:
- **Summary Cards:**
  - Total Income
  - Total Expenses
  - Current Balance
  - Budget Status

- **Transaction List:**
  - Date, Description, Category, Amount
  - Income (green) vs Expense (red)
  - Sortable and filterable
  - View receipts/attachments

- **Budget Breakdown:**
  - Pie/Bar charts showing category breakdown
  - Budget vs Actual comparison
  - Monthly trend chart

- **Export:**
  - Export to PDF/Excel
  - Print financial reports

---

## 8. ADD TRANSACTION DIALOG
**File Path:** `Views/Dialogs/TransactionDialog.xaml`

### Layout & Design:
```
┌──────────────────────────────────────────┐
│  Add Transaction                     [X] │
├──────────────────────────────────────────┤
│                                          │
│ Type:          [Income ▼] [Expense ▼]   │
│                                          │
│ Date:          [Calendar Picker]        │
│                                          │
│ Amount:        [$____________________]   │
│                                          │
│ Category:      [Select Category ▼]      │
│                 • Events                 │
│                 • Operations             │
│                 • Marketing              │
│                 • Salaries               │
│                 • Other                  │
│                                          │
│ Description:   [____________________]   │
│                                          │
│ Payment Method:[Cash  ][Cheque ][Bank]  │
│                                          │
│ Attached To:   [Event/Activity ▼]       │
│                                          │
│ Receipt:       [+ Upload File]          │
│                                          │
│ Notes:         [____________________]   │
│                [____________________]   │
│                                          │
│ [ Save ]  [ Cancel ]                    │
│                                          │
└──────────────────────────────────────────┘
```

---

## 9. REPORTS & ANALYTICS
**File Path:** `Views/ReportsWindow.xaml`

### Layout & Design:
```
┌────────────────────────────────────────────────────────────┐
│ Reports & Analytics                                        │
├────────────────────────────────────────────────────────────┤
│                                                            │
│ Report Type: [All Reports ▼] Date Range: [From - To]     │
│                                                            │
│ ┌─────────────────────────────────────────────────────┐   │
│ │ • Membership Report                          [PDF] │   │
│ │ • Event Attendance Report                    [PDF] │   │
│ │ • Financial Summary Report                   [PDF] │   │
│ │ • Budget Analysis Report                     [PDF] │   │
│ │ • Year-End Report                            [PDF] │   │
│ │ • Activity Log Report                        [PDF] │   │
│ └─────────────────────────────────────────────────────┘   │
│                                                            │
│ CHARTS & STATISTICS                                        │
│                                                            │
│ ┌──────────────────┐    ┌──────────────────┐             │
│ │ Member Growth    │    │ Budget Spending  │             │
│ │ (Line Chart)     │    │ (Pie Chart)      │             │
│ │                  │    │                  │             │
│ │ ▗▄▄▄▖            │    │   ╭─────╮       │             │
│ │ │    ╰▄╰▄         │    │  ╱       ╲      │             │
│ │ ╰▄   ╭▄╭▄        │    │  │   60%  │     │             │
│ └──────────────────┘    └─���────────────────┘             │
│                                                            │
│ ┌──────────────────┐    ┌──────────────────┐             │
│ │ Event Frequency  │    │ Expense Trends   │             │
│ │ (Bar Chart)      │    │ (Area Chart)     │             │
│ └──────────────────┘    └──────────────────┘             │
│                                                            │
│ [Export All Reports] [Print] [Email Reports]             │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Features:
- **Report Types:**
  - Membership summary and growth
  - Event attendance and participation
  - Financial summaries
  - Budget analysis
  - Year-end reports
  - Activity logs

- **Visualizations:**
  - Line charts (trends over time)
  - Pie charts (distribution)
  - Bar charts (comparisons)
  - Area charts (cumulative data)

- **Export Options:**
  - PDF download
  - Excel export
  - Email distribution
  - Print functionality

---

## 10. COMMUNICATIONS/ANNOUNCEMENTS
**File Path:** `Views/CommunicationsWindow.xaml`

### Layout & Design:
```
┌────────────────────────────────────────────────────────────┐
│ Communications                                             │
├────────────────────────────────────────────────────────────┤
│                                                            │
│ [+ New Announcement] [Messages] [Notifications]           │
│                                                            │
│ ANNOUNCEMENTS                                              │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ ▢ New SRC Policy Approved!                 Dec 5    │  │
│ │   Important update regarding member benefits        │  │
│ │                                                      │  │
│ │ ▢ Upcoming Event: Year-End Gala               Dec 1  │  │
│ │   Save the date! Details coming soon                │  │
│ │                                                      │  │
│ │ ▢ Meeting Rescheduled to Dec 12             Nov 28  │  │
│ │   Due to venue availability                         │  │
│ │                                                      │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
│ INTERNAL MESSAGES                                          │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ From: President                           Today      │  │
│ │ Subject: Urgent - Budget Review Meeting             │  │
│ │ Please review the attached budget...                │  │
│ │                                                      │  │
│ │ From: Secretary                         Yesterday    │  │
│ │ Subject: Minutes from Last Meeting                  │  │
│ │ Please find attached...                             │  │
│ │                                                      │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
│ [Compose Message]  [Mark as Read]  [Archive]             │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

---

## 11. CREATE ANNOUNCEMENT DIALOG
**File Path:** `Views/Dialogs/AnnouncementDialog.xaml`

### Layout & Design:
```
┌──────────────────────────────────────────┐
│  New Announcement                    [X] │
├──────────────────────────────────────────┤
│                                          │
│ Title:         [____________________]   │
│                                          │
│ Category:      [Select Category ▼]      │
│                 • General                │
│                 • Event                  │
│                 • Finance                │
│                 • Policy                 │
│                 • Emergency              │
│                                          │
│ Message:       [____________________]   │
│                [____________________]   │
│                [____________________]   │
│                                          │
│ Recipient:     [ All Members ]           │
│                [ Officers Only ]         │
│                [ Specific Group ▼]      │
│                                          │
│ Priority:      [◉ Normal ○ High ○ Urgent]
│                                          │
│ Schedule:      [Now] [Schedule for...]   │
│                                          │
│ Attachments:   [+ Add File]              │
│                                          │
│ [ Preview ]  [ Save as Draft ]           │
│ [ Send ] [ Cancel ]                      │
│                                          │
└──────────────────────────────────────────┘
```

---

## 12. SETTINGS PAGE
**File Path:** `Views/SettingsWindow.xaml`

### Layout & Design:
```
┌────────────────────────────────────────────────────────────┐
│ Settings                                                   │
├────────────────────────────────────────────────────────────┤
│                                                            │
│ SYSTEM SETTINGS                                            │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ ► General Settings                                   │  │
│ │   • App Theme: [Light ▼]                            │  │
│ │   • Language: [English ▼]                           │  │
│ │   • Auto-save: [☑ Enabled]                          ���  │
│ │   • Show Notifications: [☑ Enabled]                 │  │
│ │                                                      │  │
│ │ ► User Profile                                      │  │
│ │   • Name: [____________________]                    │  │
│ │   • Email: [____________________]                   │  │
│ │   • Phone: [____________________]                   │  │
│ │   • [Change Password]                               │  │
│ │   • [Change Avatar]                                 │  │
│ │                                                      │  │
│ │ ► Organization                                      │  │
│ │   • Organization Name: [____________________]       │  │
│ │   • Established Date: [Calendar]                    │  │
│ │   • Logo: [Upload File]                             │  │
│ │   • Main Color: [Color Picker]                      │  │
│ │                                                      │  │
│ │ ► Database                                          │  │
│ │   • Database Path: [____________________]           │  │
│ │   • Auto-backup: [☑ Daily]                          │  │
│ │   • [Backup Now] [Restore]                          │  │
│ │                                                      │  │
│ │ ► Permissions & Roles                               │  │
│ │   • Admin Role Setup                                │  │
│ │   • Custom Roles Management                         │  │
│ │   • Access Control Lists                            │  │
│ │                                                      │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
│ [ Apply Settings ]  [ Reset to Default ]  [ Close ]       │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

---

## 13. USER PROFILE PAGE
**File Path:** `Views/UserProfileWindow.xaml`

### Layout & Design:
```
┌────────────────────────────────────────────────────────────┐
│ My Profile                                                 │
├────────────────────────────────────────────────────────────┤
│                                                            │
│                [Avatar Image]                              │
│                                                            │
│ Name:          John Smith                                  │
│ Position:      President                                   │
│ Email:         john.smith@university.edu                  │
│ Phone:         +1-555-0123                                │
│ Joined:        January 2023                                │
│ Department:    Executive Council                           │
│                                                            │
│ ┌─────────────────────────────────────────────────────┐   │
│ │ RESPONSIBILITIES                                   │   │
│ │ • Lead SRC initiatives and projects               │   │
│ │ • Represent student body in university meetings   │   │
│ │ • Oversee SRC budget and finances                 │   │
│ │ • Chair regular council meetings                  │   │
│ └─────────────────────────────────────────────────────┘   │
│                                                            │
│ ┌─────────────────────────────────────────────────────┐   │
│ │ ACTIVITY HISTORY                                  │   │
│ │ • Organized Orientation - Dec 2024                │   │
│ │ • Attended Budget Meeting - Dec 2024              │   │
│ │ • Approved Event Request - Dec 2024               │   │
│ └─────────────────────────────────────────────────────┘   │
│                                                            │
│ [ Edit Profile ]  [ Change Password ]  [ Export Report ]  │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

---

## 14. SYSTEM NOTIFICATIONS
**File Path:** `Views/NotificationPanel.xaml`

### Layout & Design:
```
┌─────────────────────────────────┐
│ NOTIFICATIONS              [×]   │
├─────────────────────────────────┤
│                                 │
│ 🔔 New event request received   │
│    John requested "Campus Day"  │
│    2 minutes ago                │
│    [✓ Approve] [✗ Reject]       │
│                                 │
│ ℹ️ Meeting reminder              │
│    Budget Review Meeting         │
│    Today at 2:00 PM              │
│    [Open Calendar]               │
│                                 │
│ ✓ Transaction approved          │
│    $500 expense recorded         │
│    2 hours ago                   │
│                                 │
│ ⚠️ Low budget alert              │
│    Events budget at 95%          │
│    15 minutes ago                │
│                                 │
│ [Mark All as Read]  [Settings]  │
│                                 │
└─────────────────────────────────┘
```

---

## 15. HELP & SUPPORT
**File Path:** `Views/HelpWindow.xaml`

### Layout & Design:
```
┌────────────────────────────────────────────────────────────┐
│ Help & Support                                             │
├────────────────────────────────────────────────────────────┤
│                                                            │
│ Search Help: [_____________________________]              │
│                                                            │
│ FREQUENTLY ASKED QUESTIONS                                 │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ ▸ How do I add a new member?                        │  │
│ │ ▸ How do I create an event?                         │  │
│ │ ▸ How do I manage budget?                           │  │
│ │ ▸ How do I generate reports?                        │  │
│ │ ▸ How do I send announcements?                      │  │
│ │ ▸ How do I reset my password?                       │  │
│ │ ▸ How do I export data?                             │  │
│ │ ▸ What are user roles and permissions?              │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
│ CONTACT SUPPORT                                            │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ Email: support@srcms.com                            │  │
│ │ Phone: +1-555-0456                                  │  │
│ │ Chat Support: [Available 9AM - 5PM]                 │  │
│ │ Ticket System: [Create Support Ticket]              │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                            │
│ DOCUMENTATION                                              │
│ [User Manual] [Video Tutorials] [FAQ PDF] [Contact Us]   │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

---

## COLOR PALETTE SUMMARY

| Element | Color Code | Usage |
|---------|-----------|-------|
| Primary Blue | #0066CC | Main buttons, links, active states |
| Dark Blue | #1a3a52 | Sidebar, headers |
| Light Gray | #F8F9FA | Main background |
| White | #FFFFFF | Cards, panels, text backgrounds |
| Dark Text | #333333 | Body text |
| Success Green | #28A745 | Income, success messages |
| Danger Red | #DC3545 | Expenses, delete actions |
| Warning Orange | #FF9500 | Alerts, warnings |
| Light Border | #E0E0E0 | Dividers, borders |

---

## RESPONSIVE DESIGN

All interfaces should be responsive and adapt to:
- **Desktop:** 1920×1080 and above
- **Laptop:** 1366×768
- **Tablet:** 1024×768
- Mobile support for view-only dashboards

---

## TYPOGRAPHY

- **Headers:** Arial Bold, 24px
- **Subheaders:** Arial Bold, 16px
- **Body Text:** Arial Regular, 12px
- **Small Text:** Arial Regular, 10px
- **Monospace:** Courier New (for data/codes)

---

## ACCESSIBILITY

- All buttons have tooltips
- Keyboard navigation support
- High contrast mode option
- Screen reader compatible
- Clear error messages with suggested actions

