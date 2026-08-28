# Preface<a name="ZH-CN_TOPIC_0000001880631385"></a>

**Overview<a name="section64031159132213"></a>**

This document describes the structure of the CIPHER DRIVER and how to use its software interfaces.

**Product Version<a name="section278mcpsimp"></a>**

The product version corresponding to this document is as follows.

<a name="table281mcpsimp"></a>
<table><thead align="left"><tr id="row286mcpsimp"><th class="cellrowborder" valign="top" width="45%" id="mcps1.1.3.1.1"><p id="p288mcpsimp"><a name="p288mcpsimp"></a><a name="p288mcpsimp"></a>Product Name</p>
</th>
<th class="cellrowborder" valign="top" width="55.00000000000001%" id="mcps1.1.3.1.2"><p id="p290mcpsimp"><a name="p290mcpsimp"></a><a name="p290mcpsimp"></a>Product Version</p>
</th>
</tr>
</thead>
<tbody><tr id="row292mcpsimp"><td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.3.1.1 "><p id="p294mcpsimp"><a name="p294mcpsimp"></a><a name="p294mcpsimp"></a>WS63</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.1.3.1.2 "><p id="p296mcpsimp"><a name="p296mcpsimp"></a><a name="p296mcpsimp"></a>V100</p>
</td>
</tr>
</tbody>
</table>

**Intended Audience<a name="section297mcpsimp"></a>**

This document is intended for the following engineers:

-   Technical support engineers
-   Software development engineers

**Symbol Conventions<a name="section303mcpsimp"></a>**

The following symbols may appear in this document. Their meanings are as follows.

<a name="table306mcpsimp"></a>
<table><thead align="left"><tr id="row311mcpsimp"><th class="cellrowborder" valign="top" width="21%" id="mcps1.1.3.1.1"><p id="p313mcpsimp"><a name="p313mcpsimp"></a><a name="p313mcpsimp"></a><strong id="b314mcpsimp"><a name="b314mcpsimp"></a><a name="b314mcpsimp"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79%" id="mcps1.1.3.1.2"><p id="p316mcpsimp"><a name="p316mcpsimp"></a><a name="p316mcpsimp"></a><strong id="b317mcpsimp"><a name="b317mcpsimp"></a><a name="b317mcpsimp"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row319mcpsimp"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.3.1.1 "><p class="msonormal" id="p321mcpsimp"><a name="p321mcpsimp"></a><a name="p321mcpsimp"></a><a name="image123"></a><a name="image123"></a><span><img id="image123" src="figures/en_image_0000001833673048.png" height="23.94" width="67.83"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.1.3.1.2 "><p id="p323mcpsimp"><a name="p323mcpsimp"></a><a name="p323mcpsimp"></a>Indicates a hazard with a high level of risk that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row324mcpsimp"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.3.1.1 "><p class="msonormal" id="p326mcpsimp"><a name="p326mcpsimp"></a><a name="p326mcpsimp"></a><a name="image124"></a><a name="image124"></a><span><img id="image124" src="figures/en_image_0000001833832832.png" height="23.94" width="67.83"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.1.3.1.2 "><p id="p328mcpsimp"><a name="p328mcpsimp"></a><a name="p328mcpsimp"></a>Indicates a hazard with a medium level of risk that, if not avoided, could result in death or serious injury.</p>
</td>
</tr>
<tr id="row329mcpsimp"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.3.1.1 "><p class="msonormal" id="p331mcpsimp"><a name="p331mcpsimp"></a><a name="p331mcpsimp"></a><a name="image125"></a><a name="image125"></a><span><img id="image125" src="figures/en_image_0000001880632121.png" height="23.94" width="67.83"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.1.3.1.2 "><p id="p333mcpsimp"><a name="p333mcpsimp"></a><a name="p333mcpsimp"></a>Indicates a hazard with a low level of risk that, if not avoided, could result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row334mcpsimp"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.3.1.1 "><p class="msonormal" id="p336mcpsimp"><a name="p336mcpsimp"></a><a name="p336mcpsimp"></a><a name="image126"></a><a name="image126"></a><span><img id="image126" src="figures/en_image_0000001880472333.png" height="23.94" width="67.83"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.1.3.1.2 "><p id="p338mcpsimp"><a name="p338mcpsimp"></a><a name="p338mcpsimp"></a>Used to convey device or environment safety warning information. If not avoided, it may result in device damage, data loss, reduced device performance, or other unpredictable results.</p>
<p id="p339mcpsimp"><a name="p339mcpsimp"></a><a name="p339mcpsimp"></a>"Notice" does not involve personal injury.</p>
</td>
</tr>
<tr id="row340mcpsimp"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.3.1.1 "><p class="msonormal" id="p342mcpsimp"><a name="p342mcpsimp"></a><a name="p342mcpsimp"></a><a name="image127"></a><a name="image127"></a><span><img id="image127" src="figures/en_image_0000001833673052.png" height="23.94" width="67.83"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.1.3.1.2 "><p id="p344mcpsimp"><a name="p344mcpsimp"></a><a name="p344mcpsimp"></a>Supplementary explanation of key information in the text.</p>
<p id="p345mcpsimp"><a name="p345mcpsimp"></a><a name="p345mcpsimp"></a>"Note" is not safety warning information and does not involve personal, device, or environmental injury information.</p>
</td>
</tr>
</tbody>
</table>

**Revision History<a name="section346mcpsimp"></a>**

<a name="table348mcpsimp"></a>
<table><thead align="left"><tr id="row354mcpsimp"><th class="cellrowborder" valign="top" width="21%" id="mcps1.1.4.1.1"><p id="p356mcpsimp"><a name="p356mcpsimp"></a><a name="p356mcpsimp"></a><strong id="b357mcpsimp"><a name="b357mcpsimp"></a><a name="b357mcpsimp"></a>Document Version</strong></p>
</th>
<th class="cellrowborder" valign="top" width="26%" id="mcps1.1.4.1.2"><p id="p359mcpsimp"><a name="p359mcpsimp"></a><a name="p359mcpsimp"></a><strong id="b360mcpsimp"><a name="b360mcpsimp"></a><a name="b360mcpsimp"></a>Release Date</strong></p>
</th>
<th class="cellrowborder" valign="top" width="53%" id="mcps1.1.4.1.3"><p id="p362mcpsimp"><a name="p362mcpsimp"></a><a name="p362mcpsimp"></a><strong id="b363mcpsimp"><a name="b363mcpsimp"></a><a name="b363mcpsimp"></a>Modification Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row134899107451"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.4.1.1 "><p id="p3489181024519"><a name="p3489181024519"></a><a name="p3489181024519"></a>03</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.4.1.2 "><p id="p11489510134515"><a name="p11489510134515"></a><a name="p11489510134515"></a>2025-08-29</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.1.4.1.3 "><p id="p184891710134510"><a name="p184891710134510"></a><a name="p184891710134510"></a>Updated the content of the "<a href="functional_description.md">Functional Description</a>" chapter.</p>
</td>
</tr>
<tr id="row16625121412313"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.4.1.1 "><p id="p10626141462311"><a name="p10626141462311"></a><a name="p10626141462311"></a>02</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.4.1.2 "><p id="p18626161419230"><a name="p18626161419230"></a><a name="p18626161419230"></a>2024-06-27</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.1.4.1.3 "><a name="ul195351537162619"></a><a name="ul195351537162619"></a><ul id="ul195351537162619"><li>Updated the content of the "<a href="usage_process.md">Usage Process</a>" chapter.</li><li>Updated the content of the "<a href="error_types.md">Error Types</a>" chapter.</li></ul>
</td>
</tr>
<tr id="row117961384314"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.4.1.1 "><p id="p118382762110"><a name="p118382762110"></a><a name="p118382762110"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.4.1.2 "><p id="p171834279217"><a name="p171834279217"></a><a name="p171834279217"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.1.4.1.3 "><p id="p618317279212"><a name="p618317279212"></a><a name="p618317279212"></a>First official release.</p>
</td>
</tr>
<tr id="row365mcpsimp"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.4.1.1 "><p id="p367mcpsimp"><a name="p367mcpsimp"></a><a name="p367mcpsimp"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.4.1.2 "><p id="p369mcpsimp"><a name="p369mcpsimp"></a><a name="p369mcpsimp"></a>2024-03-29</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.1.4.1.3 "><p id="p371mcpsimp"><a name="p371mcpsimp"></a><a name="p371mcpsimp"></a>First interim release.</p>
</td>
</tr>
</tbody>
</table>

# Overview<a name="ZH-CN_TOPIC_0000001833669648"></a>



## Functional Description<a name="ZH-CN_TOPIC_0000001880468929"></a>

