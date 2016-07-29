---
author: joshbax-msft
title: Bluetooth - Downlevel - Bluetooth 2.1 Logo Tests (Windows 8)
description: Bluetooth - Downlevel - Bluetooth 2.1 Logo Tests (Windows 8)
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 13fef824-9fd1-4c28-b465-f7f6b29658c4
---

# Bluetooth - Downlevel - Bluetooth 2.1 Logo Tests (Windows 8)


This automated test verifies that mandatory Bluetooth 2.1 features are implemented, such as Secure Simple Pairing (SSP) and Extended Inquiry Response (EIR). Logo tests verify the previous features by running different combinations of tests on selected Bluetooth hardware.

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.BusController.Bluetooth.Base.4LeSpecification Device.BusController.Bluetooth.Base.SupportsBluetooth21AndEdr</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows RT (ARM-based) Windows 8 (x64) Windows 8 (x86)</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~30 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Certification Functional</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Automated</p></td>
</tr>
</tbody>
</table>

 

## Running the test


Before you run the test, complete the test setup as described in the test requirements: [Bluetooth Controller Testing Prerequisites](bluetooth-controller-testing-prerequisites.md).

-   This test requires two test computers (one acts as Primary, the other Secondary). The test computers must have the same operating system and have a Bluetooth 2.1 compliant radio. The primary test computer must have the radio being certified for logo (Device Under Test).

-   The Bluetooth radio must use the Microsoft Bluetooth Driver Stack for testing.

## Troubleshooting


For troubleshooting information, see [Troubleshooting Bus Controller Testing](troubleshooting-bus-controller-testing.md).

## More information


