## As the title says
regedit
HKEY_LOCAL_MACHINE
SOFTWARE
MICROSOFT
WINDOWS
Current version
Policies
System
donstdisplaylastusername (on right side) 
Right click ==> click Modify ==> Change Hex value to 1 ==> click OK ==> right click on empty space below current list of options ==> 
Select New ==> DWORD 32 bit value ==> Set new registry item name as DontDisplayLockedUserID
Then right click this new entry ==> Click Modify ==> Change Hex value to 3 ==> click OK
Then sign out of your user account to go back to the main login screen and check if this worked

