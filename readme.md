![GP Guard - urgent assistance alerts](https://github.com/ChristopherDalziel/gp-guard/raw/main/assets/readme-header.svg)

# GP Guard

Local-network urgent assistance alerts for GP clinics running Windows 10 or 11 (64-bit).

Every computer runs the same application and communicates directly with the other computers on the clinic network. This peer-to-peer design avoids a single point of failure.

One computer is designated as the **Main PC**, which manages the software licence. All other computers operate as Workstations.

GP Guard requires no user accounts, cloud services or database.

## For Clinic Staff

### Installation and Setup

1. Run `GPGuardSetup.exe` on each computer as an administrator.
2. Allow GP Guard through the Windows Firewall prompt and leave **Start GP Guard now** selected.
3. On one computer, select **Main PC**, enter a room name (for example, `Reception`) and note the 12-character pairing code.
4. On the Main PC, create a licence request and send us the pairing code. We will return a licence code. In the meantime, Trial Mode allows you to use the software.
5. On every other computer, select **Workstation**, enter a room name and provide the same pairing code.

Workstations have the same alert functionality as the Main PC but do not manage the licence.

Once setup is complete, each computer displays the connection status of the other computers as **Connected** or **OFFLINE**. The top bar turns green when the computer is connected to at least one other computer.

**Choose the appropriate installation scope:**

- **Everyone who logs in:** Recommended for shared clinic computers.
- **Only me:** Use when GP Guard should be available only to the current Windows account.

Shared data is stored in `C:\ProgramData\GPGuard\data`. Per-user data is stored in `%LOCALAPPDATA%\GPGuard`.

## Everyday Use

### Sending an Alert

An alert can be triggered in three ways:

- Click **SEND ALERT**.
- Press `Ctrl+Shift+1`.
- Use a supported controller or keyboard-style USB button.

The sending computer remains quiet and displays whether the alert has been confirmed.

All other computers will:

- Display **URGENT ASSISTANCE REQUESTED**.
- Identify the room where the alert originated.
- Bring the GP Guard window to the foreground.
- Sound the alarm.

### Acknowledging and Ending Alerts

On a computer receiving an alert, click **Silence** to stop its local alarm and notify the other computers that the alert has been heard.

Once an alert has been heard by a computer, its user can select **End alert for everyone** and confirm the action.

Any computer can end an alert. This ensures an alarm cannot remain active simply because the caller's computer is locked, unavailable or has crashed.

### Cancelling an Alert

The caller can mark themselves safe using the cancellation hotkey (`Ctrl+Shift+2` by default).

This action does not display anything on the caller's screen. Instead, the other computers display a **marked safe by caller** banner until a second computer confirms the cancellation.

This additional confirmation helps protect against situations where a caller may have been forced to cancel an alert.

Test alerts end immediately.

### Alert Handling and History

- Alerts received more than 10 minutes after they were originally raised are recorded in the history but do not sound.
- Alerts never automatically escalate.
- Test alerts are recorded in the history and displayed in blue.
- Real alerts always take priority over test alerts.

## Daily Testing

We recommend testing GP Guard every day.

1. Select **Run a test every day**.
2. Press the alert button to trigger a test alert.
3. Confirm that the other computers receive and display the test alert.

To check the alarm sound, go to **Settings → Test alarm sound**.

Before testing, ensure speakers are connected, unmuted and set above 5% volume.

## Closing and Exiting GP Guard

Closing the GP Guard window minimises the application to the Windows system tray. The application continues running in the background.

To completely stop GP Guard:

1. Open **Settings**.
2. Select **Quit GP Guard**.
3. Confirm the action when prompted.

**Important:** Quit GP Guard before shutting down a computer. This prevents other computers from incorrectly reporting it as an unexpected outage.
