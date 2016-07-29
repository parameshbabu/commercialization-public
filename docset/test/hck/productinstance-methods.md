---
author: joshbax-msft
title: ProductInstance Methods
description: ProductInstance Methods
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 87901aef-3c18-4202-9045-a29887cf5f6e
---

# ProductInstance Methods


The following table lists the methods exposed by the **ProductInstance** type.

## Public Methods


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CanCreateTarget</p></td>
<td><p>This method determines if a target can be created from <strong>TargetData</strong> object provided. The target is not added to the product instance.</p></td>
</tr>
<tr class="even">
<td><p>CreateTarget</p></td>
<td><p>This method creates a target from <strong>TargetData</strong>, and adds it to this product instance.</p></td>
</tr>
<tr class="odd">
<td><p>CreateTargetFamily</p></td>
<td><p>This method creates and adds a target family to the existing product instance, using the supplied <strong>DeviceFamily</strong>.</p></td>
</tr>
<tr class="even">
<td><p>DeleteTarget</p></td>
<td><p>Overloaded.</p></td>
</tr>
<tr class="odd">
<td><p>DeleteTargetFamily</p></td>
<td><p>This method deletes a target family.</p></td>
</tr>
<tr class="even">
<td><p>Equals</p></td>
<td><p>(Inherited from <strong>Object</strong>)</p></td>
</tr>
<tr class="odd">
<td><p>FindTargetFromContainer</p></td>
<td><p>This method creates a list of targets containing the specific container ID. There are two special container Ids to consider. The first is the system containerId (00000000-0000-0000-ffff-ffffffffffff). If this is passed in, then the method will return a list with just a single &quot;system&quot; target. The second is a zero-decorated GUID (00000000-0000-0000-0000-000000000000). This is an invalid GUID.</p></td>
</tr>
<tr class="even">
<td><p>FindTargetFromDeviceFamily</p></td>
<td><p>This method finds a list of target data that matches the family specified.</p></td>
</tr>
<tr class="odd">
<td><p>FindTargetFromId</p></td>
<td><p>Overloaded.</p></td>
</tr>
<tr class="even">
<td><p>FindTargetFromSystem</p></td>
<td><p>Overloaded.</p></td>
</tr>
<tr class="odd">
<td><p>GetFeatures</p></td>
<td><p>This method retrieves a collection of features detected for this product instance.</p></td>
</tr>
<tr class="even">
<td><p>GetHashCode</p></td>
<td><p>Overridden. This method creates a unique hash code for a <strong>MachineSet</strong> object.</p></td>
</tr>
<tr class="odd">
<td><p>GetMachines</p></td>
<td><p>This method retrieves all of the machines in a Product Instance. Machines are associated with Product Instances via their test targets. To add or remove a machine, you must add or remove the associated test target.</p></td>
</tr>
<tr class="even">
<td><p>GetProductTypes</p></td>
<td><p>This method attempts to detect product types this product instance belongs to.</p></td>
</tr>
<tr class="odd">
<td><p>GetTargetFamilies</p></td>
<td><p>This method retrieves an enumerable list of TargetFamilies that expose the product to the system.</p></td>
</tr>
<tr class="even">
<td><p>GetTargets</p></td>
<td><p>This method retrieves an enumerable list of targets that expose the product to the system.</p></td>
</tr>
<tr class="odd">
<td><p>GetTests</p></td>
<td><p>This method retrieves all tests needed for this node.</p></td>
</tr>
<tr class="even">
<td><p>GetType</p></td>
<td><p>(Inherited from Object)</p></td>
</tr>
<tr class="odd">
<td><p>QueueTest</p></td>
<td><p>Overloaded.</p></td>
</tr>
<tr class="even">
<td><p>SetCommonParameters</p></td>
<td><p>This method sets all of the parameters with a given name to the same value for all child jobs.</p></td>
</tr>
<tr class="odd">
<td><p>ToString</p></td>
<td><p>(Inherited from Object)</p></td>
</tr>
</tbody>
</table>

 

## Protected Methods


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Finalize</p></td>
<td><p>(Inherited from <strong>Object</strong>)</p></td>
</tr>
<tr class="even">
<td><p>GetAllRelevantMachinesFromPool</p></td>
<td><p>This method retrieves all the machines in the pool specified including child pools with a match of operating system platform from the product instance.</p></td>
</tr>
<tr class="odd">
<td><p>GetPlatform</p></td>
<td><p>This method retrieve the platform assigned to this product instance.</p></td>
</tr>
<tr class="even">
<td><p>MemberwiseClone</p></td>
<td><p>(Inherited from <strong>Object</strong>)</p></td>
</tr>
</tbody>
</table>

 

 

 





