
```
cd (Get-AppxPackage | where Name -like 'Microsoft. DesktopAppInstaller') . InstallLocation 

. \winget.exe install -- id Python. PythonInstallManager -- source winget -h -- force 
 
```

```
#Makefile binary (add to GIT) 
Start-Process powershell -Verb RunAs 
$Pfolder = "c:\new" 
New-Item -Path $Pfolder -ItemType Directory -Force 

  

  if (Test-Path $Pfolder) { 
  cd $Pfolder 
  $url = "https://netix.dl.sourceforge.net/project/ezwinports/make-4.4.1-without-guile-w32-bin.zip?viasf=1" 
  $zip = "make-4.4.1-without-guile-w32-bin.zip" 
  $dest = "make-4.4.1" 
  Invoke-WebRequest -Uri $url -OutFile $zip 
  Expand-Archive -Path $zip -DestinationPath $dest 
  cd $dest 
  
    
  
      $binPath = "C:\Program Files\Git\mingw64" 
      if (Test-Path $binPath) { 
      Copy-Item ".\*" $binPath -Recurse -Force 
      } 
  
  }
```
