# Windows Event Log Analysis Using Command Prompt (CMD)

> A practical Windows Event Log analysis project demonstrating how native Windows command-line tools can be used to investigate authentication events, account management activities, and system logs without relying on third-party software.

![Windows](https://img.shields.io/badge/Platform-Windows-blue)
![CMD](https://img.shields.io/badge/Tool-Command%20Prompt-green)
![Cybersecurity](https://img.shields.io/badge/Domain-Log%20Analysis-red)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## Project Overview

This project demonstrates a structured approach to Windows Event Log Analysis using the built-in **Windows Event Utility (`wevtutil`)** through Command Prompt (CMD).

The investigation focuses on identifying Windows Event Logs, querying authentication events, analyzing security-related Event IDs, and documenting findings using a professional incident investigation workflow.

The project was completed as part of practical cybersecurity training and reflects the investigative process commonly performed by Security Operations Center (SOC) analysts during Windows security investigations.

---

## Objectives

* Enumerate available Windows Event Logs
* Investigate Security, System, and Application logs
* Query authentication events using Event IDs
* Analyze successful and failed logon activities
* Investigate privileged account authentication
* Review user account creation events
* Document investigation procedures and findings
* Develop hands-on Windows log analysis skills

---

## Skills Demonstrated

* Windows Event Log Analysis
* Windows Security Monitoring
* Event ID Investigation
* Authentication Analysis
* Security Event Correlation
* Windows Command Line (CMD)
* Digital Forensics Fundamentals
* Security Documentation
* Incident Investigation
* SOC Analyst Methodology

---

## Technologies & Tools

* Windows Command Prompt (CMD)
* Windows Event Utility (`wevtutil`)
* Windows Event Viewer
* Microsoft Windows
* Git
* GitHub

---

## Windows Event IDs Investigated

| Event ID | Description                                                 |
| -------- | ----------------------------------------------------------- |
| 4624     | Successful Logon                                            |
| 4625     | Failed Logon                                                |
| 4720     | User Account Created                                        |
| 4726     | User Account Deleted *(Additional Investigation)*           |
| 4732     | User Added to Privileged Group *(Additional Investigation)* |
| 4723     | Password Change Attempt *(Additional Investigation)*        |
| 4724     | Password Reset *(Additional Investigation)*                 |
| 1074     | Planned Restart or Shutdown *(Additional Investigation)*    |
| 6008     | Unexpected Shutdown *(Additional Investigation)*            |

---

## Investigation Workflow

1. Enumerate available Windows Event Logs
2. Identify Security, System, and Application logs
3. Query authentication events
4. Analyze successful logons
5. Analyze failed logons
6. Review user account activity
7. Investigate Administrator authentication
8. Review account creation events
9. Document findings
10. Provide security recommendations

---

## Repository Structure

```
Windows-Event-Log-Analysis-CMD/
│
├── README.md
├── Windows_Event_Log_Analysis_Report.pdf
├── screenshots/
│   ├── Figure-01.png
│   ├── Figure-02.png
│   ├── Figure-03.png
│   └── ...
├── commands/
│   └── Event_Log_Commands.md
└── LICENSE
```

---

## Key Commands Used

List available event logs

```cmd
wevtutil el
```

Query successful logon events

```cmd
wevtutil qe Security /q:"*[System[(EventID=4624)]]" /f:text
```

Query failed logon events

```cmd
wevtutil qe Security /q:"*[System[(EventID=4625)]]" /f:text
```

Identify Administrator logons

```cmd
wevtutil qe Security /q:"*[System[(EventID=4624)]]" /f:text | findstr /i "Administrator"
```

Identify newly created user accounts

```cmd
wevtutil qe Security /q:"*[System[(EventID=4720)]]" /f:text
```

---

## Project Deliverables

* Professional Log Analysis Report
* Windows Event Log Investigation
* Event ID Analysis
* Command Documentation
* Investigation Workflow
* Screenshots of Practical Exercises
* Security Recommendations
* GitHub Documentation

---

## Learning Outcomes

Through this project, I gained practical experience in:

* Investigating Windows Event Logs using native tools
* Understanding Windows Security Event IDs
* Analyzing authentication events
* Performing command-line based investigations
* Documenting technical investigations in a professional format
* Applying a structured SOC analyst workflow

---

## Future Improvements

Future versions of this project may include:

* PowerShell-based event analysis
* Event Log automation scripts
* XML log filtering
* SIEM integration (Microsoft Sentinel / Splunk)
* Advanced Event ID correlation
* Timeline reconstruction
* Detection engineering use cases

---

## Author

**Sheu Abduljelil (Olamide)**

Cybersecurity Analyst

* LinkedIn: https://www.linkedin.com/in/sheu-abduljelil-olamide
* Email: [Sheuabduljelil@gmail.com](mailto:Sheuabduljelil@gmail.com)

---

## License

This project is published for educational and portfolio purposes. Feel free to use it as a learning reference while providing appropriate attribution.
