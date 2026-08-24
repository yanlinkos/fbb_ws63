# Preface<a name="ZH-CN_TOPIC_0000002563266117"></a>

**Overview<a name="section4537382116410"></a>**

This document describes in detail the methods and ideas for locating crash issues in LiteOS in combination with log information.

**Intended Audience<a name="section4378592816410"></a>**

This document is mainly applicable to LiteOS developers.

This document is mainly applicable to the following audiences:

-   Software development engineers
-   Technical support engineers

**Symbol Conventions<a name="section133020216410"></a>**

The following symbols may appear in this document. Their meanings are described as follows.

<a name="table2622507016410"></a>
<table><thead align="left"><tr id="row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="p6450074116410"><a name="p6450074116410"></a><a name="p6450074116410"></a><strong id="b2136615816410"><a name="b2136615816410"></a><a name="b2136615816410"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="p5435366816410"><a name="p5435366816410"></a><a name="p5435366816410"></a><strong id="b5941558116410"><a name="b5941558116410"></a><a name="b5941558116410"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000002532306228.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a hazard with a high level of risk that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000002532466156.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a hazard with a medium level of risk that, if not avoided, may result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000002563306087.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a hazard with a low level of risk that, if not avoided, may result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="67.83" src="figures/en_image_0000002563266119.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey device or environment safety warning information. If not avoided, it may result in device damage, data loss, degraded device performance, or other unpredictable results.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>A notice does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="25.270000000000003" width="67.83" src="figures/en_image_0000002532306230.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary explanation of key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>A note is not safety warning information and does not involve personal, device, or environmental damage.</p>
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
<th class="cellrowborder" valign="top" width="53.16%" id="mcps1.1.4.1.3"><p id="p2382284816410"><a name="p2382284816410"></a><a name="p2382284816410"></a><strong id="b3316380216410"><a name="b3316380216410"></a><a name="b3316380216410"></a>Change Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row5947359616410"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p2149706016410"><a name="p2149706016410"></a><a name="p2149706016410"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p17709349593"><a name="p17709349593"></a><a name="p17709349593"></a>2026-03-17</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>First official release</p>
</td>
</tr>
</tbody>
</table>

# Overview<a name="ZH-CN_TOPIC_0000002524734534"></a>




## Background<a name="ZH-CN_TOPIC_0000002555814459"></a>

In embedded systems, crashes occur frequently due to factors such as multi-task concurrency, resource contention, memory management exceptions, hardware driver defects, or improper configuration. FBB-RTOS adopts a single-process design and does not enable the MMU mechanism. While the globally visible physical memory feature improves efficiency, it also makes illegal memory operations more likely to cause system-level crashes. Compared with operating systems such as Android/Linux that have complete DFX toolchains and log systems, FBB-RTOS faces greater challenges in exception diagnosis. Crash issues are often difficult to locate quickly, especially when the crash does not occur at the first scene, resulting in low troubleshooting efficiency.

This document aims to systematically review the existing DFX capabilities and common diagnostic methods of FBB-RTOS, providing the R&D team with structured troubleshooting ideas. The following points need to be specially noted:

-   Crash issues are usually deeply coupled with specific business scenarios.
-   The current document only covers the usage of existing DFX tools.
-   The content will be continuously updated as DFX capabilities are enhanced.

## Interpreting Crash Logs<a name="ZH-CN_TOPIC_0000002524574584"></a>

During FBB-RTOS operation, when the system crashes, key log information is output. These logs contain critical debugging data such as exception types, error addresses, and register states. Correctly interpreting these logs is the key step in locating the root cause of the crash. Common logs and their meaning annotations when the system crashes are as follows:

<a name="table988mcpsimp"></a>
<table><tbody><tr id="row992mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p994mcpsimp"><a name="p994mcpsimp"></a><a name="p994mcpsimp"></a><strong id="b2123156153619"><a name="b2123156153619"></a><a name="b2123156153619"></a>Instruction access fault      //①Exception type: such as instruction fetch exception, Stack overflow, PMP access fault, etc.</strong></p>
<p id="p995mcpsimp"><a name="p995mcpsimp"></a><a name="p995mcpsimp"></a><strong id="b1112835613615"><a name="b1112835613615"></a><a name="b1112835613615"></a>Memory map region access fault</strong></p>
<p id="p996mcpsimp"><a name="p996mcpsimp"></a><a name="p996mcpsimp"></a>task:app_Task            <strong id="b163071328374"><a name="b163071328374"></a><a name="b163071328374"></a> //②Name of the task where the exception occurred</strong></p>
<p id="p997mcpsimp"><a name="p997mcpsimp"></a><a name="p997mcpsimp"></a>thrdPid:0x3              <strong id="b1691825153718"><a name="b1691825153718"></a><a name="b1691825153718"></a> //③ID of the task where the exception occurred</strong></p>
<p id="p998mcpsimp"><a name="p998mcpsimp"></a><a name="p998mcpsimp"></a>type:0x1</p>
<p id="p999mcpsimp"><a name="p999mcpsimp"></a><a name="p999mcpsimp"></a>nestCnt:1               <strong id="b3657105374"><a name="b3657105374"></a><a name="b3657105374"></a>  //④Exception nesting count; >1 indicates that exception re-entry occurred during exception handling</strong></p>
<p id="p1000mcpsimp"><a name="p1000mcpsimp"></a><a name="p1000mcpsimp"></a>phase:Task</p>
<p id="p1001mcpsimp"><a name="p1001mcpsimp"></a><a name="p1001mcpsimp"></a>ccause:0x1</p>
<p id="p1002mcpsimp"><a name="p1002mcpsimp"></a><a name="p1002mcpsimp"></a>mcause:0x1</p>
<p id="p1003mcpsimp"><a name="p1003mcpsimp"></a><a name="p1003mcpsimp"></a><strong id="b193118331376"><a name="b193118331376"></a><a name="b193118331376"></a>mtval:0xfffffffffe </strong>         <strong id="b871961433714"><a name="b871961433714"></a><a name="b871961433714"></a>//⑤Memory address accessed when the exception occurred</strong></p>
<p id="p1004mcpsimp"><a name="p1004mcpsimp"></a><a name="p1004mcpsimp"></a>gp:0x110004</p>
<p id="p1005mcpsimp"><a name="p1005mcpsimp"></a><a name="p1005mcpsimp"></a>mstatus:0x1880</p>
<p id="p1006mcpsimp"><a name="p1006mcpsimp"></a><a name="p1006mcpsimp"></a><strong id="b914218413375"><a name="b914218413375"></a><a name="b914218413375"></a>mepc:0xfffffffffe </strong>        <strong id="b162811923113719"><a name="b162811923113719"></a><a name="b162811923113719"></a> //⑥Address of the instruction being executed when the exception occurred (can be reverse-looked up to find the corresponding code)</strong></p>
<p id="p1007mcpsimp"><a name="p1007mcpsimp"></a><a name="p1007mcpsimp"></a><strong id="b1935011453379"><a name="b1935011453379"></a><a name="b1935011453379"></a>ra:0x1161a8 </strong>           <strong id="b1838284993715"><a name="b1838284993715"></a><a name="b1838284993715"></a> //⑦Address of the next instruction of the parent function to which the faulting instruction belongs (can be reverse-looked up to find the function)</strong></p>
<p id="p1008mcpsimp"><a name="p1008mcpsimp"></a><a name="p1008mcpsimp"></a>sp:0x103930           <strong id="b1896715220376"><a name="b1896715220376"></a><a name="b1896715220376"></a> //⑧Stack pointer of the task or interrupt when the exception occurred</strong></p>
<p id="p1009mcpsimp"><a name="p1009mcpsimp"></a><a name="p1009mcpsimp"></a>tp:0xfc631c8</p>
<p id="p1010mcpsimp"><a name="p1010mcpsimp"></a><a name="p1010mcpsimp"></a>t0:0x103875</p>
<p id="p1011mcpsimp"><a name="p1011mcpsimp"></a><a name="p1011mcpsimp"></a>t1:0xa</p>
<p id="p1012mcpsimp"><a name="p1012mcpsimp"></a><a name="p1012mcpsimp"></a>t2:0x11012000</p>
<p id="p1013mcpsimp"><a name="p1013mcpsimp"></a><a name="p1013mcpsimp"></a>s0:0x3</p>
<p id="p1014mcpsimp"><a name="p1014mcpsimp"></a><a name="p1014mcpsimp"></a>s1:0x119338</p>
</td>
</tr>
</tbody>
</table>

Note: Reverse lookup by instruction address means searching for the address in the ELF file, which will match the address of a line of assembly code in the code segment. Example:

Reverse lookup mepc:0x115df4, search for 115df4 in the ELF, indicating that the instruction being executed when the exception occurred is sw a0,0\(a1\).

<a name="table1017mcpsimp"></a>
<table><tbody><tr id="row1021mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1023mcpsimp"><a name="p1023mcpsimp"></a><a name="p1023mcpsimp"></a>00115dd8 &lt;app_init&gt;:</p>
<p id="p1024mcpsimp"><a name="p1024mcpsimp"></a><a name="p1024mcpsimp"></a>115dc: 717d addi sp,sp,-16</p>
<p id="p1025mcpsimp"><a name="p1025mcpsimp"></a><a name="p1025mcpsimp"></a>115de0: c606 sw ra,12(sp)</p>
<p id="p1026mcpsimp"><a name="p1026mcpsimp"></a><a name="p1026mcpsimp"></a>115de4: 00108b2a051f l.li a0,108b2a &lt;g_xRegsMap+0x56c&gt;</p>
<p id="p1027mcpsimp"><a name="p1027mcpsimp"></a><a name="p1027mcpsimp"></a>115de8: 7f0000ef jal ra,101196</p>
<p id="p1028mcpsimp"><a name="p1028mcpsimp"></a><a name="p1028mcpsimp"></a>115dec: 12345678051f l.li a0,12345678 &lt;__heap_end+0x12225678&gt;</p>
<p id="p1029mcpsimp"><a name="p1029mcpsimp"></a><a name="p1029mcpsimp"></a>115df0: 018005b7 lui a1,0x1800</p>
<p id="p1030mcpsimp"><a name="p1030mcpsimp"></a><a name="p1030mcpsimp"></a><strong id="b961497103819"><a name="b961497103819"></a><a name="b961497103819"></a>115df4: c188 sw a0,0(a1)</strong></p>
<p id="p1031mcpsimp"><a name="p1031mcpsimp"></a><a name="p1031mcpsimp"></a>115df8: 40b2 lw ra,12(sp)</p>
</td>
</tr>
</tbody>
</table>

## Overall Approach<a name="ZH-CN_TOPIC_0000002555654487"></a>

Based on the experience in handling historical issues, the main causes of FBB-RTOS crash issues are summarized as follows:

-   Load/Store access fault caused by memory corruption
-   Stack overflow
-   Instruction access fault (instruction fetch exception)
-   Watchdog timeout (Watchdog Timeout)
-   Out Of Memory
-   Panic
-   Illegal memory access: including access to reserved memory (Store/AMO access fault) and PMP-protected memory (PMP access fault)
-   Unaligned memory layout
-   Deadlock (Dead Lock)
-   Unaligned access (Unaligned Access)

The following chapters will systematically cover the above types of exceptions through typical problem cases, providing troubleshooting ideas and solutions in combination with real scenarios to help developers quickly identify the root cause of problems and efficiently fix system exceptions.

For fault location of crash issues, a layered and progressive analysis method can be adopted. The specific implementation steps are as follows:

-   **Trace the root cause by exception type**

    The exception type information in the crash log is generated by FBB-RTOS by parsing hardware exception registers such as mcause and ccause, which directly reflects the hardware-level or system-level exception event that triggered the crash. During analysis:

    First, lock down the exception type recorded in the log (such as instruction fetch exception, stack overflow, etc.) to identify the most direct exception trigger.

    Analyze possible causes based on the exception type (for example, the cause of an instruction fetch exception may be an abnormal function pointer or an abnormal code segment).

    Investigate and analyze the possible causes one by one.

-   **Investigate the code logic in the exception context**

    Analyzing the key register values ra, mepc, and mtval can respectively reveal the specific function being executed, the specific assembly instruction, and the memory address accessed when the crash occurred, so that the code logic in the exception context can be investigated and analyzed.

-   **Use DFX tools for dynamic diagnosis**

    When conventional analysis cannot locate the issue, enable the DFX mechanism, turn on kernel debugging configurations (such as backtrace, memory access monitoring trigger, etc.), recompile, and reproduce the problem to obtain more detailed runtime data.

# Crash Troubleshooting Guide<a name="ZH-CN_TOPIC_0000002524734536"></a>

Common key exception information and their corresponding direct crash causes are shown in the following table. Each will be elaborated in detail in the following sections.

<a name="table768mcpsimp"></a>
<table><thead align="left"><tr id="row773mcpsimp"><th class="cellrowborder" valign="top" width="45%" id="mcps1.1.3.1.1"><p id="p775mcpsimp"><a name="p775mcpsimp"></a><a name="p775mcpsimp"></a><strong id="b776mcpsimp"><a name="b776mcpsimp"></a><a name="b776mcpsimp"></a>Key Exception Information</strong></p>
</th>
<th class="cellrowborder" valign="top" width="55.00000000000001%" id="mcps1.1.3.1.2"><p id="p778mcpsimp"><a name="p778mcpsimp"></a><a name="p778mcpsimp"></a><strong id="b779mcpsimp"><a name="b779mcpsimp"></a><a name="b779mcpsimp"></a>Crash Cause</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row780mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p782mcpsimp"><a name="p782mcpsimp"></a><a name="p782mcpsimp"></a>Stack overflow</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p784mcpsimp"><a name="p784mcpsimp"></a><a name="p784mcpsimp"></a>Stack overflow</p>
</td>
</tr>
<tr id="row785mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p787mcpsimp"><a name="p787mcpsimp"></a><a name="p787mcpsimp"></a>Instruction access fault</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p789mcpsimp"><a name="p789mcpsimp"></a><a name="p789mcpsimp"></a>Instruction fetch exception</p>
</td>
</tr>
<tr id="row790mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p792mcpsimp"><a name="p792mcpsimp"></a><a name="p792mcpsimp"></a>Oops:NMI</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p794mcpsimp"><a name="p794mcpsimp"></a><a name="p794mcpsimp"></a>Watchdog timeout</p>
</td>
</tr>
<tr id="row795mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p797mcpsimp"><a name="p797mcpsimp"></a><a name="p797mcpsimp"></a>Panic</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p799mcpsimp"><a name="p799mcpsimp"></a><a name="p799mcpsimp"></a>Active Panic</p>
</td>
</tr>
<tr id="row800mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p802mcpsimp"><a name="p802mcpsimp"></a><a name="p802mcpsimp"></a>PMP access fault</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p804mcpsimp"><a name="p804mcpsimp"></a><a name="p804mcpsimp"></a>Access to a PMP-protected address</p>
</td>
</tr>
<tr id="row805mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p807mcpsimp"><a name="p807mcpsimp"></a><a name="p807mcpsimp"></a>Store/AMO access fault</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p809mcpsimp"><a name="p809mcpsimp"></a><a name="p809mcpsimp"></a>Access to reserved memory</p>
</td>
</tr>
<tr id="row810mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p812mcpsimp"><a name="p812mcpsimp"></a><a name="p812mcpsimp"></a>Dead lock</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p814mcpsimp"><a name="p814mcpsimp"></a><a name="p814mcpsimp"></a>Deadlock</p>
</td>
</tr>
<tr id="row815mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p817mcpsimp"><a name="p817mcpsimp"></a><a name="p817mcpsimp"></a>Load/Store address misaligned</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p819mcpsimp"><a name="p819mcpsimp"></a><a name="p819mcpsimp"></a>Unaligned access</p>
</td>
</tr>
</tbody>
</table>




## Stack Overflow<a name="ZH-CN_TOPIC_0000002555814461"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574586"></a>

FBB-RTOS enables stack overflow detection by default. The detection methods include magic word detection and hardware stack detection.

