#### How to enable windows terminal as permanent administrator
#### Borrowed from [this awesome webpage.](https://pureinfotech.com/always-run-windows-terminal-administrator-windows-10/)
- Right-click the Windows 10 Desktop.
- Select the New submenu and choose the Shortcut option.
- In the path field, type the following path:
`%LocalAppData%\Microsoft\WindowsApps\wt.exe`
- Click the Next button.
- Confirm a name for the shortcut – for example, Windows Terminal.
- Click the Finish button.
- Right-click the newly created shortcut and select the Properties option.
- Click the Shortcut tab.
- Click the Advanced button
- Check the Run as administrator option for the Windows Terminal shortcut.
- Click the OK button.
- (Optional) Click the Change Icon button.
- In the Look for icons in this file field, type the following path and press Enter:
`%systemroot%\system32\shell32.dll`
- Quick tip: If you want to use the actual Windows Terminal icon, you can download it from [this location.](https://raw.githubusercontent.com/microsoft/terminal/master/res/terminal.ico)
- Select an icon you want to use.
- Click the OK button.
- Click the Apply button.
- Click the OK button.
- 
Once you complete the steps, you can double-click the shortcut to open always open the Windows Terminal as administrator.

If you want, you could also drag the shortcut to the taskbar to pin it. Or you can right-click the shortcut and select the Pin to Start option to run the app as an administrator from the Start menu.
