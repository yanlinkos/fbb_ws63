# Preface<a name="ZH-CN_TOPIC_0000001787758664"></a>

**Overview<a name="section4537382116410"></a>**

This document mainly introduces the usage of the LITTLE FILE SYSTEM (LFS for short) file system module in WS63V100. It is intended to guide engineers in quickly using the file system module for secondary development.

**Product Version<a name="section27775771"></a>**

The product version corresponding to this document is as follows.

<a name="table52250146"></a>
<table><thead align="left"><tr id="row55967882"><th class="cellrowborder" valign="top" width="39.39%" id="mcps1.1.3.1.1"><p id="p37104584"><a name="p37104584"></a><a name="p37104584"></a><strong id="b48174912328"><a name="b48174912328"></a><a name="b48174912328"></a>Product Name</strong></p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.1.3.1.2"><p id="p52681331"><a name="p52681331"></a><a name="p52681331"></a><strong id="b682239163211"><a name="b682239163211"></a><a name="b682239163211"></a>Product Version</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row39329394"><td class="cellrowborder" valign="top" width="39.39%" headers="mcps1.1.3.1.1 "><p id="p15727111613530"><a name="p15727111613530"></a><a name="p15727111613530"></a>WS63</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.1.3.1.2 "><p id="p34453054"><a name="p34453054"></a><a name="p34453054"></a>V100</p>
</td>
</tr>
</tbody>
</table>

**Audience<a name="section4378592816410"></a>**

This document is mainly applicable to the following engineers:

-   Technical support engineers
-   Software engineers

**Symbol Conventions<a name="section133020216410"></a>**

The following symbols may appear in this document. Their meanings are as follows.

<a name="table2622507016410"></a>
<table><thead align="left"><tr id="row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="p6450074116410"><a name="p6450074116410"></a><a name="p6450074116410"></a><strong id="b2136615816410"><a name="b2136615816410"></a><a name="b2136615816410"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="p5435366816410"><a name="p5435366816410"></a><a name="p5435366816410"></a><strong id="b5941558116410"><a name="b5941558116410"></a><a name="b5941558116410"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001834438265.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a high-level risk hazard that will result in death or serious injury if not avoided.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001834518213.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a medium-level risk hazard that may result in death or serious injury if not avoided.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001787599012.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a low-level risk hazard that may result in minor or moderate injury if not avoided.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001787758668.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey device or environment safety warning information. If not avoided, it may result in device damage, data loss, degraded device performance, or other unpredictable results.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>"Notice" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="25.270000000000003" width="67.83" src="figures/en_image_0000001834438269.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary explanation of key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>"Description" is not a safety warning message and does not involve personal, device, or environment injury information.</p>
</td>
</tr>
</tbody>
</table>

**Revision History<a name="section2467512116410"></a>**

<a name="table1557726816410"></a>
<table><thead align="left"><tr id="row2942532716410"><th class="cellrowborder" valign="top" width="20.05%" id="mcps1.1.4.1.1"><p id="p3778275416410"><a name="p3778275416410"></a><a name="p3778275416410"></a><strong id="b5687322716410"><a name="b5687322716410"></a><a name="b5687322716410"></a>Document Version</strong></p>
</th>
<th class="cellrowborder" valign="top" width="22.91%" id="mcps1.1.4.1.2"><p id="p5627845516410"><a name="p5627845516410"></a><a name="p5627845516410"></a><strong id="b5800814916410"><a name="b5800814916410"></a><a name="b5800814916410"></a>Release Date</strong></p>
</th>
<th class="cellrowborder" valign="top" width="57.04%" id="mcps1.1.4.1.3"><p id="p2382284816410"><a name="p2382284816410"></a><a name="p2382284816410"></a><strong id="b3316380216410"><a name="b3316380216410"></a><a name="b3316380216410"></a>Revision Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row167861514343"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.1.4.1.1 "><p id="p14678715193411"><a name="p14678715193411"></a><a name="p14678715193411"></a>02</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.1.4.1.2 "><p id="p1067871513418"><a name="p1067871513418"></a><a name="p1067871513418"></a>2024-10-14</p>
</td>
<td class="cellrowborder" valign="top" width="57.04%" headers="mcps1.1.4.1.3 "><p id="p1667819156346"><a name="p1667819156346"></a><a name="p1667819156346"></a>Updated the content of the "<a href="lfs_compilation_preset.md">LFS Compilation Preset</a>" chapter.</p>
</td>
</tr>
<tr id="row147813357355"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.1.4.1.1 "><p id="p118382762110"><a name="p118382762110"></a><a name="p118382762110"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.1.4.1.2 "><p id="p171834279217"><a name="p171834279217"></a><a name="p171834279217"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="57.04%" headers="mcps1.1.4.1.3 "><p id="p618317279212"><a name="p618317279212"></a><a name="p618317279212"></a>Initial formal version release.</p>
</td>
</tr>
<tr id="row5947359616410"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.1.4.1.1 "><p id="p2149706016410"><a name="p2149706016410"></a><a name="p2149706016410"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.1.4.1.2 "><p id="p648803616410"><a name="p648803616410"></a><a name="p648803616410"></a>2024-02-22</p>
</td>
<td class="cellrowborder" valign="top" width="57.04%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>Initial temporary version release.</p>
</td>
</tr>
</tbody>
</table>