-   Magic word detection principle: A 4-byte (32-bit) magic word is filled at the top of the stack. During a task switch, the software checks whether the magic word has been modified. If the magic word has been modified, it is determined to be a stack overflow.
-   Hardware stack detection principle: Some chips provide a stack limit register. During a task switch or interrupt, the system writes the stack top pointer of the new task into the stack limit register, and the chip hardware automatically detects whether the stack pointer SP exceeds the boundary.

    When a stack overflow is detected, the system hangs and outputs "stack overflow" in the exception type. Example:

    <a name="table1339mcpsimp"></a>
    <table><tbody><tr id="row1343mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1345mcpsimp"><a name="p1345mcpsimp"></a><a name="p1345mcpsimp"></a>[2025-10-30 21:47:07] CURRENT task ID: <strong id="b1546192413818"><a name="b1546192413818"></a><a name="b1546192413818"></a>Task_A:9 stack overflow!</strong></p>
    </td>
    </tr>
    </tbody>
    </table>

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654489"></a>

-   **Oversized local variables**: Defining extremely large arrays or complex structures within a function.

-   **Insufficient stack space allocation**: **No safety margin is reserved**, that is, when setting the task stack size, the stack requirements of the worst-case execution path (such as exception handling branches) are not considered.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734538"></a>

**Location Methods<a name="section893713318437"></a>**

1.  **Thread identification**: The specific thread where the stack overflow occurred can be determined through the task name and task ID (task ID:) in the system log.
2.  **Use static estimation tools**: Use the stack estimation tool to estimate the stack usage peak of tasks/functions, identify functions with excessive stack consumption (such as functions containing large local variables), and use the task command to check the currently configured task stack size to determine whether the function stack overhead is too large or the configuration is unreasonable. For the usage of the tool, see the LiteOS Development Guide (limitation: the analysis of function pointer call chains may have errors).

**Reference Case<a name="section164812434435"></a>**

<a name="table1361mcpsimp"></a>
<table><tbody><tr id="row1365mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1367mcpsimp"><a name="p1367mcpsimp"></a><a name="p1367mcpsimp"></a>[2025-10-30 21:47:07] CURRENT task ID: <strong id="b811043433810"><a name="b811043433810"></a><a name="b811043433810"></a>Task_A:9 stack overflow!</strong></p>
<p id="p1368mcpsimp"><a name="p1368mcpsimp"></a><a name="p1368mcpsimp"></a>[2025-10-30 21:47:07] B</p>
<p id="p1369mcpsimp"><a name="p1369mcpsimp"></a><a name="p1369mcpsimp"></a>[2025-10-30 21:47:41] breakpoint</p>
<p id="p1370mcpsimp"><a name="p1370mcpsimp"></a><a name="p1370mcpsimp"></a>[2025-10-30 21:47:41] Not available</p>
<p id="p1371mcpsimp"><a name="p1371mcpsimp"></a><a name="p1371mcpsimp"></a>[2025-10-30 21:47:41] APP&gt;exception:42</p>
<p id="p1372mcpsimp"><a name="p1372mcpsimp"></a><a name="p1372mcpsimp"></a>[2025-10-30 21:47:41] task:Task_A</p>
<p id="p1373mcpsimp"><a name="p1373mcpsimp"></a><a name="p1373mcpsimp"></a>[2025-10-30 21:47:41] thrdPid:0x9</p>
<p id="p1374mcpsimp"><a name="p1374mcpsimp"></a><a name="p1374mcpsimp"></a>[2025-10-30 21:47:41] type:0x42</p>
<p id="p1375mcpsimp"><a name="p1375mcpsimp"></a><a name="p1375mcpsimp"></a>[2025-10-30 21:47:41] nestCnt:1</p>
<p id="p1376mcpsimp"><a name="p1376mcpsimp"></a><a name="p1376mcpsimp"></a>[2025-10-30 21:47:41] phase:Task</p>
<p id="p1377mcpsimp"><a name="p1377mcpsimp"></a><a name="p1377mcpsimp"></a>[2025-10-30 21:47:41] ccause:0x73616870</p>
<p id="p1378mcpsimp"><a name="p1378mcpsimp"></a><a name="p1378mcpsimp"></a>[2025-10-30 21:47:41] mcause:0x61543a65</p>
<p id="p1379mcpsimp"><a name="p1379mcpsimp"></a><a name="p1379mcpsimp"></a>[2025-10-30 21:47:41] mtval:0xaab73</p>
<p id="p1380mcpsimp"><a name="p1380mcpsimp"></a><a name="p1380mcpsimp"></a>[2025-10-30 21:47:41] gp:0x0</p>
<p id="p1381mcpsimp"><a name="p1381mcpsimp"></a><a name="p1381mcpsimp"></a>[2025-10-30 21:47:41] mstatus:0x0</p>
<p id="p1382mcpsimp"><a name="p1382mcpsimp"></a><a name="p1382mcpsimp"></a>[2025-10-30 21:47:41] mepc:0x0</p>
<p id="p1383mcpsimp"><a name="p1383mcpsimp"></a><a name="p1383mcpsimp"></a>[2025-10-30 21:47:41] ra:0x37df6</p>
<p id="p1384mcpsimp"><a name="p1384mcpsimp"></a><a name="p1384mcpsimp"></a>[2025-10-30 21:47:41] sp:0x0</p>
</td>
</tr>
</tbody>
</table>

-   Based on the "stack overflow" in the log, it can be confirmed that this is a stack overflow issue.
-   Based on "task ID: Task\_A:9" in the log, it can be confirmed that the task where the stack overflow occurred is Task\_A.
-   The task command shows that the stack size is the default value, which is too small. The issue was resolved after adjusting the stack size.

## Instruction Fetch Exception<a name="ZH-CN_TOPIC_0000002555814463"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574588"></a>

An instruction fetch exception usually occurs when the CPU attempts to read an instruction from an illegal or non-executable memory address. The exception type is Instruction access fault. Example:

<a name="table579mcpsimp"></a>
<table><tbody><tr id="row583mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p585mcpsimp"><a name="p585mcpsimp"></a><a name="p585mcpsimp"></a><strong id="b24221343183817"><a name="b24221343183817"></a><a name="b24221343183817"></a>Instruction access fault</strong></p>
<p id="p586mcpsimp"><a name="p586mcpsimp"></a><a name="p586mcpsimp"></a><strong id="b134231643143818"><a name="b134231643143818"></a><a name="b134231643143818"></a>Memory map region access fault</strong></p>
</td>
</tr>
</tbody>
</table>

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654491"></a>

-   **Use of null/dangling pointers**: When a function pointer is null or uninitialized/unassigned, the function pointer value is a random value.

-   **Corrupted code segment**: Program and data are placed in adjacent memory regions. When a data write operation goes out of bounds (memcpy/memset), the code region may be rewritten.

-   **Code segment not copied**: When the device starts up, code is usually read from an external storage medium. If the code segment is not copied to the corresponding RAM during startup, the code segment will not exist.

-   **Linker script configuration issues**: The linker script supports configuring multiple code segments. When code segment A is linked to code segment B, the code segment will be relocated to the wrong code segment.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734540"></a>

**Location Methods<a name="section96841617104412"></a>**

-   **Check the function pointer**: Locate the exception code context based on mtval and ra, and check whether the exception is caused by a function pointer. If so, check whether the function pointer is a null pointer or a dangling pointer.

-   **Check the linker script**: Check whether the code segment where the faulting function resides has a copy operation. If so, check the linker script to see whether the source and destination addresses of the copy match expectations.

-   **Check code segment copying**: Compare whether the memory value at the runtime address of the faulting function is the same as the value of the first instruction of the function in the disassembly. If they differ, check whether the code segment has been corrupted or was not copied/was incorrectly copied.

-   **Code segment monitoring**: Use PMP to configure the code segment where the faulting function resides with RX permissions to monitor whether the code segment is corrupted.

**Reference Case<a name="section158209424512"></a>**

<a name="table1141mcpsimp"></a>
<table><tbody><tr id="row1145mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1147mcpsimp"><a name="p1147mcpsimp"></a><a name="p1147mcpsimp"></a><strong id="b1879317113919"><a name="b1879317113919"></a><a name="b1879317113919"></a>Instruction access fault            // Exception information</strong></p>
<p id="p1148mcpsimp"><a name="p1148mcpsimp"></a><a name="p1148mcpsimp"></a><strong id="b479518115391"><a name="b479518115391"></a><a name="b479518115391"></a>Memory map region access fault    // Exception information</strong></p>
<p id="p1149mcpsimp"><a name="p1149mcpsimp"></a><a name="p1149mcpsimp"></a>task:app_Task</p>
<p id="p1150mcpsimp"><a name="p1150mcpsimp"></a><a name="p1150mcpsimp"></a>thrdPid:0x3</p>
<p id="p1151mcpsimp"><a name="p1151mcpsimp"></a><a name="p1151mcpsimp"></a>type:0x1</p>
<p id="p1152mcpsimp"><a name="p1152mcpsimp"></a><a name="p1152mcpsimp"></a>nestCnt:1</p>
<p id="p1153mcpsimp"><a name="p1153mcpsimp"></a><a name="p1153mcpsimp"></a>phase:Task</p>
<p id="p1154mcpsimp"><a name="p1154mcpsimp"></a><a name="p1154mcpsimp"></a>ccause:0x1</p>
<p id="p1155mcpsimp"><a name="p1155mcpsimp"></a><a name="p1155mcpsimp"></a>mcause:0x1</p>
<p id="p1156mcpsimp"><a name="p1156mcpsimp"></a><a name="p1156mcpsimp"></a>mtval:0xfffffffffe</p>
<p id="p1157mcpsimp"><a name="p1157mcpsimp"></a><a name="p1157mcpsimp"></a>gp:0x110004</p>
<p id="p1158mcpsimp"><a name="p1158mcpsimp"></a><a name="p1158mcpsimp"></a>mstatus:0x1880</p>
<p id="p1159mcpsimp"><a name="p1159mcpsimp"></a><a name="p1159mcpsimp"></a><strong id="b15431112403913"><a name="b15431112403913"></a><a name="b15431112403913"></a>mepc:0xfffffffffe                // Faulting instruction accessed</strong></p>
<p id="p1160mcpsimp"><a name="p1160mcpsimp"></a><a name="p1160mcpsimp"></a><strong id="b44311224113917"><a name="b44311224113917"></a><a name="b44311224113917"></a>ra:0x1161a8                   // Parent function</strong></p>
<p id="p1161mcpsimp"><a name="p1161mcpsimp"></a><a name="p1161mcpsimp"></a>sp:0x103930</p>
<p id="p1162mcpsimp"><a name="p1162mcpsimp"></a><a name="p1162mcpsimp"></a>tp:0xfc631c8</p>
<p id="p1163mcpsimp"><a name="p1163mcpsimp"></a><a name="p1163mcpsimp"></a>t0:0x103875</p>
<p id="p1164mcpsimp"><a name="p1164mcpsimp"></a><a name="p1164mcpsimp"></a>t1:0xa</p>
<p id="p1165mcpsimp"><a name="p1165mcpsimp"></a><a name="p1165mcpsimp"></a>t2:0x11012000</p>
<p id="p1166mcpsimp"><a name="p1166mcpsimp"></a><a name="p1166mcpsimp"></a>s0:0x3</p>
<p id="p1167mcpsimp"><a name="p1167mcpsimp"></a><a name="p1167mcpsimp"></a>s1:0x119338</p>
</td>
</tr>
</tbody>
</table>

-   Locate the faulting function: Based on the ra value 0x807556, locate the function currently being executed in the disassembly file.

    <a name="table1170mcpsimp"></a>
    <table><tbody><tr id="row1174mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1176mcpsimp"><a name="p1176mcpsimp"></a><a name="p1176mcpsimp"></a>__attribute__((weak)) void app_init(void)</p>
    <p id="p1177mcpsimp"><a name="p1177mcpsimp"></a><a name="p1177mcpsimp"></a>{</p>
    <p id="p1178mcpsimp"><a name="p1178mcpsimp"></a><a name="p1178mcpsimp"></a>fn_test_t fn = (fn_test_t)(UINT32 *)<strong id="b13407183515393"><a name="b13407183515393"></a><a name="b13407183515393"></a>0xffffffff</strong>;</p>
    <p id="p1179mcpsimp"><a name="p1179mcpsimp"></a><a name="p1179mcpsimp"></a>fn();</p>
    <p id="p1180mcpsimp"><a name="p1180mcpsimp"></a><a name="p1180mcpsimp"></a>}</p>
    </td>
    </tr>
    </tbody>
    </table>

-   It is confirmed that there is a function pointer call in the function, and the function pointer is abnormal.

## Watchdog Timeout<a name="ZH-CN_TOPIC_0000002555814465"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574590"></a>

FBB-RTOS requires periodically kicking the watchdog (resetting the timer) during runtime. If the watchdog is not kicked on time, the watchdog timer overflows and generates an NMI exception, and "Oops:NMI" is output in the exception type. Example:

<a name="table565mcpsimp"></a>
<table><tbody><tr id="row569mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p571mcpsimp"><a name="p571mcpsimp"></a><a name="p571mcpsimp"></a>try to enter wfi</p>
<p id="p572mcpsimp"><a name="p572mcpsimp"></a><a name="p572mcpsimp"></a><strong id="b61751044183917"><a name="b61751044183917"></a><a name="b61751044183917"></a>Oops:NMI</strong></p>
<p id="p573mcpsimp"><a name="p573mcpsimp"></a><a name="p573mcpsimp"></a>task:pm_suspend_task</p>
<p id="p574mcpsimp"><a name="p574mcpsimp"></a><a name="p574mcpsimp"></a>thrdPid:0x6</p>
</td>
</tr>
</tbody>
</table>

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654493"></a>

-   **CPU resources occupied**
    -   CPU resources are occupied by interrupts and high-priority tasks. Specific causes include:
        1.  **Overlong interrupt handling**: Interrupt handling takes too long, or the interrupt cannot exit normally.
        2.  **Interrupt storm**: A peripheral generates a large number of interrupts, causing the CPU to be busy handling interrupts.
        3.  **Abnormal high-priority task**: A high-priority task keeps running due to a bug (for example, entering an infinite loop), causing the low-priority watchdog-kicking task to never get a time slice.

    -   **High-priority tasks keep preempting the CPU**: The system load is too high, and the watchdog-kicking task never gets its turn.

-   **Abnormal scheduling of the watchdog-kicking task**
    -   **Incorrect task parameters**: The period of the watchdog-kicking task is greater than the watchdog timeout threshold.
    -   **Task accidentally deleted**: An erroneous API call accidentally deletes the watchdog-kicking task.
    -   **Scheduler fault**: Abnormal task scheduling.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734542"></a>

**Location Methods<a name="section1233958164712"></a>**

-   **Preliminary analysis**

    Search the disassembly based on MEPC to investigate and analyze the code logic of the exception context.

-   **Problem analysis**

    To analyze the watchdog timeout issue, it is necessary to focus on the scheduling and execution of tasks (including interrupts) during the critical period before the system hangs (that is, within the watchdog kick timeout window). Specifically, the analysis can be performed from the following three dimensions:

    1.  **CPU idle status check**: If there is a CPU idle period, it indicates abnormal scheduling of the watchdog-kicking task.
    2.  **Task CPU usage analysis**: If a task's CPU usage is significantly abnormal, the task may have fallen into an infinite loop or a logic error.
    3.  **System load evaluation**: If frequent task switching occurs and CPU utilization remains at full load, the overall system load is too high, preventing the watchdog-kicking task from being scheduled in time.

    The information for the above three dimensions can be obtained through the DFX tool trace or scheduling statistics provided by the system. For the specific usage of trace and scheduling statistics, refer to the "Trace" chapter and the "Scheduling Statistics" chapter of the LiteOS Development Guide respectively.

-   **Diagnostic method for tasks with abnormally high CPU usage**

    If a task is found to have abnormally high CPU usage, its complete call stack needs to be obtained to precisely locate the problematic code. You can enable the system's backtrace feature and add output of the call stacks of all tasks in the NMI exception.

**Reference Case<a name="section5928114265516"></a>**

