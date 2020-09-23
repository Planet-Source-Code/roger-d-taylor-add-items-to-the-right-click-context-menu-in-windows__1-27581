<div align="center">

## Add Items to the right Click Context Menu in Windows


</div>

### Description

Ever wanted to add an item to the right click context menu that you get in windows. you know, the one that you get if you rigth click on a file !! well heres how to do it.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Roger D Taylor](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/roger-d-taylor.md)
**Level**          |Beginner
**User Rating**    |4.5 (27 globes from 6 users)
**Compatibility**  |VB 6\.0
**Category**       |[Registry](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/registry__1-36.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/roger-d-taylor-add-items-to-the-right-click-context-menu-in-windows__1-27581/archive/master.zip)





### Source Code

```
Ok, now follow this and you will have no problems
open regedit
browse to the following key
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\*\shell\
you should notice that there should be a key called something like open2 with a subkey of command.
create a new 'open' key, but increment the number that follows it ... for example 'open3' or 'open4'
you should now have something like this
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\*\shell\open3\
Set this keys default value to the name of the application that you want to use. for example i will create one called 'note pad'
Now create a subkey to the 'open' key that you just created. call it 'command'. set the default value of the 'command' key to the path and file name of the application that you want to open.
you should have something like this as the path to the key
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\*\shell\open4\command\
if you want the application to be able to recieve files ... simple place a space and '%1' following the .exe. you should have something like this.
'c:\winnt\system32\notepad.exe %1'
Close the registry, go to your desktop and try it out !!
```

