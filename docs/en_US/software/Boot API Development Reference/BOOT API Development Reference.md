# Preface<a name="ZH-CN_TOPIC_0000001803116112"></a>

**Overview<a name="section4537382116410"></a>**

This document mainly describes the upgrade-related API interfaces in WS63 Flashboot. For details, refer to the interface introduction in the *WS63V100 FOTA Development Guide*.

**Product Version<a name="section111371595118"></a>**

The product versions corresponding to this document are as follows.

<a name="table22377277"></a>
<table><thead align="left"><tr id="row63051425"><th class="cellrowborder" valign="top" width="40.400000000000006%" id="mcps1.1.3.1.1"><p id="p6891761"><a name="p6891761"></a><a name="p6891761"></a><strong id="b87075663813"><a name="b87075663813"></a><a name="b87075663813"></a>Product Name</strong></p>
</th>
<th class="cellrowborder" valign="top" width="59.599999999999994%" id="mcps1.1.3.1.2"><p id="p21361741"><a name="p21361741"></a><a name="p21361741"></a><strong id="b1175145653811"><a name="b1175145653811"></a><a name="b1175145653811"></a>Product Version</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row52579486"><td class="cellrowborder" valign="top" width="40.400000000000006%" headers="mcps1.1.3.1.1 "><p id="p31080012"><a name="p31080012"></a><a name="p31080012"></a>WS63</p>
</td>
<td class="cellrowborder" valign="top" width="59.599999999999994%" headers="mcps1.1.3.1.2 "><p id="p34453054"><a name="p34453054"></a><a name="p34453054"></a>V100</p>
</td>
</tr>
</tbody>
</table>

**Target Audience<a name="section0192844173119"></a>**

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
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001849835093.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a high-level risk hazard that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001849755165.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a medium-level risk hazard that, if not avoided, may result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001802956316.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a low-level risk hazard that, if not avoided, may result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001803116124.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey safety warning information about the device or environment. If not avoided, it may result in device damage, data loss, reduced device performance, or other unpredictable results.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>"Notice" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001849835105.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary description of key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>"Note" is not safety warning information and does not involve personal, device, or environmental harm.</p>
</td>
</tr>
</tbody>
</table>

**Revision History<a name="section2467512116410"></a>**

<a name="table1557726816410"></a>
<table><thead align="left"><tr id="row2942532716410"><th class="cellrowborder" valign="top" width="20.72%" id="mcps1.1.4.1.1"><p id="p3778275416410"><a name="p3778275416410"></a><a name="p3778275416410"></a><strong id="b5687322716410"><a name="b5687322716410"></a><a name="b5687322716410"></a>Document Version</strong></p>
</th>
<th class="cellrowborder" valign="top" width="26.119999999999997%" id="mcps1.1.4.1.2"><p id="p5627845516410"><a name="p5627845516410"></a><a name="p5627845516410"></a><strong id="b5800814916410"><a name="b5800814916410"></a><a name="b5800814916410"></a>Release Date</strong></p>
</th>
<th class="cellrowborder" valign="top" width="53.16%" id="mcps1.1.4.1.3"><p id="p2382284816410"><a name="p2382284816410"></a><a name="p2382284816410"></a><strong id="b3316380216410"><a name="b3316380216410"></a><a name="b3316380216410"></a>Modification Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1699734715172"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p220313211512"><a name="p220313211512"></a><a name="p220313211512"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p52034321153"><a name="p52034321153"></a><a name="p52034321153"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1031614161639"><a name="p1031614161639"></a><a name="p1031614161639"></a>First official version release.</p>
</td>
</tr>
<tr id="row5947359616410"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p2149706016410"><a name="p2149706016410"></a><a name="p2149706016410"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p648803616410"><a name="p648803616410"></a><a name="p648803616410"></a>2024-02-22</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>First interim version release.</p>
</td>
</tr>
</tbody>
</table>

# Interface Description<a name="ZH-CN_TOPIC_0000001849825997"></a>

**Table 1**  Description of Upgrade Interfaces (Upgrade Package Storage)

