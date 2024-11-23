# Alfred Workflow: Next Meeting Assistant

A lightweight Alfred workflow that helps you quickly find and join your next scheduled meeting with just a few keystrokes. Inspired by [Open Conference URL](https://alfred.app/workflows/caleb531/open-conference-url/), this workflow simplifies the original concept by leveraging a Bash script for efficiency and ease of customization. 

---

## Features

- **Simplified Workflow**: No need for complex Python scripts or additional dependencies—everything runs via a compact Bash script.
- **Multiple Google Accounts Support**: Struggled with the wrong Google account being used to open meeting links? This workflow ensures the correct account is selected when opening Google Meet URLs.
- **Customizable and Free**: Fully open-source and designed for easy modification to suit your specific needs.

---

## How It Works

The workflow fetches your calendar events using `icalBuddy` and extracts details about your upcoming meetings, including:
- **Meeting Title**
- **Time**
- **Email (Organizer)**
- **Meeting URL (Google Meet, Zoom, etc.)**

### Example Output:
```json
{
  "title": "19:00 > Team Sync",
  "email": "youremail@example.com",
  "time": "19:00",
  "url": "https://meet.google.com/xyz?authuser=youremail@example.com",
  "variables": {
    "event_url": "https://meet.google.com/xyz?authuser=youremail@example.com"
  }
}
```

## Prerequisites
* macOS: This workflow is designed to work on macOS.
* Alfred: Download Alfred (Powerpack required to import workflows).
* icalBuddy: Ensure icalBuddy is installed to fetch calendar data.
Install via Homebrew:
```bash
brew install ical-buddy
```

## Installation

Clone the repository or download the workflow package:
```bash
git clone https://github.com/denysovkos/-Alfred-Next-meeting.git
```

Import the workflow into Alfred:
* Open Alfred Preferences (Cmd + ,).
* Navigate to the "Workflows" tab.
* Drag and drop the .alfredworkflow file into Alfred.

## Usage

Trigger the workflow by typing the assigned keyword in Alfred (default `cf`).
Alfred will display details about your upcoming meeting.
Select the meeting to open its URL directly in your browser, ensuring the correct Google account is used if applicable.
Customization

This workflow is fully open-source and can be tailored to your needs. The core logic resides in the Bash script, which you can modify to:

Add support for more meeting platforms.
Customize how events are displayed.
Include additional calendar fields.
Feedback & Contributions

##  I’d love to hear your thoughts! Feel free to:

* Share feedback or suggestions.
* Open issues or pull requests to improve the workflow.

##  License

This project is open-source and free under the MIT License. Use it, modify it, and share it!
