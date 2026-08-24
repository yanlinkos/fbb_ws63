# Preface<a name="ZH-CN_TOPIC_0000001732354354"></a>

**Overview<a name="section4537382116410"></a>**

This document describes the workflows of WS63V100 RomBoot, LoaderBoot, and FlashBoot. Users can refer to this document to perform secondary development of FlashBoot.

**Product Version<a name="section27775771"></a>**

The product versions corresponding to this document are as follows.

<a name="table52250146"></a>
<table><thead align="left"><tr id="row55967882"><th class="cellrowborder" valign="top" width="39.39%" id="mcps1.1.3.1.1"><p id="p37104584"><a name="p37104584"></a><a name="p37104584"></a><strong id="b21211131516"><a name="b21211131516"></a><a name="b21211131516"></a>Product Name</strong></p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.1.3.1.2"><p id="p52681331"><a name="p52681331"></a><a name="p52681331"></a><strong id="b18261911191515"><a name="b18261911191515"></a><a name="b18261911191515"></a>Product Version</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row39329394"><td class="cellrowborder" valign="top" width="39.39%" headers="mcps1.1.3.1.1 "><p id="p31080012"><a name="p31080012"></a><a name="p31080012"></a>WS63</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.1.3.1.2 "><p id="p34453054"><a name="p34453054"></a><a name="p34453054"></a>V100</p>
</td>
</tr>
</tbody>
</table>

**Target Audience<a name="section4378592816410"></a>**

This document is mainly applicable to the following engineers:

-   Technical Support Engineer
-   Software Development Engineer

**Symbol Conventions<a name="section133020216410"></a>**

The following symbols may appear in this document. Their meanings are described below.

<a name="table2622507016410"></a>
<table><thead align="left"><tr id="row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="p6450074116410"><a name="p6450074116410"></a><a name="p6450074116410"></a><strong id="b2136615816410"><a name="b2136615816410"></a><a name="b2136615816410"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="p5435366816410"><a name="p5435366816410"></a><a name="p5435366816410"></a><strong id="b5941558116410"><a name="b5941558116410"></a><a name="b5941558116410"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001732195226.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a high-level risk hazard that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001779394385.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a medium-level risk hazard that, if not avoided, may result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001779234653.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a low-level risk hazard that, if not avoided, may result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001732195234.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey safety warning information about the device or environment. If not avoided, it may result in device damage, data loss, reduced device performance, or other unpredictable results.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>"Notice" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="15.96" width="47.88" src="figures/en_image_0000001732195218.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary description of key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>"Note" is not safety warning information and does not involve personal, device, or environmental harm.</p>
</td>
</tr>
</tbody>
</table>

**Revision History<a name="section2467512116410"></a>**

<a name="table1557726816410"></a>
<table><thead align="left"><tr id="row2942532716410"><th class="cellrowborder" valign="top" width="15.65%" id="mcps1.1.4.1.1"><p id="p3778275416410"><a name="p3778275416410"></a><a name="p3778275416410"></a><strong id="b5687322716410"><a name="b5687322716410"></a><a name="b5687322716410"></a>Document Version</strong></p>
</th>
<th class="cellrowborder" valign="top" width="20.89%" id="mcps1.1.4.1.2"><p id="p5627845516410"><a name="p5627845516410"></a><a name="p5627845516410"></a><strong id="b5800814916410"><a name="b5800814916410"></a><a name="b5800814916410"></a>Release Date</strong></p>
</th>
<th class="cellrowborder" valign="top" width="63.46000000000001%" id="mcps1.1.4.1.3"><p id="p2382284816410"><a name="p2382284816410"></a><a name="p2382284816410"></a><strong id="b3316380216410"><a name="b3316380216410"></a><a name="b3316380216410"></a>Modification Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row820313201511"><td class="cellrowborder" valign="top" width="15.65%" headers="mcps1.1.4.1.1 "><p id="p220313211512"><a name="p220313211512"></a><a name="p220313211512"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="20.89%" headers="mcps1.1.4.1.2 "><p id="p52034321153"><a name="p52034321153"></a><a name="p52034321153"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="63.46000000000001%" headers="mcps1.1.4.1.3 "><p id="p1031614161639"><a name="p1031614161639"></a><a name="p1031614161639"></a>First official version release.</p>
</td>
</tr>
<tr id="row5947359616410"><td class="cellrowborder" valign="top" width="15.65%" headers="mcps1.1.4.1.1 "><p id="p2149706016410"><a name="p2149706016410"></a><a name="p2149706016410"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="20.89%" headers="mcps1.1.4.1.2 "><p id="p648803616410"><a name="p648803616410"></a><a name="p648803616410"></a>2023-12-18</p>
</td>
<td class="cellrowborder" valign="top" width="63.46000000000001%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>First interim version release.</p>
</td>
</tr>
</tbody>
</table>

# Boot Introduction<a name="ZH-CN_TOPIC_0000001779234629"></a>

WS63V100 Boot consists of three parts: RomBoot, FlashBoot, and LoaderBoot.

-   RomBoot functions include:
    -   Load LoaderBoot into RAM, and then use LoaderBoot to download images to Flash, burn eFuse, and so on.
    -   Verify and boot FlashBoot. FlashBoot is divided into side A and side B. If side A passes verification, it boots directly. If verification fails, side B is verified. If side B passes verification, the system boots from side B; otherwise, the system resets and restarts.

-   FlashBoot functions include:
    -   Upgrade the firmware.
    -   Verify and boot the firmware.

-   LoaderBoot functions include:
    -   Download images to Flash.
    -   Burn EFUSE (for example, keys related to secure boot/Flash encryption).

**Figure 1**  Boot startup process<a name="fig2070413408573"></a>  
![](figures/boot_startup_process.png "Boot startup process")

# RomBoot Function Description<a name="ZH-CN_TOPIC_0000001732195210"></a>



## Downloading Images and Burning EFUSE<a name="ZH-CN_TOPIC_0000001732195194"></a>

RomBoot implements the functions of downloading images to Flash and burning EFUSE by loading LoaderBoot. For specific operations, see the *WS63V100 BurnTool User Guide*.

## Verifying and Booting FlashBoot<a name="ZH-CN_TOPIC_0000001779394349"></a>

The process of verifying and booting FlashBoot is shown in [Figure 1](#fig1578634595518).

**Figure 1**  FlashBoot verification and boot flowchart<a name="fig1578634595518"></a>  
![](figures/flashboot_verification_and_boot_flowchart.png "FlashBoot verification and boot flowchart")

# LoaderBoot Function Description<a name="ZH-CN_TOPIC_0000001779394361"></a>

LoaderBoot is the component that directly interacts with BurnTool. RomBoot cannot directly implement the burning function. LoaderBoot needs to be loaded into RAM, and then the program jumps to LoaderBoot to complete the burning of related content through LoaderBoot. The content that LoaderBoot can burn includes:

-   FlashBoot
-   EFUSE parameter configuration file
-   Firmware images (including NV parameters)
-   Production test images

>![](public_sys-resources/icon-note.gif) **Note:** 
>LoaderBoot generally does not involve secondary development.

# FlashBoot Description<a name="ZH-CN_TOPIC_0000001732354346"></a>


## FlashBoot Startup Process<a name="ZH-CN_TOPIC_0000001732195198"></a>

The process of verifying and booting the firmware is shown in [Figure 1](#fig921910011115).

**Figure 1**  Firmware verification and boot flowchart<a name="fig921910011115"></a>  
![](figures/firmware_verification_and_boot_flowchart.png "Firmware verification and boot flowchart")

