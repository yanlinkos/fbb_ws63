# Preface<a name="ZH-CN_TOPIC_0000001809364380"></a>

**Overview<a name="section4537382116410"></a>**

This document describes the development implementation examples of the TLS/DTLS component.

TLS/DTLS and other cryptographic suites are implemented based on the open-source component mbedtls 3.1.0. For details, see the official documentation: [https://tls.mbed.org/api/index.html](https://tls.mbed.org/api/index.html)

If the version of the official documentation is inconsistent with the SDK version, refer to the official release notes: [https://github.com/ARMmbed/mbedtls/releases](https://github.com/ARMmbed/mbedtls/releases)

**Product Version<a name="section12266191774710"></a>**

The product versions corresponding to this document are as follows.

<a name="table2270181717471"></a>
<table><thead align="left"><tr id="row15364171712479"><th class="cellrowborder" valign="top" width="31.759999999999998%" id="mcps1.1.3.1.1"><p id="p123646174478"><a name="p123646174478"></a><a name="p123646174478"></a><strong id="b2730202411138"><a name="b2730202411138"></a><a name="b2730202411138"></a>Product Name</strong></p>
</th>
<th class="cellrowborder" valign="top" width="68.24%" id="mcps1.1.3.1.2"><p id="p1936401717470"><a name="p1936401717470"></a><a name="p1936401717470"></a><strong id="b273519247132"><a name="b273519247132"></a><a name="b273519247132"></a>Product Version</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row19364317104716"><td class="cellrowborder" valign="top" width="31.759999999999998%" headers="mcps1.1.3.1.1 "><p id="p31080012"><a name="p31080012"></a><a name="p31080012"></a>WS63</p>
</td>
<td class="cellrowborder" valign="top" width="68.24%" headers="mcps1.1.3.1.2 "><p id="p34453054"><a name="p34453054"></a><a name="p34453054"></a>V100</p>
</td>
</tr>
</tbody>
</table>

**Audience<a name="section4378592816410"></a>**

This document is mainly applicable to the following engineers:

-   Technical Support Engineer
-   Software Development Engineer

**Symbol Conventions<a name="section133020216410"></a>**

The following symbols may appear in this document. Their meanings are as follows.

<a name="table2622507016410"></a>
<table><thead align="left"><tr id="row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="p6450074116410"><a name="p6450074116410"></a><a name="p6450074116410"></a><strong id="b2136615816410"><a name="b2136615816410"></a><a name="b2136615816410"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="p5435366816410"><a name="p5435366816410"></a><a name="p5435366816410"></a><strong id="b5941558116410"><a name="b5941558116410"></a><a name="b5941558116410"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001856243053.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a hazard with a high level of risk that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809364392.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a hazard with a medium level of risk that, if not avoided, could result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001856243057.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a hazard with a low level of risk that, if not avoided, could result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001856163057.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey device or environment safety warning information. If not avoided, it may result in device damage, data loss, degraded device performance, or other unpredictable consequences.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>"Notice" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="15.96" width="47.88" src="figures/en_image_0000001809524256.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary explanation of key information in the text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>"Note" is not a safety warning and does not involve personal, device, or environmental harm.</p>
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
<tbody><tr id="row2382023171315"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p33852341310"><a name="p33852341310"></a><a name="p33852341310"></a>02</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p9389237133"><a name="p9389237133"></a><a name="p9389237133"></a>2024-10-14</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p17389239139"><a name="p17389239139"></a><a name="p17389239139"></a>Updated the content of the "<a href="notes_on_default_configuration_changes_for_fcc_certification.md">Notes on Default Configuration Changes for FCC Certification</a>" section.</p>
</td>
</tr>
<tr id="row189967461154"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p15567674319"><a name="p15567674319"></a><a name="p15567674319"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p0567117232"><a name="p0567117232"></a><a name="p0567117232"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1031614161639"><a name="p1031614161639"></a><a name="p1031614161639"></a>First official release.</p>
</td>
</tr>
<tr id="row5947359616410"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p2149706016410"><a name="p2149706016410"></a><a name="p2149706016410"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p648803616410"><a name="p648803616410"></a><a name="p648803616410"></a>2024-03-15</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>First interim release.</p>
</td>
</tr>
</tbody>
</table>

# API Interface Description<a name="ZH-CN_TOPIC_0000001856243049"></a>




## Structure Description<a name="ZH-CN_TOPIC_0000001809364372"></a>

For detailed mbedtls structure descriptions, refer to the official documentation: [https://tls.mbed.org/api/annotated.html](https://tls.mbed.org/api/annotated.html)

## API List<a name="ZH-CN_TOPIC_0000001809524248"></a>

For detailed mbedtls API descriptions, refer to the official documentation: [https://tls.mbed.org/api/globals\_func.html](https://tls.mbed.org/api/globals_func.html)

## Configuration Description<a name="ZH-CN_TOPIC_0000001856243041"></a>

For detailed mbedtls configuration item descriptions, refer to the official documentation: [https://tls.mbed.org/api/config\_8h.html\#ab3bca0048342cf2789e7d170548ff3a5](https://tls.mbed.org/api/config_8h.html#ab3bca0048342cf2789e7d170548ff3a5)

# Development Guide<a name="ZH-CN_TOPIC_0000001809524244"></a>

For detailed mbedtls development demos, refer to the official documentation: [https://tls.mbed.org/api/modules.html](https://tls.mbed.org/api/modules.html)

# Hardware Adaptation<a name="ZH-CN_TOPIC_0000001856243045"></a>



## Configuration Description<a name="ZH-CN_TOPIC_0000001809364376"></a>

Add the MBEDTLS\_HARDEN\_OPEN macro to the corresponding build target in build\\config\\target\_config\\ws63\\config.py of the project to enable the hardware acceleration callback interface registration function.

Enabling the corresponding algorithm macros in mbedtls\_v3.1.0\\harden\\platform\\connect\\mbedtls\_platform\_hardware\_config.h will directly invoke the hardware driver interfaces.

Currently supported hardware algorithms include AES, RSA, HASH, big-number modular exponentiation, random number, and ECP algorithms.

## Adaptation Description<a name="ZH-CN_TOPIC_0000001809524252"></a>







### AES Adaptation<a name="ZH-CN_TOPIC_0000001856163045"></a>

-   After MBEDTLS\_AES\_ALT is enabled, the AES algorithm locks the hardware accelerator resources when using the hardware accelerator, that is, AES operations are blocking until the driver obtains the resources or a timeout occurs and returns failure.

### Big-Number Modular Exponentiation Adaptation<a name="ZH-CN_TOPIC_0000001809364360"></a>

-   After MBEDTLS\_BIGNUM\_EXP\_MOD\_USE\_HARDWARE is enabled, the hardware driver interfaces are invoked to complete big-number modular exponentiation operations.

### Random Number Adaptation<a name="ZH-CN_TOPIC_0000001856243033"></a>

After MBEDTLS\_ENTROPY\_HARDWARE\_ALT is enabled, the system adds the hardware random number by default as a strong random number source. If this macro is disabled and the user has not registered another strong random number source, mbedTLS cannot provide secure random numbers, affecting the security of the system.

### RSA Digital Signature Adaptation<a name="ZH-CN_TOPIC_0000001809364364"></a>

After the MBEDTLS\_RSA\_ALT compile-time macro is enabled, mbedTLS performs hardware acceleration for RSA digital signature and signature verification operations.

### HASH Algorithm Adaptation<a name="ZH-CN_TOPIC_0000001863121673"></a>

The hardware-accelerated HASH algorithms supported by the current WS63 specifications include SHA1, SHA224, SHA256, SHA384, and SHA512, which are enabled by enabling MBEDTLS\_SHA1\_USE\_HARDWARE, MBEDTLS\_SHA224\_USE\_HARDWARE, MBEDTLS\_SHA256\_USE\_HARDWARE, MBEDTLS\_SHA384\_USE\_HARDWARE, and MBEDTLS\_SHA512\_USE\_HARDWARE respectively.

### ECP Adaptation<a name="ZH-CN_TOPIC_0000001809364368"></a>

The hardware-accelerated ECP algorithms supported by the current WS63 specifications include SECP192R1, SECP224R1, SECP256R1, SECP384R1, SECP521R1, BP256R1, BP384R1, BP512R1, CURVE25519, and CURVE448, which are enabled by enabling MBEDTLS\_SECP192R1\_USE\_HARDWARE, MBEDTLS\_SECP224R1\_USE\_HARDWARE, MBEDTLS\_SECP256R1\_USE\_HARDWARE, MBEDTLS\_SECP384R1\_USE\_HARDWARE, MBEDTLS\_SECP521R1\_USE\_HARDWARE, MBEDTLS\_BP256R1\_USE\_HARDWARE, MBEDTLS\_BP384R1\_USE\_HARDWARE, MBEDTLS\_BP512R1\_USE\_HARDWARE, MBEDTLS\_CURVE25519\_USE\_HARDWARE, and MBEDTLS\_CURVE448\_USE\_HARDWARE.

# Precautions<a name="ZH-CN_TOPIC_0000001809524240"></a>





## Precautions on Configuring the SSL Receive Buffer<a name="ZH-CN_TOPIC_0000001856163033"></a>

-   The SSL receive buffer is controlled by the compile-time option MBEDTLS\_SSL\_IN\_CONTENT\_LEN, which defaults to 16KB. In actual applications, if the user can ensure that the maximum length of the SSL upper-layer data packets does not exceed 2KB or 4KB, the length of the SSL receive buffer can be set through the mbedtls\_ssl\_conf\_max\_frag\_len interface to save memory.

    **Note: The mbedtls\_ssl\_conf\_max\_frag\_len interface must be called before the mbedtls\_ssl\_setup interface.**

-   Considering that multi-level digital certificates may cause the TLS handshake packet to be longer than 1KB, when the mbedtls\_ssl\_conf\_max\_frag\_len interface is called, mbedtls modifies the receive buffer only when mfl\_code is MBEDTLS\_SSL\_MAX\_FRAG\_LEN\_2048 or MBEDTLS\_SSL\_MAX\_FRAG\_LEN\_4096. If mfl\_code is MBEDTLS\_SSL\_MAX\_FRAG\_LEN\_512 or MBEDTLS\_SSL\_MAX\_FRAG\_LEN\_1024, the receive buffer remains 16KB.
-   If the SSL receive buffer is changed to 2KB or 4KB and the Client receives a packet larger than 2KB or 4KB from the Server, the mbedtls\_ssl\_read interface returns failure at this time, with the error code MBEDTLS\_ERR\_SSL\_MSG\_TOO\_LONG (a newly added specific error code). When the user obtains this error code, the SSL connection must be closed, and no further data may be received from the SSL link.
-   Setting the SSL receive buffer through the mbedtls\_ssl\_conf\_max\_frag\_len interface currently takes effect only for the SSL Client.

## Precautions on Digital Certificate Validity Verification<a name="ZH-CN_TOPIC_0000001856243037"></a>

Because the WS63 platform has no Real Time Controller, the UTC time cannot be obtained after the system starts. In this case, the validity verification of digital certificates fails, causing TLS link establishment to fail. To address this situation, mbedtls disables MBEDTLS\_HAVE\_TIME\_DATE by default, and TLS certificate verification is disabled accordingly. If the user can obtain the UTC time through other means (for example, SNTP) before TLS certificate verification, the MBEDTLS\_HAVE\_TIME\_DATE compile-time macro can be enabled.

## Notes on Changes to Some Default Configurations<a name="ZH-CN_TOPIC_0000001856163041"></a>

The default configuration of the MbedTLS security library is defined in the include/mbedtls/mbedtls\_config.h file. The open-source version enables most features by default. LiteOS has moderately modified the default configuration of MbedTLS, mainly to enhance the security of MbedTLS and reduce the code size. The modified MbedTLS meets most IoT scenarios. The main principles of the changes are as follows:

-   The default configuration must guarantee security requirements.
-   Disable insecure algorithms or features.
-   Disable features unsuitable for IoT scenarios, such as the TLS Server mode and X509 certificate signing request (CSR).
-   Disable algorithms unsuitable for IoT scenarios, such as the SECP521R1 ECC curve. In IoT scenarios, ECC curves with 128-bit security strength are recommended.
-   Disable rarely used algorithms or features, such as PKCS\#12 certificates, which are rarely used in IoT scenarios. Enabling PKCS\#12 may pose certain application risks.

## Notes on Default Configuration Changes for FCC Certification<a name="ZH-CN_TOPIC_0000002070167405"></a>

FCC certification is a mandatory EMC certification mainly for electronic and electrical products ranging from 9K to 3000GHZ, covering radio, communication, and other aspects. The FCC certification process relies on the KEY\_EXCHANGE\_ECDHE\_RSA algorithm, which is not enabled by default. If the device needs to pass FCC certification, this algorithm can be enabled. Enabling method: modify the open\_source/mbedtls/mbedtls\_v3.1.0/harden/platform/connect/mbedtls\_platform\_hardware\_config.h file and comment out \#undef MBEDTLS\_KEY\_EXCHANGE\_ECDHE\_RSA\_ENABLED.

