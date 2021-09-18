#### How to convert a Windows server evaluation license for free
#### Borrowed from [this awesome webpage.](https://msguides.com/convert-windows-server-evaluation)

-  determine which version of windows server is in use: `dism /online /get-currentedition`
-  Convert your Windows to the edition you want. Execute the command below to start a conversion process:
-  `dism /online /set-edition:<-Edition-> /productkey:X-X-X-X-X /accepteula`
-  I just want to make a conversion, not an upgrade so the above command is.
-  `dism /online /set-edition:serverstandard /productkey:N69G4-B89J2-4G8F4-WWYCC-J464C /accepteula`
-  Restart your machine then check the properties again. After completing the 3rd step, you will be asked to reboot your server. Just answer ‘Y’.
-  All done! Now you can back to [this post](https://msguides.com/windows-server) then try activating your Windows again.


















Generic Volume License Keys (GVLK)
In the tables that follow, you will find the GVLKs for each version and edition of Windows. LTSC is Long-Term Servicing Channel, while LTSB is Long-Term Servicing Branch.

Windows Server (LTSC versions)
Windows Server 2022
WINDOWS SERVER 2022
Operating system edition	KMS Client Product Key
Windows Server 2022 Datacenter	WX4NM-KYWYW-QJJR4-XV3QB-6VM33
Windows Server 2022 Standard	VDYBN-27WPP-V4HQT-9VMD4-VMK7H
Windows Server 2019
WINDOWS SERVER 2019
Operating system edition	KMS Client Product Key
Windows Server 2019 Datacenter	WMDGN-G9PQG-XVVXX-R3X43-63DFG
Windows Server 2019 Standard	N69G4-B89J2-4G8F4-WWYCC-J464C
Windows Server 2019 Essentials	WVDHN-86M7X-466P6-VHXV7-YY726
Windows Server 2016
WINDOWS SERVER 2016
Operating system edition	KMS Client Product Key
Windows Server 2016 Datacenter	CB7KF-BWN84-R7R2Y-793K2-8XDDG
Windows Server 2016 Standard	WC2BQ-8NRM3-FDDYY-2BFGV-KHKQY
Windows Server 2016 Essentials	JCKRF-N37P4-C2D82-9YXRT-4M63B
Windows Server (Semi-Annual Channel versions)
Windows Server, versions 20H2, 2004, 1909, 1903, and 1809
WINDOWS SERVER, VERSIONS 20H2, 2004, 1909, 1903, AND 1809
Operating system edition	KMS Client Product Key
Windows Server Datacenter	6NMRW-2C8FM-D24W7-TQWMY-CWH2D
Windows Server Standard	N2KJX-J94YW-TQVFB-DG9YT-724CC

