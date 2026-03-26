# PowerShell-Living-off-the-Land
## 🕵️ Detection Case Study: PowerShell "Living off the Land."
To validate the effectiveness of the Sysmon integration, I simulated a common attack technique: **PowerShell Execution Policy Bypass**.

* **Objective:** Detect a hidden PowerShell process attempting to reach a remote URL.
* **Technique:** Used `powershell.exe` with `-ExecutionPolicy Bypass` and `-WindowStyle Hidden`.
* **Detection Logic:** Created a KQL query filtering for **Event ID 1** (Process Creation) where the command line contained suspicious flags.
* **Result:** Successfully identified the source user, the parent process, and the exact timestamp of the execution.
* <img width="1115" height="850" alt="image" src="https://github.com/user-attachments/assets/9987bec5-2be2-4b8b-9150-2f3fcfc68a65" />

<img width="1904" height="854" alt="image" src="https://github.com/user-attachments/assets/73c47ab0-40d3-4d84-a4dd-36975bb007de" />
