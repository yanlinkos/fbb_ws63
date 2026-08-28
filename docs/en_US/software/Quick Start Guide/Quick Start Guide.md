# Preface<a name="ZH-CN_TOPIC_0000001795272176"></a>

**Overview<a name="section4537382116410"></a>**

This document is written for developers who are using this version for the first time. It aims to help developers quickly grasp the overall architecture of the documentation and guide them step by step through in-depth development. It also helps different developers quickly find the documents they need.

>![](public_sys-resources/icon-notice.gif) **Notice:** 
>-   Chapter 1 describes the document directory of the release package, outlining the overall document structure.
>-   Chapter 2 describes the environment setup part, including chip evaluation, development board introduction, and development environment setup.
>-   Chapter 3 describes basic function development, including the interfaces, command descriptions, and Demo development references for basic function development.
>-   Chapter 4 describes feature development, including individual feature descriptions and related documentation.
>-   Chapter 5 describes test guidance, including environment setup and operation instructions for performance testing and hardware testing.
>-   Chapter 6 is the test report, containing reference data such as power consumption and hardware testing.

**Product Version<a name="section358mcpsimp"></a>**

The product version corresponding to this document is as follows.

<a name="table361mcpsimp"></a>
<table><thead align="left"><tr id="row366mcpsimp"><th class="cellrowborder" valign="top" width="32%" id="mcps1.1.3.1.1"><p id="p368mcpsimp"><a name="p368mcpsimp"></a><a name="p368mcpsimp"></a>Product Name</p>
</th>
<th class="cellrowborder" valign="top" width="68%" id="mcps1.1.3.1.2"><p id="p370mcpsimp"><a name="p370mcpsimp"></a><a name="p370mcpsimp"></a>Product Version</p>
</th>
</tr>
</thead>
<tbody><tr id="row372mcpsimp"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.3.1.1 "><p id="p374mcpsimp"><a name="p374mcpsimp"></a><a name="p374mcpsimp"></a>WS63</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.1.3.1.2 "><p id="p376mcpsimp"><a name="p376mcpsimp"></a><a name="p376mcpsimp"></a>V100</p>
</td>
</tr>
<tr id="row195710915813"><td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.3.1.1 "><p id="p69581398815"><a name="p69581398815"></a><a name="p69581398815"></a>WS63E</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.1.3.1.2 "><p id="p1695839289"><a name="p1695839289"></a><a name="p1695839289"></a>V100</p>
</td>
</tr>
</tbody>
</table>

**Intended Audience<a name="section4378592816410"></a>**

This document (this guide) is mainly intended for the following engineers:

-   Technical support engineers
-   Software development engineers

**Symbol Conventions<a name="section133020216410"></a>**

The following symbols may appear in this document. Their meanings are as follows.

<a name="table2622507016410"></a>
<table><thead align="left"><tr id="row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="p6450074116410"><a name="p6450074116410"></a><a name="p6450074116410"></a><strong id="b2136615816410"><a name="b2136615816410"></a><a name="b2136615816410"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="p5435366816410"><a name="p5435366816410"></a><a name="p5435366816410"></a><strong id="b5941558116410"><a name="b5941558116410"></a><a name="b5941558116410"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001795431956.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a hazard with a high level of risk that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001795272188.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a hazard with a medium level of risk that, if not avoided, could result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001842071165.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a hazard with a low level of risk that, if not avoided, could result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001842191225.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey equipment or environmental safety warnings. If not avoided, it may result in equipment damage, data loss, degraded device performance, or other unpredictable consequences.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>"Notice" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001795431952.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary explanation of key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>"Note" is not a safety warning and does not involve personal, equipment, or environmental damage.</p>
</td>
</tr>
</tbody>
</table>

**Revision History<a name="section2467512116410"></a>**