<a name="table848mcpsimp"></a>
<table><tbody><tr id="row852mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p854mcpsimp"><a name="p854mcpsimp"></a><a name="p854mcpsimp"></a>[APP][00026106]:[INFO app_pm_suspend-&gt;15]:app_pm_suspend</p>
<p id="p855mcpsimp"><a name="p855mcpsimp"></a><a name="p855mcpsimp"></a>pm_suspend.</p>
<p id="p856mcpsimp"><a name="p856mcpsimp"></a><a name="p856mcpsimp"></a>try to enter wfi</p>
<p id="p857mcpsimp"><a name="p857mcpsimp"></a><a name="p857mcpsimp"></a><strong id="b1190115313914"><a name="b1190115313914"></a><a name="b1190115313914"></a>Oops:NMI</strong></p>
<p id="p858mcpsimp"><a name="p858mcpsimp"></a><a name="p858mcpsimp"></a>task:pm_suspend_task</p>
<p id="p859mcpsimp"><a name="p859mcpsimp"></a><a name="p859mcpsimp"></a>thrdPid:0x6</p>
<p id="p860mcpsimp"><a name="p860mcpsimp"></a><a name="p860mcpsimp"></a>type:0xc</p>
<p id="p861mcpsimp"><a name="p861mcpsimp"></a><a name="p861mcpsimp"></a>nestCnt:0</p>
<p id="p862mcpsimp"><a name="p862mcpsimp"></a><a name="p862mcpsimp"></a>phase:1</p>
<p id="p863mcpsimp"><a name="p863mcpsimp"></a><a name="p863mcpsimp"></a>ccause:0x2</p>
<p id="p864mcpsimp"><a name="p864mcpsimp"></a><a name="p864mcpsimp"></a>mcause:0x8000000c</p>
<p id="p865mcpsimp"><a name="p865mcpsimp"></a><a name="p865mcpsimp"></a>mtval:0x0</p>
<p id="p866mcpsimp"><a name="p866mcpsimp"></a><a name="p866mcpsimp"></a>gp:0x7720572a</p>
<p id="p867mcpsimp"><a name="p867mcpsimp"></a><a name="p867mcpsimp"></a>mstatus:0x1880</p>
<p id="p868mcpsimp"><a name="p868mcpsimp"></a><a name="p868mcpsimp"></a><strong id="b122301928404"><a name="b122301928404"></a><a name="b122301928404"></a>mepc:0x1182c4</strong></p>
<p id="p869mcpsimp"><a name="p869mcpsimp"></a><a name="p869mcpsimp"></a>ra:0x1182bc</p>
<p id="p870mcpsimp"><a name="p870mcpsimp"></a><a name="p870mcpsimp"></a>sp:0x103920</p>
</td>
</tr>
</tbody>
</table>

According to the mepc value 0x1182c4, check the disassembly:

<a name="table872mcpsimp"></a>
<table><tbody><tr id="row876mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p878mcpsimp"><a name="p878mcpsimp"></a><a name="p878mcpsimp"></a>001182C0 &lt;wfi_loop&gt;:</p>
<p id="p879mcpsimp"><a name="p879mcpsimp"></a><a name="p879mcpsimp"></a>1182c0: 10500073	   wfi</p>
<p id="p880mcpsimp"><a name="p880mcpsimp"></a><a name="p880mcpsimp"></a><strong id="b778210136409"><a name="b778210136409"></a><a name="b778210136409"></a>1182c4: bff5	            j 1182c0 &lt;wfi_loop&gt;</strong></p>
<p id="p881mcpsimp"><a name="p881mcpsimp"></a><a name="p881mcpsimp"></a>1182c6: bfcd	            j 1182b8 &lt;drv_pm_suspend+0x76&gt;</p>
</td>
</tr>
</tbody>
</table>

Find the corresponding code:

<a name="table883mcpsimp"></a>
<table><tbody><tr id="row887mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p889mcpsimp"><a name="p889mcpsimp"></a><a name="p889mcpsimp"></a>while (1)  {</p>
<p id="p890mcpsimp"><a name="p890mcpsimp"></a><a name="p890mcpsimp"></a>pm_printk("try to enter wfi\n");</p>
<p id="p891mcpsimp"><a name="p891mcpsimp"></a><a name="p891mcpsimp"></a>asm volatile("fence\n\r"</p>
<p id="p892mcpsimp"><a name="p892mcpsimp"></a><a name="p892mcpsimp"></a>"wfi_loop:\n\r"</p>
<p id="p893mcpsimp"><a name="p893mcpsimp"></a><a name="p893mcpsimp"></a>"wfi\n\r"</p>
<p id="p894mcpsimp"><a name="p894mcpsimp"></a><a name="p894mcpsimp"></a>"j wfi_loop\n\r");</p>
<p id="p895mcpsimp"><a name="p895mcpsimp"></a><a name="p895mcpsimp"></a>}</p>
</td>
</tr>
</tbody>
</table>

This indicates that the system has entered low-power/standby mode, in which only interrupts can wake it up. Analyzing the interrupt intervals reveals that the interrupt frequency is lower than the watchdog kick period, causing a watchdog timeout reset, which falls into the category of scheduling anomalies.

## Panic<a name="ZH-CN_TOPIC_0000002555814467"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574592"></a>

An active software Panic is a proactive termination mechanism adopted by the system for unrecoverable errors or serious violations of system rules. The system outputs detailed error diagnostic information, mainly including the following key contents:

-   **Error description**: The cause of the panic (for example, "ASSERT ERROR!  at xxx.c:123").
-   **Context of the currently running task**: Current task name, task ID, and register values.

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654495"></a>

-   **Assertion**: The LOS\_ASSERT\(expr\) macro is triggered when the condition is not satisfied, usually indicating a program logic error or an abnormal system state.

-   **LOS\_Panic**: The LOS\_Panic\(\) function is called when critical system exceptions are detected, such as repeated memory release or corruption of the heap memory node header.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734544"></a>

1.  **Location methods**

-   **Preliminary location of the Panic source**

    If the log contains a file name and line number, directly view the corresponding source code to confirm the problem location.

    Search for the printed information in the code, or combine it with mepc (PC register value) to locate the hung code line.

    If it is an assertion failure, check the assertion expression and analyze why it does not hold (such as null pointer, out-of-bounds, illegal state, etc.).

-   **In-depth investigation based on the LOS\_PANIC cause**

    Based on the LOS\_PANIC cause, such as repeated memory release or heap memory node header corruption, refer to the analysis methods in the corresponding chapters.

**Reference Case<a name="section16978820165611"></a>**

**Example 1: Assertion failure**

<a name="table181143365716"></a>
<table><tbody><tr id="row4111133155716"><td class="cellrowborder" valign="top" width="100%"><p id="p91113332578"><a name="p91113332578"></a><a name="p91113332578"></a><strong id="b63758254407"><a name="b63758254407"></a><a name="b63758254407"></a>ASSERT ERROR! los_cpup.c, 378, OsCpupGetCycle</strong></p>
<p id="p711123319571"><a name="p711123319571"></a><a name="p711123319571"></a>task:CpupGuardCreator</p>
<p id="p13111033125718"><a name="p13111033125718"></a><a name="p13111033125718"></a>thrdPid:0x0</p>
<p id="p13118334572"><a name="p13118334572"></a><a name="p13118334572"></a>type:0x2</p>
<p id="p011133165717"><a name="p011133165717"></a><a name="p011133165717"></a>nestCnt:1</p>
<p id="p1911113312577"><a name="p1911113312577"></a><a name="p1911113312577"></a>phase:1</p>
<p id="p311173316571"><a name="p311173316571"></a><a name="p311173316571"></a>ccause:0x0</p>
<p id="p511133316572"><a name="p511133316572"></a><a name="p511133316572"></a>mcause:0x0</p>
<p id="p1611133317576"><a name="p1611133317576"></a><a name="p1611133317576"></a>mtval:0x0</p>
<p id="p8117335579"><a name="p8117335579"></a><a name="p8117335579"></a>gp:0x0</p>
<p id="p131110332576"><a name="p131110332576"></a><a name="p131110332576"></a>mstatus:0x0</p>
<p id="p1511143355710"><a name="p1511143355710"></a><a name="p1511143355710"></a>mepc:0x0</p>
<p id="p61113332571"><a name="p61113332571"></a><a name="p61113332571"></a>ra:0xd</p>
<p id="p171173395715"><a name="p171173395715"></a><a name="p171173395715"></a>sp:0x0</p>
</td>
</tr>
</tbody>
</table>

From the above exception print information, we can know:

Exception location: line 378 of los\_cpup.c.

Assertion condition: LOS\_ASSERT\(cycles \>= g\_startCycles\).

Direct cause: The system detected that the cycles value is less than g\_startCycles, violating the expected logic.

**Example 2: LOS\_PANIC example**

<a name="table234mcpsimp"></a>
<table><tbody><tr id="row238mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p240mcpsimp"><a name="p240mcpsimp"></a><a name="p240mcpsimp"></a>The node:0x112270 is not used!</p>
<p id="p241mcpsimp"><a name="p241mcpsimp"></a><a name="p241mcpsimp"></a>task:app_Task</p>
<p id="p242mcpsimp"><a name="p242mcpsimp"></a><a name="p242mcpsimp"></a>thrdPid:0x3</p>
<p id="p243mcpsimp"><a name="p243mcpsimp"></a><a name="p243mcpsimp"></a>type:0xb</p>
<p id="p244mcpsimp"><a name="p244mcpsimp"></a><a name="p244mcpsimp"></a>nestCnt:1</p>
<p id="p245mcpsimp"><a name="p245mcpsimp"></a><a name="p245mcpsimp"></a>phase:1</p>
<p id="p246mcpsimp"><a name="p246mcpsimp"></a><a name="p246mcpsimp"></a>ccause:0x0</p>
<p id="p247mcpsimp"><a name="p247mcpsimp"></a><a name="p247mcpsimp"></a>mcause:0xb</p>
<p id="p248mcpsimp"><a name="p248mcpsimp"></a><a name="p248mcpsimp"></a>mtval:0x0</p>
<p id="p249mcpsimp"><a name="p249mcpsimp"></a><a name="p249mcpsimp"></a>gp:0x10ff00</p>
<p id="p250mcpsimp"><a name="p250mcpsimp"></a><a name="p250mcpsimp"></a>mstatus:0x1800</p>
<p id="p251mcpsimp"><a name="p251mcpsimp"></a><a name="p251mcpsimp"></a><strong id="b9978233124011"><a name="b9978233124011"></a><a name="b9978233124011"></a>mepc:0x1008fe</strong></p>
<p id="p252mcpsimp"><a name="p252mcpsimp"></a><a name="p252mcpsimp"></a>ra:0x1008fe</p>
<p id="p253mcpsimp"><a name="p253mcpsimp"></a><a name="p253mcpsimp"></a>sp:0x111690</p>
</td>
</tr>
</tbody>
</table>

Exception location: Reverse-lookup the code segment in the disassembly file based on the mepc value, or search for the printed information in the source code, to find the Panic source LOS\_PANIC\("The node:%p is not used!\\n", node\).

## Accessing PMP-Protected Memory<a name="ZH-CN_TOPIC_0000002555814469"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574594"></a>

After PMP is configured on the system, permission checks are performed on bus instruction fetches, data accesses, and data stores according to the PMP configuration. If a check fails, an exception is reported (the ongoing instruction fetch, data access, or data store operation is not executed). "PMP access fault" is output in the exception information, and the exception type also clearly indicates the type of the exceptional operation.

-   Instruction access fault // The exceptional operation is "instruction fetch"
-   Load access fault// The exceptional operation is "Load"
-   Store/AMO access fault // The exceptional operation is "Store"

Example:

<a name="table594mcpsimp"></a>
<table><tbody><tr id="row598mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p600mcpsimp"><a name="p600mcpsimp"></a><a name="p600mcpsimp"></a>Instruction access fault</p>
<p id="p601mcpsimp"><a name="p601mcpsimp"></a><a name="p601mcpsimp"></a><strong id="b042254110402"><a name="b042254110402"></a><a name="b042254110402"></a>PMP access fault</strong></p>
</td>
</tr>
</tbody>
</table>

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654497"></a>

-   Mismatch between operations and permissions. A PMP exception is reported in the following cases, where × indicates that an exception is reported:

    <a name="table1423mcpsimp"></a>
    <table><thead align="left"><tr id="row1430mcpsimp"><th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.1"><p id="p1432mcpsimp"><a name="p1432mcpsimp"></a><a name="p1432mcpsimp"></a>Operation/Permission</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.2"><p id="p1434mcpsimp"><a name="p1434mcpsimp"></a><a name="p1434mcpsimp"></a>R</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.3"><p id="p1436mcpsimp"><a name="p1436mcpsimp"></a><a name="p1436mcpsimp"></a>W</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.4"><p id="p1438mcpsimp"><a name="p1438mcpsimp"></a><a name="p1438mcpsimp"></a>X</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1439mcpsimp"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="p1441mcpsimp"><a name="p1441mcpsimp"></a><a name="p1441mcpsimp"></a>Instruction fetch</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 "><p id="p1443mcpsimp"><a name="p1443mcpsimp"></a><a name="p1443mcpsimp"></a>×</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><p id="p1445mcpsimp"><a name="p1445mcpsimp"></a><a name="p1445mcpsimp"></a>×</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 ">&nbsp;&nbsp;</td>
    </tr>
    <tr id="row1447mcpsimp"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="p1449mcpsimp"><a name="p1449mcpsimp"></a><a name="p1449mcpsimp"></a>Load</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 ">&nbsp;&nbsp;</td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><p id="p1452mcpsimp"><a name="p1452mcpsimp"></a><a name="p1452mcpsimp"></a>×</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 "><p id="p1454mcpsimp"><a name="p1454mcpsimp"></a><a name="p1454mcpsimp"></a>×</p>
    </td>
    </tr>
    <tr id="row1455mcpsimp"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="p1457mcpsimp"><a name="p1457mcpsimp"></a><a name="p1457mcpsimp"></a>Store</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 "><p id="p1459mcpsimp"><a name="p1459mcpsimp"></a><a name="p1459mcpsimp"></a>×</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 ">&nbsp;&nbsp;</td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 "><p id="p1462mcpsimp"><a name="p1462mcpsimp"></a><a name="p1462mcpsimp"></a>×</p>
    </td>
    </tr>
    </tbody>
    </table>

-   PMP exceptions can also be triggered in the following scenarios.

    Operations that cross PMP regions, for example: reading 4 bytes of data where the first 2 bytes are in region A and the last 2 bytes are in region B.

    PMP entry ≥ 1, and the memory access does not match any PMP entry.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734546"></a>

**Location Methods<a name="section55480256474"></a>**

-   **Locate the faulting instruction address via mepc**

    Based on the mepc register value, confirm the address of the instruction that the CPU attempted to execute when the exception occurred.

-   **Confirm the exceptional access address via mtval**

    Based on mtval, confirm the memory address accessed (for Load/Store exceptions) or the instruction address (for instruction fetch exceptions) when the exception occurred.

-   **If the exceptional address/instruction matches the expected memory layout, check the PMP configuration**

    If the faulting instruction address or the accessed address matches the system memory layout (for example, located in a legal code segment, data segment, stack, etc.), first check whether the PMP (Physical Memory Protection) configuration is correct.

-   **If the faulting instruction (fetch) does not match expectations**, refer to the "[Instruction Fetch Exception](instruction_fetch_exception.md)" chapter.
-   **If the faulting instruction accesses a memory region not covered by PMP configuration, refer to the memory corruption chapter for location.**

**Reference Case<a name="section17222182674819"></a>**

<a name="table691mcpsimp"></a>
<table><tbody><tr id="row695mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p697mcpsimp"><a name="p697mcpsimp"></a><a name="p697mcpsimp"></a>Instruction access fault</p>
<p id="p698mcpsimp"><a name="p698mcpsimp"></a><a name="p698mcpsimp"></a><strong id="b299825324017"><a name="b299825324017"></a><a name="b299825324017"></a>PMP access fault</strong></p>
<p id="p699mcpsimp"><a name="p699mcpsimp"></a><a name="p699mcpsimp"></a>APP exception:1</p>
<p id="p700mcpsimp"><a name="p700mcpsimp"></a><a name="p700mcpsimp"></a>task: at</p>
<p id="p701mcpsimp"><a name="p701mcpsimp"></a><a name="p701mcpsimp"></a>thrdPid:0xb</p>
<p id="p702mcpsimp"><a name="p702mcpsimp"></a><a name="p702mcpsimp"></a>type:0x1</p>
<p id="p703mcpsimp"><a name="p703mcpsimp"></a><a name="p703mcpsimp"></a>nestCnt:1</p>
<p id="p704mcpsimp"><a name="p704mcpsimp"></a><a name="p704mcpsimp"></a>phase:Task</p>
<p id="p705mcpsimp"><a name="p705mcpsimp"></a><a name="p705mcpsimp"></a>ccause:0x7</p>
<p id="p706mcpsimp"><a name="p706mcpsimp"></a><a name="p706mcpsimp"></a>mcause:0x38000001</p>
<p id="p707mcpsimp"><a name="p707mcpsimp"></a><a name="p707mcpsimp"></a><strong id="b18352026419"><a name="b18352026419"></a><a name="b18352026419"></a>mtval:0x22082444</strong></p>
<p id="p708mcpsimp"><a name="p708mcpsimp"></a><a name="p708mcpsimp"></a>gp:0x10017bed</p>
<p id="p709mcpsimp"><a name="p709mcpsimp"></a><a name="p709mcpsimp"></a>mstatus:0x80207880</p>
<p id="p710mcpsimp"><a name="p710mcpsimp"></a><a name="p710mcpsimp"></a><strong id="b1679825124119"><a name="b1679825124119"></a><a name="b1679825124119"></a>mepc:0x22082444</strong></p>
<p id="p711mcpsimp"><a name="p711mcpsimp"></a><a name="p711mcpsimp"></a>ra:0x2b09e</p>
<p id="p712mcpsimp"><a name="p712mcpsimp"></a><a name="p712mcpsimp"></a>sp:0x1003f5e0</p>
</td>
</tr>
</tbody>
</table>