<a name="table1585372681620"></a>
<table><thead align="left"><tr id="row385412616166"><th class="cellrowborder" valign="top" width="37.74%" id="mcps1.2.3.1.1"><p id="p373695616166"><a name="p373695616166"></a><a name="p373695616166"></a>Interface Name</p>
</th>
<th class="cellrowborder" valign="top" width="62.260000000000005%" id="mcps1.2.3.1.2"><p id="p15736756151620"><a name="p15736756151620"></a><a name="p15736756151620"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row1486763081710"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p18867133051718"><a name="p18867133051718"></a><a name="p18867133051718"></a>uapi_upg_init</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p1486713307174"><a name="p1486713307174"></a><a name="p1486713307174"></a>Initializes the upgrade module.</p>
</td>
</tr>
<tr id="row11854122671616"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p126138161710"><a name="p126138161710"></a><a name="p126138161710"></a>uapi_upg_prepare</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p19611380177"><a name="p19611380177"></a><a name="p19611380177"></a>Preparation work before saving the upgrade package to the local storage.</p>
</td>
</tr>
<tr id="row685452616161"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p16616811719"><a name="p16616811719"></a><a name="p16616811719"></a>uapi_upg_write_package_async/uapi_upg_write_package_sync</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p3611486173"><a name="p3611486173"></a><a name="p3611486173"></a>Writes the upgrade package data to the local storage. (Asynchronous/Synchronous)</p>
</td>
</tr>
<tr id="row98547262169"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p259718589312"><a name="p259718589312"></a><a name="p259718589312"></a>uapi_upg_read_package</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p5615811714"><a name="p5615811714"></a><a name="p5615811714"></a>Reads upgrade package data from the local storage.</p>
</td>
</tr>
<tr id="row177421859153715"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p107431159183718"><a name="p107431159183718"></a><a name="p107431159183718"></a>uapi_upg_request_upgrade</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p57432059133712"><a name="p57432059133712"></a><a name="p57432059133712"></a>Requests to start a local upgrade. Call this interface after all upgrade package data has been saved.</p>
</td>
</tr>
<tr id="row3828154123820"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p1066210362417"><a name="p1066210362417"></a><a name="p1066210362417"></a>uapi_upg_get_storage_size</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p1182824143810"><a name="p1182824143810"></a><a name="p1182824143810"></a>Obtains the size of the space available for storing the upgrade package.</p>
</td>
</tr>
</tbody>
</table>

**Table 2**  Description of Upgrade Interfaces (Local Upgrade)

