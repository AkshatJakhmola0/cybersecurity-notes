wmic
wmic os get Caption,Version,BuildNumber
wmic computersystem get Manufacturer,Model,Name
wmic bios get Manufacturer,SerialNumber,Version
wmic cpu get Name,NumberOfCores,MaxClockSpeed
wmic memorychip get Capacity,Speed,Manufacturer
wmic logicaldisk get DeviceID,FileSystem,Size,FreeSpace
wmic diskdrive get Model,Size,InterfaceType
wmic useraccount get Name,SID
wmic process get Name,ProcessId
wmic nicconfig get Description,IPAddress
wmic /?
