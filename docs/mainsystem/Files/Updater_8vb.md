---
title: C:/Users/rfranks/Documents/Development/EHMR/SignallingSystem/EHMR Signalling System/Misc/Updater.vb

---

# C:/Users/rfranks/Documents/Development/EHMR/SignallingSystem/EHMR Signalling System/Misc/Updater.vb



## Functions

|                | Name           |
| -------------- | -------------- |
| [void](/SignallingSystem-doc/mainsystem/Files/SerialPixelLeds_8vb/#variable-void) | **[UpdateNow](/SignallingSystem-doc/mainsystem/Files/Updater_8vb/#function-updatenow)**() |


## Functions Documentation

### function UpdateNow

```csharp
void UpdateNow()
```




## Source code

```csharp
Module Updater
    Public Sub UpdateNow()
        If Main.HasUpdate = True Then Errors.NewError("Performing software update!")
        Dim p As New ProcessStartInfo
        p.FileName = ("C:\SignallingSystem\Updater\Signalling-Updater.exe")
        p.WorkingDirectory = "C:\SignllaingSystem\Updater"
        p.UseShellExecute = True
        p.WindowStyle = ProcessWindowStyle.Normal
        Dim proc As Process = Process.Start(p)
    End Sub
End Module
```


-------------------------------

Updated on 2022-11-18 at 16:49:21 +0000