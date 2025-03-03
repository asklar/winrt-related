---
description: Defines the root element of an app package manifest (Windows 10).
Search.Product: eADQiWindows 10XVcnh
title: Package (Windows 10)
ms.assetid: ea0f5af0-8191-4ce0-9594-c647f800bd53


keywords: windows 10, uwp, schema, package manifest


ms.topic: reference
ms.date: 04/05/2017
---

# Package (Windows 10)


Defines the root element of an app package manifest. The manifest describes the structure and capabilities of the software to the system.

## Element hierarchy


**&lt;Package&gt;**
## Syntax

``` syntax
<Package IgnorableNamespaces? = A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end. >

  <!-- Child elements -->
  ( Identity
  & mp:PhoneIdentity?
  & Properties
  & Resources
  & Dependencies
  & Capabilities?
  & Extensions?
  & Applications?
  )

</Package>
```

### Key

`?`   optional (zero or one)
`&`   interleave connector (may occur in any order)

## Attributes and Elements


### Attributes

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Description</th>
<th>Data type</th>
<th>Required</th>
<th>Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>IgnorableNamespaces</strong></td>
<td><p>Declares namespaces used in the manifest that should be ignored. Ignored namespace elements are not validated and should be considered untrusted. Multiple namespaces are specified with a space between each namespace.</p></td>
<td>A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end.</td>
<td>No</td>
<td></td>
</tr>
</tbody>
</table>

 

### Child Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Child Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-applications.md">Applications</a> </td>
<td><p>Represents one or more apps that comprise the package.</p></td>
</tr>
<tr class="even">
<td><a href="element-capabilities.md">Capabilities</a> </td>
<td><p>Declares the access to protected user resources that the package requires.</p></td>
</tr>
<tr class="odd">
<td><a href="element-dependencies.md">Dependencies</a> </td>
<td><p>Declares other packages that a package depends on to complete its software.</p></td>
</tr>
<tr class="even">
<td><a href="element-extensions.md">Extensions (type: CT_PackageExtensions)</a> </td>
<td><p>Defines one or more extensibility points for the package.</p></td>
</tr>
<tr class="odd">
<td><a href="element-identity.md">Identity</a> </td>
<td><p>Defines a globally unique identifier for a package. A package identity is represented as a tuple of attributes of the package.</p></td>
</tr>
<tr class="even">
<td><a href="element-properties.md">Properties</a> </td>
<td><p>Defines additional metadata about the package including attributes that describe how the package appears to users.</p>
<div class="alert">
<strong>Note</strong>  You may get an error if the manifest elements DisplayName or Description contain characters disallowed by the Windows firewall; namely “|” and “all”, due to which Windows fails to create the AppContainer profile for the package . Use this reference for <a href="/windows/win32/appxpkg/troubleshooting">troubleshooting</a> if you get an error.
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td><a href="element-resources.md">Resources</a> </td>
<td><p>Declares languages for the resources that the package contains. Every package must declare at least one language for resources. The scale and DirectX feature level attributes are common for all resources in the package.</p></td>
</tr>
<tr class="even">
<td><a href="element-mp-phoneidentity.md">mp:PhoneIdentity</a> </td>
<td><p>If your app is an update to an app previously made available on Windows Phone, ensure that this element matches what is in the app manifest of your previous app. Use the same GUIDs that were assigned to the app by the Store. This ensures that users of your app who are upgrading to Windows 10 will receive your new app as an update, and not as a duplicate.</p></td>
</tr>
</tbody>
</table>

 

### Parent Elements

This outermost (document) element may not be contained by any other elements.

## Requirements

|   | Value |
|--|--|
| **Namespace** | `http://schemas.microsoft.com/appx/manifest/foundation/windows10` |


 

 