# LFS Introduction<a name="ZH-CN_TOPIC_0000001834437381"></a>

The LFS file system is a file system created for small embedded systems. It provides users with functions such as opening, closing, reading, writing, and deleting files. By using these interfaces, users can store data in NOR FLASH.

-   Power-loss recovery - LFS is designed to handle random power loss. All file operations have strong copy-on-write guarantees. If power is lost, the file system will fall back to the last known good state.
-   Dynamic wear leveling - LFS is designed with flash in mind and provides wear leveling on dynamic blocks. In addition, LFS can detect bad blocks and resolve them.
-   Bounded RAM/ROM - LFS is designed to use a small amount of memory. RAM usage is strictly bounded, which means RAM usage does not change as the file system grows. The file system contains no unbounded recursion, and dynamic memory is limited to configurable buffers that can be statically provisioned.

# LFS Compilation Preset<a name="ZH-CN_TOPIC_0000001834517317"></a>

The current SDK provides the LFS feature, but it is not compiled and enabled by default. To use it, compile and configure the feature according to the following guidance:

1.  Add to compilation. Add the components 'little\_fs' and 'littlefs\_adapt\_ws63' to the compilation target that requires the LFS feature.
2.  Feature macros. Use menuconfig to enable the feature macro corresponding to this feature in the compilation target that requires the LFS feature. The feature macro configuration path is: middleware-\>chip-\>Choose Chip \(ws63\)-\> Chip Configurations for ws63-\> enable littlefs adapt, which enables the CONFIG\_MIDDLEWARE\_SUPPORT\_LFS feature macro. After the macro is enabled, LFS will automatically complete the mount operation during runtime.
3.  FLASH allocation. Note the code (file path: middleware/chips/ws63/littlefs/littlefs\_adapt.c): the interface littlefs\_adapt\_get\_block\_info reads the partition table information, and the corresponding partition is

    CONFIG\_LFS\_PARTITION\_ID;

    This macro needs to be replaced or modified to another partition ID macro in the partition table ID file \(middleware/chips/ws63/partition/include/partition\_resource\_id.h\), and the FLASH address and size corresponding to this macro ID need to be configured in the partition table configuration file (build/config/target\_config/ws63/param\_sector/param\_sector.json) as the basis for LFS operation;

    The configuration is done through menuconfig. After the CONFIG\_MIDDLEWARE\_SUPPORT\_LFS macro is enabled, this macro is displayed automatically. Its default value is 0x21; modify it to the corresponding assigned ID. However, only decimal numbers can be entered in menuconfig, so pay attention to radix conversion. Note that every time the LFS address is adjusted, the content in LFS will be lost;

4.  Other adaptation. To adapt to different upper-layer VFS implementations, the oflag parameter passed in when opening a file is converted so that it can adapt to the lower-layer implementation of LFS. To ensure normal use, the fs\_adapt\_flag\_format interface needs to be re-implemented to adapt to the upper-layer flags.
5.  The POSIX file interface functions open, read, write, lseek, and close are supported. This configuration can be enabled or disabled as needed and is disabled by default.

    The corresponding feature macro can be enabled through menuconfig: "Middleware-\>Chips-\>Chip Configurations for ws63-\>littlefs adapt-\>littlefs support posix interface". When there is no conflict, the open, read, write, lseek, close, unlink, and sync interfaces can be supported.

# LFS Interface API<a name="ZH-CN_TOPIC_0000001787757768"></a>



