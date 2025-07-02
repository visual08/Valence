## Valence Guide & Troubleshooting

Welcome to the Valence! This guide will help you get started with using the application and provide solutions for common issues you might encounter.

## 1. Getting Started: How to Use Valence
**1.1. Downloading the Application**
Go to the Valence App GitHub Readme and press the download link

Look for the latest release (e.g., v1.0.0).

**1.2. Extracting the Application**
This step is crucial for avoiding permission issues!

Make sure to extract the .zip, if you are using windows default extraction method then choose Extract All...

When prompted for a destination, choose a user-writable location such as:

Your Desktop

Your Documents folder

Your Downloads folder

A custom folder directly under your user profile

Click "Extract."

**1.3. Running the Application**
Navigate to the folder where you extracted the application (e.g., C:\Users\YourUsername\Desktop\Valence).

Right click Valence.exe and Run As Administrator **IMPORTANT**

**1.4. Basic UI Overview**
Editor Area: This is the main section where you will write or view your Lua scripts.

Console Box: Located at the bottom, this displays logs, errors, and status messages from the application.

Buttons:

Execute: Runs the script currently in the editor.

Clear: Clears the content of the editor.

Load: Opens a file dialog to load an existing Lua script into the editor.

Save: Opens a file dialog to save the current editor content as a Lua script.

Attach: Attempts to inject into the running Roblox process.

Options: Opens a separate window for application settings (e.g., Auto-Inject, Music).

Minimize/Exit: Standard window controls.

Roblox Status Indicator: A colored circle (usually green for connected, red for disconnected) indicating the injection status.

**1.5. Loading, Saving, and Executing Scripts**
To load a script: Click the "Load" button, navigate to your .lua file, and open it.

To save a script: Write your script in the editor, then click the "Save" button. Choose a location (the Scripts folder in the application directory is a good default).

To execute a script: After loading or writing your script, ensure Roblox is running, then click the "Execute" button. Check the Console Box for feedback.

**1.6. Attaching to Roblox**
Ensure the Roblox game client (RobloxPlayerBeta.exe) is running.

Click the "Attach" button.

The Roblox Status indicator should turn green, and a "Injected into Roblox" message should appear in the Console Box upon success.

If "Auto-Inject" is enabled in the Options, Valence will attempt to attach automatically when Roblox launches.

## 2. Troubleshooting Common Issues
**2.1. "Access to the path '...' is denied." Error**
Problem: You see an error message like "Access to the path 'C:\Users\UsernameHere\source\repos\Valence\Valence\bin\x64\Release\Bin\current_version.txt' is denied." or similar, preventing the app from running or updating.

Reason: Windows security features (User Account Control - UAC) prevent applications from writing data directly into program folders (like Program Files or even certain subfolders of your user profile if they are treated as application installation locations). Your application tries to save version information or other data in these restricted areas.

Solution:

Extract the ZIP to a user-writable location. Do NOT extract or run the application from Program Files, Program Files (x86), or directly from a Downloads folder that might have restrictive permissions.

Recommended locations: Your Desktop, your Documents folder, or a custom folder you create directly under C:\Users\YourUsername\.

Re-extract the entire application to one of these recommended locations.

**2.3. Application Not Launching / Crashing on Startup**
Problem: Valence.exe doesn't open, or crashes immediately.

Possible Reasons & Solutions:

Missing .NET Framework: Valence requires a specific version of the .NET Framework (likely .NET Framework 4.8). Ensure it's installed on your system. Windows Update usually handles this, but you might need to install it manually.

Missing WebView2 Runtime: Valence uses WebView2 for its editor. This runtime needs to be installed. It's often bundled with Windows, but if not, you can download the Evergreen Bootstrapper from the Microsoft WebView2 website.

Corrupted Files: Re-extract the application from the .zip to a new, clean directory.

Antivirus Interference: Your antivirus software might be blocking Valence.exe or its components. Temporarily disable your antivirus (at your own risk) to test, or add an exception for the Valence application folder.

**2.4. Injection / Attach Fails**
Problem: Clicking "Attach" doesn't work, or the Roblox Status remains red.

Possible Reasons & Solutions:

Roblox Not Running: Ensure the Roblox game client (RobloxPlayerBeta.exe) is actively running before attempting to attach.

Antivirus/Firewall Blocking: Your security software might be preventing the injection process. Temporarily disable it to test, or add exceptions for Valence.exe and RobloxPlayerBeta.exe.

Permissions: Ensure Valence is extracted to a user-writable location (see 2.1).

The executor API may be down, please wait for an update.

**2.5. Auto-Update Issues**
Problem: The application doesn't auto-update, or reports an error during update.

Possible Reasons & Solutions:

No Internet Connection: Ensure your device has an active internet connection.

GitHub Access Blocked: Your firewall, proxy, or ISP might be blocking access to GitHub's raw content (where update information is hosted).

Permission to Write: The application needs write access to its own Bin folder to update QuorumAPI.dll. Ensure it's extracted to a user-writable location (see 2.1).

Incorrect Update Link: The update link might be broken or outdated. This would require a new release from the developer.

**2.6. Music Playback Issues**
Problem: Music doesn't play or stops unexpectedly.

Possible Reasons & Solutions:

No Internet Connection: Music is streamed/downloaded from a URL.

Firewall/Antivirus Blocking: Your security software might be blocking the music download.

Temporary File Access: The application downloads music to a temporary folder. Ensure it has write access to C:\Users\YourUsername\AppData\Local\Temp\ValenceMusic.

Corrupted Audio File: The downloaded MP3 might be corrupted.

Media Player Component: Ensure Windows Media Player components are functional on your system, as the MediaPlayer class relies on them.

## 3. Need More Help?
If you've tried the troubleshooting steps and are still experiencing issues, please report them to the discord support channel

A detailed description of the problem.

Any error messages you see (screenshots are helpful!).

Steps to reproduce the issue.

Your operating system (e.g., Windows 10, Windows 11).

Whether you extracted the app to a recommended location.
