# Telegram Bot for User Management and Reporting

This project is a **Telegram Bot** designed for user management, report collection, and task assignment. It includes functionalities like user authentication, file handling, report generation, and task prioritization.

---

## Features

- **User Authentication**: Authenticate users using predefined codes.
- **Report Submission**: Collect user reports with the option to attach files or photos.
- **File Handling**: Save reports to JSON, Excel, and CSV files.
- **Task Management**:
  - Managers can assign tasks to multiple users with a specified priority and deadline.
  - Notifications for pending tasks.
- **Automated Messages**: Send scheduled reminders for reports and regular data backups.
- **Secure Design**: Bot token is securely loaded, and file operations are thread-safe.

---

## Getting Started

### Prerequisites

- **Python 3.8+**
- Required libraries: `os`, `json`, `jdatetime`, `pandas`, `schedule`, `telebot`

Install dependencies:
```bash
pip install pyTelegramBotAPI pandas schedule openpyxl
```

### Environment Setup

Set your Telegram Bot token as an environment variable:
```bash
export TELEGRAM_BOT_TOKEN="YOUR_BOT_TOKEN"
```

---

## File Structure

- **`user_reports.json`**: Stores user reports.
- **`users2.json`**: Keeps user authentication details.
- **`user_reports.xlsx`**: Excel backup of user reports.
- **`user_reports.csv`**: CSV backup of user reports.

---

## Usage

1. **Run the bot**:
   ```bash
   python bot.py
   ```

2. **User Commands**:
   - `/start`: Begin interaction with the bot.
   - Enter the assigned user code to authenticate.

3. **Manager Commands**:
   - Assign tasks to users with priority and deadline.
   - View user reports in CSV format.

---

## Key Functions

### User Authentication

- Checks user codes from `USER_CODES` dictionary.
- Assigns roles as `Manager` or `User`.

### Report Submission

- Users can submit reports via text or file.
- Reports are saved to JSON and exported to Excel and CSV formats.

### Task Assignment

- Managers can assign tasks to multiple users.
- Task includes details like priority and deadline.

### Scheduled Messages

- Sends automated reminders daily at `19:00`.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contact

For any inquiries or support, contact the project maintainer.

---

## Disclaimer

This bot stores user data locally. Ensure appropriate security measures when deploying the bot to protect user privacy.

