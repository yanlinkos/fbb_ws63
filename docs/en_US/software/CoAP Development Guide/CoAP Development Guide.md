# Preface<a name="ZH-CN_TOPIC_0000001809346148"></a>

**Overview<a name="section4537382116410"></a>**

CoAP, i.e., Constrained Application Protocol, is a lightweight network protocol designed specifically for constrained environments (such as IoT devices). It aims to provide a simple and efficient way for constrained devices to communicate over the Internet. This document describes development implementation examples of CoAP functions based on libcoap, as well as the interface descriptions of the thread-safe wrappers for certain libcoap interfaces based on the lwIP (A Lightweight TCP/IP stack) protocol stack.

**Product Version<a name="section111371595118"></a>**

The product versions corresponding to this document are as follows.

<a name="table22377277"></a>
<table><thead align="left"><tr id="row63051425"><th class="cellrowborder" valign="top" width="40.400000000000006%" id="mcps1.1.3.1.1"><p id="p6891761"><a name="p6891761"></a><a name="p6891761"></a><strong id="b35031421172411"><a name="b35031421172411"></a><a name="b35031421172411"></a>Product Name</strong></p>
</th>
<th class="cellrowborder" valign="top" width="59.599999999999994%" id="mcps1.1.3.1.2"><p id="p21361741"><a name="p21361741"></a><a name="p21361741"></a><strong id="b13516921132418"><a name="b13516921132418"></a><a name="b13516921132418"></a>Product Version</strong></p>
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

**Intended Audience<a name="section4378592816410"></a>**

This document is mainly applicable to the following audiences:

-   Software development engineers
-   Technical support engineers

**Symbol Conventions<a name="section133020216410"></a>**

The following symbols may appear in this document. Their meanings are as follows.

<a name="table2622507016410"></a>
<table><thead align="left"><tr id="row1530720816410"><th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.1.3.1.1"><p id="p6450074116410"><a name="p6450074116410"></a><a name="p6450074116410"></a><strong id="b2136615816410"><a name="b2136615816410"></a><a name="b2136615816410"></a>Symbol</strong></p>
</th>
<th class="cellrowborder" valign="top" width="79.42%" id="mcps1.1.3.1.2"><p id="p5435366816410"><a name="p5435366816410"></a><a name="p5435366816410"></a><strong id="b5941558116410"><a name="b5941558116410"></a><a name="b5941558116410"></a>Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809346152.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a hazard with a high level of risk that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809346160.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a hazard with a medium level of risk that, if not avoided, could result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809506012.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a hazard with a low level of risk that, if not avoided, could result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001856224825.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey device or environment safety warning information. If not avoided, it may result in device damage, data loss, degraded device performance, or other unpredictable results.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>"Notice" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="15.96" width="47.88" src="figures/en_image_0000001856224821.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary explanation of the key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>"Note" is not safety warning information and does not involve personal, device, or environmental injury information.</p>
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
<tbody><tr id="row88399385216"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p108391538162114"><a name="p108391538162114"></a><a name="p108391538162114"></a>02</p>
</td>
<td class="cellrowborder" valign="top" width="26.119999999999997%" headers="mcps1.1.4.1.2 "><p id="p118391938202114"><a name="p118391938202114"></a><a name="p118391938202114"></a>2024-06-27</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><a name="ul11946426152312"></a><a name="ul11946426152312"></a><ul id="ul11946426152312"><li>Updated the interface descriptions in "<a href="overview.md">Overview</a>".</li><li>Updated the configuration descriptions in "<a href="resource_configuration.md">Resource Configuration</a>".</li><li>Updated the code samples in "<a href="code_examples.md">Code Examples</a>".</li></ul>
</td>
</tr>
<tr id="row733754412327"><td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.4.1.1 "><p id="p15567674319"><a name="p15567674319"></a><a name="p15567674319"></a>01</p>
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
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>First interim version release.</p>
</td>
</tr>
</tbody>
</table>

# API Interface Description<a name="ZH-CN_TOPIC_0000001809346140"></a>


## Overview<a name="ZH-CN_TOPIC_0000001856144785"></a>

CoAP uses the open-source library libcoap to provide basic functional support. For CoAP-based service implementations, please call the libcoap interfaces. For usage instructions of the APIs provided by the open-source library itself, please refer to the open-source API interface description information. For the current lwIP protocol stack adapted to libcoap, the open-source provides the following interfaces:

-   coap\_new\_context   Create a CoAP context
-   coap\_free\_context   Release or destroy a CoAP context
-   coap\_check\_notify   Check whether a notification needs to be sent
-   coap\_send   Send a CoAP message
-   coap\_send\_ack   Send a CoAP ACK
-   coap\_send\_error   Send a CoAP error
-   coap\_send\_message\_type   Define the type of the CoAP message to be sent

# Development Guide<a name="ZH-CN_TOPIC_0000001809346136"></a>



## Development Constraints<a name="ZH-CN_TOPIC_0000001856144773"></a>


### Resource Configuration<a name="ZH-CN_TOPIC_0000001856224801"></a>

