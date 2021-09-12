ps> Get-Process | Format-Table,@{n='Virtual Memory';e={$_.VM/1MB};formatSting='N2'} -AutoSize
