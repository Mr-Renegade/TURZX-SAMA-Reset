[README.txt](https://github.com/user-attachments/files/22131105/README.txt)
TURZX / SAMA Auto-Reset (Sleep/Wake)
====================================

What this does
--------------
- On wake, resets the TURZX/SAMA HID "vendor-defined" interface (VID_04D9 & PID_A118) using built-in pnputil.
- Relaunches whichever app is installed: **SAMA.exe** or **TURZX.exe** (preferred).
- Logs per app into Logs\SAMA or Logs\TURZX; keeps the last 10 timestamped logs.

Quick install
-------------
1) Extract this zip anywhere.
2) Right-click **Setup_TURZX_SAMA_Reset.bat** → **Run as administrator**.
   - Installs to: C:\Scripts\TURZX Reset Script\
   - Registers scheduled task: **Reset_Screen_On_Resume**
3) Sleep → Wake to test, or run the task manually in Task Scheduler.

Manual install (optional)
-------------------------
- Copy folder "TURZX Reset Script" to: C:\Scripts\TURZX Reset Script\
- Import **turzx-sama-task.xml** in Task Scheduler (Run with highest privileges).
- Confirm the task action points to:
  Program: cmd.exe
  Args: /c "C:\Scripts\TURZX Reset Script\reset-panel.bat"
  Start in: C:\Scripts\TURZX Reset Script
