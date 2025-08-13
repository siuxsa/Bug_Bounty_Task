# SIUXSA Checklist - Bug Bounty & Pentest Task Manager

![Screenshot](https://raw.githubusercontent.com/siuxsa/Bug_Bounty_Task/refs/heads/main/Screenshot/Screenshot%202025-08-14%20015359.png) *(placeholder for actual screenshot)*

A modern, browser-based checklist manager for bug bounty hunters and penetration testers to track tasks across multiple targets.

## Features

- **Target Management**: Organize tasks by target (domains, IPs, apps)
- **Task Categories**: Recon, Enumeration, Scanning, Web Vulns, Auth, Cloud, Mobile, Reporting
- **Persistent Storage**: All data saved in browser's `localStorage`
- **Quick Filtering**: Filter by keyword or `#category`
- **Progress Tracking**: See completed/pending tasks at a glance
- **Portable**: Export/import JSON for backups or sharing
- **Responsive**: Works on desktop and mobile
- **Dark UI**: Easy on the eyes during long testing sessions

## Usage

1. **Add Targets**: Enter domains or IP addresses
2. **Create Tasks**: Add manual tasks or use the template for common pentest activities
3. **Track Progress**: Check off completed items
4. **Filter**: Use search box for `#category` or keywords
5. **Export**: Save your progress as JSON

## Keyboard Shortcuts

- **Enter** in task field: Quick-add new task
- **Click checkbox**: Toggle task completion

## Installation

No installation required! Just open `index.html` in any modern browser.

For persistent access:
1. Clone this repo
2. Host the HTML file on a local web server or cloud storage

## Data Structure

All data is stored in browser localStorage under key `pentestChecklist.v1` with this structure:
```json
{
  "targets": {
    "example.com": [
      {
        "id": "abc123",
        "title": "Run subfinder",
        "notes": "subfinder -d example.com -o subs.txt",
        "category": "Recon",
        "done": false,
        "createdAt": "2023-01-01T00:00:00.000Z",
        "updatedAt": "2023-01-01T00:00:00.000Z"
      }
    ]
  },
  "order": ["example.com"]
}
