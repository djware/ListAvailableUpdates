# ListAvailableUpdates
Powershell script that will list available Windows Updates

This Powershell script which requires no modules will list pending Windows Updates for your device. 

```
$UpdateSession = New-Object -ComObject Microsoft.Update.Session
$UpdateSearcher = $UpdateSession.CreateUpdateSearcher()
$SearchResult = $UpdateSearcher.Search("IsInstalled=0")
foreach ($Update in $SearchResult.Updates) {
    $Update.Title
}

```
