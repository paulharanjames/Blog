
For one of our customers, we need to develop feed from Genesys Infomart for MI reporting and hence, we developed tool for this functionality. While this worked perfectly fine on development machine & testing environment, it failed with error &#8216;Could not load file or assembly **&#8216;system.core , Version=2.0.5.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e**, Retargetable=Yes&#8217; or one of its dependencies. The given assembly name or codebase was invalid. (Exception from HRESULT: 0x80131047) &#8216;

It is weird as I am using .NET Framework 4.0 for this application which included system.core version 4.0 :-(. It turns out that system.core version 2.0.5 is part of portable libraries and **NET framework 4.0 need to be patched.**

## Solution

* * *

## 

To fix this issue, we need to apply .NET framework update [KB2468871](http://support.microsoft.com/kb/2468871 "KB2468871") to the server, which includes support for portable libraries.

As it was production server, it wasn&#8217;t receiving windows update and once we applied update [KB2468871](http://support.microsoft.com/kb/2468871 "KB2468871"), it worked perfectly.