The resources used in libcoap are pre-allocated in lwIP. The resources include the number of supported nodes and the limits on the numbers of contexts, endpoints, sessions, PDUs, resources, and so on. Developers are advised to configure them properly according to the actual scenarios that need to be supported. The specific configuration values are set in the open\_source/libcoap/libcoap/examples/lwip/config/lwippools.h file in the form of macros. Developers can modify them in this file for adaptation. Using these resources will enlarge the memory pool pre-allocated by lwIP and increase the RAM size. Therefore, the pre-allocation of these resources is not enabled by default in the code. You need to modify the global macro definition in build/cmake/open\_source/libcoap.cmake as follows:

```
set(PUBLIC_DEFINES
    MEMP_USE_CUSTOM_POOLS=1
)
```

## Code Examples<a name="ZH-CN_TOPIC_0000001856144769"></a>



### Server<a name="ZH-CN_TOPIC_0000001856224797"></a>

The following is the sample code for the server to expose the GET and POST methods:

```
#include "lwip/netifapi.h"
#include "lwip/sockets.h"
#include "lwip/netifapi.h"
#include "lwip/sockets.h"
#include "coap3/coap.h"
#include "osal_debug.h"
#include "osal_task.h"

#define SERVER_PORT 5683
static int quit = 0;

static void hello_handler(coap_resource_t *resource, coap_session_t  *session,
             const coap_pdu_t *request, const coap_string_t *query,
             coap_pdu_t *response)
{
    unsigned char buf[3];
    const char *response_data = "Hello World!";
    char coap_msg[64] = {0};
    size_t len = 0;
    u32_t cnt;
    unsigned char *data = NULL;
    (void)resource;
    (void)query;
    if (coap_get_data(request, &len, (const uint8_t **)&data)) {
        if (len < 6) {
            osal_printk("[%s][%d] len %d\n", __FUNCTION__, __LINE__, len);
            (void)snprintf_s(coap_msg, sizeof(coap_msg), sizeof(coap_msg)-1, "%s", response_data);
            quit = 1;
        } else {
            memcpy(coap_msg, data, 4);
            (void)snprintf_s(coap_msg + 4, sizeof(coap_msg) - 4, sizeof(coap_msg) - 5, "%s", response_data);
            cnt = ntohl(*((u32_t *)data));
            len -= 4;
            data += 4;
            osal_printk("[%s][%d] <%u> len : %d, data : %.*s\n", __FUNCTION__, __LINE__, cnt, len, len, data);
            quit = 1;
        }
    }
    response->code = COAP_RESPONSE_CODE(205);
    coap_add_option(response, COAP_OPTION_CONTENT_TYPE, coap_encode_var_safe(buf, sizeof(buf),
        COAP_MEDIATYPE_TEXT_PLAIN), buf);
    coap_add_data(response, 4 + strlen(coap_msg + 4), (unsigned char *)coap_msg);
}

int server_main_task(void *p_data)
{
    coap_address_t serv_addr;
    coap_address_init(&serv_addr);
    serv_addr.port = SERVER_PORT;
    ipaddr_aton("192.168.3.68", &(serv_addr.addr)); /* Server IP address */
    coap_context_t *ctx = coap_new_context(&serv_addr);
    if (!ctx) {
        osal_printk("coap_new_context ctx = NULL\n");
        return 0;
    }

    coap_resource_t *hello_resource = coap_resource_init(coap_make_str_const("hello"), 0);
    if (hello_resource == NULL) {
        osal_printk("hello_resource = NULL\n");
    }
    coap_register_handler(hello_resource, COAP_REQUEST_GET, hello_handler);
    coap_register_handler(hello_resource, COAP_REQUEST_POST, hello_handler);
    coap_add_resource(ctx, hello_resource);
    /*Listen for incoming connections */
    osal_printk("Server listening for connections\n");

    while (!quit) { /* Change the stop condition as required */
        osal_msleep(1000);
        uapi_watchdog_kick();
    }
    osal_printk("Process terminated\n");
    return 0;
}

int server_main(void)
{
    osal_task *coap_server_thread = osal_kthread_create(server_main_task, NULL, "coap_server", 0x1200);
    if (coap_server_thread == NULL) {
        osal_printk("create server_main_task kthread failed\n");
        return -1;
    }

    osal_kthread_set_priority(coap_server_thread, 20);
    return 0;
}
```

The client obtains the response result using the POST method, as shown in the following figure:

![](figures/en_image_0000001956861489.png)

### Client<a name="ZH-CN_TOPIC_0000001809505996"></a>

The following is the sample code for the client to obtain the server response using the GET method:

