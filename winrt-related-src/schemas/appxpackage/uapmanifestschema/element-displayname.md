---
description: A friendly name that can be displayed to users (Windows 10).
Search.Product: eADQiWindows 10XVcnh
title: DisplayName (Windows 10)
ms.assetid: e5d9a0b1-73cf-4c17-90c8-1a0cb57779dd


keywords: windows 10, uwp, schema, package manifest


ms.topic: reference
ms.date: 04/05/2017
---

# DisplayName (Windows 10)


A friendly name that can be displayed to users.

## Element hierarchy

<dl>
<dt><a href="element-package.md">&lt;Package&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-properties.md">&lt;Properties&gt;</a></dt>
<dd><b>&lt;DisplayName&gt;</b></dd>
</dl>
</dd>
</dl>

## Syntax

``` syntax
<DisplayName>

  A string between 1 and 256 characters in length. This string is localizable. 

</DisplayName>
```

## Attributes and Elements


### Attributes

None.

### Child Elements

None.

### Parent Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-properties.md">Properties</a> </td>
<td><p>Defines additional metadata about the package including attributes that describe how the package appears to users.</p>
<div class="alert">
<strong>Note</strong>  You may get an error if the manifest elements DisplayName or Description contain characters disallowed by the Windows firewall; namely “|” and “all”, due to which Windows fails to create the AppContainer profile for the package . Use this reference for <a href="/windows/win32/appxpkg/troubleshooting">troubleshooting</a> if you get an error.
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

## Remarks

This string is localizable. 

## Requirements

|   | Value  |
|--|--|
| **Namespace** | `http://schemas.microsoft.com/appx/manifest/foundation/windows10` |


 

 