## API<a name="ZH-CN_TOPIC_0000001834600269"></a>

The APIs currently provided do not represent all capabilities of LFS. Use them as needed.

**Table 1** 

<a name="table1316241613216"></a>
<table><thead align="left"><tr id="row201632164215"><th class="cellrowborder" colspan="2" valign="top" id="mcps1.2.4.1.1"><p id="p1316381682117"><a name="p1316381682117"></a><a name="p1316381682117"></a>Function Category</p>
</th>
<th class="cellrowborder" valign="top" id="mcps1.2.4.1.2"><p id="p14163116102110"><a name="p14163116102110"></a><a name="p14163116102110"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row7163316182111"><td class="cellrowborder" rowspan="2" align="center" valign="top" width="12.55125512551255%" headers="mcps1.2.4.1.1 "><p id="p1163151682110"><a name="p1163151682110"></a><a name="p1163151682110"></a>File System Mount/Unmount</p>
</td>
<td class="cellrowborder" valign="top" width="24.162416241624165%" headers="mcps1.2.4.1.1 "><p id="p1648161192411"><a name="p1648161192411"></a><a name="p1648161192411"></a>fs_adapt_mount</p>
</td>
<td class="cellrowborder" valign="top" width="63.28632863286329%" headers="mcps1.2.4.1.2 "><p id="p1116321618214"><a name="p1116321618214"></a><a name="p1116321618214"></a>Mount the file system.</p>
</td>
</tr>
<tr id="row18485191247"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p690431920243"><a name="p690431920243"></a><a name="p690431920243"></a>fs_adapt_unmount</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p164871922415"><a name="p164871922415"></a><a name="p164871922415"></a>Unmount the file system.</p>
</td>
</tr>
<tr id="row716314165211"><td class="cellrowborder" rowspan="5" valign="top" width="12.55125512551255%" headers="mcps1.2.4.1.1 "><p id="p19163181616217"><a name="p19163181616217"></a><a name="p19163181616217"></a>File I/O Operations</p>
</td>
<td class="cellrowborder" valign="top" width="24.162416241624165%" headers="mcps1.2.4.1.1 "><p id="p54371175260"><a name="p54371175260"></a><a name="p54371175260"></a>fs_adapt_open</p>
</td>
<td class="cellrowborder" valign="top" width="63.28632863286329%" headers="mcps1.2.4.1.2 "><p id="p31639161219"><a name="p31639161219"></a><a name="p31639161219"></a>Open a file. If the file does not exist, whether to create the file is determined by the passed-in oflag parameter. This oflag is a converted parameter. If the path contained in the path parameter does not exist, the path will be created by default.</p>
</td>
</tr>
<tr id="row1232126112613"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p535617203267"><a name="p535617203267"></a><a name="p535617203267"></a>fs_adapt_close</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1123286172620"><a name="p1123286172620"></a><a name="p1123286172620"></a>Close a file handle.</p>
</td>
</tr>
<tr id="row1374910244267"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1990122792612"><a name="p1990122792612"></a><a name="p1990122792612"></a>fs_adapt_read</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p7177111618291"><a name="p7177111618291"></a><a name="p7177111618291"></a>Read file operation. On success, returns the number of bytes read; on failure, returns -1 and sets an error code. If the end of the file has been reached before calling this interface, this read returns 0.</p>
</td>
</tr>
<tr id="row1772042252611"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1911153022617"><a name="p1911153022617"></a><a name="p1911153022617"></a>fs_adapt_write</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p15721182212618"><a name="p15721182212618"></a><a name="p15721182212618"></a>On success, returns the number of bytes written; on error, returns -1 and sets an error code.</p>
</td>
</tr>
<tr id="row1950483142613"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p831363312615"><a name="p831363312615"></a><a name="p831363312615"></a>fs_adapt_delete</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p115041932260"><a name="p115041932260"></a><a name="p115041932260"></a>Delete a file by its path name.</p>
</td>
</tr>
<tr id="row416371613215"><td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.4.1.1 "><p id="p121636169211"><a name="p121636169211"></a><a name="p121636169211"></a>Set Read/Write Offset</p>
</td>
<td class="cellrowborder" valign="top" width="24.162416241624165%" headers="mcps1.2.4.1.1 "><p id="p8529153519267"><a name="p8529153519267"></a><a name="p8529153519267"></a>fs_adapt_seek</p>
</td>
<td class="cellrowborder" valign="top" width="63.28632863286329%" headers="mcps1.2.4.1.2 "><p id="p125423403015"><a name="p125423403015"></a><a name="p125423403015"></a>Set the read/write file offset.</p>
<a name="ul023910419820"></a><a name="ul023910419820"></a><ul id="ul023910419820"><li>LFS_SEEK_SET: Start from the beginning of the file and offset by offset bytes.</li><li>LFS_SEEK_CUR: Start from the current read/write pointer position of the file and add an offset of offset bytes.</li><li>LFS_SEEK_END: Set the file offset to the file size plus the offset bytes. The offset value is only allowed to be negative.</li></ul>
</td>
</tr>
<tr id="row18163716202118"><td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.4.1.1 "><p id="p171639160214"><a name="p171639160214"></a><a name="p171639160214"></a>Get File Size</p>
</td>
<td class="cellrowborder" valign="top" width="24.162416241624165%" headers="mcps1.2.4.1.1 "><p id="p11841389268"><a name="p11841389268"></a><a name="p11841389268"></a>fs_adapt_stat</p>
</td>
<td class="cellrowborder" valign="top" width="63.28632863286329%" headers="mcps1.2.4.1.2 "><p id="p916341615219"><a name="p916341615219"></a><a name="p916341615219"></a>Get the file size by file name.</p>
</td>
</tr>
<tr id="row1249022215407"><td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.4.1.1 "><p id="p14901322134019"><a name="p14901322134019"></a><a name="p14901322134019"></a>Sync File Content</p>
</td>
<td class="cellrowborder" valign="top" width="24.162416241624165%" headers="mcps1.2.4.1.1 "><p id="p15700734114013"><a name="p15700734114013"></a><a name="p15700734114013"></a>fs_adapt_sync</p>
</td>
<td class="cellrowborder" valign="top" width="63.28632863286329%" headers="mcps1.2.4.1.2 "><p id="p949012225400"><a name="p949012225400"></a><a name="p949012225400"></a><span>Synchronize memory with off-chip storage and write buffered data to off-chip storage</span>.</p>
</td>
</tr>
<tr id="row18654205710404"><td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.4.1.1 "><p id="p156549577409"><a name="p156549577409"></a><a name="p156549577409"></a>Create Path</p>
</td>
<td class="cellrowborder" valign="top" width="24.162416241624165%" headers="mcps1.2.4.1.1 "><p id="p186579024113"><a name="p186579024113"></a><a name="p186579024113"></a>fs_adapt_mkdir</p>
</td>
<td class="cellrowborder" valign="top" width="63.28632863286329%" headers="mcps1.2.4.1.2 "><p id="p1065405764016"><a name="p1065405764016"></a><a name="p1065405764016"></a>Create a path.</p>
</td>
</tr>
</tbody>
</table>

