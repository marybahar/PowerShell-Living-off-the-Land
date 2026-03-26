# PowerShell-Living-off-the-Land
## 🕵️ Detection Case Study: PowerShell "Living off the Land."
To validate the effectiveness of the Sysmon integration, I simulated a common attack technique: **PowerShell Execution Policy Bypass**.

* **Objective:** Detect a hidden PowerShell process attempting to reach a remote URL.
* **Technique:** Used `powershell.exe` with `-ExecutionPolicy Bypass` and `-WindowStyle Hidden`.
* **Detection Logic:** Created a KQL query filtering for **Event ID 1** (Process Creation) where the command line contained suspicious flags.
* **Result:** Successfully identified the source user, the parent process, and the exact timestamp of the execution.
<img width="1906" height="847" alt="image" src="https://github.com/user-attachments/assets/b285dac2-20ed-4cae-a9cb-af7b9cad30cc" />
