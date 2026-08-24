# Preface<a name="ZH-CN_TOPIC_0000001856239829"></a>

**Overview<a name="section4537382116410"></a>**

This document describes implementation examples for developing the HTTP Client feature.

**Product Version<a name="section12266191774710"></a>**

The product versions corresponding to this document are as follows.

<a name="table2270181717471"></a>
<table><thead align="left"><tr id="row15364171712479"><th class="cellrowborder" valign="top" width="31.759999999999998%" id="mcps1.1.3.1.1"><p id="p123646174478"><a name="p123646174478"></a><a name="p123646174478"></a><strong id="b18318438175111"><a name="b18318438175111"></a><a name="b18318438175111"></a>Product Name</strong></p>
</th>
<th class="cellrowborder" valign="top" width="68.24%" id="mcps1.1.3.1.2"><p id="p1936401717470"><a name="p1936401717470"></a><a name="p1936401717470"></a><strong id="b73231638195111"><a name="b73231638195111"></a><a name="b73231638195111"></a>Product Version</strong></p>
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

**Reader Object<a name="section4378592816410"></a>**

This document is mainly applicable to the following engineers:

-   Technical support engineer
-   Software development engineer

**Symbol Conventions<a name="section133020216410"></a>**

The following symbols may appear in this document. Their meanings are as follows.

<a name="table2622507016410"></a>
<table><thead align="left"><tr id="row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="p6450074116410"><a name="p6450074116410"></a><a name="p6450074116410"></a><strong id="b2136615816410"><a name="b2136615816410"></a><a name="b2136615816410"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="p5435366816410"><a name="p5435366816410"></a><a name="p5435366816410"></a><strong id="b5941558116410"><a name="b5941558116410"></a><a name="b5941558116410"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809521032.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a hazard with a high level of risk that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809361188.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a hazard with a medium level of risk that, if not avoided, could result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809521036.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a hazard with a low level of risk that, if not avoided, could result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001856159813.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey device or environment safety warning information. If not avoided, it may result in device damage, data loss, performance degradation, or other unpredictable results.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>A "Caution" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="15.96" width="47.88" src="figures/en_image_0000001856239833.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary explanation of key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>A "Note" is not safety warning information and does not involve personal, device, or environmental injury information.</p>
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
<tbody><tr id="row18669491524"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p10678491228"><a name="p10678491228"></a><a name="p10678491228"></a>02</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p16734915217"><a name="p16734915217"></a><a name="p16734915217"></a>2024-10-12</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p467949123"><a name="p467949123"></a><a name="p467949123"></a>Updated the content of the "<a href="overview.md">Overview</a>" section.</p>
</td>
</tr>
<tr id="row1474911532217"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p15567674319"><a name="p15567674319"></a><a name="p15567674319"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p0567117232"><a name="p0567117232"></a><a name="p0567117232"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1031614161639"><a name="p1031614161639"></a><a name="p1031614161639"></a>First official version release.</p>
</td>
</tr>
<tr id="row5947359616410"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p2149706016410"><a name="p2149706016410"></a><a name="p2149706016410"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p648803616410"><a name="p648803616410"></a><a name="p648803616410"></a>2024-03-15</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>First provisional version release.</p>
</td>
</tr>
</tbody>
</table>

# Development Guide<a name="ZH-CN_TOPIC_0000001856159809"></a>



## Overview<a name="ZH-CN_TOPIC_0000001809521024"></a>

The HTTP example uses the APIs provided by lwIP to establish a connection to the specified IP address and obtain web pages.

>![](public_sys-resources/icon-note.gif) **Note:** 
>The HTTP implementation does not add new APIs. It relies only on the APIs provided by lwIP. For related API descriptions, see the WS63V100 lwIP Development Guide.

## Code Example<a name="ZH-CN_TOPIC_0000001809361184"></a>

The following is a code example of the HTTP Client actively obtaining the homepage of the IP address passed in by the user:

```
#include <stdio.h>
#include "lwip/sockets.h"
#include "lwip/netdb.h"

#define HTTPC_DEMO_RECV_BUFSIZE 64
#define SOCK_TARGET_PORT  80
static const char *g_request = "GET / HTTP/1.1\r\n\
    Content-Type: application/x-www-form-urlencoded;charset=UTF-8\r\n\
    Host: baidu.com\r\n\
    Connection: close\r\n\
    \r\n";

unsigned int http_clienti_get(int argc, char* argv[])
{
    if ((argc != 1) || (argv == NULL)) {
        return 1;
    }
    struct sockaddr_in addr = {0};
    int s, r;
    char recv_buf[HTTPC_DEMO_RECV_BUFSIZE];
    addr.sin_family = AF_INET;
    addr.sin_port = PP_HTONS(SOCK_TARGET_PORT);
    addr.sin_addr.s_addr = inet_addr(argv[0]);
    s = socket(AF_INET, SOCK_STREAM, 0);
    if (s < 0) {
        return 1;
    }
    printf("... allocated socket");
    if (connect(s, (struct sockaddr*)&addr, sizeof(addr)) != 0) {
        printf("... socket connect failed errno=%d", errno);
        lwip_close(s);
        return 1;
    }
    printf("... connected");
    if (lwip_write(s, g_request, strlen(g_request)) < 0) {
        lwip_close(s);
        return 1;
    }
    printf("... socket send success");
    struct timeval receiving_timeout;
    /* 5S Timeout */
    receiving_timeout.tv_sec = 5;
    receiving_timeout.tv_usec = 0;
    if (setsockopt(s, SOL_SOCKET, SO_RCVTIMEO, &receiving_timeout, sizeof(receiving_timeout)) < 0) {
        printf("... failed to set socket receiving timeout");
        lwip_close(s);
        return 1;
    }
    printf("... set socket receiving timeout success");
    /* Read HTTP response */
    do {
        (void)memset_s(recv_buf, sizeof(recv_buf), 0, sizeof(recv_buf));
        r = lwip_read(s, recv_buf, sizeof(recv_buf) - 1);
        for (int i = 0; i < r; i++) {
            putchar(recv_buf[i]);
        }
    } while (r > 0);
    printf("... done reading from socket. Last read return=%d errno=%d\r\n", r, errno);
    lwip_close(s);
    return 0;
}
```