<a name="table1660824542212"></a>
<table><thead align="left"><tr id="row1860864518228"><th class="cellrowborder" valign="top" width="37.74%" id="mcps1.2.3.1.1"><p id="p1060916458228"><a name="p1060916458228"></a><a name="p1060916458228"></a>Interface Name</p>
</th>
<th class="cellrowborder" valign="top" width="62.260000000000005%" id="mcps1.2.3.1.2"><p id="p13609184532213"><a name="p13609184532213"></a><a name="p13609184532213"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row560934513229"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p960934513228"><a name="p960934513228"></a><a name="p960934513228"></a>uapi_upg_init</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p176091045102215"><a name="p176091045102215"></a><a name="p176091045102215"></a>Initializes the upgrade module.</p>
</td>
</tr>
<tr id="row35427913505"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p5856111017502"><a name="p5856111017502"></a><a name="p5856111017502"></a>uapi_upg_register_progress_callback</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p7856161015507"><a name="p7856161015507"></a><a name="p7856161015507"></a>Registers a callback function for upgrade progress notifications. After registration, the callback function is invoked during the local upgrade to notify the current progress.</p>
</td>
</tr>
<tr id="row19609154562210"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p5609745202212"><a name="p5609745202212"></a><a name="p5609745202212"></a>uapi_upg_start</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p20609245172211"><a name="p20609245172211"></a><a name="p20609245172211"></a>Starts the local upgrade.</p>
</td>
</tr>
<tr id="row1612214129385"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p9861102283820"><a name="p9861102283820"></a><a name="p9861102283820"></a>uapi_upg_get_result</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p386142213387"><a name="p386142213387"></a><a name="p386142213387"></a>Obtains the upgrade result.</p>
</td>
</tr>
<tr id="row1260944511226"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p1821544917386"><a name="p1821544917386"></a><a name="p1821544917386"></a>uapi_upg_verify_file_head</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p122151749113812"><a name="p122151749113812"></a><a name="p122151749113812"></a>Verifies the upgrade package header structure.</p>
</td>
</tr>
<tr id="row126175548388"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p1355184103910"><a name="p1355184103910"></a><a name="p1355184103910"></a>uapi_upg_verify_file_image</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p1355154163918"><a name="p1355154163918"></a><a name="p1355154163918"></a>Verifies the upgrade image in the upgrade package.</p>
</td>
</tr>
<tr id="row18734135723817"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p18827963914"><a name="p18827963914"></a><a name="p18827963914"></a>uapi_upg_verify_file</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p10821694394"><a name="p10821694394"></a><a name="p10821694394"></a>Verifies the entire upgrade package.</p>
</td>
</tr>
<tr id="row43871712163916"><td class="cellrowborder" valign="top" width="37.74%" headers="mcps1.2.3.1.1 "><p id="p9285101916398"><a name="p9285101916398"></a><a name="p9285101916398"></a>uapi_upg_register_user_defined_verify_func</p>
</td>
<td class="cellrowborder" valign="top" width="62.260000000000005%" headers="mcps1.2.3.1.2 "><p id="p152851419163917"><a name="p152851419163917"></a><a name="p152851419163917"></a>Registers a verification function for user-defined fields.</p>
<p id="p32851119103910"><a name="p32851119103910"></a><a name="p32851119103910"></a>The upgrade package structure reserves 48Byte for the verification of user-defined data. After a custom verification function is registered, the registered function is invoked when uapi_upg_verify_file_head and uapi_upg_verify_file are called. If the verification of user-defined data fails, uapi_upg_verify_file_head and uapi_upg_verify_file return a failure.</p>
</td>
</tr>
</tbody>
</table>

**Table 3**  Description of Upgrade Interface Input Parameters and Return Values

