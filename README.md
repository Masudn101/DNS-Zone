 Below is a PowerShell script to create a primary DNS zone on a Windows Server:

```powershell
# Define parameters for DNS zone
$ZoneName = "example.com"
$ZoneFile = "$ZoneName.dns"
$ZoneType = "Primary"
$DynamicUpdate = "Secure"

# Import DNS module
Import-Module DNSServer

# Create primary DNS zone
Add-DnsServerPrimaryZone -Name $ZoneName -ZoneFile $ZoneFile -ZoneType $ZoneType -DynamicUpdate $DynamicUpdate

# Verify DNS zone creation
Get-DnsServerZone -Name $ZoneName
```

This script defines parameters such as the zone name, zone file name, zone type, and dynamic update setting. Then it imports the DNS module and creates a primary DNS zone with the specified parameters.

Make sure to replace the placeholders (`$ZoneName`, `$ZoneFile`, `$ZoneType`, and `$DynamicUpdate`) with your actual values.

Save the script with a `.ps1` extension and execute it on your Windows Server with appropriate administrative privileges.
