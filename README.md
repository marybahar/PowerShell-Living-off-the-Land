# PowerShell-Living-off-the-Land
## 🕵️ Detection Case Study: PowerShell "Living off the Land."
To validate the effectiveness of the Sysmon integration, I simulated a common attack technique: **PowerShell Execution Policy Bypass**.

* **Objective:** Detect a hidden PowerShell process attempting to reach a remote URL.
* **Technique:** Used `powershell.exe` with `-ExecutionPolicy Bypass` and `-WindowStyle Hidden`.
* **Detection Logic:** Created a KQL query filtering for **Event ID 1** (Process Creation) where the command line contained suspicious flags.
* **Result:** Successfully identified the source user, the parent process, and the exact timestamp of the execution.
<img width="1625" height="706" alt="image" src="https://github.com/user-attachments/assets/317d24c8-b920-4abc-a37a-9ed695577b80" />