<a name="table543918111242"></a>
<table><thead align="left"><tr id="row64392119417"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p1343919111645"><a name="p1343919111645"></a><a name="p1343919111645"></a>Interface Prototype</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p174391011448"><a name="p174391011448"></a><a name="p174391011448"></a>Parameter and Return Value Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row19439131110414"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1969441615612"><a name="p1969441615612"></a><a name="p1969441615612"></a>errcode_t uapi_upg_init(const upg_func_t *func_list)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul1384395376"></a><a name="ul1384395376"></a><ul id="ul1384395376"><li>Input parameter description:<p id="p743931115420"><a name="p743931115420"></a><a name="p743931115420"></a>func_list: callback list to register, of type upg_func_t.</p>
</li></ul>
<a name="ul368214575374"></a><a name="ul368214575374"></a><ul id="ul368214575374"><li>Return value:<a name="ul13561878384"></a><a name="ul13561878384"></a><ul id="ul13561878384"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row174394111548"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p172791358273"><a name="p172791358273"></a><a name="p172791358273"></a>errcode_t uapi_upg_start(void)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul1417191953814"></a><a name="ul1417191953814"></a><ul id="ul1417191953814"><li>Input parameter description: None.</li><li>Return value:<a name="ul4292432183815"></a><a name="ul4292432183815"></a><ul id="ul4292432183815"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row1943941111416"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p7912209817"><a name="p7912209817"></a><a name="p7912209817"></a>errcode_t uapi_upg_register_progress_callback(uapi_upg_progress_cb func)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul18751138203816"></a><a name="ul18751138203816"></a><ul id="ul18751138203816"><li>Input parameter description:<p id="p874642615811"><a name="p874642615811"></a><a name="p874642615811"></a>func: callback function, which needs to be implemented by the service.</p>
</li><li>Return value:<a name="ul1534612502382"></a><a name="ul1534612502382"></a><ul id="ul1534612502382"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row443915117411"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p413413720912"><a name="p413413720912"></a><a name="p413413720912"></a>errcode_t uapi_upg_get_result(upg_result_t *result, uint32_t *last_image_index)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul5512203183912"></a><a name="ul5512203183912"></a><ul id="ul5512203183912"><li>Input parameter description:<a name="ul1285514154399"></a><a name="ul1285514154399"></a><ul id="ul1285514154399"><li>result: output parameter, memory address for storing the upgrade result, of type upg_result_t.</li><li>last_image_index: output parameter, index of the last processed image.</li></ul>
</li><li>Return value:<a name="ul93412817391"></a><a name="ul93412817391"></a><ul id="ul93412817391"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row17439131117411"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p115282109111"><a name="p115282109111"></a><a name="p115282109111"></a>errcode_t uapi_upg_prepare(upg_prepare_info_t *prepare_info)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul28461128173912"></a><a name="ul28461128173912"></a><ul id="ul28461128173912"><li>Input parameter description:<p id="p182641143164"><a name="p182641143164"></a><a name="p182641143164"></a>prepare_info: input parameter, of type upg_prepare_info_t*, a pointer to the preparation information.</p>
</li><li>Return value:<a name="ul101051345399"></a><a name="ul101051345399"></a><ul id="ul101051345399"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row1972014489105"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p59591437498"><a name="p59591437498"></a><a name="p59591437498"></a>errcode_t uapi_upg_write_package_async(uint32_t offset, const uint8_t *buff, uint16_t len, uapi_upg_write_done_cb callback)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul13324126134011"></a><a name="ul13324126134011"></a><ul id="ul13324126134011"><li>Input parameter description:<a name="ul6565151412407"></a><a name="ul6565151412407"></a><ul id="ul6565151412407"><li>offset: input parameter, of type uint32_t, offset from the beginning of the upgrade package.</li><li>buff: input parameter, of type const uint8_t *, buffer for storing the upgrade package data.</li><li>len: input parameter, of type uint16_t, length of the upgrade package data buffer.</li><li>callback: input parameter, of type uapi_upg_write_done_cb, callback function invoked when the write is complete.</li></ul>
</li><li>Return value:<a name="ul135574198410"></a><a name="ul135574198410"></a><ul id="ul135574198410"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row18571245918"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p96711599112"><a name="p96711599112"></a><a name="p96711599112"></a>errcode_t uapi_upg_write_package_sync(uint32_t offset, const uint8_t *buff, uint16_t len)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul6730191311914"></a><a name="ul6730191311914"></a><ul id="ul6730191311914"><li>Input parameter description:<a name="ul1730513290"></a><a name="ul1730513290"></a><ul id="ul1730513290"><li>offset: input parameter, of type uint32_t, offset from the beginning of the upgrade package.</li><li>buff: input parameter, of type const uint8_t *, buffer for storing the upgrade package data.</li><li>len: input parameter, of type uint16_t, length of the upgrade package data buffer.</li></ul>
</li><li>Return value:<a name="ul13731513999"></a><a name="ul13731513999"></a><ul id="ul13731513999"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row16820205217100"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1415605316124"><a name="p1415605316124"></a><a name="p1415605316124"></a>errcode_t uapi_upg_read_package(uint32_t offset, uint8_t *buff, uint32_t len)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul942818368418"></a><a name="ul942818368418"></a><ul id="ul942818368418"><li>Input parameter description:<a name="ul540820427411"></a><a name="ul540820427411"></a><ul id="ul540820427411"><li>offset: input parameter, of type uint32_t, offset from the beginning of the upgrade package.</li><li>buff: output parameter, of type uint8_t *, buffer for storing the upgrade package data.</li><li>len: input parameter, of type uint32_t, length of the buffer for reading data.</li></ul>
</li><li>Return value:<a name="ul92624479419"></a><a name="ul92624479419"></a><ul id="ul92624479419"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row9731115618106"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1642912184138"><a name="p1642912184138"></a><a name="p1642912184138"></a>uint32_t uapi_upg_get_storage_size(void)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul11468249184212"></a><a name="ul11468249184212"></a><ul id="ul11468249184212"><li>Input parameter description: None.</li><li>Return value:<a name="ul1471417015437"></a><a name="ul1471417015437"></a><ul id="ul1471417015437"><li>0: Returns 0 on failure.</li><li>Others: Returns the space size on success.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row99221759121014"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p17782242205"><a name="p17782242205"></a><a name="p17782242205"></a>errcode_t uapi_upg_request_upgrade(bool reset)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul93401214124320"></a><a name="ul93401214124320"></a><ul id="ul93401214124320"><li>Input parameter description:<p id="p12873129121711"><a name="p12873129121711"></a><a name="p12873129121711"></a>reset: input parameter, of type bool, whether to restart the system after the request process ends.</p>
</li><li>Return value:<a name="ul112601188436"></a><a name="ul112601188436"></a><ul id="ul112601188436"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row1168225117190"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p17933151517497"><a name="p17933151517497"></a><a name="p17933151517497"></a>errcode_t uapi_upg_verify_file_head(const upg_package_header_t *pkg_header)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul172091039114315"></a><a name="ul172091039114315"></a><ul id="ul172091039114315"><li>Input parameter description:<p id="p577525916436"><a name="p577525916436"></a><a name="p577525916436"></a>pkg_header: input parameter, of type upg_package_header_t *, a pointer to the upgrade package header structure.</p>
</li><li>Return value:<a name="ul106384575434"></a><a name="ul106384575434"></a><ul id="ul106384575434"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row16741055171920"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p15451248507"><a name="p15451248507"></a><a name="p15451248507"></a>errcode_t uapi_upg_verify_file_image(const upg_image_header_t *img_header, const uint8_t *hash, uint32_t hash_len, bool verify_old)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul083121716446"></a><a name="ul083121716446"></a><ul id="ul083121716446"><li>Input parameter description:<a name="ul195551433164420"></a><a name="ul195551433164420"></a><ul id="ul195551433164420"><li>img_header: input parameter, of type upg_image_header_t*, a pointer to the upgrade image header structure in the upgrade package.</li><li>hash: input parameter, of type uint8_t*, HASH value of the upgrade image.</li><li>hash_len: input parameter, of type uint32_t, length of the HASH (unit: Byte).</li><li>verify_old: input parameter, of type bool, whether to verify the old image.</li></ul>
</li><li>Return value:<a name="ul1095818223448"></a><a name="ul1095818223448"></a><ul id="ul1095818223448"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row1456615911192"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p194291932165215"><a name="p194291932165215"></a><a name="p194291932165215"></a>errcode_t uapi_upg_verify_file(const upg_package_header_t *pkg_header)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul7532122417456"></a><a name="ul7532122417456"></a><ul id="ul7532122417456"><li>Input parameter description:<p id="p492743714514"><a name="p492743714514"></a><a name="p492743714514"></a>pkg_header: input parameter, of type upg_package_header_t *, a pointer to the upgrade package header structure.</p>
</li><li>Return value:<a name="ul668363524515"></a><a name="ul668363524515"></a><ul id="ul668363524515"><li>ERRCODE_SUCC: Success.</li><li>Others: Failure.</li></ul>
</li></ul>
</td>
</tr>
<tr id="row1521203202011"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p44763015318"><a name="p44763015318"></a><a name="p44763015318"></a>void uapi_upg_register_user_defined_verify_func(uapi_upg_user_defined_check func, uintptr_t param)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><a name="ul643116487459"></a><a name="ul643116487459"></a><ul id="ul643116487459"><li>Input parameter description:<a name="ul123651753194513"></a><a name="ul123651753194513"></a><ul id="ul123651753194513"><li>func: input parameter, of type upg_package_header_t *, a verification function used to verify user-defined fields.</li><li>param: input parameter, of type uintptr_t, registration parameter.</li></ul>
</li><li>Return value: None.</li></ul>
</td>
</tr>
</tbody>
</table>

