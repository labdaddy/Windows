### Powershell commands


### Creating new files
$null > textfile.txt
$null | sc textfile.txt


ps> Get-Process | Format-Table Name,@{n=‘Virtual Memory’;e={$_.VM/1MB};formatString=‘N2’} -AutoSize