-   Exception address location: According to mepc, the address accessed by the exception is 0x22082444. mtval confirms that the protected address is also 0x22082444, indicating that this address has not been configured with executable permission, but the system attempted to fetch an instruction from it.
-   Check the PMP permission configuration: Check the PMP configuration for this memory in the code and confirm whether the PMP permissions are configured reasonably based on business requirements.

    <a name="table716mcpsimp"></a>
    <table><tbody><tr id="row720mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p722mcpsimp"><a name="p722mcpsimp"></a><a name="p722mcpsimp"></a>pmpRegion.accPermission.readAcc = E_MEM_RD_ACC_RD;</p>
    <p id="p723mcpsimp"><a name="p723mcpsimp"></a><a name="p723mcpsimp"></a>pmpRegion.accPermission.writeAcc = E_MEM_WR_ACC_NON_WR;</p>
    <p id="p724mcpsimp"><a name="p724mcpsimp"></a><a name="p724mcpsimp"></a>pmpRegion.accPermission.executeAcc = E_MEM_EX_ACC_NON_EX;</p>
    <p id="p725mcpsimp"><a name="p725mcpsimp"></a><a name="p725mcpsimp"></a>pmpRegion.memAttr = MEM_ATTR_DEV_NON_BUF;</p>
    <p id="p726mcpsimp"><a name="p726mcpsimp"></a><a name="p726mcpsimp"></a>pmpRegion.blocked = FALSE;</p>
    <p id="p727mcpsimp"><a name="p727mcpsimp"></a><a name="p727mcpsimp"></a>pmpRegion.ucaAddressMatch = PMP_RGN_ADDR_MATCH_NAPOT;</p>
    <p id="p728mcpsimp"><a name="p728mcpsimp"></a><a name="p728mcpsimp"></a>/* Configure nonsecure pagetable */</p>
    <p id="p729mcpsimp"><a name="p729mcpsimp"></a><a name="p729mcpsimp"></a>pmpRegion.ucNumber = PMP_REGION_NS_PAGE_TABLE_START;</p>
    <p id="p730mcpsimp"><a name="p730mcpsimp"></a><a name="p730mcpsimp"></a>pmpRegion.uwBaseAddress = pt-&gt;nonsec.baseAddr;</p>
    <p id="p731mcpsimp"><a name="p731mcpsimp"></a><a name="p731mcpsimp"></a>pmpRegion.uwRegionSize = pt-&gt;nonsec.tableSize;</p>
    <p id="p732mcpsimp"><a name="p732mcpsimp"></a><a name="p732mcpsimp"></a>pmpRegion.sectl = SEC_CONTROl_NOSECURE_NONMMU;</p>
    <p id="p733mcpsimp"><a name="p733mcpsimp"></a><a name="p733mcpsimp"></a>ret = ArchProtectionRegionSet(&amp;pmpRegion);</p>
    <p id="p734mcpsimp"><a name="p734mcpsimp"></a><a name="p734mcpsimp"></a>if (ret != LOS_OK) {</p>
    <p id="p735mcpsimp"><a name="p735mcpsimp"></a><a name="p735mcpsimp"></a>PRINT_ERR("ArchProtectionRegionSet failed!!", _FUNCTION_, __LINE__, ret);</p>
    <p id="p736mcpsimp"><a name="p736mcpsimp"></a><a name="p736mcpsimp"></a>return LOS_NOK;</p>
    <p id="p737mcpsimp"><a name="p737mcpsimp"></a><a name="p737mcpsimp"></a>}</p>
    </td>
    </tr>
    </tbody>
    </table>

## Accessing Reserved Memory<a name="ZH-CN_TOPIC_0000002555814471"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574596"></a>

Accessing the reserved address space triggers an exception. The exception information contains Store/AMO access fault and does not contain PMP access fault.

Example:

<a name="table260mcpsimp"></a>
<table><tbody><tr id="row264mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p266mcpsimp"><a name="p266mcpsimp"></a><a name="p266mcpsimp"></a><strong id="b14631327134112"><a name="b14631327134112"></a><a name="b14631327134112"></a>Store/AMO access fault      // Exception information</strong></p>
<p id="p267mcpsimp"><a name="p267mcpsimp"></a><a name="p267mcpsimp"></a>AXIM error response</p>
</td>
</tr>
</tbody>
</table>

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654499"></a>

The system accessed the reserved address space.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734548"></a>

**Location Methods<a name="section10405194804811"></a>**

-   **Locate the exceptional access address via mtval and verify its validity.**

    mtval can be used to lock down the memory address that the CPU attempted to access when the exception occurred. Combined with the address space allocation table provided by the system, confirm whether the address belongs to reserved addresses. If it is not a reserved address, check whether the address meets the memory alignment requirements, for the LINX core architecture.

    lw / sw (32-bit load/store): The address must be 4-byte aligned (that is, the address ends with 0x00, 0x04, 0x08, etc.).

    lh / sh (16-bit load/store): The address must be 2-byte aligned (that is, the address ends with 0x00, 0x02, etc.).

-   **Locate the faulting instruction address via mepc, reverse-lookup the disassembly, and locate the faulting source code.**

**Reference Case<a name="section124911642494"></a>**

<a name="table284mcpsimp"></a>
<table><tbody><tr id="row288mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p290mcpsimp"><a name="p290mcpsimp"></a><a name="p290mcpsimp"></a><strong id="b12704113564117"><a name="b12704113564117"></a><a name="b12704113564117"></a>Store/AMO access fault      // Exception information</strong></p>
<p id="p291mcpsimp"><a name="p291mcpsimp"></a><a name="p291mcpsimp"></a><strong id="b5705193534116"><a name="b5705193534116"></a><a name="b5705193534116"></a>AXIM error response        // Exception information</strong></p>
<p id="p292mcpsimp"><a name="p292mcpsimp"></a><a name="p292mcpsimp"></a>task:app_Task</p>
<p id="p293mcpsimp"><a name="p293mcpsimp"></a><a name="p293mcpsimp"></a>thrdPid:0x3</p>
<p id="p294mcpsimp"><a name="p294mcpsimp"></a><a name="p294mcpsimp"></a>type:0x7</p>
<p id="p295mcpsimp"><a name="p295mcpsimp"></a><a name="p295mcpsimp"></a>nestCnt:1</p>
<p id="p296mcpsimp"><a name="p296mcpsimp"></a><a name="p296mcpsimp"></a>phase:Task</p>
<p id="p297mcpsimp"><a name="p297mcpsimp"></a><a name="p297mcpsimp"></a>ccause:0x2</p>
<p id="p298mcpsimp"><a name="p298mcpsimp"></a><a name="p298mcpsimp"></a>mcause:0x7</p>
<p id="p299mcpsimp"><a name="p299mcpsimp"></a><a name="p299mcpsimp"></a>mtval:0x18000000          // Address of the exceptional access</p>
<p id="p300mcpsimp"><a name="p300mcpsimp"></a><a name="p300mcpsimp"></a>gp:0x110004</p>
<p id="p301mcpsimp"><a name="p301mcpsimp"></a><a name="p301mcpsimp"></a>mstatus:0x1880</p>
<p id="p302mcpsimp"><a name="p302mcpsimp"></a><a name="p302mcpsimp"></a>mepc:0x115df8            // Address of the instruction that triggered the exception</p>
<p id="p303mcpsimp"><a name="p303mcpsimp"></a><a name="p303mcpsimp"></a>ra:0x11687c</p>
<p id="p304mcpsimp"><a name="p304mcpsimp"></a><a name="p304mcpsimp"></a>sp:0x103910</p>
</td>
</tr>
</tbody>
</table>

-   Based on mtval, the memory address of the exceptional access can be locked down as 0x1800000, confirming it is a reserved memory address.
-   Reverse-looking up the disassembly file based on mepc reveals the line where the problematic code is located.

    <a name="table308mcpsimp"></a>
    <table><tbody><tr id="row312mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p314mcpsimp"><a name="p314mcpsimp"></a><a name="p314mcpsimp"></a>00115dd8 &lt;app_init&gt;:</p>
    <p id="p315mcpsimp"><a name="p315mcpsimp"></a><a name="p315mcpsimp"></a>115dc: 717d addi sp,sp,-16</p>
    <p id="p316mcpsimp"><a name="p316mcpsimp"></a><a name="p316mcpsimp"></a>115de0: c606 sw ra,12(sp)</p>
    <p id="p317mcpsimp"><a name="p317mcpsimp"></a><a name="p317mcpsimp"></a>115de4: 00108b2a051f l.li a0,108b2a &lt;g_xRegsMap+0x56c&gt;</p>
    <p id="p318mcpsimp"><a name="p318mcpsimp"></a><a name="p318mcpsimp"></a>115de8: 7f0000ef jal ra,101196</p>
    <p id="p319mcpsimp"><a name="p319mcpsimp"></a><a name="p319mcpsimp"></a>115dec: 12345678051f l.li a0,12345678 &lt;__heap_end+0x12225678&gt;</p>
    <p id="p320mcpsimp"><a name="p320mcpsimp"></a><a name="p320mcpsimp"></a>115df0: 018005b7 lui a1,0x1800</p>
    <p id="p321mcpsimp"><a name="p321mcpsimp"></a><a name="p321mcpsimp"></a><strong id="b107671951174114"><a name="b107671951174114"></a><a name="b107671951174114"></a>115df4: c188 sw a0,0(a1)</strong></p>
    <p id="p322mcpsimp"><a name="p322mcpsimp"></a><a name="p322mcpsimp"></a>115df8: 40b2 lw ra,12(sp)</p>
    <p id="p323mcpsimp"><a name="p323mcpsimp"></a><a name="p323mcpsimp"></a>115dfc: 6141 addi sp,sp,16</p>
    <p id="p324mcpsimp"><a name="p324mcpsimp"></a><a name="p324mcpsimp"></a>115e00: bdd9 j 100890 &lt;tc_mem_013_7&gt;</p>
    </td>
    </tr>
    </tbody>
    </table>

<a name="table325mcpsimp"></a>
<table><tbody><tr id="row329mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p331mcpsimp"><a name="p331mcpsimp"></a><a name="p331mcpsimp"></a>__attribute__((weak)) void app_init(void)</p>
<p id="p332mcpsimp"><a name="p332mcpsimp"></a><a name="p332mcpsimp"></a>{</p>
<p id="p333mcpsimp"><a name="p333mcpsimp"></a><a name="p333mcpsimp"></a>UINT32 t = 0x1800000;</p>
<p id="p334mcpsimp"><a name="p334mcpsimp"></a><a name="p334mcpsimp"></a>*(UINT32 *)t = 0x12345678;</p>
<p id="p335mcpsimp"><a name="p335mcpsimp"></a><a name="p335mcpsimp"></a>}</p>
</td>
</tr>
</tbody>
</table>

## Deadlock<a name="ZH-CN_TOPIC_0000002555814473"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574598"></a>

FBB-RTOS provides the deadlock detection DFX feature, which supports deadlock detection for four types of locks: spinlocks, mutexes, binary semaphores, and thread locks, as well as detection of repeated locking, erroneous release, and lock depth overflow. The related kernel configurations are as follows:

<a name="table103mcpsimp"></a>
<table><thead align="left"><tr id="row110mcpsimp"><th class="cellrowborder" valign="top" width="35%" id="mcps1.1.5.1.1"><p id="p112mcpsimp"><a name="p112mcpsimp"></a><a name="p112mcpsimp"></a>Configuration Item</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.1.5.1.2"><p id="p114mcpsimp"><a name="p114mcpsimp"></a><a name="p114mcpsimp"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.1.5.1.3"><p id="p116mcpsimp"><a name="p116mcpsimp"></a><a name="p116mcpsimp"></a>Default Value</p>
</th>
<th class="cellrowborder" valign="top" width="32%" id="mcps1.1.5.1.4"><p id="p118mcpsimp"><a name="p118mcpsimp"></a><a name="p118mcpsimp"></a>Dependency</p>
</th>
</tr>
</thead>
<tbody><tr id="row119mcpsimp"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p121mcpsimp"><a name="p121mcpsimp"></a><a name="p121mcpsimp"></a>LOSCFG_KERNEL_LOCKDEP</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p123mcpsimp"><a name="p123mcpsimp"></a><a name="p123mcpsimp"></a>Enable deadlock detection</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.1.5.1.3 "><p id="p125mcpsimp"><a name="p125mcpsimp"></a><a name="p125mcpsimp"></a>N</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.5.1.4 "><p id="p127mcpsimp"><a name="p127mcpsimp"></a><a name="p127mcpsimp"></a>LOSCFG_KERNEL_MEM_ALLOC</p>
</td>
</tr>
<tr id="row128mcpsimp"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p130mcpsimp"><a name="p130mcpsimp"></a><a name="p130mcpsimp"></a>LOSCFG_KERNEL_SPINDEP</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p132mcpsimp"><a name="p132mcpsimp"></a><a name="p132mcpsimp"></a>Enable spinlock deadlock detection</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.1.5.1.3 "><p id="p134mcpsimp"><a name="p134mcpsimp"></a><a name="p134mcpsimp"></a>N</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.5.1.4 "><p id="p136mcpsimp"><a name="p136mcpsimp"></a><a name="p136mcpsimp"></a>LOSCFG_KERNEL_SMP</p>
</td>
</tr>
<tr id="row137mcpsimp"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p139mcpsimp"><a name="p139mcpsimp"></a><a name="p139mcpsimp"></a>LOSCFG_KERNEL_MUXDEP</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p141mcpsimp"><a name="p141mcpsimp"></a><a name="p141mcpsimp"></a>Enable mutex deadlock detection</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.1.5.1.3 "><p id="p143mcpsimp"><a name="p143mcpsimp"></a><a name="p143mcpsimp"></a>N</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.5.1.4 "><p id="p145mcpsimp"><a name="p145mcpsimp"></a><a name="p145mcpsimp"></a>LOSCFG_BASE_IPC_MUX</p>
</td>
</tr>
<tr id="row146mcpsimp"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p148mcpsimp"><a name="p148mcpsimp"></a><a name="p148mcpsimp"></a>LOSCFG_KERNEL_SEMDEP</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p150mcpsimp"><a name="p150mcpsimp"></a><a name="p150mcpsimp"></a>Enable binary semaphore deadlock detection</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.1.5.1.3 "><p id="p152mcpsimp"><a name="p152mcpsimp"></a><a name="p152mcpsimp"></a>N</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.5.1.4 "><p id="p154mcpsimp"><a name="p154mcpsimp"></a><a name="p154mcpsimp"></a>LOSCFG_BASE_IPC_SEM</p>
</td>
</tr>
<tr id="row155mcpsimp"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p157mcpsimp"><a name="p157mcpsimp"></a><a name="p157mcpsimp"></a>LOSCFG_PTHREAD_MUXDEP</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p159mcpsimp"><a name="p159mcpsimp"></a><a name="p159mcpsimp"></a>Enable thread lock deadlock detection</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.1.5.1.3 "><p id="p161mcpsimp"><a name="p161mcpsimp"></a><a name="p161mcpsimp"></a>N</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.1.5.1.4 "><p id="p163mcpsimp"><a name="p163mcpsimp"></a><a name="p163mcpsimp"></a>LOSCFG_COMPAT_POSIX</p>
</td>
</tr>
</tbody>
</table>