## Programming Example<a name="ZH-CN_TOPIC_0000001834640317"></a>

The code provides a basic calling example lfs\_test. It opens a file named lfs\_test in the root directory, reads the first byte and prints it as an integer, adds 1 to the byte and writes it back to the file header, and finally closes the file.

```
void lfs_test(void)
{
    // read current count
    char boot_count = 0;
    int fp = fs_adapt_open("/lfs_test", O_RDWR | O_CREAT);
    if (fp < 0) {
        return;
    }
    int ret = fs_adapt_read(fp, &boot_count, sizeof(boot_count));
    lfs_debug_print_info("lfs_test read, ret = 0x%x\r\n", ret);
    // print the boot count
    lfs_debug_print_info("===========boot_count: %d=============\r\n", boot_count);
    // update boot count
    boot_count = (char)((uint8_t)boot_count + 1);
    ret = fs_adapt_seek(fp, 0, LFS_SEEK_SET);
    lfs_debug_print_info("lfs_test seek, ret = 0x%x\r\n", ret);
    if (ret < LFS_ERR_OK) {
        return;
    }
    ret = fs_adapt_write(fp, &boot_count, sizeof(boot_count));
    lfs_debug_print_info("lfs_test write, ret = 0x%x\r\n", ret);
    // remember the storage is not updated until the file is closed successfully
    ret = fs_adapt_close(fp);
    lfs_debug_print_info("lfs_test close, ret = 0x%x\r\n", ret);
    if (ret < LFS_ERR_OK) {
        return;
    }
}
```

