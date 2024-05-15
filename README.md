# DNS-Zone

```
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