```

#include "lwip/netifapi.h"
#include "lwip/sockets.h"
#include "coap3/coap.h"
#include "osal_debug.h"
#define SERVER_PORT 5683
#define PAYLOAD_SIZE 60
#define MICE_URI "/"
static coap_context_t *g_ctx = NULL;

static coap_response_t mice_handler(coap_session_t *session, const coap_pdu_t *sent, const coap_pdu_t *received,
    const coap_mid_t mid)
{
    unsigned char *data;
    size_t data_len;
    if (COAP_RESPONSE_CLASS(received->code) == 2) {
        if (coap_get_data(received, &data_len, (const uint8_t **)&data)) {
            osal_printk("Reply OK. TID %d msgID %d\n", mid, ntohs(received->mid));
            osal_printk("Payload***[%s]***\n", data);
        }
    } else {
        osal_printk("code error");
        osal_printk("Mice unsuccessful, code: %hu \n", received->code);
    }
}
static void coap_recv_client(void *arg, struct udp_pcb *upcb, struct pbuf *p, const ip_addr_t *addr, u16_t port)
{
    coap_session_t *session = arg;
    coap_pdu_t *pdu = coap_new_pdu(COAP_MESSAGE_CON, COAP_REQUEST_GET, session);
    memset_s(pdu, sizeof(coap_pdu_t), 0, sizeof(coap_pdu_t));
    pdu->max_hdr_size = COAP_PDU_MAX_UDP_HEADER_SIZE;
    pdu->pbuf = p;
    pdu->token = (uint8_t *)p->payload + pdu->max_hdr_size;
    pdu->alloc_size = p->tot_len - pdu->max_hdr_size;
    coap_pdu_clear(pdu, pdu->alloc_size);
    if (!coap_pdu_parse(COAP_PROTO_UDP, p->payload, p->len, pdu)) {
        return;
    }
    coap_dispatch(g_ctx, session, pdu);
    (void)pbuf_free(p);
    pdu->pbuf = NULL;
    coap_delete_pdu(pdu);
    udp_remove(session->sock.pcb);
    if (g_ctx != NULL) {
        coap_free_context(g_ctx);
        g_ctx = NULL;
    }
    coap_session_release(session);
}

void snd_msg(void)
{
    osal_printk("------method get msg-------\n");
    coap_pdu_t *request = coap_pdu_init(COAP_MESSAGE_CON, COAP_REQUEST_GET, coap_new_message_id(g_ctx->sessions),
        coap_session_max_pdu_size(g_ctx->sessions));
    if (request == NULL) {
        osal_printk("request init error");
        return;
    }
    coap_uri_t uri;
    coap_split_uri((const uint8_t *)MICE_URI, strlen(MICE_URI), &uri);
    coap_add_option(request, COAP_OPTION_URI_PATH, uri.path.length, uri.path.s);

    char *request_data = (char *)malloc(64);
    if (request_data == NULL) {
        osal_printk("[%s][%d]: malloc error\n", __FUNCTION__, __LINE__);
        return;
    }
    (void)snprintf_s(request_data + 4, sizeof(request_data) - 4, sizeof(request_data)-5, "%s", "testcoap");

    coap_add_data(request, 4 + strlen((const char *)(request_data+4)), (unsigned char *)request_data);
    free(request_data);
    if (coap_send(g_ctx->sessions, request) < 0) {
        osal_printk("[%s][%d]: coap send error\n", __FUNCTION__, __LINE__);
    }
    return;
}
void snd_continuous(char *address, int port)
{
    if (g_ctx == NULL) {
        osal_printk("snd_continuous 1\r\n");
        coap_address_t src_addr;
        coap_address_init(&src_addr);
        ip_addr_set_any(false, &(src_addr.addr));
        src_addr.port = port;
        g_ctx = coap_new_context(NULL);
        if (g_ctx == NULL) {
            osal_printk("new context error\n");
            return;
        }
        coap_context_set_keepalive(g_ctx, 60);
        coap_address_t dst_addr;
        coap_address_init(&dst_addr);
        ipaddr_aton(address, &(dst_addr.addr));
        dst_addr.port = port;
        coap_session_t *session = coap_new_client_session(g_ctx, NULL, &dst_addr, COAP_PROTO_UDP);
        if (session == NULL) {
            osal_printk("------session is null\n");
            return;
        }
        session->sock.pcb = udp_new_ip_type(IPADDR_TYPE_ANY);
        if (session->sock.pcb == NULL) {
            osal_printk("coap_new_endpoint: udp new fail\n");
            return;
        }
        session->sock.pcb->netif_idx = NETIF_NO_INDEX;
        udp_recv(session->sock.pcb, coap_recv_client, session);
        if (udp_bind(session->sock.pcb, &(src_addr.addr), 0)) {
            osal_printk("--------udp bind error\n");
            udp_remove(session->sock.pcb);
            return;
        }
        /* register mice handler */ 
        coap_register_response_handler(g_ctx, mice_handler);
    }
    snd_msg();
}

int coap_client(void)
{
    osal_printk("client_main start\n");
    int port = 5683; /* CoAP service port */
    char *address = "192.168.3.65"; /* Server IP address */
    osal_printk("Start on port %d, connect to %s\n", port, address);
    osal_printk("Client started\n");
    osal_printk("\r\nsnd_continuous\r\n");
    snd_continuous(address, port);
    return 0;
}


```

The server response is shown in the following figure:

![](figures/en_image_0000001929350884.png)