If the related kernel configurations are enabled, the system hangs when a deadlock is detected, and "dead lock" is output in the exception information. Example:

<a name="table165mcpsimp"></a>
<table><tbody><tr id="row169mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p171mcpsimp"><a name="p171mcpsimp"></a><a name="p171mcpsimp"></a>[2025-11-17 11:20:49] lockdep check failed</p>
<p id="p172mcpsimp"><a name="p172mcpsimp"></a><a name="p172mcpsimp"></a>[2025-11-17 11:20:49] error type   : <strong id="b532141334212"><a name="b532141334212"></a><a name="b532141334212"></a>dead lock</strong></p>
<p id="p173mcpsimp"><a name="p173mcpsimp"></a><a name="p173mcpsimp"></a>[2025-11-17 11:20:49] request addr : 0x47262</p>
<p id="p174mcpsimp"><a name="p174mcpsimp"></a><a name="p174mcpsimp"></a>[2025-11-17 11:20:49] task name    : Task_B</p>
</td>
</tr>
</tbody>
</table>

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654501"></a>

Two tasks are each waiting for the resources held by the other.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734550"></a>

**Location Methods<a name="section4521631134916"></a>**

**Reverse-lookup the request address to locate the faulting lock function:** Copy the request addr value that triggered the exception into the disassembly file of the system image, and locate the specific code line by address to identify which lock function had an exception during execution.

Note: The reverse lookup result of request addr usually points to the entry of a specific lock function. If multiple locks of the same type exist in a task, they can be further distinguished by the lock ID to precisely locate the specific lock object.

**Reference Case<a name="section983475124913"></a>**

<a name="table911mcpsimp"></a>
<table><tbody><tr id="row915mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p917mcpsimp"><a name="p917mcpsimp"></a><a name="p917mcpsimp"></a>[2025-11-17 11:20:49] app_init start ok</p>
<p id="p918mcpsimp"><a name="p918mcpsimp"></a><a name="p918mcpsimp"></a>[2025-11-17 11:20:49] Task_A pend muxid 31</p>
<p id="p919mcpsimp"><a name="p919mcpsimp"></a><a name="p919mcpsimp"></a>[2025-11-17 11:20:49] Task_B pend muxid 32</p>
<p id="p920mcpsimp"><a name="p920mcpsimp"></a><a name="p920mcpsimp"></a>[2025-11-17 11:20:49] APP|thread_main start</p>
<p id="p921mcpsimp"><a name="p921mcpsimp"></a><a name="p921mcpsimp"></a>[2025-11-17 11:20:49] lockdep check failed</p>
<p id="p922mcpsimp"><a name="p922mcpsimp"></a><a name="p922mcpsimp"></a>[2025-11-17 11:20:49] <strong id="b12781025144220"><a name="b12781025144220"></a><a name="b12781025144220"></a>error type   : dead lock</strong></p>
<p id="p923mcpsimp"><a name="p923mcpsimp"></a><a name="p923mcpsimp"></a>[2025-11-17 11:20:49] <strong id="b17117129154215"><a name="b17117129154215"></a><a name="b17117129154215"></a>request addr : 0x47262</strong></p>
<p id="p924mcpsimp"><a name="p924mcpsimp"></a><a name="p924mcpsimp"></a>[2025-11-17 11:20:49] <strong id="b1158293224216"><a name="b1158293224216"></a><a name="b1158293224216"></a>task name    : Task_B</strong></p>
<p id="p925mcpsimp"><a name="p925mcpsimp"></a><a name="p925mcpsimp"></a>[2025-11-17 11:20:49] task id      : 8</p>
<p id="p926mcpsimp"><a name="p926mcpsimp"></a><a name="p926mcpsimp"></a>[2025-11-17 11:20:49] cpu num      : 0</p>
<p id="p927mcpsimp"><a name="p927mcpsimp"></a><a name="p927mcpsimp"></a>[2025-11-17 11:20:49] start dumping lockdep information</p>
<p id="p928mcpsimp"><a name="p928mcpsimp"></a><a name="p928mcpsimp"></a>[2025-11-17 11:20:49] [0] <strong id="b1617114013428"><a name="b1617114013428"></a><a name="b1617114013428"></a>Mutex ID: 0032</strong></p>
<p id="p929mcpsimp"><a name="p929mcpsimp"></a><a name="p929mcpsimp"></a>[2025-11-17 11:20:49] [1] <strong id="b1482154415420"><a name="b1482154415420"></a><a name="b1482154415420"></a>Mutex ID: 0031 &lt;-- now</strong></p>
<p id="p930mcpsimp"><a name="p930mcpsimp"></a><a name="p930mcpsimp"></a>[2025-11-17 11:20:49] task name    : Task_A</p>
<p id="p931mcpsimp"><a name="p931mcpsimp"></a><a name="p931mcpsimp"></a>[2025-11-17 11:20:49] task id      : 7</p>
<p id="p932mcpsimp"><a name="p932mcpsimp"></a><a name="p932mcpsimp"></a>[2025-11-17 11:20:49] cpu num      : 0</p>
<p id="p933mcpsimp"><a name="p933mcpsimp"></a><a name="p933mcpsimp"></a>[2025-11-17 11:20:49] start dumping lockdep information</p>
<p id="p934mcpsimp"><a name="p934mcpsimp"></a><a name="p934mcpsimp"></a>[2025-11-17 11:20:49] [0] <strong id="b11352195213428"><a name="b11352195213428"></a><a name="b11352195213428"></a>Mutex ID: 0031</strong></p>
<p id="p935mcpsimp"><a name="p935mcpsimp"></a><a name="p935mcpsimp"></a>[2025-11-17 11:20:49] [1] <strong id="b16295155624216"><a name="b16295155624216"></a><a name="b16295155624216"></a>Mutex ID: 0032 &lt;-- now</strong></p>
<p id="p936mcpsimp"><a name="p936mcpsimp"></a><a name="p936mcpsimp"></a>[2025-11-17 11:20:49] runTask-&gt;taskName = Task_B</p>
<p id="p937mcpsimp"><a name="p937mcpsimp"></a><a name="p937mcpsimp"></a>[2025-11-17 11:20:49] runTask-&gt;taskId = 8</p>
<p id="p938mcpsimp"><a name="p938mcpsimp"></a><a name="p938mcpsimp"></a>[2025-11-17 11:20:49] fp:0x10021010</p>
</td>
</tr>
</tbody>
</table>

-   From the exception information, it can be known that tasks Task\_A and Task\_B are in a deadlock: Task\_B holds lock 0032 and requests lock 0031, while Task\_A holds lock 0031 and requests lock 0032.
-   Based on the request addr value (0x47262 in this example), find this address in the disassembly file of the system image to determine the specific lock function LOS\_MuxPend, and further locate the position where Task A calls the mutex.

    <a name="table942mcpsimp"></a>
    <table><tbody><tr id="row946mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p948mcpsimp"><a name="p948mcpsimp"></a><a name="p948mcpsimp"></a>000253da &lt;Task_A&gt;:</p>
    <p id="p949mcpsimp"><a name="p949mcpsimp"></a><a name="p949mcpsimp"></a>253da: 40 99        	c.push	{ra,s0-s1}, -16</p>
    <p id="p950mcpsimp"><a name="p950mcpsimp"></a><a name="p950mcpsimp"></a>253dc: 00 08        	addi	s0, sp, 16</p>
    <p id="p951mcpsimp"><a name="p951mcpsimp"></a><a name="p951mcpsimp"></a>253de: 37 d5 01 20  	lui	a0, 131101</p>
    <p id="p952mcpsimp"><a name="p952mcpsimp"></a><a name="p952mcpsimp"></a>253e2: 93 04 c5 ed  	addi	s1, a0, -292</p>
    <p id="p953mcpsimp"><a name="p953mcpsimp"></a><a name="p953mcpsimp"></a>253e6: c8 44        	lw	a0, 12(s1)</p>
    <p id="p954mcpsimp"><a name="p954mcpsimp"></a><a name="p954mcpsimp"></a>253e8: fd 55        	addi	a1, zero, -1</p>
    <p id="p955mcpsimp"><a name="p955mcpsimp"></a><a name="p955mcpsimp"></a><strong id="b10190314194317"><a name="b10190314194317"></a><a name="b10190314194317"></a>253ea: ef 10 12 60  	jal	ra, 0x471ea &lt;LOS_MuxPend&gt;</strong></p>
    <p id="p956mcpsimp"><a name="p956mcpsimp"></a><a name="p956mcpsimp"></a>253ee: 11 e9        	bne	a0, zero, 0x25402 &lt;Task_A+0x28&gt;</p>
    <p id="p957mcpsimp"><a name="p957mcpsimp"></a><a name="p957mcpsimp"></a>253f0: d0 44        	lw	a2, 12(s1)</p>
    <p id="p958mcpsimp"><a name="p958mcpsimp"></a><a name="p958mcpsimp"></a>253f2: 55 65        	lui	a0, 21</p>
    <p id="p959mcpsimp"><a name="p959mcpsimp"></a><a name="p959mcpsimp"></a>253f4: 13 05 75 e8  	addi	a0, a0, -377</p>
    <p id="p960mcpsimp"><a name="p960mcpsimp"></a><a name="p960mcpsimp"></a>253f8: d1 65        	lui	a1, 20</p>
    <p id="p961mcpsimp"><a name="p961mcpsimp"></a><a name="p961mcpsimp"></a>253fa: 93 85 45 fe  	addi	a1, a1, -28</p>
    <p id="p962mcpsimp"><a name="p962mcpsimp"></a><a name="p962mcpsimp"></a>253fe: ef 20 c2 1c  	jal	ra, 0x475ca &lt;dprintf&gt;</p>
    <p id="p963mcpsimp"><a name="p963mcpsimp"></a><a name="p963mcpsimp"></a>25402: 09 45        	addi	a0, zero, 2</p>
    <p id="p964mcpsimp"><a name="p964mcpsimp"></a><a name="p964mcpsimp"></a>25404: ef 10 52 2a  	jal	ra, 0x46ea8 &lt;LOS_Msleep&gt;</p>
    <p id="p965mcpsimp"><a name="p965mcpsimp"></a><a name="p965mcpsimp"></a>25408: 88 48        	lw	a0, 16(s1)</p>
    <p id="p966mcpsimp"><a name="p966mcpsimp"></a><a name="p966mcpsimp"></a>2540a: fd 55        	addi	a1, zero, -1</p>
    <p id="p967mcpsimp"><a name="p967mcpsimp"></a><a name="p967mcpsimp"></a><strong id="b15278104215430"><a name="b15278104215430"></a><a name="b15278104215430"></a>2540c: ef 10 f2 5d  	jal	ra, 0x471ea &lt;LOS_MuxPend&gt;</strong></p>
    <p id="p968mcpsimp"><a name="p968mcpsimp"></a><a name="p968mcpsimp"></a>……..</p>
    <p id="p969mcpsimp"><a name="p969mcpsimp"></a><a name="p969mcpsimp"></a>000471ea &lt;LOS_MuxPend&gt;:</p>
    <p id="p970mcpsimp"><a name="p970mcpsimp"></a><a name="p970mcpsimp"></a>471ea: c0 9b        	c.push	{ra,s0-s6}, -32</p>
    <p id="p971mcpsimp"><a name="p971mcpsimp"></a><a name="p971mcpsimp"></a>471ec: 00 10        	addi	s0, sp, 32</p>
    <p id="p972mcpsimp"><a name="p972mcpsimp"></a><a name="p972mcpsimp"></a>471ee: 2a 8b        	add	s6, a0, zero</p>
    <p id="p973mcpsimp"><a name="p973mcpsimp"></a><a name="p973mcpsimp"></a>471f0: 28 91        	c.zext.h	a0, a0</p>
    <p id="p974mcpsimp"><a name="p974mcpsimp"></a><a name="p974mcpsimp"></a>……..</p>
    <p id="p975mcpsimp"><a name="p975mcpsimp"></a><a name="p975mcpsimp"></a>4724e: 63 0d 55 03  	beq	a0, s5, 0x47288 &lt;LOS_MuxPend+0x9e&gt;</p>
    <p id="p976mcpsimp"><a name="p976mcpsimp"></a><a name="p976mcpsimp"></a>47252: 5a 85        	add	a0, s6, zero</p>
    <p id="p977mcpsimp"><a name="p977mcpsimp"></a><a name="p977mcpsimp"></a>47254: ef e0 9f c5  	jal	ra, 0x45eac &lt;OsMuxLockDepGet&gt;</p>
    <p id="p978mcpsimp"><a name="p978mcpsimp"></a><a name="p978mcpsimp"></a>47258: aa 85        	add	a1, a0, zero</p>
    <p id="p979mcpsimp"><a name="p979mcpsimp"></a><a name="p979mcpsimp"></a>4725a: 01 45        	addi	a0, zero, 0</p>
    <p id="p980mcpsimp"><a name="p980mcpsimp"></a><a name="p980mcpsimp"></a>4725c: 5a 86        	add	a2, s6, zero</p>
    <p id="p981mcpsimp"><a name="p981mcpsimp"></a><a name="p981mcpsimp"></a>4725e: ef e0 9f dd  	jal	ra, 0x46036 &lt;OsLockDepCheckIn&gt;</p>
    <p id="p982mcpsimp"><a name="p982mcpsimp"></a><a name="p982mcpsimp"></a><strong id="b1465410551431"><a name="b1465410551431"></a><a name="b1465410551431"></a>47262: 52 85        	add	a0, s4, zero</strong></p>
    <p id="p983mcpsimp"><a name="p983mcpsimp"></a><a name="p983mcpsimp"></a>47264: db 55 c5 00  	lhu.u	a1, 12(a0)</p>
    <p id="p984mcpsimp"><a name="p984mcpsimp"></a><a name="p984mcpsimp"></a>47268: 9d c5        	beq	a1, zero, 0x47296 &lt;LOS_MuxPend+0xac&gt;</p>
    <p id="p985mcpsimp"><a name="p985mcpsimp"></a><a name="p985mcpsimp"></a>4726a: 63 85 09 04  	beq	s3, zero, 0x472b4 &lt;LOS_MuxPend+0xca&gt;</p>
    </td>
    </tr>
    </tbody>
    </table>

## Unaligned Access<a name="ZH-CN_TOPIC_0000002555814475"></a>




### Problem Identification<a name="ZH-CN_TOPIC_0000002524574600"></a>

Memory alignment access requirement: When accessing data, its physical address must be an integer multiple of the byte width of the data type.

32-bit data (such as uint32\_t, float): The address must be a multiple of 4 (for example, 0x0000, 0x0004, 0x0008);

16-bit data (such as uint16\_t): The address must be a multiple of 2;

8-bit data (such as uint8\_t): The address can be any value (no alignment required).

An unaligned access is an access behavior that violates the above rules. When a program attempts to load or store data at an unaligned address, the hardware triggers an exception, and the keywords "Load address misaligned" or "Store/AMO address misaligned" appear in the crash log. Example:

<a name="table182mcpsimp"></a>
<table><tbody><tr id="row186mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p188mcpsimp"><a name="p188mcpsimp"></a><a name="p188mcpsimp"></a>[2025-10-30 21:47:41] <strong id="b735514124410"><a name="b735514124410"></a><a name="b735514124410"></a>Load address misaligned</strong></p>
</td>
</tr>
</tbody>
</table>

### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654503"></a>

-   **Core cause**

    The memory access model does not match the hardware alignment requirements. The chip does not support unaligned accesses, and the software does not take this into account. This often occurs when code suddenly crashes after being ported to a new platform, and is especially prominent on customer-customized chip architectures.

-   **Typical scenarios**
    -   **Structure padding and alignment control**: By default, the compiler pads structure members for memory alignment to improve access efficiency. If directives such as \#pragma pack\(1\) are used to force the removal of alignment, and then structure members are accessed directly, unaligned accesses are likely to occur.
    -   **Pointer type casting**: Casting a char\* or void\* pointer to a pointer of a more strictly aligned type (such as int\*, float\*) and dereferencing it can easily cause unaligned accesses.
    -   **Network protocol packet/binary file parsing**: In network communication or file parsing scenarios, raw byte buffers (char\[\]) are often directly mapped to structure pointers. If the data fields defined by the protocol are not aligned, or alignment is not considered during parsing, unaligned accesses will occur.

