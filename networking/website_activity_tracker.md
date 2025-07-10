# Problem Statement: Website Activity Tracker and Auto Blocker

## Objective

The goal of this task is to create a Python-based monitoring and control tool that tracks user web activity and automatically blocks access to selected websites based on predefined rules or user-defined thresholds. The system aims to improve productivity, enforce parental controls, or enhance digital wellness by restricting access to distracting or harmful content.

---

## Functional Requirements

### 1. Website Tracker

- Monitor and log all websites visited by the user in real-time.
- Record essential information such as:
  - URL
  - Timestamp of visit
  - Duration of visit (optional for enhancement)
- Store logs locally in a structured format (e.g., CSV, SQLite, or JSON).

### 2. Automatic Website Blocker

- Automatically block access to blacklisted websites based on:
  - Static block list (e.g., predefined sites like `facebook.com`, `youtube.com`)
  - Dynamic rules (e.g., visiting a site more than N times in an hour)
- Modify the system's `hosts` file to redirect blocked sites to `127.0.0.1`.
- Optionally unblock sites after a cooldown period or by admin input.

---

## Non-Functional Requirements

- Cross-platform support (Windows, macOS, Linux preferred).
- Lightweight and runs in the background with minimal resource usage.
- Must run with elevated/admin privileges to modify the system `hosts` file.

---

## Deliverables

- Python script(s) for:
  - Website tracking
  - Auto-blocking logic
  - Blocklist maintenance
- Logs of visited websites with timestamps
- Blocklist configuration file
- Screenshots or terminal logs demonstrating:
  - Real-time tracking
  - Auto-blocking behavior
- Optional GUI or CLI interface for managing block rules

---

## Approach

1. **Tracking Websites Visited**
   - Use platform-specific APIs:
     - Windows: `psutil`, browser history files, or a browser extension
     - Linux/macOS: Use `mitmproxy`, browser logs, or packet sniffing
   - Log visited URLs with timestamps into a local database or file.

2. **Blocking Mechanism**
   - Modify `/etc/hosts` (Linux/macOS) or `C:\Windows\System32\drivers\etc\hosts` (Windows).
   - Add lines like:
     ```
     127.0.0.1 www.youtube.com
     127.0.0.1 youtube.com
     ```
   - Flush DNS cache if necessary to apply changes immediately.

3. **Automation Logic**
   - Define thresholds or rules (e.g., visits > 5 in 1 hour).
   - Continuously analyze log file in real-time or batch mode.
   - Update blocklist and `hosts` file automatically.
