---
title: SkipAdministratorProfileRemoval
description: Use SkipAdministratorProfileRemoval to skip removal of the administrator profile when in VM mode.
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: C4CD25BC-A012-4237-B5AD-F62ED5F654F5
ms.prod: W10
ms.mktglfcycl: deploy
ms.sitesec: msdn
ms.author: alhopper
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# SkipAdministratorProfileRemoval


Use `SkipAdministratorProfileRemoval` to skip removal of the administrator profile when in VM mode.

**Note**  You must specify /mode:vm during sysprep to fully enable this setting.

 

## Values


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>false</p></td>
<td><p>Does not skip removal of the administrator profile when in VM mode.</p>
<p>This is the default OS value.</p></td>
</tr>
<tr class="even">
<td><p>true</p></td>
<td><p>Skips removal of the administrator profile when in VM mode.</p></td>
</tr>
</tbody>
</table>

 

## Valid Configuration Passes


oobeSystem

## Parent Hierarchy


[Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md) | [OOBE](microsoft-windows-shell-setup-oobe.md) | [VMModeOptimizations](microsoft-windows-shell-setup-oobe-vmmodeoptimizations.md) | **SkipAdministratorProfileRemoval**

## Applies To


Windows 10 for desktop editions (Home, Pro, Enterprise, and Education)

For a list of the Windows editions and architectures that this component supports, see [Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md).

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_unattend\p_unattend%5D:%20SkipAdministratorProfileRemoval%20%20RELEASE:%20%2810/3/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




