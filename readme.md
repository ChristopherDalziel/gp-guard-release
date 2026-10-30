<p><img src="assets/readme-header.svg" alt="GP Guard - urgent assistance alerts"></p>

Local-network urgent assistance alerts for GP clinics on Windows 10 and 11 (64-bit). One **main PC** and any number of **workstations** communicate over the clinic network. There are no accounts, cloud services or database.

## For clinic staff

### Install and set up

1. Run `GPGuardSetup.exe` on every computer as an administrator. Allow the Windows firewall prompt and leave **Start GP Guard now** selected.
2. On one computer choose **Main PC**, give it a room name such as `Reception`, and note the 12-character pairing code.
3. On every other computer choose **Workstation**, give it a room name, and enter the same pairing code.
4. The main PC lists workstations as **Connected** or **OFFLINE**. A workstation's top bar turns green when it is connected.

Choose **Everyone who logs in** during setup for a shared clinic computer. Choose **Only me** when GP Guard should belong to one Windows account. Shared data is stored in `C:\ProgramData\GPGuard\data`; per-user data is stored in `%LOCALAPPDATA%\GPGuard`.
