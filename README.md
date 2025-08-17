# 🛡️ Greaton Triage Tool
**Version:** 1.7.9 (USB Ready)  
**Author:** Greaton Forensics  

## 📖 Overview
The **Greaton Triage Tool** is a lightweight and portable digital forensics utility designed to quickly collect essential system information during incident response and forensic triage. It provides investigators, IT administrators, and security teams with a structured view of a system’s configuration, usage, and potential traces of malicious activity.  

By automating data gathering, the tool reduces the time needed to perform initial assessments and ensures consistent, repeatable results. It is especially useful in live response scenarios where time is critical and no additional software installation should be performed on the target system.

## 💡 Value
- **Rapid Triage** – Collects valuable system information within minutes.  
- **Non-Intrusive** – Runs directly from USB, leaving a minimal footprint.  
- **Standardized Output** – Produces logs, structured CSV files, and summary reports for quick analysis or integration with SIEMs.  
- **Versatile Use Cases** – Supports both corporate IT investigations and educational/training purposes.  

## 📂 Output Structure
- **Collector.log** – full transcript of execution  
- **Report.html / Report.pdf** – formatted summary for quick review  
- **CSVs** – structured tabular data for further analysis (Excel, Splunk, ELK)  
- **Artifacts** – raw collected artifacts (registry/config exports, event logs, task XML, startup items)  

## 🚀 Usage
### From USB
1. Copy `Greaton-Triage-Tool.exe` to your USB drive.  
2. Run as **Administrator** (UAC prompt will appear).  
3. Wait for the process to complete (usually a few minutes).  
4. Review the generated `.\Output\` folder (or `.\Cases\<CaseId>\Output\...`).  

### From Command Line
```powershell
.\Greaton-Triage-Tool.exe -CaseId "CASE123"
```

### Optional arguments
- `-CaseId <ID>` : Tag output under `.\Cases\<ID>\Output\<HOST>_<timestamp>\...`  
- `-IncludeWifiKeys:$false` : Export Wi-Fi profiles without plaintext keys  
- `-DeepFDEScan:$false` : Skip deep scan of Program Files/ProgramData for FDE traces  
- `-GenerateReport:$false` : Skip HTML/PDF report generation  

## ⚠️ Requirements
- Windows 10 / 11 (x64) or Windows Server 2016+  
- Administrator privileges  
- ~50–200 MB free disk space for output (varies with event log size)  
- If external tools are used, place them alongside the EXE (e.g., `.\Tools\...`) and reference relatively  

## 📜 License & Disclaimer
This tool is shared with the community for **lawful purposes only**, such as incident response, digital forensics training, or authorized system information gathering.  

- **Use it at your own risk.**  
- The authors are **not liable** for misuse of this tool.  
- Do **not** run it on systems you do not own or do not have explicit permission to investigate.  

## 📧 Contact
For support or professional services:  
**Greaton Forensics**  
✉️ admin@greaton.co.uk  
🌐 https://greaton.co.uk  

## ⭐ Support the Project
If you find this tool useful, please consider giving it a ⭐ on GitHub — it helps the community discover it!
