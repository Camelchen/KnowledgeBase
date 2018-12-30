#### invoke commands
* CURL
> In PowerShell `curl` is a built in alias to `Invoke-WebRequest` cmdlet, so use `curl.exe` instead of `curl`.
```powershell
curl.exe -X POST http://192.168.1.230:8079/job/RoutineTask/job/ColdLoading/build
```