<a name="table1557726816410"></a>
<table><thead align="left"><tr id="row2942532716410"><th class="cellrowborder" valign="top" width="20.72%" id="mcps1.1.4.1.1"><p id="p3778275416410"><a name="p3778275416410"></a><a name="p3778275416410"></a>Document Version</p>
</th>
<th class="cellrowborder" valign="top" width="26.119999999999997%" id="mcps1.1.4.1.2"><p id="p5627845516410"><a name="p5627845516410"></a><a name="p5627845516410"></a>Release Date</p>
</th>
<th class="cellrowborder" valign="top" width="53.16%" id="mcps1.1.4.1.3"><p id="p2382284816410"><a name="p2382284816410"></a><a name="p2382284816410"></a>Revision Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row158747468138"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p1887519462134"><a name="p1887519462134"></a><a name="p1887519462134"></a>03</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p1687512467131"><a name="p1687512467131"></a><a name="p1687512467131"></a>2024-06-27</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><a name="ul4820150141413"></a><a name="ul4820150141413"></a><ul id="ul4820150141413"><li>Updated the "<a href="hardware_design_introduction.md">Hardware Design Introduction</a>" and "<a href="hardware_component_selection_guide.md">Hardware Component Selection Guide</a>" sections.</li></ul>
</td>
</tr>
<tr id="row188432116291"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p188515218294"><a name="p188515218294"></a><a name="p188515218294"></a>02</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p188562142914"><a name="p188562142914"></a><a name="p188562142914"></a>2024-05-08</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><a name="ul132211559102213"></a><a name="ul132211559102213"></a><ul id="ul132211559102213"><li>Updated the "<a href="environment_setup.md">Environment Setup</a>" section.</li><li>Added the "<a href="radar_quick_development.md">Radar Quick Development</a>" section.</li><li>Added the "<a href="harmonyos_xts_certification_development.md">HarmonyOS XTS Certification Development</a>" and "<a href="harmonyos_connect_development.md">HarmonyOS Connect Development</a>" sections.</li><li>Updated the "<a href="test_guide.md">Test Guide</a>" section.</li><li>Updated the "<a href="test_report.md">Test Report</a>" section.</li></ul>
</td>
</tr>
<tr id="row1858012715382"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p105811763815"><a name="p105811763815"></a><a name="p105811763815"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p12581177173817"><a name="p12581177173817"></a><a name="p12581177173817"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p10745111523817"><a name="p10745111523817"></a><a name="p10745111523817"></a>First official version release.</p>
</td>
</tr>
<tr id="row1815217511024"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p115216511624"><a name="p115216511624"></a><a name="p115216511624"></a>00B02</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p615295111213"><a name="p615295111213"></a><a name="p615295111213"></a>2024-03-15</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p515365110214"><a name="p515365110214"></a><a name="p515365110214"></a>Updated the "<a href="feature_development.md">Feature Development</a>" section.</p>
</td>
</tr>
<tr id="row5947359616410"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p447mcpsimp"><a name="p447mcpsimp"></a><a name="p447mcpsimp"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p449mcpsimp"><a name="p449mcpsimp"></a><a name="p449mcpsimp"></a>2024-02-22</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p451mcpsimp"><a name="p451mcpsimp"></a><a name="p451mcpsimp"></a>First interim version release.</p>
</td>
</tr>
</tbody>
</table>

# Document Directory<a name="ZH-CN_TOPIC_0000001795272172"></a>

In the ReleaseDoc/ directory:

```
├── 00.hardware               #Documents related to hardware and chips  
├── 01.software               #Software-related documents  
│   ├── board                  #Documents related to board-side software development
│   └── tools                  #Tool software documents  
│   └── test                   #Test guidance documents
└── 02.only for reference     #Documents for reference only  
     ├── hardware              # Hardware design reference documents
     ├── software              # Software debugging and testing documents
     └── test report           # Performance, power consumption, and compatibility test reports, and some hardware test reports
```

# Environment Setup<a name="ZH-CN_TOPIC_0000001795431948"></a>






## Chip Specification Evaluation<a name="ZH-CN_TOPIC_0000001842071157"></a>

Documents such as the chip introduction and detailed chip specification descriptions.

-   Documents such as the chip introduction and detailed chip specification descriptions can be obtained from the FAE.

## Development Board Introduction<a name="ZH-CN_TOPIC_0000001795272184"></a>

Describes the development board hardware functions, PIN definitions, debug UART connection methods, and flashing tool connections.

-   \\00.hardware\\WS63V100 Development Board User Guide.pdf
-   \\00.hardware\\WS63EV100 Radar Module Board User Guide.pdf

## Hardware Design Introduction<a name="ZH-CN_TOPIC_0000001874223064"></a>

Describes hardware pin packaging, electrical characteristics, schematic design recommendations, PCB design recommendations, thermal design recommendations, soldering processes, moisture sensitivity parameters, interface timing, and precautions.

-   \\00.hardware\\WS63V100 Series Wi-Fi BLE and SLE Combo Chip Hardware User Guide.pdf

## Hardware Component Selection Guide<a name="ZH-CN_TOPIC_0000001920344769"></a>

Describes the recommended parameters and selection guide for key components during hardware design.

-   \\00.hardware\\WS63V100 Single Board Hardware Key Component Selection Guide.pdf