### Problem Location<a name="ZH-CN_TOPIC_0000002524734552"></a>

**Location Methods<a name="section1275482620501"></a>**

The code line where the unaligned access caused the hang can be located based on mepc (PC register value).

**Reference Case<a name="section184735382504"></a>**

<a name="table1296mcpsimp"></a>
<table><tbody><tr id="row1300mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1302mcpsimp"><a name="p1302mcpsimp"></a><a name="p1302mcpsimp"></a>DOORBELL_VERSION = 20231205_V0.0001_test1</p>
<p id="p1303mcpsimp"><a name="p1303mcpsimp"></a><a name="p1303mcpsimp"></a>[app_main:903] p = 0x4886440</p>
<p id="p1304mcpsimp"><a name="p1304mcpsimp"></a><a name="p1304mcpsimp"></a>[app_main:907] p1 = 0x4886441</p>
<p id="p1305mcpsimp"><a name="p1305mcpsimp"></a><a name="p1305mcpsimp"></a>==================================================exception_analyze==================================================</p>
<p id="p1306mcpsimp"><a name="p1306mcpsimp"></a><a name="p1306mcpsimp"></a>CPU0 run addr = 0x403de7e</p>
<p id="p1307mcpsimp"><a name="p1307mcpsimp"></a><a name="p1307mcpsimp"></a>!!! cpu 1 exception_analyze: DEBUG_MSG = 0x0, DEBUG_PRP_NUM = 0xffffffff DSPCON=e00</p>
<p id="p1308mcpsimp"><a name="p1308mcpsimp"></a><a name="p1308mcpsimp"></a>R0: 42312a6</p>
<p id="p1309mcpsimp"><a name="p1309mcpsimp"></a><a name="p1309mcpsimp"></a>R1: 4224043</p>
<p id="p1310mcpsimp"><a name="p1310mcpsimp"></a><a name="p1310mcpsimp"></a>R2: 38d</p>
<p id="p1311mcpsimp"><a name="p1311mcpsimp"></a><a name="p1311mcpsimp"></a>R3: 0</p>
<p id="p1312mcpsimp"><a name="p1312mcpsimp"></a><a name="p1312mcpsimp"></a>R4: 4224043</p>
<p id="p1313mcpsimp"><a name="p1313mcpsimp"></a><a name="p1313mcpsimp"></a>R5: 42234e0</p>
<p id="p1314mcpsimp"><a name="p1314mcpsimp"></a><a name="p1314mcpsimp"></a>R6: 4886441</p>
<p id="p1315mcpsimp"><a name="p1315mcpsimp"></a><a name="p1315mcpsimp"></a>R7: 422b1f2</p>
<p id="p1316mcpsimp"><a name="p1316mcpsimp"></a><a name="p1316mcpsimp"></a>R8: 423128d</p>
<p id="p1317mcpsimp"><a name="p1317mcpsimp"></a><a name="p1317mcpsimp"></a>R9: 46d9e90</p>
<p id="p1318mcpsimp"><a name="p1318mcpsimp"></a><a name="p1318mcpsimp"></a>R10: 10101010</p>
<p id="p1319mcpsimp"><a name="p1319mcpsimp"></a><a name="p1319mcpsimp"></a>R11: 11111111</p>
<p id="p1320mcpsimp"><a name="p1320mcpsimp"></a><a name="p1320mcpsimp"></a>R12: 12121212</p>
<p id="p1321mcpsimp"><a name="p1321mcpsimp"></a><a name="p1321mcpsimp"></a>R13: 13131313</p>
<p id="p1322mcpsimp"><a name="p1322mcpsimp"></a><a name="p1322mcpsimp"></a>R14: 14141414</p>
<p id="p1323mcpsimp"><a name="p1323mcpsimp"></a><a name="p1323mcpsimp"></a>R15: 15151515</p>
<p id="p1324mcpsimp"><a name="p1324mcpsimp"></a><a name="p1324mcpsimp"></a>icfg: 7010280</p>
<p id="p1325mcpsimp"><a name="p1325mcpsimp"></a><a name="p1325mcpsimp"></a>psr: 0</p>
<p id="p1326mcpsimp"><a name="p1326mcpsimp"></a><a name="p1326mcpsimp"></a>rets: 0x40937c2</p>
<p id="p1327mcpsimp"><a name="p1327mcpsimp"></a><a name="p1327mcpsimp"></a>rete: 0x0</p>
<p id="p1328mcpsimp"><a name="p1328mcpsimp"></a><a name="p1328mcpsimp"></a>retx: 0x0</p>
<p id="p1329mcpsimp"><a name="p1329mcpsimp"></a><a name="p1329mcpsimp"></a>reti: 0x4000e32</p>
<p id="p1330mcpsimp"><a name="p1330mcpsimp"></a><a name="p1330mcpsimp"></a>usp: 489680c, ssp: 42eee68 sp: 42eee68</p>
</td>
</tr>
</tbody>
</table>

When adapting for customer J, the above hang occurred due to an unaligned access. This scenario belongs to FBB-RTOS adaptation to a chip from another vendor, where the chip does not support unaligned accesses. (The print information provided by the customer itself did not indicate the current exception type)

Solution: Convert unaligned access operations into byte-by-byte operations.

## Other Exceptions<a name="ZH-CN_TOPIC_0000002555814477"></a>

When the root cause cannot be directly located from the system exception log and code context, or when the analysis methods provided above can only narrow it down to an abnormal variable, memory block, or resource, it is usually necessary to suspect memory corruption, insufficient memory, or unaligned memory layout issues. Such exceptions do not have a fixed exception type, and the exception often does not occur at the first scene, making problem location difficult. For such exceptions, FBB-RTOS provides corresponding DFX tools that can precisely locate high-frequency memory exception problems, including out-of-bounds access of dynamically allocated memory, corruption of fixed memory regions, wild writes caused by repeated release of pointers, and memory leaks.




### Memory Corruption<a name="ZH-CN_TOPIC_0000002524574602"></a>




#### Cause Analysis<a name="ZH-CN_TOPIC_0000002555654505"></a>

When memory corruption occurs, the system usually does not hang at the first scene. The exception typically appears only when the corrupted content is accessed, manifesting as system crashes, abnormal variable values, data transmission errors, abnormal business results, abnormal task suspension or exit, invalid instructions, memory validity check failures, and other issues.

The root causes of memory corruption include array overflow, dynamic memory overflow, wild writes, repeated release, and so on.

#### Problem Location<a name="ZH-CN_TOPIC_0000002524734554"></a>

**Location Methods<a name="section1275482620501"></a>**

The DFX capabilities currently provided by the FBB-RTOS system mainly solve the following three types of typical memory corruption problems:

-   Fixed-region memory corruption (the same memory region or a fixed variable is corrupted every time)

    Monitor read/write operations on the fixed region through trigger to capture the first scene of memory corruption. First determine the corrupted memory address, then enable the LOSCFG\_TRIGGER\_ENABLE kernel configuration and use trigger for monitoring. Two usage methods are currently provided:

    Method 1 (recommended): For products that do not have a command line adapted, the trigger interface can be called directly.

    <a name="table387mcpsimp"></a>
    <table><tbody><tr id="row391mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p393mcpsimp"><a name="p393mcpsimp"></a><a name="p393mcpsimp"></a>UINT32 ArchProtectionSetAddrRo(UINT32 addr, UINT32 size)</p>
    <p id="p394mcpsimp"><a name="p394mcpsimp"></a><a name="p394mcpsimp"></a>Function description: Configure protection based on the provided address and range;</p>
    <p id="p395mcpsimp"><a name="p395mcpsimp"></a><a name="p395mcpsimp"></a>Parameter description:</p>
    <p id="p396mcpsimp"><a name="p396mcpsimp"></a><a name="p396mcpsimp"></a>addr: The start address of the protected range. When size is 4, addr needs to be 4-byte aligned;</p>
    <p id="p397mcpsimp"><a name="p397mcpsimp"></a><a name="p397mcpsimp"></a>size: The size of the protected range;</p>
    <p id="p398mcpsimp"><a name="p398mcpsimp"></a><a name="p398mcpsimp"></a>Usage example:</p>
    <p id="p399mcpsimp"><a name="p399mcpsimp"></a><a name="p399mcpsimp"></a>ArchProtectionSetAddrRo(0x100000, 4): The protected address range is [0x100000, 0x100003], 4 bytes in total;</p>
    <p id="p400mcpsimp"><a name="p400mcpsimp"></a><a name="p400mcpsimp"></a>************************************************************************************</p>
    <p id="p401mcpsimp"><a name="p401mcpsimp"></a><a name="p401mcpsimp"></a>UINT32 ArchProtectionUnSetAddrRo(UINT32 index)</p>
    <p id="p402mcpsimp"><a name="p402mcpsimp"></a><a name="p402mcpsimp"></a>Function description: Cancel the protection of the trigger at the specified index</p>
    <p id="p403mcpsimp"><a name="p403mcpsimp"></a><a name="p403mcpsimp"></a>Parameter description: index: The trigger index, valid range [0, 3]. index == 0xffffffff indicates canceling all trigger protection.</p>
    </td>
    </tr>
    </tbody>
    </table>

    Method 2: Use commands in the command line

    <a name="table405mcpsimp"></a>
    <table><tbody><tr id="row409mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p411mcpsimp"><a name="p411mcpsimp"></a><a name="p411mcpsimp"></a>trigger set addr size</p>
    <p id="p412mcpsimp"><a name="p412mcpsimp"></a><a name="p412mcpsimp"></a>Command description: Set a trigger to protect size bytes starting from address addr</p>
    <p id="p413mcpsimp"><a name="p413mcpsimp"></a><a name="p413mcpsimp"></a>Example: trigger set 0x1405ca4 4 protects the 4 bytes starting from address 0x1405ca4</p>
    <p id="p414mcpsimp"><a name="p414mcpsimp"></a><a name="p414mcpsimp"></a>Note: After the trigger is set, the current trigger information is printed</p>
    <p id="p415mcpsimp"><a name="p415mcpsimp"></a><a name="p415mcpsimp"></a>************************************************************************************</p>
    <p id="p416mcpsimp"><a name="p416mcpsimp"></a><a name="p416mcpsimp"></a>trigger unset</p>
    <p id="p417mcpsimp"><a name="p417mcpsimp"></a><a name="p417mcpsimp"></a>Command description: Remove the current trigger</p>
    <p id="p418mcpsimp"><a name="p418mcpsimp"></a><a name="p418mcpsimp"></a>Example: trigger unset</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Heap out-of-bounds corruption of the memory node header

    Use the DFX tool provided by FBB\_RTOS to determine the corrupted memory node, and then locate it based on information such as the taskId in the corrupted memory node. For specific operation methods, refer to Chapter 8.3.3 of the LiteOS Development Guide.

-   Repeated memory release

    Use the DFX tool provided by FBB\_RTOS to determine the repeated release instruction, then determine the problematic function through the disassembly file, and locate it step by step using information such as callerRA.

    The specific steps are:

    Enable the LOSCFG\_MEM\_DFX\_DOUBLE\_FREE\_CHECK kernel configuration.

    Add the compilation option and recompile and run.

    <a name="table428mcpsimp"></a>
    <table><tbody><tr id="row432mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p434mcpsimp"><a name="p434mcpsimp"></a><a name="p434mcpsimp"></a># Add the compilation option</p>
    <p id="p435mcpsimp"><a name="p435mcpsimp"></a><a name="p435mcpsimp"></a># target_standard_sw21_application_template    add the compilation option to linkflags</p>
    <p id="p436mcpsimp"><a name="p436mcpsimp"></a><a name="p436mcpsimp"></a>'linkflags': [</p>
    <p id="p437mcpsimp"><a name="p437mcpsimp"></a><a name="p437mcpsimp"></a>'-Wl,--wrap=LOS_MemFree'</p>
    <p id="p438mcpsimp"><a name="p438mcpsimp"></a><a name="p438mcpsimp"></a>],</p>
    </td>
    </tr>
    </tbody>
    </table>

    Based on the printed information combined with the disassembly file, the call site of the repeated free function can be determined.

    ![](figures/en_image_0000002563509625.png)

    For detailed usage and introduction, refer to the "Memory Repeated Release Detection" chapter of the LiteOS Development Guide.

    For other issues such as wild writes, there is currently no particularly good method; they are mainly analyzed further by combining the business code at the exception point. For detailed analysis ideas, refer to the following figure.

    ![](figures/en_image_0000002563589583.png)

**Reference Case<a name="section33891826135114"></a>**

Example 1 (heap out-of-bounds corruption of the memory node header):

<a name="table447mcpsimp"></a>
<table><tbody><tr id="row451mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p453mcpsimp"><a name="p453mcpsimp"></a><a name="p453mcpsimp"></a><strong id="b1565573020455"><a name="b1565573020455"></a><a name="b1565573020455"></a>The node:0x1137b4 has been damaged!</strong></p>
<p id="p454mcpsimp"><a name="p454mcpsimp"></a><a name="p454mcpsimp"></a><strong id="b665613010459"><a name="b665613010459"></a><a name="b665613010459"></a>node:0x1137b4 has been damaged! pre node:0x11379c，pre node CallerRA：0x100864</strong></p>
<p id="p455mcpsimp"><a name="p455mcpsimp"></a><a name="p455mcpsimp"></a>task:app_Task</p>
<p id="p456mcpsimp"><a name="p456mcpsimp"></a><a name="p456mcpsimp"></a>thrdPid:0x3</p>
<p id="p457mcpsimp"><a name="p457mcpsimp"></a><a name="p457mcpsimp"></a>type:0xb</p>
<p id="p458mcpsimp"><a name="p458mcpsimp"></a><a name="p458mcpsimp"></a>nestCnt:1</p>
<p id="p459mcpsimp"><a name="p459mcpsimp"></a><a name="p459mcpsimp"></a>phase:1</p>
<p id="p460mcpsimp"><a name="p460mcpsimp"></a><a name="p460mcpsimp"></a>ccause:0x0</p>
<p id="p461mcpsimp"><a name="p461mcpsimp"></a><a name="p461mcpsimp"></a>mcause:0xb</p>
<p id="p462mcpsimp"><a name="p462mcpsimp"></a><a name="p462mcpsimp"></a>mtval:0x0</p>
<p id="p463mcpsimp"><a name="p463mcpsimp"></a><a name="p463mcpsimp"></a>gp:0x10fda0</p>
<p id="p464mcpsimp"><a name="p464mcpsimp"></a><a name="p464mcpsimp"></a>mstatus:0x1800</p>
<p id="p465mcpsimp"><a name="p465mcpsimp"></a><a name="p465mcpsimp"></a>mepc:0x1008ae</p>
<p id="p466mcpsimp"><a name="p466mcpsimp"></a><a name="p466mcpsimp"></a>ra:0x1008ae</p>
<p id="p467mcpsimp"><a name="p467mcpsimp"></a><a name="p467mcpsimp"></a>sp:0x113540</p>
<p id="p468mcpsimp"><a name="p468mcpsimp"></a><a name="p468mcpsimp"></a>X4 :0x0</p>
<p id="p469mcpsimp"><a name="p469mcpsimp"></a><a name="p469mcpsimp"></a>X5 :0xffffd8f0</p>
<p id="p470mcpsimp"><a name="p470mcpsimp"></a><a name="p470mcpsimp"></a>X6 :0x1134bb</p>
<p id="p471mcpsimp"><a name="p471mcpsimp"></a><a name="p471mcpsimp"></a>X7 :0xa</p>
<p id="p472mcpsimp"><a name="p472mcpsimp"></a><a name="p472mcpsimp"></a>X8 :0x113670</p>
<p id="p473mcpsimp"><a name="p473mcpsimp"></a><a name="p473mcpsimp"></a>X9 :0x1137cc</p>
<p id="p474mcpsimp"><a name="p474mcpsimp"></a><a name="p474mcpsimp"></a>X10:0x11359c</p>
<p id="p475mcpsimp"><a name="p475mcpsimp"></a><a name="p475mcpsimp"></a>X11:0x40e5f3e4</p>
<p id="p476mcpsimp"><a name="p476mcpsimp"></a><a name="p476mcpsimp"></a>X12:0x24</p>
<p id="p477mcpsimp"><a name="p477mcpsimp"></a><a name="p477mcpsimp"></a>X13:0x1</p>
</td>
</tr>
</tbody>
</table>

