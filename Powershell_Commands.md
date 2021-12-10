### Powershell commands


#### Creating new files
$null > textfile.txt
$null | sc textfile.txt


ps> Get-Process | Format-Table Name,@{n=‘Virtual Memory’;e={$_.VM/1MB};formatString=‘N2’} -AutoSize

#### Set staic IP address
- List all network adapters available: `Get-NetAdapter -Name *`
- Remove any IP address configuration from the network adapter: `Remove-NetIPAddress -InterfaceIndex 22 -Confirm:$false`
- Remove any DNS configuration from the network adapter: `Remove-NetRoute -InterfaceIndex 22 -Confirm:$false`
- Configure a static IP address on a network interface: `New-NetIPAddress -InterfaceIndex 22 -IPAddress 10.10.10.2 -AddressFamily IPv4 -PrefixLength 24 -DefaultGateway 10.10.10.1`
- Configure the DNS servers of a network adapter: `Set-DnsClientServerAddress -InterfaceIndex 22 -ServerAddresses ("8.8.8.8","8.8.4.4")`
- Verify the DNS servers configured on a network interface: `Get-DnsClientServerAddress -InterfaceIndex 22`
- Verify the configuration of a network interface: `Get-NetIPConfiguration -InterfaceIndex 22 -Detailed`
