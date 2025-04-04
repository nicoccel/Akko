# Vendetta x Windows

MUPP Sadfriendd

## Info

### Strange file

- `pagefile.sys`  
    a system file in Windows operating systems that serves as the virtual memory paging file.  
    It's used to store data that's not currently being used by the system, allowing the operating system to free up physical RAM for other tasks.

## Security

- Disable policy restriction of script
    Run PowerShell with Administrator
    `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`
    After press Y

## Clean file

### Random command

```txt
del /q /f /s %temp%\*
ipconfig /flushdns
DISM /Online /Cleanup-Image /StartComponentCleanup
```
