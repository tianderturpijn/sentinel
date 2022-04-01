###Create a new incident

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftianderturpijn%2Fsentinel%2Fmaster%2FARM%2FCreateNewIncident.json" target="_blank"><img src="https://aka.ms/deploytoazurebutton"/>
</a>

**Test with PowerShell:**
```powershell
$body = @{

    incidentTitle = "My new incident"
    incidentDescription = "My description"
}
$body = $body | ConvertTo-Json
$Params = @{
    Method = "PUT"
    Uri = "<your HTTP Trigger URL>"
    Body = $body
    ContentType = "application/json"
}
Invoke-RestMethod @Params
```