Tests are copied locally to the WTTJobsWorking directory and logs are copied to the default Logs server. This test completes the following individual test cases:

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
<th>Test ID</th>
<th>Title</th>
<th>Description</th>
<th>Procedures</th>
<th>Timeout (seconds)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>VerifyAuthForAuthMethOOB</p></td>
<td><p>Verify that authentication succeeds for authentication method OOB</p></td>
<td><p>Verify authentication procedure when out-of-band data is present</p></td>
<td><p>Master initiates the authentication. Master uses subordinate OOB data for authentication. Verify callback function registered should not be called. Verify authentication successes for authentication method OOB</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyEventLogNotGenForDebugEnabled</p></td>
<td><p>Verify event log message is not generated on debug system when both of the system is in debug enabled mode</p></td>
<td><p>Verify debug mode supported by BT radio</p></td>
<td><p>Master and subordinate registers for authentication. Master and subordinate is in debug mode and initiates the authentication. Verify that authentication succeeds and on no event log is generated on both computers.</p></td>
<td><p>120</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapMxSx</p></td>
<td><p>Verify authentication procedure for various authentication method as defined in BT specification when different IO capability is specified by system</p></td>
<td><p>Possible IO capabilities are as follows:</p>
<ul>
<li><p>DisplayOnly - 0</p></li>
<li><p>DisplayYesNo - 1</p></li>
<li><p>KeyBoardOnly - 2</p></li>
<li><p>NoInputNoOutput - 3</p></li>
</ul></td>
<td><p>In Test names M stands for Master Device IO capability and S stands for Subordinate Device IO Capability</p></td>
<td><p>[This content isn't available yet.]</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM0S0</p></td>
<td><p>Verify authentication successes for authentication method LEGACY when master and subordinate has device capability set to NoInputNoOutput</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description.</p>
<p>Verify authentication successes for IOCapabilities DisplayOnly for master and subordinate</p></td>
<td><p>Master and subordinate registers for authentication. Master initiates the authentication and Subordinate accepts authentication request and sent positive response. Verify that authentication succeed</p>
<div class="alert">
<strong>Warning</strong>  
<p>Make sure that the correct configuration test case is executed before setting I/O capabilities</p>
</div>
<div>
 
</div></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM0S1</p></td>
<td><p>Verify authentication successes for IOCapabilities DisplayOnly for master and DisplayYesNo for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities DisplayOnly for master and DisplayYesNo for subordinate</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities DisplayOnly on master and DisplayYesNo on Subordinate. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeed</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM0S2</p></td>
<td><p>Verify authentication successes for IO capabilities DisplayOnly for master and KeyboardOnly for subordinate.</p>
<div class="alert">
<strong>Warning</strong>  
<p>See VerifyAuthForIOCapMxSx Tests Description</p>
</div>
<div>
 
</div></td>
<td><p>Verify authentication successes for IOCapabilities DisplayOnly for master and KeyBoardOnly for subordinate</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities display only on master and Display YesNo on Subordinate. Master initiates the authentication, Subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM0S3</p></td>
<td><p>Verify authentication successes for IO capabilities DisplayOnly for master and NoInputNoOutput for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description Verify authentication successes for IOCapabilities DisplayOnly for master and NoInputNoOutput for subordinate</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities display only on master and NoInputNoOutput on Subordinate. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM1S0</p></td>
<td><p>Verify authentication successes for IO capabilities DisplayYesNo for master and DisplayOnly for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities DisplayYesNo for master and DisplayOnly for subordinate.</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities display only on both. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM1S1</p></td>
<td><p>Verify authentication successes for IO capabilities DisplayYesNo for both master and subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description Verify authentication successes for IOCapabilities DisplayYesNo for master and subordinate.</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities displayYesNo on both. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM1S2</p></td>
<td><p>Verify authentication successes for IO capability DisplayYesNo for master and KeyboardOnly for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities DisplayYesNo for master and KeyBoardOnly for subordinate</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities DisplayYesNo for master and KeyBoardOnly on SubordinateMaster initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM1S3</p></td>
<td><p>Verify authentication successes for IO capabilities DisplayYesNo for master and NoInputNoOutput for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities DisplayYesNo for master and KeyBoardOnly for subordinate</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities display YesNo on master and NoInputNoOutput on SubordinateMaster initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM2S0</p></td>
<td><p>Verify authentication successes for IOCapabilities KeyBoardOnly for master and DisplayOnly for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities KeyBoardOnly for master and DisplayOnly for subordinate.</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities KeyBoardOnly on master and DisplayOnly on Subordinate Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM2S1</p></td>
<td><p>Verify authentication successes for IOcapabilities KeyBoardOnly for master and DisplayYesNo for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description Verify authentication successes for IOCapabilities KeyBoardOnly for master and DisplayYesNo for subordinate</p></td>
<td><p>Master and subordinate registers for authentication with IOcapabilities KeyBoardOnly for master and DisplayYesNo for subordinate. Master initiates the authentication subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM2S2</p></td>
<td><p>Verify authentication successes for IO capabilities KeyBoardOnly for master and subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities KeyBoardOnly for master and DisplayYesNo for subordinate.</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities KeyBoardOnly on both. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM2S3</p></td>
<td><p>Verify authentication successes for IO capabilities KeyBoardOnly for master and NoInputNoOutput for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities KeyBoardOnly for Master and NoInputNoOutput for subordinate.</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities KeyBoardOnly on master and NoInputNoOutput on Subordinate Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM3S0</p></td>
<td><p>Verify authentication successes for IO capabilities NoInputNoOutput for master and DisplayOnly for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities NoInputNoOutput for Master and DisplayOnly for subordinate.</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities NoInputNoOutput for master and DisplayOnly for Subordinate. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM3S1</p></td>
<td><p>Verify authentication successes for IO capability NoInputNoOutput for master and DisplayYesNo for subordinate</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities NoInputNoOutput for Master and DisplayYesNo for subordinate</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities NoInputNoOutput for master and DislpayYesNo for Subordinate. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>VerifyAuthForIOCapM3S2</p></td>
<td><p>Verify authentication successes for IO capabilities NoInputNoOutput for master and KeyBoradOnly for Subordinate.</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities NoInputNoOutput for Master and KeyBoardOnly for subordinate.</p></td>
<td><p>Procedures: Master and subordinate registers for authentication with IOCapabilities NoInputNoOutput for Master and KeyBoardOnly for Subordinate. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="odd">
<td><p>VerifyAuthForIOCapM3S3</p></td>
<td><p>Verify authentication successes for IO capabilities NoInputNoOutput for master and Subordinate.</p></td>
<td><p>See VerifyAuthForIOCapMxSx Tests Description. Verify authentication successes for IOCapabilities NoInputNoOutput for Master and Subordinate.</p></td>
<td><p>Master and subordinate registers for authentication with IOCapabilities NoInputNoOutput for both Master and Subordinate. Master initiates the authentication, subordinate accepts authentication request and sent positive response. Verify that authentication succeeds.</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>EIREE1.1</p></td>
<td><p>Complete EIR name is present and not null</p></td>
<td><p>Complete EIR name is present and not null</p></td>
<td><p>[This content isn't available yet.]</p></td>
<td><p>250</p></td>
</tr>
<tr class="odd">
<td><p>EIREE1.2</p></td>
<td><p>Partial EIR name is present and not null</p></td>
<td><p>Partial EIR name is present and not null</p></td>
<td><p>[This content isn't available yet.]</p></td>
<td><p>250</p></td>
</tr>
<tr class="even">
<td><p>EIREE1.3</p></td>
<td><p>Complete EIR name is present and null.</p></td>
<td><p>Complete EIR name is present and null</p></td>
<td><p>[This content isn't available yet.]</p></td>
<td><p>110</p></td>
</tr>
<tr class="odd">
<td><p>EIREE1.4</p></td>
<td><p>Partial EIR name is present and null</p></td>
<td><p>Partial EIR name is present and null</p></td>
<td><p>[This content isn't available yet.]</p></td>
<td><p>125</p></td>
</tr>
</tbody>
</table>

 

### Parameters

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ENABLETRACING</p></td>
<td><p>Enables collection of ETW traces. If <strong>True</strong>, the ETW traces are enabled on the collection. If <strong>False</strong>, the ETW traces on the collection are turned off.</p>
<p>Default value: False</p></td>
</tr>
</tbody>
</table>

 

 

 