CIPHER DRIVER is a security algorithm module that provides two types of interfaces externally: mbedtls API and service layer, as shown in [Figure 1](#fig727383712313).

-   mbedtls API
    -   The security driver integrates with the open-source third-party mbedtls interface. Hardware security capabilities can be used by calling the mbedtls API.
    -   mbedtls integration is completed for all hardware-supported specifications. For the hardening scope and API usage, refer to the "WS63V100 TLS & DTLS Development Guide".

-   service layer
    -   The self-developed security driver interface provides upper-layer services with the capability to use hardware security directly, supporting OS environments such as LiteOS/FreeRTOS/AliOS and non-OS environments such as flashboot/bootrom.

-   CIPHER DRIVER provides the following algorithms:
    -   Symmetric encryption and decryption algorithms such as AES and SM4.
    -   Digest algorithms such as HASH, SM3, HASH-MAC, and SM3-MAC.
    -   Asymmetric algorithms such as RSA, ECC, SM2 signing and verification, key agreement, encryption and decryption, and large number arithmetic.
    -   Hardware key management.
    -   Random number algorithm.
    -   FLASH on-the-fly decryption.
    -   Mainly used in scenarios such as secure boot, secure storage, and secure communication of AIOT products.

-   CIPHER DRIVER consists of 5 sub-modules: SPACC (symc, hash), PKE, KM, TRNG, and FAPC.

**Figure 1**  CIPHER DRIVER context diagram<a name="fig727383712313"></a>  
![](figures/cipher_driver_context_diagram.png "cipher_driver_context_diagram.png")






### SPACC<a name="ZH-CN_TOPIC_0000001880628701"></a>

The SPACC (Security Protocol Accelerator) module implements the cipher symmetric encryption/decryption algorithms and the HASH and HMAC digest algorithms.



#### Symmetric Encryption and Decryption Algorithms<a name="ZH-CN_TOPIC_0000001833829428"></a>

-   AES: Supports 9 working modes: ECB/CBC/CFB/OFB/CTR/CCM/GCM/CMAC/CBC\_MAC. Among them:
    -   In CFB mode, the encryption data width can be 8/128 bits.
    -   In OFB mode, the encryption data width can be 128 bits.
    -   In CCM/GCM modes, the TAG value must be obtained once after encryption/decryption is complete.
    -   In ECB, CBC, and CBC\_MAC modes, the encrypted data length must be aligned to 16 bytes. In CMAC mode, the last block of encrypted data is allowed to be not aligned to 16 bytes.
    -   Supports AES-128, AES-192, and AES-256 (128, 192, and 256 refer to the length of the key passed in, in bits).

-   SM4: Supports 5 working modes: ECB/CBC/CTR/CFB/OFB. Supports SM4-128. Except in CTR mode, the encrypted data length must be aligned to 16 bytes.

The cipher driver supports software multi-channel, and each chip can configure it in the porting file as needed. It supports low-power mode, which is enabled by default. It supports polling and wait\_event modes. If a wait func is registered, the wait\_event mode is used; otherwise, the polling mode is used.

>![](public_sys-resources/icon-note.gif) **Note:** 
>The ECB mode is a non-secure algorithm and is not recommended.

#### Digest Algorithms<a name="ZH-CN_TOPIC_0000001833669652"></a>

-   HASH: Supports SHA1/SHA224/SHA256/SHA384/SHA512/SM3.
-   HMAC: Supports HMAC-SHA1/HMAC-SHA224/HMAC-SHA256/HMAC-SHA384/HMAC-SHA512/HMAC-SM3.

HASH and HMAC support passing data blocks that are not aligned to the block size mid-stream. They support software multi-channel, which each chip can configure in the porting file as needed. They support low-power mode, which is enabled by default. They support polling and wait\_event modes. If a wait func is registered, the wait\_event mode is used; otherwise, the polling mode is used. HASH supports a retry mechanism: if an interface call fails mid-process, the interface can be called again until it succeeds, without restarting the entire computation flow. For details, refer to the usage descriptions of the uapi\_drv\_cipher\_hash\_start, uapi\_drv\_cipher\_hash\_update, and uapi\_drv\_cipher\_hash\_finish interfaces in the "WS63V100 SECURITY DRIVER API manual".

>![](public_sys-resources/icon-note.gif) **Note:** 
>SHA1/SHA224 are non-secure algorithms and are not recommended.

### PKE<a name="ZH-CN_TOPIC_0000001880468933"></a>

PKE (Public Key Encryption) is the asymmetric encryption and decryption algorithm. It is commonly used for file signing and signature verification, as well as for encrypting and decrypting symmetric keys. It mainly includes the following algorithms:

-   RSA
    -   Supports private key signing and public key verification in two modes: PKCS\#1 v1.5 and PKCS\#1 v2.1 PSS.
    -   Supports public key encryption and private key decryption in two modes: PKCS\#1 v1.5 and PKCS\#1 v2.1 OAEP.
    -   Supports key widths of 1024/2048/3072/4096.

-   ECC
    -   Supports private key signing and public key verification for RFC 5639-Brainpool P256/384/512r1, NIST FIPS 186-4 P192/224/256/384/521, and RFC 8032-ED25519 (that is, EDDSA).
    -   Supports key widths of 192/224/256/384/512\(521\).

-   SM2
    -   Supports SM2 public key encryption and private key decryption.
    -   Supports SM2 private key signing and public key verification.

-   Key Agreement
    -   Supports public-private key pair generation for RFC 5639-Brainpool P256/384/512r1, NIST FIPS 186-4 P192/224/256/384/521, RFC 7748-Curve25519/Curve448, RFC 8032-ED25519 (that is, EDDSA), and SM2, as well as generating the corresponding public key from a given private key.
    -   Supports key exchange (ECDH) for RFC 5639-Brainpool P256/384/512r1, NIST FIPS 186-4 P192/224/256/384/521, RFC 7748-Curve25519/Curve448, and SM2.
    -   Supports DH key agreement of 192/224/256/384/512/521/1024/2048/3072/4096 bits.

-   Verification of Points on a Curve
    -   Supports verification of whether a point lies on the curve for RFC 5639-Brainpool P256/384/512r1, NIST FIPS 186-4 P192/224/256/384/521, and SM2.

-   Large Number Arithmetic
    -   Supports modular addition, modular subtraction, modular multiplication, modular inverse, modular exponentiation, and modular arithmetic of up to 4096 bits.
    -   Supports regular large number multiplication of up to 2048 bits.

PKE supports low-power mode, which is enabled by default. It supports polling and wait\_event modes. If a wait func is registered, the wait\_event mode is used; otherwise, the polling mode is used.

>![](public_sys-resources/icon-note.gif) **Note:** 
>NIST FIPS 186-4 P192/224/256/384/521, PKCS\#1 v1.5, RSA 1024/2048, ECDH below 256 bits, and DH below 2048 bits are non-secure algorithms and are not recommended.

### KM<a name="ZH-CN_TOPIC_0000001880628705"></a>

KM is the key management module, which enhances key security strength. It is used to load keys into keyslots for use by SPACC and FLASH on-the-fly decryption. It supports hardware keys and software keys, 8 cipher keyslot channels, and 2 hmac keyslot channels.

### TRNG<a name="ZH-CN_TOPIC_0000001833829432"></a>

The random number acquisition module obtains true random numbers generated by hardware.

### FAPC<a name="ZH-CN_TOPIC_0000001833669656"></a>

Through the fapc controller, the parameters related to the FLASH on-the-fly decryption operation are configured. fapc supports configuring 4 regions, and regions can use the same IV value. FLASH on-the-fly decryption uses the AES-128-CTR algorithm.

## Usage Process<a name="ZH-CN_TOPIC_0000001880468937"></a>

During system initialization, uapi\_drv\_cipher\_env\_init is automatically called to complete the basic initialization environment configuration of the CIPHER DRIVER. Users do not need to call it separately.

















### Key Configuration<a name="ZH-CN_TOPIC_0000001880628709"></a>





#### Scenario Description<a name="ZH-CN_TOPIC_0000001833829436"></a>

Generates and configures the software keys and hardware keys required by SPACC and the on-the-fly decryption module. Software keys can be generated using the PBKDF2 and HKDF algorithms. The keyslot stores the final software or hardware key for use by SPACC and on-the-fly decryption. Supports AES 128/192/256-bit encryption and decryption, and supports HMAC.

#### Software Key Configuration Workflow<a name="ZH-CN_TOPIC_0000001833669660"></a>

1.  Initialize the KM module by calling uapi\_drv\_km\_init.
2.  Create a keyslot channel. This operation is not required for FLASH on-the-fly decryption. Use the uapi\_drv\_keyslot\_create interface. (If the configured key is used by the SPACC module, this step must be completed before the caller calls the SPACC module interface to bind the keyslot channel.)
3.  Create a klad and obtain the klad handle. Use the uapi\_drv\_klad\_create interface.
4.  Bind the keyslot channel to the klad handle. Use the uapi\_drv\_klad\_attach interface. The order of steps 2 and 4 can be swapped.
5.  Configure the klad attributes. These include:

    -   The root\_key type corresponding to the key.
    -   The algorithms for which the key can be used.
    -   Whether the key can be used for encryption or decryption operations.
    -   Whether the key is a secure or non-secure key.
    -   Whether the key can only be used by the CPU that configured it.
    -   Whether the source and destination buffer types are secure or non-secure (see the note below for details).

    Use the uapi\_drv\_klad\_set\_attr interface.

6.  Configure the software key. Use the uapi\_drv\_klad\_set\_clear\_key interface. SPACC
7.  Unbind the keyslot and the klad handle. For FLASH on-the-fly decryption operations, specify the corresponding operation type. Use the uapi\_drv\_klad\_detach interface.
8.  Destroy the klad handle. Use the uapi\_drv\_klad\_destroy interface.
9.  Destroy the keyslot handle. Use the uapi\_drv\_keyslot\_destroy interface.
10. Deinitialize the KM module by calling uapi\_drv\_km\_deinit.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >The source and destination buffer types configured by klad correspond to the buffer types of the SPACC module. If the source data buffer here is configured to support only secure buffers while the SPACC module source buffer is configured as a non-secure buffer, an error will be reported during the computation. Steps 9 and 10 must be performed after SPACC, HMAC, and FLASH on-the-fly decryption have finished using the keyslot; otherwise, computation errors will occur.

#### Hardware Key Configuration Workflow<a name="ZH-CN_TOPIC_0000001880468941"></a>

1.  Initialize the KM module by calling uapi\_drv\_km\_init.
2.  Create a keyslot channel. This operation is not required for FLASH on-the-fly decryption. Use the uapi\_drv\_keyslot\_create interface. (If the configured key is used by the SPACC module, this step must be completed before the caller calls the SPACC module interface to bind the keyslot channel.)
3.  Create a klad and obtain the klad handle. Use the uapi\_drv\_klad\_create interface.
4.  Bind the keyslot channel to the klad handle. For FLASH on-the-fly decryption operations, specify the corresponding operation type. Use the uapi\_drv\_klad\_attach interface. The order of steps 2 and 4 can be swapped.
5.  Configure the klad attributes. These include:

    -   The root\_key type corresponding to the key.
    -   The algorithms for which the key can be used.
    -   Whether the key can be used for encryption or decryption operations.
    -   Whether the key is a secure or non-secure key.
    -   Whether the key can only be used by the CPU that configured it.
    -   Whether the source and destination buffer types are secure or non-secure (see the note below for details).

    Use the uapi\_drv\_klad\_set\_attr interface.

6.  Configure the hardware key. Use the uapi\_drv\_klad\_set\_effective\_key interface.
7.  Unbind the keyslot and the klad handle. For FLASH on-the-fly decryption operations, specify the corresponding operation type. Use the uapi\_drv\_klad\_detach interface.
8.  Destroy the klad handle. Use the uapi\_drv\_klad\_destroy interface.
9.  Destroy the keyslot handle. Use the uapi\_drv\_keyslot\_destroy interface.
10. Deinitialize the KM module by calling uapi\_drv\_km\_deinit.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >-   The source and destination buffer types configured by klad correspond to the buffer types of the SPACC module. If the source data buffer here is configured to support only secure buffers while the SPACC module source buffer is configured as a non-secure buffer, an error will be reported during the computation. Steps 9 and 10 must be performed after SPACC, HMAC, and FLASH on-the-fly decryption have finished using the keyslot; otherwise, computation errors will occur.
    >-   To configure a hardware key, the corresponding eFuse must be programmed so that the correct working key can be obtained in the keyslot channel. Otherwise, the result of the computation using this key will be incorrect. For the eFuse programming process, see the "[1.2.16 Security-related eFuse Programming Recommendations](security_related_efuse_programming_recommendations.md)" section.

#### Precautions<a name="ZH-CN_TOPIC_0000001880628713"></a>

Hardware key configuration depends on the corresponding EFUSE. For details on how to program the eFuse, see the "[Security-related eFuse Programming Recommendations](security_related_efuse_programming_recommendations.md)" section.

### Symmetric Encryption and Decryption<a name="ZH-CN_TOPIC_0000001833829440"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001833669664"></a>

Encrypts or decrypts data and supports encryption/decryption operations in the following scenarios:

-   The source data resides in DDR, RAM, or flash.
-   The destination data resides in DDR or RAM.

In-place encryption and decryption operations are supported, that is, the input and output use the same buffer address.

#### Workflow<a name="ZH-CN_TOPIC_0000001880468945"></a>

1.  Initialize the SYMC module by calling uapi\_drv\_cipher\_symc\_init.
2.  Create a symc channel and obtain the symc handle. Use the uapi\_drv\_cipher\_symc\_create interface.
3.  Create a keyslot channel. Use the uapi\_drv\_keyslot\_create interface.
4.  Bind the keyslot channel to the symc handle. Use the uapi\_drv\_cipher\_symc\_attach interface. For keyslot channel creation, refer to the descriptions of the KEYSLOT & KLAD interfaces.
5.  <a name="li845893131117"></a>Configure the symc algorithm parameter information. These include:

    -   Basic key attributes (length, parity).
    -   Initial vector.
    -   Encryption/decryption data width (CFB/OFB modes).
    -   Key update method (reset the IV each time / use the IV configured for the previous data packet).
    -   Additional Authenticated Data (GCM/CCM modes).

    Use the uapi\_drv\_cipher\_symc\_set\_config interface.

6.  <a name="li858441161019"></a>Encrypt or decrypt the data. Users can call either of the following interfaces for encryption and decryption.
    -   Encryption: uapi\_drv\_cipher\_symc\_encrypt
    -   Decryption: uapi\_drv\_cipher\_symc\_decrypt

7.  If the mode is CCM or GCM, continue to call the uapi\_drv\_cipher\_symc\_get\_tag interface to obtain the TAG value. Otherwise, proceed directly to [Step 8](#li1458421120101).
8.  <a name="li1458421120101"></a>Unbind the keyslot channel from the cipher handle. Use the uapi\_drv\_cipher\_symc\_detach interface.
9.  Destroy the symc handle. Use the uapi\_drv\_cipher\_symc\_destroy interface.
10. Deinitialize the SYMC module by calling uapi\_drv\_cipher\_symc\_deinit.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >After [Step 5](#li845893131117) is configured, multiple packets are allowed to use the same configuration information, and the operation in [Step 6](#li858441161019) can be performed continuously based on it. In this case, the scenario is similar to configuring the IV update method in [Step 5](#li845893131117) as using the IV configured for the previous data packet (CRYPTO\_SYMC\_CCM\_IV\_DO\_NOT\_CHANGE/UAPI\_DRV\_CIPHER\_SYMC\_GCM\_IV\_DO\_NOT\_CHANGE/UAPI\_DRV\_CIPHER\_SYMC\_CCM\_IV\_DO\_NOT\_CHANGE).

#### Precautions<a name="ZH-CN_TOPIC_0000001880628721"></a>

-   Supports 7 AES modes: ECB/CBC/CFB/OFB/CTR/CCM/GCM.
    -   For ECB/CBC/CFB/OFB/CTR modes, retry is supported. That is, if the uapi\_drv\_cipher\_symc\_encrypt/uapi\_drv\_cipher\_symc\_decrypt interface call fails, the interface can still be called again with correct parameters to complete the subsequent data encryption and decryption.
    -   For CCM/GCM modes, retry is supported. That is, if the uapi\_drv\_cipher\_symc\_encrypt/uapi\_drv\_cipher\_symc\_decrypt or uapi\_drv\_cipher\_symc\_get\_tag interface call fails, the interface can still be called again with correct parameters to complete the subsequent data encryption and decryption.

-   Supports software multi-channel.
    -   Multiple data encryption/decryption operations can be performed simultaneously. That is, after starting an operation in step 2, before the current operation is complete (that is, before [Step 8](workflow.md#li1458421120101) is executed), a new channel can be requested to start another data encryption/decryption operation, until no more channels can be requested.
    -   The maximum number of supported software channels can be configured by each chip in the porting file.

### MAC Value Acquisition<a name="ZH-CN_TOPIC_0000001833829444"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001833669668"></a>

Obtains the MAC value of data. The following scenarios are supported: the source data resides in DDR, RAM, or flash.

#### Workflow<a name="ZH-CN_TOPIC_0000001880468949"></a>

1.  Initialize the SYMC module by calling uapi\_drv\_cipher\_symc\_init.
2.  Create a symc channel, obtain the symc handle, and configure the parameter information required for MAC calculation. These include:

    -   Basic key attributes (length, parity).
    -   Encryption/decryption data width.
    -   The keyslot channel to be used. For keyslot channel creation, refer to the descriptions of the KEYSLOT & KLAD interfaces.

    Use the uapi\_drv\_cipher\_mac\_start interface.

3.  Encrypt the data. Use the uapi\_drv\_cipher\_mac\_update interface (can be called once or multiple times).
4.  Obtain the MAC value and destroy the handle. Use the uapi\_drv\_cipher\_mac\_finish interface.
5.  Deinitialize the SYMC module by calling the uapi\_drv\_cipher\_symc\_deinit interface.

#### Precautions<a name="ZH-CN_TOPIC_0000001880628725"></a>

-   Supports two modes: AES CBC\_MAC and AES CMAC.
-   Supports software multi-channel.
    -   Multiple data encryption/decryption operations can be performed simultaneously. That is, after starting an operation in step 2, before the current operation is complete (that is, before step 4 is executed), a new channel can be requested to start another data encryption/decryption operation, until no more channels can be requested.
    -   The maximum number of supported software channels can be configured by each chip in the porting file.

### HASH Calculation<a name="ZH-CN_TOPIC_0000001833829448"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001833669672"></a>

Obtains the message digest. The following scenarios are supported: the source data resides in DDR, RAM, or flash.

#### Workflow<a name="ZH-CN_TOPIC_0000001880468953"></a>

1.  Initialize the HASH module by calling uapi\_drv\_cipher\_hash\_init.
2.  Create a hash channel, configure the current hash calculation type, and obtain the hash handle. Use the uapi\_drv\_cipher\_hash\_start interface.
3.  Pass in the message data and calculate the message digest. Use the uapi\_drv\_cipher\_hash\_update interface.
4.  Obtain the message digest. Use the uapi\_drv\_cipher\_hash\_finish interface.
5.  Deinitialize the HASH module by calling uapi\_drv\_cipher\_hash\_deinit.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >If step 4 succeeds, the hash handle is destroyed automatically, and no additional hash interface call is required. After step 2 starts successfully, regardless of whether the subsequent steps succeed or fail, the uapi\_drv\_cipher\_hash\_destroy interface can be called to destroy the hash handle (except when step 4 succeeds).

#### Precautions<a name="ZH-CN_TOPIC_0000001880628729"></a>

-   When calling the uapi\_drv\_cipher\_hash\_finish interface to obtain the message digest, the result buffer passed in must be allocated by the caller, with a size of result\_len, and result\_len must not be smaller than the digest calculation result length corresponding to the current hash type.
-   Multiple segments of data can be updated continuously, and the result is the same as updating all segments of data at once.
-   Hash clone is supported. That is, the current hash handle1 information is copied through the uapi\_drv\_cipher\_hash\_get interface and set to another hash handle2 through the uapi\_drv\_cipher\_hash\_set interface, and the new hash handle2 continues to complete the subsequent calculation operations. If the subsequent calculation operations of hash handle1 and hash handle2 are the same, the final hash digest results of both are the same.
-   Retry is supported. That is, if the uapi\_drv\_cipher\_hash\_update/uapi\_drv\_cipher\_hash\_finish interface call fails, the interface can still be called again with correct parameters to complete the subsequent digest calculation operations.

### HMAC Calculation<a name="ZH-CN_TOPIC_0000001833829452"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001833669676"></a>

Obtains the message digest based on the key data passed in by the caller. The key data is agreed upon in advance by both parties of the message exchange. The following scenarios are supported: the source data resides in DDR, RAM, or flash.

#### Workflow<a name="ZH-CN_TOPIC_0000001880468957"></a>

1.  Initialize the HASH module by calling uapi\_drv\_cipher\_hash\_init.
2.  Create a hash channel, configure the current hash calculation type and the keyslot channel where the key resides, and obtain the hash handle. Use the uapi\_drv\_cipher\_hash\_start interface.
3.  Pass in the message data and calculate the message digest. Use the uapi\_drv\_cipher\_hash\_update interface.
4.  <a name="li142717119487"></a>Obtain the message digest. Use the uapi\_drv\_cipher\_hash\_finish interface.
5.  Deinitialize the HASH module by calling uapi\_drv\_cipher\_hash\_deinit.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >If step 4 succeeds, the hash handle is destroyed automatically, and no additional hash interface call is required. After step 2 starts successfully, regardless of whether the subsequent steps succeed or fail, the uapi\_drv\_cipher\_hash\_destroy interface can be called to destroy the hash handle (except when [Step 5](#li142717119487) succeeds).

#### Precautions<a name="ZH-CN_TOPIC_0000001880628733"></a>

When calling the uapi\_drv\_cipher\_hash\_finish interface to obtain the message digest, the result buffer passed in must be allocated by the caller, with a size of result\_len, and result\_len must not be smaller than the digest calculation result length corresponding to the current hash type.

For the key data passed in by the caller: if it is a plaintext key, the key length must not be greater than the block\_size of the current hash type. If the key length is greater than the block\_size of the current hash type, the caller must first perform a hash calculation on the key so that its length is smaller than block\_size. If it is a ciphertext key, the key length can only be 16 bytes, 24 bytes, or 32 bytes.

### RSA Encryption and Decryption<a name="ZH-CN_TOPIC_0000001833829456"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001833669680"></a>

The application scenario of RSA encryption and decryption is public key encryption and private key decryption.

#### Workflow<a name="ZH-CN_TOPIC_0000001880468961"></a>

1.  Public key encryption. Use the uapi\_drv\_cipher\_pke\_rsa\_public\_encrypt interface.
2.  Private key decryption. Use the uapi\_drv\_cipher\_pke\_rsa\_private\_decrypt interface.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >When calling the encryption interface, the buffer that stores the encryption result must have a buffer size no smaller than the bit width of the key N.

#### Precautions<a name="ZH-CN_TOPIC_0000001880628737"></a>

Supports two modes: PKCS\#1 v1.5 and PKCS\#1 v2.1 OAEP. The user label data is optional and is only used in PKCS\#1 v2.1 OAEP mode. PKCS\#1 v1.5 is a non-secure algorithm and is not recommended.

### RSA Signing and Verification<a name="ZH-CN_TOPIC_0000001833829460"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001833669684"></a>

The main application scenario of RSA signing and verification is private key signing and public key verification.

#### Workflow<a name="ZH-CN_TOPIC_0000001880468965"></a>

1.  Private key signing. Use the uapi\_drv\_cipher\_pke\_rsa\_sign interface.
2.  Public key verification. Use the uapi\_drv\_cipher\_pke\_rsa\_verify interface.

#### Precautions<a name="ZH-CN_TOPIC_0000001880628741"></a>

Supports private key signing and public key verification in two modes: PKCS\#1 v1.5 and PKCS\#1 v2.1 PSS. PKCS\#1 v1.5 is a non-secure algorithm and is not recommended.

### SM2 Encryption and Decryption<a name="ZH-CN_TOPIC_0000001833829464"></a>



#### Scenario Description<a name="ZH-CN_TOPIC_0000001833669688"></a>

The application scenario of SM2 encryption and decryption is public key encryption and private key decryption.

#### Workflow<a name="ZH-CN_TOPIC_0000001880468969"></a>

1.  Public key encryption. Use the uapi\_drv\_cipher\_pke\_sm2\_public\_encrypt interface.
2.  Private key decryption. Use the uapi\_drv\_cipher\_pke\_sm2\_private\_decrypt interface.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >The public-private key pair required for encryption and decryption can be generated by calling uapi\_drv\_cipher\_pke\_ecc\_gen\_key.

### SM2 Signing and Verification<a name="ZH-CN_TOPIC_0000001880628745"></a>



#### Scenario Description<a name="ZH-CN_TOPIC_0000001833829472"></a>

The main application scenario of SM2 signing and verification is private key signing and public key verification.

#### Workflow<a name="ZH-CN_TOPIC_0000001833669692"></a>

1.  Generate the hash digest corresponding to the message. Use the uapi\_drv\_cipher\_pke\_sm2\_dsa\_hash interface.
2.  Private key signing. Use the uapi\_drv\_cipher\_pke\_ecdsa\_sign interface.
3.  Public key verification. Use the uapi\_drv\_cipher\_pke\_ecdsa\_verify interface.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >The public-private key pair required for signing and verification can be generated by calling the uapi\_drv\_cipher\_pke\_ecc\_gen\_key interface. The uapi\_drv\_cipher\_pke\_check\_dot\_on\_curve interface can be called to confirm that the public key is indeed a point on the curve.

### ECC Signing and Verification<a name="ZH-CN_TOPIC_0000001880468973"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001880628749"></a>

The main application scenario of ECC signing and verification is private key signing and public key verification.

#### Workflow<a name="ZH-CN_TOPIC_0000001833829476"></a>

1.  Generate the hash digest corresponding to the message. Use the corresponding HASH/HMAC interfaces.
2.  Private key signing. Use the uapi\_drv\_cipher\_pke\_ecdsa\_sign interface.
3.  Public key verification. Use the uapi\_drv\_cipher\_pke\_ecdsa\_verify interface.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >The public-private key pair required for signing and verification can be generated by calling the uapi\_drv\_cipher\_pke\_ecc\_gen\_key interface. The uapi\_drv\_cipher\_pke\_check\_dot\_on\_curve interface can be called to confirm that the public key is indeed a point on the curve. The hash digest must be calculated before signing; the signing process signs the digest.

#### Precautions<a name="ZH-CN_TOPIC_0000001833669696"></a>

Supports private key signing and public key verification for RFC 5639 - Brainpool P256/384/512r1 and NIST FIPS 186 - 4 P192/224/256/384/521.

### EDDSA Signing and Verification<a name="ZH-CN_TOPIC_0000001880468977"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001880628753"></a>

The main application scenario of EDDSA signing and verification is private key signing and public key verification, using the special curve ed25519 for signing and verification.

#### Workflow<a name="ZH-CN_TOPIC_0000001833829480"></a>

1.  Private key signing. Use the uapi\_drv\_cipher\_pke\_eddsa\_sign interface.
2.  Public key verification. Use the uapi\_drv\_cipher\_pke\_eddsa\_verify interface.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >The public-private key pair required for signing and verification can be generated by calling the uapi\_drv\_cipher\_pke\_ecc\_gen\_key interface. The uapi\_drv\_cipher\_pke\_check\_dot\_on\_curve interface can be called to confirm that the public key is indeed a point on the curve. EDDSA signing does not require calculating the hash in advance; the message can be passed in directly for signing.

#### Precautions<a name="ZH-CN_TOPIC_0000001833669700"></a>

Supports private key signing and public key verification for RFC 8032 - ED25519.

### Large Number Arithmetic<a name="ZH-CN_TOPIC_0000001880468981"></a>



#### Scenario Description<a name="ZH-CN_TOPIC_0000001880628757"></a>

Large number arithmetic is mainly used in the computation process of asymmetric encryption/decryption and signing/verification.

#### Workflow<a name="ZH-CN_TOPIC_0000001833829484"></a>

Simply call the large number calculation interface to complete the corresponding type of large number calculation. For example, modular addition can be completed by directly calling the uapi\_drv\_cipher\_pke\_add\_mod interface.

### ECDH Key Agreement<a name="ZH-CN_TOPIC_0000001833669704"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001880468985"></a>

Key agreement is mainly used for the two message-transmitting parties to exchange keys after generating their own public-private key pairs.

#### Workflow<a name="ZH-CN_TOPIC_0000001880628761"></a>

1.  Message sender a generates its own public-private key pair. Use the uapi\_drv\_cipher\_pke\_ecc\_gen\_key interface.
2.  Message receiver b generates its own public-private key pair. Use the uapi\_drv\_cipher\_pke\_ecc\_gen\_key interface.
3.  Key agreement: message sender a/message receiver b uses its own private key and the other party's public key to generate a shared key. Use the uapi\_drv\_cipher\_pke\_ecc\_gen\_ecdh\_key interface.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >-   For a given private key, the public key generated by uapi\_drv\_cipher\_pke\_ecc\_gen\_key is always fixed. When no private key is given, the public-private key pair generated by uapi\_drv\_cipher\_pke\_ecc\_gen\_key is random.
    >-   After the shared key is generated, both message-transmitting parties can compare the generated shared keys to verify the correctness of the shared key.

#### Precautions<a name="ZH-CN_TOPIC_0000001833829488"></a>

-   Supports public-private key pair generation for RFC 5639 - Brainpool P256/384/512r1, NIST FIPS 186 - 4 P192/224/256/384/521, RFC 7748 - Curve448/Curve25519, RFC 8032 - ED25519 (that is, EDDSA), and SM2, as well as generating the corresponding public key from a given private key.
-   Supports key exchange (ECDH) for RFC 5639 - Brainpool P256/384/512r1, NIST FIPS 186 - 4 P192/224/256/384/521, RFC 7748 - Curve448/Curve25519, and SM2. ECDH below 256 bits and the curves corresponding to NIST FIPS are non-secure algorithms and are not recommended.

### DH Key Agreement<a name="ZH-CN_TOPIC_0000001833669708"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001880468989"></a>

Key agreement is mainly used for the two message-transmitting parties to exchange keys after generating their own public-private key pairs. DH key agreement is used for non-curve types.

#### Workflow<a name="ZH-CN_TOPIC_0000001880628765"></a>

1.  Message sender a generates its own public-private key pair. Use the uapi\_drv\_cipher\_pke\_dh\_gen\_key interface.
2.  Message receiver b generates its own public-private key pair. Use the uapi\_drv\_cipher\_pke\_dh\_gen\_key interface.
3.  Key agreement: message sender a/message receiver b uses its own private key and the other party's public key to generate a shared key. Use the uapi\_drv\_cipher\_pke\_dh\_compute\_key interface.

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >-   For a given private key, the public key generated by uapi\_drv\_cipher\_pke\_dh\_gen\_key is always fixed. When no private key is given, the public-private key pair generated by uapi\_drv\_cipher\_pke\_dh\_gen\_key is random.
    >-   After the shared key is generated, both message-transmitting parties can compare the generated shared keys to verify the correctness of the shared key.

#### Precautions<a name="ZH-CN_TOPIC_0000001833829492"></a>

-   Supports DH key agreement of 192/224/256/384/512/521/1024/2048/3072/4096 bits. DH below 3072 bits is a non-secure algorithm and is not recommended.

### FLASH On-the-fly Decryption<a name="ZH-CN_TOPIC_0000001833669712"></a>




#### Scenario Description<a name="ZH-CN_TOPIC_0000001880468997"></a>

Since the OS and applications running on the CPU are encrypted and run on FLASH, during the secure boot process, Boot needs to configure the FLASH on-the-fly decryption of the OS image. This module is mainly exposed to boot for use; upper-layer services do not use it.

#### Workflow<a name="ZH-CN_TOPIC_0000001880628769"></a>

1.  Configure the region for the on-the-fly decryption operation and the start address of its corresponding flash area. Use the drv\_fapc\_set\_config interface.
2.  Configure the iv used for the on-the-fly decryption operation. Use the drv\_fapc\_set\_iv interface.
3.  Configure the key used for the on-the-fly decryption operation. For details, see the "[Key Configuration](key_configuration.md)" section.
4.  Directly read the content of the flash area for which the on-the-fly decryption operation has been configured. The read result is the decrypted result.

#### Precautions<a name="ZH-CN_TOPIC_0000001833829496"></a>

The algorithm used for FLASH on-the-fly decryption is AES\_128\_CTR. Therefore, when using this function, the encryption method of the corresponding flash area should also be AES\_128\_CTR.

When boot configures the FLASH on-the-fly decryption of an image, the root key type used is selected by the corresponding chip.

### Security-related eFuse Programming Recommendations<a name="ZH-CN_TOPIC_0000001833669716"></a>

There are many eFuse bits related to security features, which involve the correct use of the security features. The relevant eFuses, their corresponding usage scenarios, and programming recommendations are listed here for reference. Each project should configure them appropriately based on specific requirements and the actual eFuse layout table. [Table 1](#_table1523256143518) lists the eFuses used by OEM in different scenarios, along with the recommended programming stage and recommended programming values.

**Table 1**  Usage scenarios and programming recommendations of security-feature eFuses

<a name="_table1523256143518"></a>
<table><thead align="left"><tr id="row1130mcpsimp"><th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.6.1.1"><p id="p1132mcpsimp"><a name="p1132mcpsimp"></a><a name="p1132mcpsimp"></a>Usage Scenario</p>
</th>
<th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.6.1.2"><p id="p1134mcpsimp"><a name="p1134mcpsimp"></a><a name="p1134mcpsimp"></a>Key Item</p>
</th>
<th class="cellrowborder" valign="top" width="11.061106110611062%" id="mcps1.2.6.1.3"><p id="p1136mcpsimp"><a name="p1136mcpsimp"></a><a name="p1136mcpsimp"></a>Programming Stage</p>
</th>
<th class="cellrowborder" valign="top" width="17.581758175817583%" id="mcps1.2.6.1.4"><p id="p1138mcpsimp"><a name="p1138mcpsimp"></a><a name="p1138mcpsimp"></a>Whether Lock Is Required After Programming</p>
</th>
<th class="cellrowborder" valign="top" width="35.713571357135706%" id="mcps1.2.6.1.5"><p id="p1140mcpsimp"><a name="p1140mcpsimp"></a><a name="p1140mcpsimp"></a>Programming Method and Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row1142mcpsimp"><td class="cellrowborder" rowspan="6" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.1 "><p id="p1144mcpsimp"><a name="p1144mcpsimp"></a><a name="p1144mcpsimp"></a>Secure boot</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.2 "><p id="p1146mcpsimp"><a name="p1146mcpsimp"></a><a name="p1146mcpsimp"></a>sec_verify_enable</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.6.1.3 "><p id="p1148mcpsimp"><a name="p1148mcpsimp"></a><a name="p1148mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" width="17.581758175817583%" headers="mcps1.2.6.1.4 "><p id="p1150mcpsimp"><a name="p1150mcpsimp"></a><a name="p1150mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="35.713571357135706%" headers="mcps1.2.6.1.5 "><p id="p1152mcpsimp"><a name="p1152mcpsimp"></a><a name="p1152mcpsimp"></a>Use the Burntool programming tool. Determined by whether the secure boot function is enabled.</p>
</td>
</tr>
<tr id="row1153mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1155mcpsimp"><a name="p1155mcpsimp"></a><a name="p1155mcpsimp"></a>mcu_ver</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1157mcpsimp"><a name="p1157mcpsimp"></a><a name="p1157mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1159mcpsimp"><a name="p1159mcpsimp"></a><a name="p1159mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1161mcpsimp"><a name="p1161mcpsimp"></a><a name="p1161mcpsimp"></a>If the anti-rollback function is supported, program the correct image version number information through the Burntool programming tool based on the actual situation.</p>
</td>
</tr>
<tr id="row1162mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1164mcpsimp"><a name="p1164mcpsimp"></a><a name="p1164mcpsimp"></a>flashboot_ver</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1166mcpsimp"><a name="p1166mcpsimp"></a><a name="p1166mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1168mcpsimp"><a name="p1168mcpsimp"></a><a name="p1168mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1170mcpsimp"><a name="p1170mcpsimp"></a><a name="p1170mcpsimp"></a>If the anti-rollback function is supported, program the correct image version number information through the Burntool programming tool based on the actual situation.</p>
</td>
</tr>
<tr id="row1171mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1173mcpsimp"><a name="p1173mcpsimp"></a><a name="p1173mcpsimp"></a>params_ver</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1175mcpsimp"><a name="p1175mcpsimp"></a><a name="p1175mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1177mcpsimp"><a name="p1177mcpsimp"></a><a name="p1177mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1179mcpsimp"><a name="p1179mcpsimp"></a><a name="p1179mcpsimp"></a>If the anti-rollback function is supported, program the correct image version number information through the Burntool programming tool based on the actual situation.</p>
</td>
</tr>
<tr id="row1180mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1182mcpsimp"><a name="p1182mcpsimp"></a><a name="p1182mcpsimp"></a>Hash_root_public_key</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1184mcpsimp"><a name="p1184mcpsimp"></a><a name="p1184mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1186mcpsimp"><a name="p1186mcpsimp"></a><a name="p1186mcpsimp"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1188mcpsimp"><a name="p1188mcpsimp"></a><a name="p1188mcpsimp"></a>Use the Burntool programming tool. The HASH value of the root public key image.</p>
</td>
</tr>
<tr id="row1189mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1191mcpsimp"><a name="p1191mcpsimp"></a><a name="p1191mcpsimp"></a>MSID</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1193mcpsimp"><a name="p1193mcpsimp"></a><a name="p1193mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1195mcpsimp"><a name="p1195mcpsimp"></a><a name="p1195mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1197mcpsimp"><a name="p1197mcpsimp"></a><a name="p1197mcpsimp"></a>Use the Burntool programming tool. Market ID.</p>
</td>
</tr>
<tr id="row1198mcpsimp"><td class="cellrowborder" rowspan="4" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.1 "><p id="p1200mcpsimp"><a name="p1200mcpsimp"></a><a name="p1200mcpsimp"></a>Security driver</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.2 "><p id="p1202mcpsimp"><a name="p1202mcpsimp"></a><a name="p1202mcpsimp"></a>otp_crc_rd_disable（KM）</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.6.1.3 "><p id="p1204mcpsimp"><a name="p1204mcpsimp"></a><a name="p1204mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" width="17.581758175817583%" headers="mcps1.2.6.1.4 "><p id="p1206mcpsimp"><a name="p1206mcpsimp"></a><a name="p1206mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="35.713571357135706%" headers="mcps1.2.6.1.5 "><p id="p1208mcpsimp"><a name="p1208mcpsimp"></a><a name="p1208mcpsimp"></a>Use the Burntool programming tool. The programming value is determined by whether the CRC debug function is retained.</p>
</td>
</tr>
<tr id="row1209mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1211mcpsimp"><a name="p1211mcpsimp"></a><a name="p1211mcpsimp"></a>sha1_disable</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1213mcpsimp"><a name="p1213mcpsimp"></a><a name="p1213mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1215mcpsimp"><a name="p1215mcpsimp"></a><a name="p1215mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1217mcpsimp"><a name="p1217mcpsimp"></a><a name="p1217mcpsimp"></a>Use the Burntool programming tool. Determined by whether SHA1 is disabled.</p>
</td>
</tr>
<tr id="row1218mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1220mcpsimp"><a name="p1220mcpsimp"></a><a name="p1220mcpsimp"></a>rkp_deob_alg_sel</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1222mcpsimp"><a name="p1222mcpsimp"></a><a name="p1222mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1224mcpsimp"><a name="p1224mcpsimp"></a><a name="p1224mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1226mcpsimp"><a name="p1226mcpsimp"></a><a name="p1226mcpsimp"></a>Use the Burntool programming tool. Configures the DEOB algorithm.</p>
</td>
</tr>
<tr id="row1227mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1229mcpsimp"><a name="p1229mcpsimp"></a><a name="p1229mcpsimp"></a>sm_disable</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1231mcpsimp"><a name="p1231mcpsimp"></a><a name="p1231mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1233mcpsimp"><a name="p1233mcpsimp"></a><a name="p1233mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1235mcpsimp"><a name="p1235mcpsimp"></a><a name="p1235mcpsimp"></a>Use the Burntool programming tool. Determined by whether the national cryptographic (SM) algorithms are disabled.</p>
</td>
</tr>
<tr id="row1236mcpsimp"><td class="cellrowborder" rowspan="2" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.1 "><p id="p1238mcpsimp"><a name="p1238mcpsimp"></a><a name="p1238mcpsimp"></a>AES/SM4 encryption and decryption, HMAC</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.2 "><p id="p1240mcpsimp"><a name="p1240mcpsimp"></a><a name="p1240mcpsimp"></a>obfu_mrk1_owner_id</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.6.1.3 "><p id="p1242mcpsimp"><a name="p1242mcpsimp"></a><a name="p1242mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" width="17.581758175817583%" headers="mcps1.2.6.1.4 "><p id="p1244mcpsimp"><a name="p1244mcpsimp"></a><a name="p1244mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="35.713571357135706%" headers="mcps1.2.6.1.5 "><p id="p1246mcpsimp"><a name="p1246mcpsimp"></a><a name="p1246mcpsimp"></a>Use the Burntool programming tool. A 16-bit random value.</p>
</td>
</tr>
<tr id="row1247mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1249mcpsimp"><a name="p1249mcpsimp"></a><a name="p1249mcpsimp"></a>obfu_mrk</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1251mcpsimp"><a name="p1251mcpsimp"></a><a name="p1251mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1253mcpsimp"><a name="p1253mcpsimp"></a><a name="p1253mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1255mcpsimp"><a name="p1255mcpsimp"></a><a name="p1255mcpsimp"></a>Use the Burntool programming tool. A 128-bit random value for encryption/decryption and HMAC hardware key derivation.</p>
</td>
</tr>
<tr id="row1256mcpsimp"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.1 "><p id="p1258mcpsimp"><a name="p1258mcpsimp"></a><a name="p1258mcpsimp"></a>Secure storage</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.6.1.2 "><p id="p1260mcpsimp"><a name="p1260mcpsimp"></a><a name="p1260mcpsimp"></a>obfu_rusk</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.6.1.3 "><p id="p1262mcpsimp"><a name="p1262mcpsimp"></a><a name="p1262mcpsimp"></a>OEM</p>
</td>
<td class="cellrowborder" valign="top" width="17.581758175817583%" headers="mcps1.2.6.1.4 "><p id="p1264mcpsimp"><a name="p1264mcpsimp"></a><a name="p1264mcpsimp"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="35.713571357135706%" headers="mcps1.2.6.1.5 "><p id="p1266mcpsimp"><a name="p1266mcpsimp"></a><a name="p1266mcpsimp"></a>Use the Burntool programming tool. A 128-bit random value used to derive the secure storage key.</p>
</td>
</tr>
</tbody>
</table>

# Error Codes<a name="ZH-CN_TOPIC_0000001880469001"></a>

>![](public_sys-resources/icon-note.gif) **Note:** 
>This chapter describes the error codes of the CIPHER DRIVER to help developers understand and locate the errors that occur.


## CIPHER DRIVER Error Code Structure and Description<a name="ZH-CN_TOPIC_0000001880628773"></a>

The return values of the Cipher driver usually have two types: success and failure, as shown in [Table 1](#_d0e16563).

**Table 1**  Cipher driver return values

<a name="_d0e16563"></a>
<table><thead align="left"><tr id="row652mcpsimp"><th class="cellrowborder" valign="top" width="48%" id="mcps1.2.3.1.1"><p id="p654mcpsimp"><a name="p654mcpsimp"></a><a name="p654mcpsimp"></a>Member Name</p>
</th>
<th class="cellrowborder" valign="top" width="52%" id="mcps1.2.3.1.2"><p id="p656mcpsimp"><a name="p656mcpsimp"></a><a name="p656mcpsimp"></a>Enumeration Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row658mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.3.1.1 "><p id="p660mcpsimp"><a name="p660mcpsimp"></a><a name="p660mcpsimp"></a>CRYPTO_SUCCESS</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.3.1.2 "><p id="p662mcpsimp"><a name="p662mcpsimp"></a><a name="p662mcpsimp"></a>0</p>
</td>
</tr>
<tr id="row663mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.3.1.1 "><p id="p665mcpsimp"><a name="p665mcpsimp"></a><a name="p665mcpsimp"></a>CRYPTO_FAILURE</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.2.3.1.2 "><p id="p667mcpsimp"><a name="p667mcpsimp"></a><a name="p667mcpsimp"></a>0xFFFFFFFF</p>
</td>
</tr>
</tbody>
</table>

To identify the specific information about an error more clearly through the error code, a hierarchical structure is used for information concatenation. Its structure is:

Env\(4 bits\) | Layer\(4 bits\) | Modules\(4 bits\) | Reserved\(12 bits\) | Error Code\(8 bits\)





### ENV<a name="ZH-CN_TOPIC_0000001833829500"></a>

【Description】

The operating system environment where the error code occurs.

【Definition】

```
#define ERROR_ENV_LINUX         0x1 
#define ERROR_ENV_ITRUSTEE      0x2 
#define ERROR_ENV_OPTEE         0x3 
#define ERROR_ENV_LITEOS        0x4 
#define ERROR_ENV_SELITEOS      0x5 
#define ERROR_ENV_NOOS          0x6 
```

【Members】

<a name="table1292mcpsimp"></a>
<table><thead align="left"><tr id="row1297mcpsimp"><th class="cellrowborder" valign="top" width="48%" id="mcps1.1.3.1.1"><p id="p1299mcpsimp"><a name="p1299mcpsimp"></a><a name="p1299mcpsimp"></a>Member Name</p>
</th>
<th class="cellrowborder" valign="top" width="52%" id="mcps1.1.3.1.2"><p id="p1301mcpsimp"><a name="p1301mcpsimp"></a><a name="p1301mcpsimp"></a>Enumeration Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row1303mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1305mcpsimp"><a name="p1305mcpsimp"></a><a name="p1305mcpsimp"></a>ERROR_ENV_LINUX</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1307mcpsimp"><a name="p1307mcpsimp"></a><a name="p1307mcpsimp"></a>LINUX</p>
</td>
</tr>
<tr id="row1308mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1310mcpsimp"><a name="p1310mcpsimp"></a><a name="p1310mcpsimp"></a>ERROR_ENV_ITRUSTEE</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1312mcpsimp"><a name="p1312mcpsimp"></a><a name="p1312mcpsimp"></a>ITRUSTEE</p>
</td>
</tr>
<tr id="row1313mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1315mcpsimp"><a name="p1315mcpsimp"></a><a name="p1315mcpsimp"></a>ERROR_ENV_OPTEE</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1317mcpsimp"><a name="p1317mcpsimp"></a><a name="p1317mcpsimp"></a>OPTEE</p>
</td>
</tr>
<tr id="row1318mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1320mcpsimp"><a name="p1320mcpsimp"></a><a name="p1320mcpsimp"></a>ERROR_ENV_LITEOS</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1322mcpsimp"><a name="p1322mcpsimp"></a><a name="p1322mcpsimp"></a>LITEOS</p>
</td>
</tr>
<tr id="row1323mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1325mcpsimp"><a name="p1325mcpsimp"></a><a name="p1325mcpsimp"></a>ERROR_ENV_SELITEOS</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1327mcpsimp"><a name="p1327mcpsimp"></a><a name="p1327mcpsimp"></a>SELITEOS</p>
</td>
</tr>
<tr id="row1328mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1330mcpsimp"><a name="p1330mcpsimp"></a><a name="p1330mcpsimp"></a>ERROR_ENV_NOOS</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1332mcpsimp"><a name="p1332mcpsimp"></a><a name="p1332mcpsimp"></a>Non-OS environment</p>
</td>
</tr>
</tbody>
</table>

【Notes】

None

### LAYER<a name="ZH-CN_TOPIC_0000001833669720"></a>

【Description】

The code layer where the error code occurs.

【Definition】

```
enum { 
    ERROR_LAYER_UAPI = 0x1, 
    ERROR_LAYER_DISPATCH, 
    ERROR_LAYER_KAPI, 
    ERROR_LAYER_DRV, 
    ERROR_LAYER_HAL, 
};
```

【Members】

<a name="table1043mcpsimp"></a>
<table><thead align="left"><tr id="row1048mcpsimp"><th class="cellrowborder" valign="top" width="48%" id="mcps1.1.3.1.1"><p id="p1050mcpsimp"><a name="p1050mcpsimp"></a><a name="p1050mcpsimp"></a>Member Name</p>
</th>
<th class="cellrowborder" valign="top" width="52%" id="mcps1.1.3.1.2"><p id="p1052mcpsimp"><a name="p1052mcpsimp"></a><a name="p1052mcpsimp"></a>Enumeration Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row1054mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1056mcpsimp"><a name="p1056mcpsimp"></a><a name="p1056mcpsimp"></a>ERROR_LAYER_UAPI</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1058mcpsimp"><a name="p1058mcpsimp"></a><a name="p1058mcpsimp"></a>User interface layer</p>
</td>
</tr>
<tr id="row1059mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1061mcpsimp"><a name="p1061mcpsimp"></a><a name="p1061mcpsimp"></a>ERROR_LAYER_DISPATCH</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1063mcpsimp"><a name="p1063mcpsimp"></a><a name="p1063mcpsimp"></a>Command dispatch layer</p>
</td>
</tr>
<tr id="row1064mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1066mcpsimp"><a name="p1066mcpsimp"></a><a name="p1066mcpsimp"></a>ERROR_LAYER_KAPI</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1068mcpsimp"><a name="p1068mcpsimp"></a><a name="p1068mcpsimp"></a>Kernel interface layer</p>
</td>
</tr>
<tr id="row1069mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1071mcpsimp"><a name="p1071mcpsimp"></a><a name="p1071mcpsimp"></a>ERROR_LAYER_DRV</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1073mcpsimp"><a name="p1073mcpsimp"></a><a name="p1073mcpsimp"></a>Driver logic layer</p>
</td>
</tr>
<tr id="row1074mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p1076mcpsimp"><a name="p1076mcpsimp"></a><a name="p1076mcpsimp"></a>ERROR_LAYER_HAL</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p1078mcpsimp"><a name="p1078mcpsimp"></a><a name="p1078mcpsimp"></a>Hardware adaptation layer</p>
</td>
</tr>
</tbody>
</table>

【Notes】

None

### MODULE<a name="ZH-CN_TOPIC_0000001880469005"></a>

【Description】

The CIPHER module where the error code occurs.

【Definition】

```
enum { 
    ERROR_MODULE_SYMC = 0x1, 
    ERROR_MODULE_HASH, 
    ERROR_MODULE_PKE, 
    ERROR_MODULE_TRNG, 
    ERROR_MODULE_OTHER 
};
```

【Members】

<a name="table228mcpsimp"></a>
<table><thead align="left"><tr id="row233mcpsimp"><th class="cellrowborder" valign="top" width="48%" id="mcps1.1.3.1.1"><p id="p235mcpsimp"><a name="p235mcpsimp"></a><a name="p235mcpsimp"></a>Member Name</p>
</th>
<th class="cellrowborder" valign="top" width="52%" id="mcps1.1.3.1.2"><p id="p237mcpsimp"><a name="p237mcpsimp"></a><a name="p237mcpsimp"></a>Enumeration Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row239mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p241mcpsimp"><a name="p241mcpsimp"></a><a name="p241mcpsimp"></a>ERROR_MODULE_SYMC</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p243mcpsimp"><a name="p243mcpsimp"></a><a name="p243mcpsimp"></a>Symmetric encryption and decryption module</p>
</td>
</tr>
<tr id="row244mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p246mcpsimp"><a name="p246mcpsimp"></a><a name="p246mcpsimp"></a>ERROR_MODULE_HASH</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p248mcpsimp"><a name="p248mcpsimp"></a><a name="p248mcpsimp"></a>Digest algorithm module</p>
</td>
</tr>
<tr id="row249mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p251mcpsimp"><a name="p251mcpsimp"></a><a name="p251mcpsimp"></a>ERROR_MODULE_PKE</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p253mcpsimp"><a name="p253mcpsimp"></a><a name="p253mcpsimp"></a>Asymmetric encryption and decryption module</p>
</td>
</tr>
<tr id="row254mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p256mcpsimp"><a name="p256mcpsimp"></a><a name="p256mcpsimp"></a>ERROR_MODULE_TRNG</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p258mcpsimp"><a name="p258mcpsimp"></a><a name="p258mcpsimp"></a>Random number module</p>
</td>
</tr>
<tr id="row259mcpsimp"><td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.3.1.1 "><p id="p261mcpsimp"><a name="p261mcpsimp"></a><a name="p261mcpsimp"></a>ERROR_MODULE_OTHER</p>
</td>
<td class="cellrowborder" valign="top" width="52%" headers="mcps1.1.3.1.2 "><p id="p263mcpsimp"><a name="p263mcpsimp"></a><a name="p263mcpsimp"></a>Other modules</p>
</td>
</tr>
</tbody>
</table>

【Notes】

None

### Error Types<a name="ZH-CN_TOPIC_0000001880628777"></a>

【Description】

The specific error type where the error code occurs.

【Definition】

```
/* Common Error Code. 0x00 ~ 0x3F. */
ERROR_INVALID_PARAM = 0x0,      /* return when the input param's value is not in the valid range. */
ERROR_PARAM_IS_NULL,            /* return when the input param is NULL and required not NULL. */
ERROR_NOT_INIT,                 /* return when call other functions before call init function. */
ERROR_UNSUPPORT,                /* return when some configuration is unsupport. */
ERROR_UNEXPECTED,               /* reture when unexpected error occurs. */
ERROR_CHN_BUSY,                 /* return when try to create one channel but all channels are busy. */
ERROR_CTX_CLOSED,               /* return when using one ctx to do something but has been closed. */
ERROR_NOT_SET_CONFIG,           /* return when not set_config but need for symc. */
ERROR_NOT_ATTACHED,             /* return when not attach but need for symc. */
ERROR_NOT_MAC_START,            /* return when not mac_start but need for symc. */
ERROR_INVALID_HANDLE,           /* return when pass one invalid handle. */
ERROR_GET_PHYS_ADDR,            /* return when transfer from virt_addr to phys_addr failed. */
ERROR_SYMC_LEN_NOT_ALIGNED,     /* return when length isn't aligned to 16-Byte except CTR/CCM/GCM.  */
ERROR_SYMC_ADDR_NOT_ALIGNED,    /* return when the phys_addr writing to register is not aligned to 4-Byte. */
ERROR_PKE_RSA_SAME_DATA,        /* return when rsa exp_mod, the input is equal to output. */
ERROR_PKE_RSA_CRYPTO_V15_CHECK, /* return when rsa crypto v15 padding check failed. */
ERROR_PKE_RSA_CRYPTO_OAEP_CHECK,    /* return when rsa crypto oaep padding check failed. */
ERROR_PKE_RSA_VERIFY_V15_CHECK,     /* return when rsa verify v15 padding check failed. */
ERROR_PKE_RSA_VERIFY_PSS_CHECK,     /* return when rsa verify pss padding check failed. */
ERROR_PKE_RSA_GEN_KEY,          /* return when rsa generate key failed. */
ERROR_PKE_ECDSA_VERIFY_CHECK,   /* return when ecdsa verify check failed. */
/* Outer's Error Code. 0x40 ~ 0x5F. */
ERROR_MEMCPY_S      = 0x40,     /* return when call memcpy_s failed. */
ERROR_MALLOC,                   /* return when call xxx_malloc failed. */
ERROR_MUTEX_INIT,               /* return when call xxx_mutex_init failed. */
ERROR_MUTEX_LOCK,               /* return when call xxx_lock failed. */
/* Specific Error Code for UAPI. 0x60 ~ 0x6F. */
ERROR_DEV_OPEN_FAILED,          /* return when open dev failed. */
ERROR_COUNT_OVERFLOW,           /* return when call init too many times. */
/* Specific Error Code for Dispatch. 0x70 ~ 0x7F. */
ERROR_CMD_DISMATCH  = 0x70,     /* return when cmd is dismatched. */
ERROR_COPY_FROM_USER,           /* return when call copy_from_user failed. */
ERROR_COPY_TO_USER,             /* return when call copy_to_user failed. */
ERROR_MEM_HANDLE_GET,           /* return when parse user's mem handle to kernel's mem handle failed. */
ERROR_GET_OWNER,                /* return when call crypto_get_owner failed. */
/* Specific Error Code for KAPI. 0x80 ~ 0x8F. */
ERROR_PROCESS_NOT_INIT = 0x80,  /* return when one process not call kapi_xxx_init first. */
ERROR_MAX_PROCESS,              /* return when process's num is over the limit. */
ERROR_MEMORY_ACCESS,            /* return when access the memory that does not belong to itself.  */
ERROR_INVALID_PROCESS,          /* return when the process accesses resources of other processes. */
/* Specific Error Code for DRV. 0x90 ~ 0x9F. */
/* Specific Error Code for HAL. 0xA0 ~ 0xAF. */
ERROR_HASH_LOGIC    = 0xA0,     /* return when hash logic's error occurs. */
ERROR_PKE_LOGIC,                /* return when pke logic's error occurs. */
ERROR_INVALID_CPU_TYPE,         /* return when logic get the invalid cpu type. */
ERROR_INVALID_REGISTER_VALUE,   /* return when value in register is invalid. */
ERROR_INVALID_PHYS_ADDR,        /* return when phys_addr is invalid. */
/* Specific Error Code for Timeout. 0xB0 ~ 0xBF. */
ERROR_GET_TRNG_TIMEOUT = 0xB0,  /* return when logic get rnd timeout. */
ERROR_HASH_CLEAR_CHN_TIMEOUT,   /* return when clear hash channel timeout. */
ERROR_HASH_CALC_TIMEOUT,        /* return when hash calculation timeout. */
ERROR_SYMC_CLEAR_CHN_TIMEOUT,   /* return when clear symc channel timeout. */
ERROR_SYMC_CALC_TIMEOUT,        /* return when symc crypto timeout. */
ERROR_SYMC_GET_TAG_TIMEOUT,     /* return when symc get tag timeout. */
ERROR_PKE_LOCK_TIMEOUT,         /* return when pke lock timeout. */
ERROR_PKE_WAIT_DONE_TIMEOUT,    /* return when pke wait done timeout. */
ERROR_PKE_ROBUST_WARNING,    /* return when pke get robust warning. */
```

【Members】

<a name="table733mcpsimp"></a>
<table><thead align="left"><tr id="row739mcpsimp"><th class="cellrowborder" valign="top" id="mcps1.1.4.1.1"><p id="p741mcpsimp"><a name="p741mcpsimp"></a><a name="p741mcpsimp"></a>Type</p>
</th>
<th class="cellrowborder" colspan="2" valign="top" id="mcps1.1.4.1.2"><p id="p743mcpsimp"><a name="p743mcpsimp"></a><a name="p743mcpsimp"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row745mcpsimp"><td class="cellrowborder" rowspan="21" valign="top" width="28.000000000000004%" headers="mcps1.1.4.1.1 "><p id="p747mcpsimp"><a name="p747mcpsimp"></a><a name="p747mcpsimp"></a>COMMON</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.1.4.1.2 "><p id="p749mcpsimp"><a name="p749mcpsimp"></a><a name="p749mcpsimp"></a>ERROR_INVALID_PARAM</p>
</td>
<td class="cellrowborder" valign="top" width="34%" headers="mcps1.1.4.1.2 "><p id="p751mcpsimp"><a name="p751mcpsimp"></a><a name="p751mcpsimp"></a>The input parameter is in an invalid range</p>
</td>
</tr>
<tr id="row752mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p754mcpsimp"><a name="p754mcpsimp"></a><a name="p754mcpsimp"></a>ERROR_PARAM_IS_NULL</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p756mcpsimp"><a name="p756mcpsimp"></a><a name="p756mcpsimp"></a>An invalid NULL pointer parameter is passed in</p>
</td>
</tr>
<tr id="row757mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p759mcpsimp"><a name="p759mcpsimp"></a><a name="p759mcpsimp"></a>ERROR_NOT_INIT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p761mcpsimp"><a name="p761mcpsimp"></a><a name="p761mcpsimp"></a>The initialization function has not been called</p>
</td>
</tr>
<tr id="row762mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p764mcpsimp"><a name="p764mcpsimp"></a><a name="p764mcpsimp"></a>ERROR_UNSUPPORT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p766mcpsimp"><a name="p766mcpsimp"></a><a name="p766mcpsimp"></a>The algorithm or configuration is not supported</p>
</td>
</tr>
<tr id="row767mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p769mcpsimp"><a name="p769mcpsimp"></a><a name="p769mcpsimp"></a>ERROR_UNEXPECTED</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p771mcpsimp"><a name="p771mcpsimp"></a><a name="p771mcpsimp"></a>An unexpected error</p>
</td>
</tr>
<tr id="row772mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p774mcpsimp"><a name="p774mcpsimp"></a><a name="p774mcpsimp"></a>ERROR_CHN_BUSY</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p776mcpsimp"><a name="p776mcpsimp"></a><a name="p776mcpsimp"></a>A channel is attempted to be created when all channels are busy</p>
</td>
</tr>
<tr id="row777mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p779mcpsimp"><a name="p779mcpsimp"></a><a name="p779mcpsimp"></a>ERROR_CTX_CLOSED</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p781mcpsimp"><a name="p781mcpsimp"></a><a name="p781mcpsimp"></a>Attempting to use a closed CTX</p>
</td>
</tr>
<tr id="row782mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p784mcpsimp"><a name="p784mcpsimp"></a><a name="p784mcpsimp"></a>ERROR_NOT_SET_CONFIG</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p786mcpsimp"><a name="p786mcpsimp"></a><a name="p786mcpsimp"></a>SYMC has not called the set_config function</p>
</td>
</tr>
<tr id="row787mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p789mcpsimp"><a name="p789mcpsimp"></a><a name="p789mcpsimp"></a>ERROR_NOT_ATTACHED</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p791mcpsimp"><a name="p791mcpsimp"></a><a name="p791mcpsimp"></a>SYMC has not been attached to a KEYSLOT</p>
</td>
</tr>
<tr id="row792mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p794mcpsimp"><a name="p794mcpsimp"></a><a name="p794mcpsimp"></a>ERROR_NOT_MAC_START</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p796mcpsimp"><a name="p796mcpsimp"></a><a name="p796mcpsimp"></a>SYMC has not called the mac_start function</p>
</td>
</tr>
<tr id="row797mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p799mcpsimp"><a name="p799mcpsimp"></a><a name="p799mcpsimp"></a>ERROR_INVALID_HANDLE</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p801mcpsimp"><a name="p801mcpsimp"></a><a name="p801mcpsimp"></a>An invalid handle is passed in</p>
</td>
</tr>
<tr id="row802mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p804mcpsimp"><a name="p804mcpsimp"></a><a name="p804mcpsimp"></a>ERROR_GET_PHYS_ADDR</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p806mcpsimp"><a name="p806mcpsimp"></a><a name="p806mcpsimp"></a>Failed to obtain the physical address</p>
</td>
</tr>
<tr id="row807mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p809mcpsimp"><a name="p809mcpsimp"></a><a name="p809mcpsimp"></a>ERROR_SYMC_LEN_NOT_ALIGNED</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p811mcpsimp"><a name="p811mcpsimp"></a><a name="p811mcpsimp"></a>The SYMC length is not aligned to 16 bytes except in (CTR/CCM/GCM) modes</p>
</td>
</tr>
<tr id="row812mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p814mcpsimp"><a name="p814mcpsimp"></a><a name="p814mcpsimp"></a>ERROR_SYMC_ADDR_NOT_ALIGNED</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p816mcpsimp"><a name="p816mcpsimp"></a><a name="p816mcpsimp"></a>The physical address written by SYMC to the register is not aligned to 4 bytes</p>
</td>
</tr>
<tr id="row817mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p819mcpsimp"><a name="p819mcpsimp"></a><a name="p819mcpsimp"></a>ERROR_PKE_RSA_SAME_DATA</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p821mcpsimp"><a name="p821mcpsimp"></a><a name="p821mcpsimp"></a>In RSA modular exponentiation, the input is equal to the output</p>
</td>
</tr>
<tr id="row822mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p824mcpsimp"><a name="p824mcpsimp"></a><a name="p824mcpsimp"></a>ERROR_PKE_RSA_CRYPTO_V15_CHECK</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p826mcpsimp"><a name="p826mcpsimp"></a><a name="p826mcpsimp"></a>RSA PKCSV15 decryption padding check failed</p>
</td>
</tr>
<tr id="row827mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p829mcpsimp"><a name="p829mcpsimp"></a><a name="p829mcpsimp"></a>ERROR_PKE_RSA_CRYPTO_OAEP_CHECK</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p831mcpsimp"><a name="p831mcpsimp"></a><a name="p831mcpsimp"></a>RSA OAEP decryption padding check failed</p>
</td>
</tr>
<tr id="row832mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p834mcpsimp"><a name="p834mcpsimp"></a><a name="p834mcpsimp"></a>ERROR_PKE_RSA_VERIFY_V15_CHECK</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p836mcpsimp"><a name="p836mcpsimp"></a><a name="p836mcpsimp"></a>RSA PKCSV15 verification padding check failed</p>
</td>
</tr>
<tr id="row837mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p839mcpsimp"><a name="p839mcpsimp"></a><a name="p839mcpsimp"></a>ERROR_PKE_RSA_VERIFY_PSS_CHECK</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p841mcpsimp"><a name="p841mcpsimp"></a><a name="p841mcpsimp"></a>RSA PSS verification padding check failed</p>
</td>
</tr>
<tr id="row842mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p844mcpsimp"><a name="p844mcpsimp"></a><a name="p844mcpsimp"></a>ERROR_PKE_RSA_GEN_KEY</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p846mcpsimp"><a name="p846mcpsimp"></a><a name="p846mcpsimp"></a>RSA key generation failed</p>
<p id="p847mcpsimp"><a name="p847mcpsimp"></a><a name="p847mcpsimp"></a>This function is not supported for now</p>
</td>
</tr>
<tr id="row848mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p850mcpsimp"><a name="p850mcpsimp"></a><a name="p850mcpsimp"></a>ERROR_PKE_ECDSA_VERIFY_CHECK</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p852mcpsimp"><a name="p852mcpsimp"></a><a name="p852mcpsimp"></a>ECDSA verification failed</p>
</td>
</tr>
<tr id="row853mcpsimp"><td class="cellrowborder" rowspan="4" valign="top" width="28.000000000000004%" headers="mcps1.1.4.1.1 "><p id="p855mcpsimp"><a name="p855mcpsimp"></a><a name="p855mcpsimp"></a>OUTER</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.1.4.1.2 "><p id="p857mcpsimp"><a name="p857mcpsimp"></a><a name="p857mcpsimp"></a>ERROR_MEMCPY_S</p>
</td>
<td class="cellrowborder" valign="top" width="34%" headers="mcps1.1.4.1.2 "><p id="p859mcpsimp"><a name="p859mcpsimp"></a><a name="p859mcpsimp"></a>Failed to call memcpy_s</p>
</td>
</tr>
<tr id="row860mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p862mcpsimp"><a name="p862mcpsimp"></a><a name="p862mcpsimp"></a>ERROR_MALLOC</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p864mcpsimp"><a name="p864mcpsimp"></a><a name="p864mcpsimp"></a>Failed to call xxx_malloc</p>
</td>
</tr>
<tr id="row865mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p867mcpsimp"><a name="p867mcpsimp"></a><a name="p867mcpsimp"></a>ERROR_MUTEX_INIT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p869mcpsimp"><a name="p869mcpsimp"></a><a name="p869mcpsimp"></a>Failed to call xxx_mutex_init</p>
</td>
</tr>
<tr id="row870mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p872mcpsimp"><a name="p872mcpsimp"></a><a name="p872mcpsimp"></a>ERROR_MUTEX_LOCK</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p874mcpsimp"><a name="p874mcpsimp"></a><a name="p874mcpsimp"></a>Failed to call xxx_lock</p>
</td>
</tr>
<tr id="row875mcpsimp"><td class="cellrowborder" rowspan="2" valign="top" width="28.000000000000004%" headers="mcps1.1.4.1.1 "><p id="p877mcpsimp"><a name="p877mcpsimp"></a><a name="p877mcpsimp"></a>SPECIFIC UAPI</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.1.4.1.2 "><p id="p879mcpsimp"><a name="p879mcpsimp"></a><a name="p879mcpsimp"></a>ERROR_DEV_OPEN_FAILED</p>
</td>
<td class="cellrowborder" valign="top" width="34%" headers="mcps1.1.4.1.2 "><p id="p881mcpsimp"><a name="p881mcpsimp"></a><a name="p881mcpsimp"></a>Failed to open the device</p>
</td>
</tr>
<tr id="row882mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p884mcpsimp"><a name="p884mcpsimp"></a><a name="p884mcpsimp"></a>ERROR_COUNT_OVERFLOW</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p886mcpsimp"><a name="p886mcpsimp"></a><a name="p886mcpsimp"></a>The initialization has been called too many times</p>
</td>
</tr>
<tr id="row887mcpsimp"><td class="cellrowborder" rowspan="5" valign="top" width="28.000000000000004%" headers="mcps1.1.4.1.1 "><p id="p889mcpsimp"><a name="p889mcpsimp"></a><a name="p889mcpsimp"></a>SPECIFIC DISPATCH</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.1.4.1.2 "><p id="p891mcpsimp"><a name="p891mcpsimp"></a><a name="p891mcpsimp"></a>ERROR_CMD_DISMATCHED</p>
</td>
<td class="cellrowborder" valign="top" width="34%" headers="mcps1.1.4.1.2 "><p id="p893mcpsimp"><a name="p893mcpsimp"></a><a name="p893mcpsimp"></a>The CMD has no matching item</p>
</td>
</tr>
<tr id="row894mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p896mcpsimp"><a name="p896mcpsimp"></a><a name="p896mcpsimp"></a>ERROR_COPY_FROM_USER</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p898mcpsimp"><a name="p898mcpsimp"></a><a name="p898mcpsimp"></a>An error occurred while copying from the user space</p>
</td>
</tr>
<tr id="row899mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p901mcpsimp"><a name="p901mcpsimp"></a><a name="p901mcpsimp"></a>ERROR_COPY_TO_USER</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p903mcpsimp"><a name="p903mcpsimp"></a><a name="p903mcpsimp"></a>An error occurred while copying to the user space</p>
</td>
</tr>
<tr id="row904mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p906mcpsimp"><a name="p906mcpsimp"></a><a name="p906mcpsimp"></a>ERROR_MEM_HANDLE_GET</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p908mcpsimp"><a name="p908mcpsimp"></a><a name="p908mcpsimp"></a>An error occurred while obtaining the handle</p>
</td>
</tr>
<tr id="row909mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p911mcpsimp"><a name="p911mcpsimp"></a><a name="p911mcpsimp"></a>ERROR_GET_OWNER</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p913mcpsimp"><a name="p913mcpsimp"></a><a name="p913mcpsimp"></a>An error occurred while obtaining the owner</p>
</td>
</tr>
<tr id="row914mcpsimp"><td class="cellrowborder" rowspan="4" valign="top" width="28.000000000000004%" headers="mcps1.1.4.1.1 "><p id="p916mcpsimp"><a name="p916mcpsimp"></a><a name="p916mcpsimp"></a>SPECIFIC KAPI</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.1.4.1.2 "><p id="p918mcpsimp"><a name="p918mcpsimp"></a><a name="p918mcpsimp"></a>ERROR_PROCESS_NOT_INIT</p>
</td>
<td class="cellrowborder" valign="top" width="34%" headers="mcps1.1.4.1.2 "><p id="p920mcpsimp"><a name="p920mcpsimp"></a><a name="p920mcpsimp"></a>The process has not been initialized</p>
</td>
</tr>
<tr id="row921mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p923mcpsimp"><a name="p923mcpsimp"></a><a name="p923mcpsimp"></a>ERROR_MAX_PROCESS</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p925mcpsimp"><a name="p925mcpsimp"></a><a name="p925mcpsimp"></a>The value exceeds the maximum value</p>
</td>
</tr>
<tr id="row926mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p928mcpsimp"><a name="p928mcpsimp"></a><a name="p928mcpsimp"></a>ERROR_MEMORY_ACCESS</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p930mcpsimp"><a name="p930mcpsimp"></a><a name="p930mcpsimp"></a>No access permission to the memory</p>
</td>
</tr>
<tr id="row931mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p933mcpsimp"><a name="p933mcpsimp"></a><a name="p933mcpsimp"></a>ERROR_INVALID_PROCESS</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p935mcpsimp"><a name="p935mcpsimp"></a><a name="p935mcpsimp"></a>A process without access permission accessed the resource</p>
</td>
</tr>
<tr id="row936mcpsimp"><td class="cellrowborder" rowspan="5" valign="top" width="28.000000000000004%" headers="mcps1.1.4.1.1 "><p id="p938mcpsimp"><a name="p938mcpsimp"></a><a name="p938mcpsimp"></a>SPECIFIC HAL</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.1.4.1.2 "><p id="p940mcpsimp"><a name="p940mcpsimp"></a><a name="p940mcpsimp"></a>ERROR_HASH_LOGIC</p>
</td>
<td class="cellrowborder" valign="top" width="34%" headers="mcps1.1.4.1.2 "><p id="p942mcpsimp"><a name="p942mcpsimp"></a><a name="p942mcpsimp"></a>A hardware logic error occurred in HASH</p>
</td>
</tr>
<tr id="row943mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p945mcpsimp"><a name="p945mcpsimp"></a><a name="p945mcpsimp"></a>ERROR_PKE_LOGIC</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p947mcpsimp"><a name="p947mcpsimp"></a><a name="p947mcpsimp"></a>A hardware logic error occurred in PKE</p>
</td>
</tr>
<tr id="row948mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p950mcpsimp"><a name="p950mcpsimp"></a><a name="p950mcpsimp"></a>ERROR_INVALID_CPU_TYPE</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p952mcpsimp"><a name="p952mcpsimp"></a><a name="p952mcpsimp"></a>The logic obtained an invalid CPU type</p>
</td>
</tr>
<tr id="row953mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p955mcpsimp"><a name="p955mcpsimp"></a><a name="p955mcpsimp"></a>ERROR_INVALID_REGISTER_VALUE</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p957mcpsimp"><a name="p957mcpsimp"></a><a name="p957mcpsimp"></a>The value in the register is invalid</p>
</td>
</tr>
<tr id="row958mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p960mcpsimp"><a name="p960mcpsimp"></a><a name="p960mcpsimp"></a>ERROR_INVALID_PHYS_ADDR</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p962mcpsimp"><a name="p962mcpsimp"></a><a name="p962mcpsimp"></a>An invalid physical address</p>
</td>
</tr>
<tr id="row963mcpsimp"><td class="cellrowborder" rowspan="9" valign="top" width="28.000000000000004%" headers="mcps1.1.4.1.1 "><p id="p965mcpsimp"><a name="p965mcpsimp"></a><a name="p965mcpsimp"></a>TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" width="38%" headers="mcps1.1.4.1.2 "><p id="p967mcpsimp"><a name="p967mcpsimp"></a><a name="p967mcpsimp"></a>ERROR_GET_TRNG_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" width="34%" headers="mcps1.1.4.1.2 "><p id="p969mcpsimp"><a name="p969mcpsimp"></a><a name="p969mcpsimp"></a>Timeout while obtaining the random number</p>
</td>
</tr>
<tr id="row970mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p972mcpsimp"><a name="p972mcpsimp"></a><a name="p972mcpsimp"></a>ERROR_HASH_CLEAR_CHN_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p974mcpsimp"><a name="p974mcpsimp"></a><a name="p974mcpsimp"></a>Timeout while clearing the HASH channel</p>
</td>
</tr>
<tr id="row975mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p977mcpsimp"><a name="p977mcpsimp"></a><a name="p977mcpsimp"></a>ERROR_HASH_CALC_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p979mcpsimp"><a name="p979mcpsimp"></a><a name="p979mcpsimp"></a>Timeout during HASH calculation</p>
</td>
</tr>
<tr id="row980mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p982mcpsimp"><a name="p982mcpsimp"></a><a name="p982mcpsimp"></a>ERROR_SYMC_CLEAR_CHN_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p984mcpsimp"><a name="p984mcpsimp"></a><a name="p984mcpsimp"></a>Timeout while clearing the SYMC channel</p>
</td>
</tr>
<tr id="row985mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p987mcpsimp"><a name="p987mcpsimp"></a><a name="p987mcpsimp"></a>ERROR_SYMC_CALC_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p989mcpsimp"><a name="p989mcpsimp"></a><a name="p989mcpsimp"></a>Timeout during SYMC calculation</p>
</td>
</tr>
<tr id="row990mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p992mcpsimp"><a name="p992mcpsimp"></a><a name="p992mcpsimp"></a>ERROR_SYMC_GET_TAG_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p994mcpsimp"><a name="p994mcpsimp"></a><a name="p994mcpsimp"></a>Timeout while obtaining the tag value</p>
</td>
</tr>
<tr id="row995mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p997mcpsimp"><a name="p997mcpsimp"></a><a name="p997mcpsimp"></a>ERROR_PKE_LOCK_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p999mcpsimp"><a name="p999mcpsimp"></a><a name="p999mcpsimp"></a>Timeout while locking PKE</p>
</td>
</tr>
<tr id="row1000mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1002mcpsimp"><a name="p1002mcpsimp"></a><a name="p1002mcpsimp"></a>ERROR_PKE_WAIT_DONE_TIMEOUT</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1004mcpsimp"><a name="p1004mcpsimp"></a><a name="p1004mcpsimp"></a>Timeout during PKE calculation</p>
</td>
</tr>
<tr id="row1005mcpsimp"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1007mcpsimp"><a name="p1007mcpsimp"></a><a name="p1007mcpsimp"></a>ERROR_PKE_ROBUST_WARNING</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1009mcpsimp"><a name="p1009mcpsimp"></a><a name="p1009mcpsimp"></a>PKE robustness warning</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **Note:** 
>security\_unified designs the error codes in a hierarchical manner to facilitate rapid location during debugging. The error codes returned when users call service-layer interfaces do not carry the hierarchy information. Their error meanings correspond one-to-one with the error codes in the table above. For details, see the definitions of the error codes of the security\_unified module in the API manual. The error code segment is 0x80001500\~0x8001600.

# Network Security Precautions<a name="ZH-CN_TOPIC_0000001833829504"></a>



## Security Driver<a name="ZH-CN_TOPIC_0000001833669724"></a>

-   The Cipher driver implements the standard symmetric encryption algorithms AES/SM4, asymmetric algorithms RSA, ECDSA/SM2/ED25519, digest algorithms SHA/SM3/HMAC\_SHA/SM3, key agreement algorithm ECDH, and key derivation algorithm PBKDF2. No proprietary algorithms are used.
-   Recommendations for symmetric algorithms:
    -   The ECB mode of the AES/SM4 algorithms is a non-secure algorithm and is not recommended.
    -   The longer the key of a symmetric algorithm, the higher the security level. It is recommended that users use AES keys of 128 bits or above.

-   Recommendations for asymmetric algorithms:
    -   It is recommended to use RSA keys with a key length of 3072 bits or above.
    -   For the RSA signing algorithm, the PSS padding method is recommended.
    -   For the RSA encryption/decryption algorithm, the OAEP padding method is recommended.
    -   It is recommended to use ECDSA keys with a key length of 256 bits or above.
    -   The NIST P256/384/521 curves are not recommended for the ECDSA algorithm.

-   Recommendations for digest algorithms:
    -   SHA1/SHA224 algorithms have low security and are not recommended for users.
    -   For the SHA/HMAC\_SHA algorithms, it is recommended to use SHA256/HMAC\_SHA256 or above.

-   Recommendations for key agreement algorithms:
    -   For the ECDH algorithm, it is recommended to use keys with a length of 256 bits or above.
    -   For the DH algorithm, it is recommended to use keys with a length of 3072 bits or above.

-   Recommendations for key derivation algorithms:
    -   The number of iterations is directly proportional to security and also to computation time. A larger number of iterations means a longer key derivation time and stronger resistance to brute-force attacks. For performance-insensitive scenarios or scenarios with high security requirements, an iteration count of at least 10000000 is recommended; for other scenarios, an iteration count of at least 10000 is recommended by default. For products with special performance requirements, the minimum iteration count can be 1000 (NIST SP 800 132).
    -   It is recommended to choose SHA256 or a more secure hash algorithm as the hash function.
    -   The salt value should be at least 16 bytes and should use secure random numbers.
    -   When used for one-way hashing of passwords, the output length should be no less than 256 bits.

## Other Security Precautions for Usage<a name="ZH-CN_TOPIC_0000001880469009"></a>


### JTAG Interface<a name="ZH-CN_TOPIC_0000001880628781"></a>

Malicious users can tamper with the system and its configurations through the JTAG interface, maliciously damaging the system.

Users are advised to take the following measures:

-   Physically remove the JTAG interface when the product leaves the factory.
-   The chip provides a JTAG disable function. Software can permanently disable JTAG at the chip level by programming the EFUSE.