The key print information "The node:0x1137b4 has been damaged" confirms that the heap memory has been corrupted. Usually, it is the out-of-bounds access of the preceding node that corrupts the memory node header of the following node. Directly use the callerRA information of the preceding node (prenode) to determine the allocator of the adjacent preceding node, and then search for the callerRA address in the disassembly to determine the code line.

Example 2 (locating fixed-region corruption via trigger):

The exception information is as follows:

<a name="table481mcpsimp"></a>
<table><tbody><tr id="row485mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p487mcpsimp"><a name="p487mcpsimp"></a><a name="p487mcpsimp"></a>ptr_node:0x11cfdc</p>
<p id="p488mcpsimp"><a name="p488mcpsimp"></a><a name="p488mcpsimp"></a>task:app_Task</p>
<p id="p489mcpsimp"><a name="p489mcpsimp"></a><a name="p489mcpsimp"></a>thrdId:0x3</p>
<p id="p490mcpsimp"><a name="p490mcpsimp"></a><a name="p490mcpsimp"></a>type:0x5</p>
<p id="p491mcpsimp"><a name="p491mcpsimp"></a><a name="p491mcpsimp"></a>phase:1</p>
<p id="p492mcpsimp"><a name="p492mcpsimp"></a><a name="p492mcpsimp"></a>ccause:0x0</p>
<p id="p493mcpsimp"><a name="p493mcpsimp"></a><a name="p493mcpsimp"></a>mcause:0x0</p>
<p id="p494mcpsimp"><a name="p494mcpsimp"></a><a name="p494mcpsimp"></a>mtval:0xababeffc</p>
<p id="p495mcpsimp"><a name="p495mcpsimp"></a><a name="p495mcpsimp"></a>gp:0x115c50</p>
<p id="p496mcpsimp"><a name="p496mcpsimp"></a><a name="p496mcpsimp"></a>mstatus:0x1800</p>
<p id="p497mcpsimp"><a name="p497mcpsimp"></a><a name="p497mcpsimp"></a><strong id="b1116264134513"><a name="b1116264134513"></a><a name="b1116264134513"></a>mepc:0x102ee0</strong></p>
<p id="p498mcpsimp"><a name="p498mcpsimp"></a><a name="p498mcpsimp"></a>ra:0x2ed4</p>
<p id="p499mcpsimp"><a name="p499mcpsimp"></a><a name="p499mcpsimp"></a>sp:0x11a170</p>
</td>
</tr>
</tbody>
</table>

-   Find the function running when the exception occurred via mepc: 0x102ee0.

    <a name="table502mcpsimp"></a>
    <table><tbody><tr id="row506mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p508mcpsimp"><a name="p508mcpsimp"></a><a name="p508mcpsimp"></a>00102eac &lt;OsMemFreeNode&gt;:</p>
    <p id="p509mcpsimp"><a name="p509mcpsimp"></a><a name="p509mcpsimp"></a>102eac: 713d addi sp,sp,-32</p>
    <p id="p510mcpsimp"><a name="p510mcpsimp"></a><a name="p510mcpsimp"></a>102eae: ce06 sw ra,28(sp)</p>
    <p id="p511mcpsimp"><a name="p511mcpsimp"></a><a name="p511mcpsimp"></a>102eb0: cc22 sw s0,24(sp)</p>
    <p id="p512mcpsimp"><a name="p512mcpsimp"></a><a name="p512mcpsimp"></a>102eb2: ca26 sw s1,20(sp)</p>
    <p id="p513mcpsimp"><a name="p513mcpsimp"></a><a name="p513mcpsimp"></a>102eb4: c84a sw s2,16(sp)</p>
    <p id="p514mcpsimp"><a name="p514mcpsimp"></a><a name="p514mcpsimp"></a>102eb6: c64e sw s3,12(sp)</p>
    <p id="p515mcpsimp"><a name="p515mcpsimp"></a><a name="p515mcpsimp"></a>102eb8: 84aa mv s1,a0</p>
    <p id="p516mcpsimp"><a name="p516mcpsimp"></a><a name="p516mcpsimp"></a>102eba: 3fffffff099f l.li s3,3fffffff &lt;_heap_end+0x3fedffff&gt;</p>
    <p id="p517mcpsimp"><a name="p517mcpsimp"></a><a name="p517mcpsimp"></a>102ec0: 4554 lw a3,12(a0)</p>
    <p id="p518mcpsimp"><a name="p518mcpsimp"></a><a name="p518mcpsimp"></a>102ec2: 00455603 lhu a2,4(a0)</p>
    <p id="p519mcpsimp"><a name="p519mcpsimp"></a><a name="p519mcpsimp"></a>102ec6: 05c58913 addi s2,a1,92</p>
    <p id="p520mcpsimp"><a name="p520mcpsimp"></a><a name="p520mcpsimp"></a>102eca: 00858513 addi a0,a1,8</p>
    <p id="p521mcpsimp"><a name="p521mcpsimp"></a><a name="p521mcpsimp"></a>102ece: 0136f5b3 and a1,a3,s3</p>
    <p id="p522mcpsimp"><a name="p522mcpsimp"></a><a name="p522mcpsimp"></a>102ed2: 2ca9 jal ra,10312c</p>
    <p id="p523mcpsimp"><a name="p523mcpsimp"></a><a name="p523mcpsimp"></a>102ed4: 44c8 lw a0,12(s1)</p>
    <p id="p524mcpsimp"><a name="p524mcpsimp"></a><a name="p524mcpsimp"></a>102ed6: 4480 lw s0,8(s1)</p>
    <p id="p525mcpsimp"><a name="p525mcpsimp"></a><a name="p525mcpsimp"></a>102ed8: 013575b3 and a1,a0,s3</p>
    <p id="p526mcpsimp"><a name="p526mcpsimp"></a><a name="p526mcpsimp"></a>102edc: c4cc sw a1,12(s1)</p>
    <p id="p527mcpsimp"><a name="p527mcpsimp"></a><a name="p527mcpsimp"></a>102ede: cc2d beqz s0,102f58 &lt;OsMemFreeNode+0xac&gt;</p>
    <p id="p528mcpsimp"><a name="p528mcpsimp"></a><a name="p528mcpsimp"></a><strong id="b158478541455"><a name="b158478541455"></a><a name="b158478541455"></a>102ee0: 4448 lw a0,12(s0)</strong></p>
    </td>
    </tr>
    </tbody>
    </table>