## Development Environment Setup<a name="ZH-CN_TOPIC_0000001842191217"></a>

Describes software development environment setup, SDK directory structure, SDK compilation, Demo APP development, and image flashing.

-   \\01.software\\board\\WS63V100 SDK Development Environment Setup User Guide.pdf

Describes the detailed steps for flashing the software image.

-   \\01.software\\tools\\WS63V100 BurnTool User Guide.pdf

Describes the setup of the log debugging tool.

-   \\01.software\\tools\\WS63V100 DebugKits User Guide.pdf

Describes the use of the Windows IDE compilation tool.

-   \\01.software\\tools\\WS63V100 IDE User Guide.pdf

# Basic Function Development<a name="ZH-CN_TOPIC_0000001842071161"></a>



## Basic Service Development<a name="ZH-CN_TOPIC_0000001842071153"></a>

Describes Wi-Fi and BLE & SLE driver development and interface descriptions.

-   \\01.software\\board\\WS63V100 Software Development Guide.pdf

## Command Line Description<a name="ZH-CN_TOPIC_0000001795431940"></a>

AT command description document.

-   \\01.software\\board\\WS63V100 AT Command User Guide.pdf

# Radar Quick Development<a name="ZH-CN_TOPIC_0000001920232789"></a>

Describes radar module functions, module design, installation constraints, production testing design, interference troubleshooting, software development, and test guidance.

-   \\01.software\\board\\WS63V100 Radar Quick Start Guide.pdf

# Feature Development<a name="ZH-CN_TOPIC_0000001842191221"></a>




## Common Feature Development<a name="ZH-CN_TOPIC_0000001920245077"></a>

Describes software feature development design.

-   \\01.software\\board\\WS63V100 Feature Development Guide.pdf

Describes boot development design.

-   \\01.software\\board\\WS63V100 BOOT API Development Reference.pdf
-   \\01.software\\board\\WS63V100 Boot Porting Application Development Guide.pdf

Describes OTA development design.

-   \\01.software\\board\\WS63V100 FOTA Development Guide.pdf

Describes open-source software development design.

-   \\01.software\\board\\WS63V100 CJSON Development Guide.pdf
-   \\01.software\\board\\WS63V100 CoAP Development Guide.pdf
-   \\01.software\\board\\WS63V100 lwIP Development Guide.pdf
-   \\01.software\\board\\WS63V100 MQTT Development Guide.pdf

Describes security software development design.

-   \\01.software\\board\\WS63V100 Security Software Development Guide.pdf

Describes network security for secondary development.

-   \\01.software\\board\\WS63V100 Secondary Development Network Security Precautions.pdf

## HarmonyOS XTS Certification Development<a name="ZH-CN_TOPIC_0000001874233416"></a>

Describes OpenHarmony XTS.

-   \\01.software\\board\\WS63V100 HarmonyOS XTS Certification Guide.pdf

## HarmonyOS Connect Development<a name="ZH-CN_TOPIC_0000001920352441"></a>

Describes HarmonyOS Connect compilation and feature development.

-   \\01.software\\board\\WS63V100 HiLink Compilation User Guide.pdf

# Test Guide<a name="ZH-CN_TOPIC_0000001795272180"></a>





## Single-Board Smoke Test Guide<a name="ZH-CN_TOPIC_0000001842191213"></a>

Operation instructions and command descriptions for smoke testing of basic software service functions.

\\01.software\\test\\WS63V100 Single Board Smoke Test Guide.pdf

## RF Test<a name="ZH-CN_TOPIC_0000001795431944"></a>

Descriptions of commands and parameters related to RF testing.

\\02.only for reference\\hardware\\WS63V100 Series RF Test User Guide.pdf

## Production Line Fixture Test<a name="ZH-CN_TOPIC_0000001920359605"></a>

Descriptions of commands and parameters related to production line fixture testing.

\\01.software\\board\\WS63V100 Production Line Tooling User Guide.pdf

## Development Board Power Consumption Test Guide<a name="ZH-CN_TOPIC_0000001849383725"></a>

Power consumption and test guide for three scenarios: working state, Shutdown, and sleep state.

\\02.only for reference\\hardware\\WS63V100 Series Development Board Power Consumption Test User Guide.pdf

# Test Report<a name="ZH-CN_TOPIC_0000001842191209"></a>

\\02.only for reference\\test report\\WS63V100 BLE BQB Certification Test Guide.pdf

\\02.only for reference\\test report\\WS63V100 WFA Certification Test Guide.pdf

\\02.only for reference\\test report\\WS63V100 SLE Certification Test Guide.pdf