-   It is found that the faulting instruction is a load operation, and the base address is stored in the s0 register. Combined with the exception information, it is found that the s0 register holds an abnormal address (0xababeff2).
-   Combined with the code and disassembly, the exception occurs when a field is fetched from a structure at the faulting instruction, so it is suspected that the structure has been corrupted.

    <a name="table531mcpsimp"></a>
    <table><tbody><tr id="row535mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p537mcpsimp"><a name="p537mcpsimp"></a><a name="p537mcpsimp"></a>if ((<strong id="b13880675464"><a name="b13880675464"></a><a name="b13880675464"></a>node-&gt;selfNode.preNode != NULL</strong>) &amp;&amp;</p>
    <p id="p538mcpsimp"><a name="p538mcpsimp"></a><a name="p538mcpsimp"></a>!OS_MEM_NODE_GET_USED_FLAG(node-&gt;selfNode.preNode-&gt;selfNode.sizeAndFlag)) {</p>
    <p id="p539mcpsimp"><a name="p539mcpsimp"></a><a name="p539mcpsimp"></a>LosMemDynNode *preNode = node-&gt;selfNode.preNode;</p>
    <p id="p540mcpsimp"><a name="p540mcpsimp"></a><a name="p540mcpsimp"></a>OsMemMergeNode(node);</p>
    <p id="p541mcpsimp"><a name="p541mcpsimp"></a><a name="p541mcpsimp"></a>nextNode = OS_MEM_NEXT_NODE(preNode);</p>
    <p id="p542mcpsimp"><a name="p542mcpsimp"></a><a name="p542mcpsimp"></a>if (!OS_MEM_NODE_GET_USED_FLAG(nextNode-&gt;selfNode.sizeAndFlag)) {</p>
    <p id="p543mcpsimp"><a name="p543mcpsimp"></a><a name="p543mcpsimp"></a>OsMemListDelete(&amp;nextNode-&gt;selfNode.freeNodeInfo, firstNode);</p>
    <p id="p544mcpsimp"><a name="p544mcpsimp"></a><a name="p544mcpsimp"></a>OsMemMergeNode(nextNode);</p>
    <p id="p545mcpsimp"><a name="p545mcpsimp"></a><a name="p545mcpsimp"></a>}</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Since the corrupted node is a dynamically allocated memory node, enable the CallerRA recording capability to record the top-level function address of the memory node allocation, and add a print statement before the position of the red box in step 3 to print out the CallerRA of the memory node.
-   Combined with the CallerRA, find the function that allocated the memory node, and after the node is allocated, use Trigger to monitor the node.

    <a name="table548mcpsimp"></a>
    <table><tbody><tr id="row552mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p554mcpsimp"><a name="p554mcpsimp"></a><a name="p554mcpsimp"></a>ArchProtectionSetAddrRo(node_addr, 4);</p>
    </td>
    </tr>
    </tbody>
    </table>

-   When the exception is triggered again, mepc reveals that the culprit of the memory corruption is 0x299f8.

    <a name="table556mcpsimp"></a>
    <table><tbody><tr id="row560mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p562mcpsimp"><a name="p562mcpsimp"></a><a name="p562mcpsimp"></a>task name: osMain, mepc: <strong id="b9651202574616"><a name="b9651202574616"></a><a name="b9651202574616"></a>0x299f8</strong>, caller: 0x2666e, diff addr: 0Ox22130304, old val: Ox0001254d, new val: 0xababeff2</p>
    </td>
    </tr>
    </tbody>
    </table>

### Out Of Memory\(oom\)<a name="ZH-CN_TOPIC_0000002555814479"></a>




#### Cause Analysis<a name="ZH-CN_TOPIC_0000002524574604"></a>

-   Memory leak

    This usually occurs when a function is called repeatedly and the dynamically allocated memory inside the function is not released. The leaked memory accumulates over time to a certain level, eventually exhausting the system memory and triggering a system exception hang.

-   Excessively large memory request

    When a program attempts to allocate a large block of memory but the system does not have enough memory, the memory allocation function may return failure. Failing to properly handle such exceptions triggers a program crash.

#### Problem Location<a name="ZH-CN_TOPIC_0000002555654507"></a>

**Location Methods<a name="section1726125494915"></a>**

-   Check whether the requested memory size matches business expectations

    If the requested size is abnormally large, confirm whether it is a business logic error or an erroneous operation.

    If the requested size is reasonable, further investigate whether there is a memory leak or insufficient system memory resources.

-   Check the current memory status

    If freesize < the requested amount, the memory is exhausted. Further confirm whether it is a memory leak or the total heap size is insufficient.

    If freesize \> the requested amount, but a specific mem pool has insufficient memory, adjust the memory size of the corresponding mem pool based on business requirements.

    If freesize \> the requested amount, and maxfreeNodeSize < the requested amount, it may be a memory leak or fragmentation.

-   Memory leak location process

    Enable the LOSCFG\_MEM\_DFX\_SHOW\_CALLER\_RA kernel configuration, recompile the system, and enable the memory leak tracking feature. For details, refer to Chapter 8.4 of the LiteOS Development Guide.

    During system operation, execute the task\_mem command multiple times to view the usage of memory nodes, and pay attention to whether the number of memory nodes with the same callerRA (call stack return address) keeps growing. If it grows, a memory leak exists; confirm the leak point with the callerRA.

-   Memory fragmentation location and optimization

    Fragmentation assessment: Use the LOS\_MemFragInfo interface to obtain the number of free blocks in each memory block size range. If there are many small free blocks, fragmentation is severe.

    Fragmentation optimization strategy: Optimize the slab configuration based on the frequency and size of business requests; modules with high-frequency allocation/release use a dedicated memory pool to reduce the impact of fragmentation.

-   If the memory status is normal, memory miniaturization optimization can be considered.

**Reference Case<a name="section6505331155017"></a>**

-   Parsing the dump file shows that the current PC points to panic\_deal, the crash cause is in g\_preserve\_data\_lib, and the crash cause code = 0x0B.

    ![](figures/en_image_0000002532605220.png)

    ![](figures/en_image_0000002532765182.png)

    -   Based on the caller, reverse-looking up the disassembly file shows that the exception context is at line 124 of sysc\_monitor.c.

    ![](figures/en_image_0000002563605099.png)

-   The error code 0xB means REBOOT\_CAUSE\_MON\_MEM\_ALMOST\_EMPTY, that is, the crash cause is insufficient memory. Combined with the analysis of the business-side code logic, a memory leak is highly likely. Checking the memory usage of the task, it is found that the used memory size keeps increasing, which basically confirms that the OOM is caused by a memory leak. The memory leak DFX tool provided by FBB-RTOS was used to locate the problematic code.

    <a name="table637mcpsimp"></a>
    <table><tbody><tr id="row641mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p643mcpsimp"><a name="p643mcpsimp"></a><a name="p643mcpsimp"></a>ID:11 Name:transmit, Priority:20, Status:8, Stack size:3072, Top stack:0x20013100, Heap Curr used:0, Heap Peak used:0</p>
    <p id="p644mcpsimp"><a name="p644mcpsimp"></a><a name="p644mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7240, Heap Peak used:7884</p>
    <p id="p645mcpsimp"><a name="p645mcpsimp"></a><a name="p645mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7332, Heap Peak used:7988</p>
    <p id="p646mcpsimp"><a name="p646mcpsimp"></a><a name="p646mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7424, Heap Peak used:8076</p>
    <p id="p647mcpsimp"><a name="p647mcpsimp"></a><a name="p647mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7516, Heap Peak used:8160</p>
    <p id="p648mcpsimp"><a name="p648mcpsimp"></a><a name="p648mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7608, Heap Peak used:8260</p>
    <p id="p649mcpsimp"><a name="p649mcpsimp"></a><a name="p649mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7700, Heap Peak used:8352</p>
    <p id="p650mcpsimp"><a name="p650mcpsimp"></a><a name="p650mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7792, Heap Peak used:8444</p>
    <p id="p651mcpsimp"><a name="p651mcpsimp"></a><a name="p651mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7884, Heap Peak used:8536</p>
    <p id="p652mcpsimp"><a name="p652mcpsimp"></a><a name="p652mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:7976, Heap Peak used:8628</p>
    <p id="p653mcpsimp"><a name="p653mcpsimp"></a><a name="p653mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8068, Heap Peak used:8720</p>
    <p id="p654mcpsimp"><a name="p654mcpsimp"></a><a name="p654mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8160, Heap Peak used:8812</p>
    <p id="p655mcpsimp"><a name="p655mcpsimp"></a><a name="p655mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8252, Heap Peak used:8904</p>
    <p id="p656mcpsimp"><a name="p656mcpsimp"></a><a name="p656mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8344, Heap Peak used:8996</p>
    <p id="p657mcpsimp"><a name="p657mcpsimp"></a><a name="p657mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8436, Heap Peak used:9264</p>
    <p id="p658mcpsimp"><a name="p658mcpsimp"></a><a name="p658mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8528, Heap Peak used:9264</p>
    <p id="p659mcpsimp"><a name="p659mcpsimp"></a><a name="p659mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8620, Heap Peak used:9272</p>
    <p id="p660mcpsimp"><a name="p660mcpsimp"></a><a name="p660mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8712, Heap Peak used:9364</p>
    <p id="p661mcpsimp"><a name="p661mcpsimp"></a><a name="p661mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8804, Heap Peak used:9456</p>
    <p id="p662mcpsimp"><a name="p662mcpsimp"></a><a name="p662mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8896, Heap Peak used:9548</p>
    <p id="p663mcpsimp"><a name="p663mcpsimp"></a><a name="p663mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:8988, Heap Peak used:9640</p>
    <p id="p664mcpsimp"><a name="p664mcpsimp"></a><a name="p664mcpsimp"></a>ID:12 Name:ux_task, Priority:10, Status:8, Stack size:8192, Top stack:0x20013d20, Heap Curr used:9080, Heap Peak used:9732</p>
    </td>
    </tr>
    </tbody>
    </table>

### Unaligned Memory Layout<a name="ZH-CN_TOPIC_0000002524734556"></a>




#### Cause Analysis<a name="ZH-CN_TOPIC_0000002555814481"></a>

The main cause of exceptions in this scenario is incorrect configuration of the linker script.

#### Problem Location and Resolution<a name="ZH-CN_TOPIC_0000002524574606"></a>

**Location Methods<a name="section5604638152416"></a>**

-   For exceptions during the startup phase, check the linker script and memory layout first.

    If the system exception occurs during the startup phase, first check whether each section in the linker script meets the memory alignment requirements. If the alignment requirements are met, use a tool to dump the code/data sections in RAM and verify whether they are consistent with the linker script expectations.

-   For exceptions during task creation, check the stack start address alignment first.

    If the exception occurs during task creation, first judge based on the return value of the task creation interface.

-   For exceptions when reading structure fields, check the dynamic memory node alignment first.

    If the exception occurs when reading fields of a dynamically allocated structure, and destructive writes such as memory corruption have been ruled out, first print the memory header node address and check whether the memory address meets 4-byte alignment.

**Reference Case<a name="section1394575011241"></a>**

-   Using the LOS\_MemTaskIdGet function to obtain the task to which a pointer belongs returns an abnormal result (ret != taskID).

    <a name="table1051mcpsimp"></a>
    <table><tbody><tr id="row1055mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1057mcpsimp"><a name="p1057mcpsimp"></a><a name="p1057mcpsimp"></a>static UINT32 testcase(VOID)</p>
    <p id="p1058mcpsimp"><a name="p1058mcpsimp"></a><a name="p1058mcpsimp"></a>{</p>
    <p id="p1059mcpsimp"><a name="p1059mcpsimp"></a><a name="p1059mcpsimp"></a>UINT32 ret;</p>
    <p id="p1060mcpsimp"><a name="p1060mcpsimp"></a><a name="p1060mcpsimp"></a>UINT32 size = 0x100;</p>
    <p id="p1061mcpsimp"><a name="p1061mcpsimp"></a><a name="p1061mcpsimp"></a>void *p = NULL;</p>
    <p id="p1062mcpsimp"><a name="p1062mcpsimp"></a><a name="p1062mcpsimp"></a>ret = LOS_MemTaskIdGet(p);</p>
    <p id="p1063mcpsimp"><a name="p1063mcpsimp"></a><a name="p1063mcpsimp"></a>ICUNIT_ASSERT_EQUAL(ret, OS_INVALID, ret);</p>
    <p id="p1064mcpsimp"><a name="p1064mcpsimp"></a><a name="p1064mcpsimp"></a>p = LOS_MemAlloc(OS_SYS_MEM_ADDR, size);</p>
    <p id="p1065mcpsimp"><a name="p1065mcpsimp"></a><a name="p1065mcpsimp"></a>printf("p:%p\n", p);</p>
    <p id="p1066mcpsimp"><a name="p1066mcpsimp"></a><a name="p1066mcpsimp"></a>ICUNIT_ASSERT_NOT_EQUAL(p, NULL, p);</p>
    <p id="p1067mcpsimp"><a name="p1067mcpsimp"></a><a name="p1067mcpsimp"></a><strong id="b01390116485"><a name="b01390116485"></a><a name="b01390116485"></a>ret = LOS_MemTaskIdGet(p);   // Where the exception occurred</strong></p>
    <p id="p1068mcpsimp"><a name="p1068mcpsimp"></a><a name="p1068mcpsimp"></a>ICUNIT_ASSERT_EQUAL(ret, OsCurrTaskGet()-&gt;taskId, ret);</p>
    <p id="p1069mcpsimp"><a name="p1069mcpsimp"></a><a name="p1069mcpsimp"></a>ret = LOS_MemFree(OS_SYS_MEM_ADDR, p);</p>
    <p id="p1070mcpsimp"><a name="p1070mcpsimp"></a><a name="p1070mcpsimp"></a>ICUNIT_ASSERT_EQUAL(ret, LOS_OK, ret);</p>
    <p id="p1071mcpsimp"><a name="p1071mcpsimp"></a><a name="p1071mcpsimp"></a>size = 0x1;</p>
    <p id="p1072mcpsimp"><a name="p1072mcpsimp"></a><a name="p1072mcpsimp"></a>p = LOS_MemAlloc(OS_SYS_MEM_ADDR, size);</p>
    <p id="p1073mcpsimp"><a name="p1073mcpsimp"></a><a name="p1073mcpsimp"></a>printf("p:%p\n", p);</p>
    <p id="p1074mcpsimp"><a name="p1074mcpsimp"></a><a name="p1074mcpsimp"></a>ICUNIT_ASSERT_NOT_EQUAL(p, NULL, p);</p>
    <p id="p1075mcpsimp"><a name="p1075mcpsimp"></a><a name="p1075mcpsimp"></a>}</p>
    </td>
    </tr>
    </tbody>
    </table>

-   After adding print statements, when traversing memory nodes, a large number of unaligned memory nodes appear (memory nodes should be at least 2-byte aligned).

    <a name="table1078mcpsimp"></a>
    <table><tbody><tr id="row1082mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1084mcpsimp"><a name="p1084mcpsimp"></a><a name="p1084mcpsimp"></a>[XTS_I] ====&gt; ts [liteos_memory] start</p>
    <p id="p1085mcpsimp"><a name="p1085mcpsimp"></a><a name="p1085mcpsimp"></a>[XTS_I] ---&gt; tc [IT_LOS_MEM_043] start</p>
    <p id="p1086mcpsimp"><a name="p1086mcpsimp"></a><a name="p1086mcpsimp"></a>[ERR] input ptr is out of system memory range</p>
    <p id="p1087mcpsimp"><a name="p1087mcpsimp"></a><a name="p1087mcpsimp"></a>p:0x117f59        // Abnormal memory address, unaligned</p>
    <p id="p1088mcpsimp"><a name="p1088mcpsimp"></a><a name="p1088mcpsimp"></a>tmpNode:0x116b59</p>
    <p id="p1089mcpsimp"><a name="p1089mcpsimp"></a><a name="p1089mcpsimp"></a>tmpNode:0x116e01</p>
    <p id="p1090mcpsimp"><a name="p1090mcpsimp"></a><a name="p1090mcpsimp"></a>tmpNode:0x117069</p>
    <p id="p1091mcpsimp"><a name="p1091mcpsimp"></a><a name="p1091mcpsimp"></a>tmpNode:0x1172ad</p>
    <p id="p1092mcpsimp"><a name="p1092mcpsimp"></a><a name="p1092mcpsimp"></a>tmpNode:0x1174e1</p>
    <p id="p1093mcpsimp"><a name="p1093mcpsimp"></a><a name="p1093mcpsimp"></a>tmpNode:0x117cfl</p>
    <p id="p1094mcpsimp"><a name="p1094mcpsimp"></a><a name="p1094mcpsimp"></a>tmpNode:0x117f49</p>
    <p id="p1095mcpsimp"><a name="p1095mcpsimp"></a><a name="p1095mcpsimp"></a>[XIS_E][testcase:46] ret=1</p>
    <p id="p1096mcpsimp"><a name="p1096mcpsimp"></a><a name="p1096mcpsimp"></a>[XIS_E][testcase:46] [step0: NULL] Check [(ret) == (0)] failed, errno = 0x78740002</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Checking the ld file reveals that the heap start position was not aligned, causing the memory pool exception.

    <a name="table1099mcpsimp"></a>
    <table><tbody><tr id="row1103mcpsimp"><td class="cellrowborder" valign="top" width="100%"><p id="p1105mcpsimp"><a name="p1105mcpsimp"></a><a name="p1105mcpsimp"></a>.bss : ALIGN(0x20) {</p>
    <p id="p1106mcpsimp"><a name="p1106mcpsimp"></a><a name="p1106mcpsimp"></a>__bss_start = .;</p>
    <p id="p1107mcpsimp"><a name="p1107mcpsimp"></a><a name="p1107mcpsimp"></a>*(.bss .bss.* .sbss* .gnu.linkonce.b.* COMMON)</p>
    <p id="p1108mcpsimp"><a name="p1108mcpsimp"></a><a name="p1108mcpsimp"></a>__bss_end = .;</p>
    <p id="p1109mcpsimp"><a name="p1109mcpsimp"></a><a name="p1109mcpsimp"></a><strong id="b311652624816"><a name="b311652624816"></a><a name="b311652624816"></a>. = ALIGN(0x10);  // Add alignment</strong></p>
    <p id="p1110mcpsimp"><a name="p1110mcpsimp"></a><a name="p1110mcpsimp"></a>__heap_start = .;</p>
    <p id="p1111mcpsimp"><a name="p1111mcpsimp"></a><a name="p1111mcpsimp"></a>} &gt; SRAM_DATA</p>
    <p id="p1112mcpsimp"><a name="p1112mcpsimp"></a><a name="p1112mcpsimp"></a>__heap_end = ORIGIN(SRAM_DATA) + LENGTH(SRAM_DATA);</p>
    <p id="p1113mcpsimp"><a name="p1113mcpsimp"></a><a name="p1113mcpsimp"></a>__startup_stack = __heap_end - 0x20;</p>
    <p id="p1114mcpsimp"><a name="p1114mcpsimp"></a><a name="p1114mcpsimp"></a>__heap_size = __heap_end - __heap_start;</p>
    <p id="p1115mcpsimp"><a name="p1115mcpsimp"></a><a name="p1115mcpsimp"></a>. = ALIGN(0x10);</p>
    <p id="p1116mcpsimp"><a name="p1116mcpsimp"></a><a name="p1116mcpsimp"></a>__end = .;</p>
    </td>
    </tr>
    </tbody>
    </table>

## Summary<a name="ZH-CN_TOPIC_0000002555654509"></a>

<a name="table1184mcpsimp"></a>
<table><thead align="left"><tr id="row1190mcpsimp"><th class="cellrowborder" valign="top" width="18.81%" id="mcps1.1.4.1.1"><p id="p1192mcpsimp"><a name="p1192mcpsimp"></a><a name="p1192mcpsimp"></a><strong id="b1193mcpsimp"><a name="b1193mcpsimp"></a><a name="b1193mcpsimp"></a>Key Exception Information</strong></p>
</th>
<th class="cellrowborder" valign="top" width="15.840000000000002%" id="mcps1.1.4.1.2"><p id="p1195mcpsimp"><a name="p1195mcpsimp"></a><a name="p1195mcpsimp"></a><strong id="b1196mcpsimp"><a name="b1196mcpsimp"></a><a name="b1196mcpsimp"></a>Crash Cause</strong></p>
</th>
<th class="cellrowborder" valign="top" width="65.35%" id="mcps1.1.4.1.3"><p id="p1198mcpsimp"><a name="p1198mcpsimp"></a><a name="p1198mcpsimp"></a><strong id="b1199mcpsimp"><a name="b1199mcpsimp"></a><a name="b1199mcpsimp"></a>Root Cause Investigation Steps</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1200mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1202mcpsimp"><a name="p1202mcpsimp"></a><a name="p1202mcpsimp"></a>Stack overflow</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1204mcpsimp"><a name="p1204mcpsimp"></a><a name="p1204mcpsimp"></a>Stack overflow</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><p id="p18189184394811"><a name="p18189184394811"></a><a name="p18189184394811"></a>The specific thread where the stack overflow occurred can be determined through the task name and task ID (task ID:) in the log, and then the stack size can be adjusted or the code rectified in combination with the stack estimation tool.</p>
</td>
</tr>
<tr id="row1208mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1210mcpsimp"><a name="p1210mcpsimp"></a><a name="p1210mcpsimp"></a>Instruction access fault</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1212mcpsimp"><a name="p1212mcpsimp"></a><a name="p1212mcpsimp"></a>Instruction fetch exception</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><a name="ol1214mcpsimp"></a><a name="ol1214mcpsimp"></a><ol id="ol1214mcpsimp"><li>Locate the exception code context based on mtval and ra, and investigate the function pointer.</li><li>Check whether the code segment where the function resides has a copy operation; if so, investigate the linker script.</li><li>Investigate whether the code segment has been corrupted, which can be located through the PMP mechanism.</li></ol>
</td>
</tr>
<tr id="row1218mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1220mcpsimp"><a name="p1220mcpsimp"></a><a name="p1220mcpsimp"></a>Oops:NMI</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1222mcpsimp"><a name="p1222mcpsimp"></a><a name="p1222mcpsimp"></a>Watchdog timeout</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><p id="p12484145812485"><a name="p12484145812485"></a><a name="p12484145812485"></a>The cause can be determined based on the scheduling information recorded by trace before the timeout, the CPU usage information, and the call stacks of all tasks at the time of the exception.</p>
</td>
</tr>
<tr id="row1226mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1228mcpsimp"><a name="p1228mcpsimp"></a><a name="p1228mcpsimp"></a>Panic</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1230mcpsimp"><a name="p1230mcpsimp"></a><a name="p1230mcpsimp"></a>Active Panic</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><a name="ol1232mcpsimp"></a><a name="ol1232mcpsimp"></a><ol id="ol1232mcpsimp"><li>If the print contains the file name and line number, the source code location can be confirmed directly.</li><li>If the assertion fails, check why the assertion expression does not hold.</li><li>Search for printed information in the code or locate the hung code line based on mepc.</li></ol>
</td>
</tr>
<tr id="row1236mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1238mcpsimp"><a name="p1238mcpsimp"></a><a name="p1238mcpsimp"></a>PMP access fault</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1240mcpsimp"><a name="p1240mcpsimp"></a><a name="p1240mcpsimp"></a>Access to a PMP-protected address</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><a name="ol1242mcpsimp"></a><a name="ol1242mcpsimp"></a><ol id="ol1242mcpsimp"><li>Based on mepc and mtval, the memory address with the permission exception can be determined; investigate the PMP configuration.</li><li>If it is an instruction fetch issue, refer to the instruction fetch exception chapter for location.</li><li>If it is access to a memory region not covered by PMP configuration, refer to the memory corruption chapter for location.</li></ol>
</td>
</tr>
<tr id="row1246mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1248mcpsimp"><a name="p1248mcpsimp"></a><a name="p1248mcpsimp"></a>Store/AMO access fault</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1250mcpsimp"><a name="p1250mcpsimp"></a><a name="p1250mcpsimp"></a>Access to reserved memory</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><a name="ol1252mcpsimp"></a><a name="ol1252mcpsimp"></a><ol id="ol1252mcpsimp"><li>Locate the exceptional access address based on mtval and verify its validity.</li><li>Locate the faulting instruction address via mepc, reverse-lookup the disassembly, and locate the faulting source code.</li></ol>
</td>
</tr>
<tr id="row1255mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1257mcpsimp"><a name="p1257mcpsimp"></a><a name="p1257mcpsimp"></a>Dead lock</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1259mcpsimp"><a name="p1259mcpsimp"></a><a name="p1259mcpsimp"></a>Deadlock</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><p id="p1344355620488"><a name="p1344355620488"></a><a name="p1344355620488"></a>Reverse-lookup the request address to locate the faulting lock function.</p>
</td>
</tr>
<tr id="row1263mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="p1265mcpsimp"><a name="p1265mcpsimp"></a><a name="p1265mcpsimp"></a>Load/Store address misaligned</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1267mcpsimp"><a name="p1267mcpsimp"></a><a name="p1267mcpsimp"></a>Unaligned access</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><p id="p08275564814"><a name="p08275564814"></a><a name="p08275564814"></a>The code line where the unaligned access caused the hang can be located based on mepc.</p>
</td>
</tr>
<tr id="row1271mcpsimp"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.1.4.1.1 "><p id="entry1272mcpsimpp0"><a name="entry1272mcpsimpp0"></a><a name="entry1272mcpsimpp0"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="15.840000000000002%" headers="mcps1.1.4.1.2 "><p id="p1274mcpsimp"><a name="p1274mcpsimp"></a><a name="p1274mcpsimp"></a>Memory corruption, OOM, unaligned memory layout</p>
</td>
<td class="cellrowborder" valign="top" width="65.35%" headers="mcps1.1.4.1.3 "><a name="ol1276mcpsimp"></a><a name="ol1276mcpsimp"></a><ol id="ol1276mcpsimp"><li>After confirming the suspicion point, use the existing DFX tools to investigate.</li><li>Analyze in combination with business logic.</li></ol>
</td>
</tr>
</tbody>
</table>



