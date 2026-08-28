# Preface<a name="ZH-CN_TOPIC_0000001856160653"></a>

**Overview<a name="section4537382116410"></a>**

This document mainly introduces examples of feature development based on MQTT.

MQTT is implemented based on the open-source component paho.mqtt.c-1.3.12. For detailed instructions, refer to the official documentation: [https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/index.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/index.html)

**Product Version<a name="section12266191774710"></a>**

The product versions corresponding to this document are as follows.

<a name="table2270181717471"></a>
<table><thead align="left"><tr id="row15364171712479"><th class="cellrowborder" valign="top" width="31.759999999999998%" id="mcps1.1.3.1.1"><p id="p123646174478"><a name="p123646174478"></a><a name="p123646174478"></a><strong id="b192148202"><a name="b192148202"></a><a name="b192148202"></a>Product Name</strong></p>
</th>
<th class="cellrowborder" valign="top" width="68.24%" id="mcps1.1.3.1.2"><p id="p1936401717470"><a name="p1936401717470"></a><a name="p1936401717470"></a><strong id="b187248502"><a name="b187248502"></a><a name="b187248502"></a>Product Version</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row19364317104716"><td class="cellrowborder" valign="top" width="31.759999999999998%" headers="mcps1.1.3.1.1 "><p id="p7195145011178"><a name="p7195145011178"></a><a name="p7195145011178"></a>WS63</p>
</td>
<td class="cellrowborder" valign="top" width="68.24%" headers="mcps1.1.3.1.2 "><p id="p34453054"><a name="p34453054"></a><a name="p34453054"></a>V100</p>
</td>
</tr>
</tbody>
</table>

**Audience<a name="section4378592816410"></a>**

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
<tbody><tr id="row1372280416410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p3734547016410"><a name="p3734547016410"></a><a name="p3734547016410"></a><a name="image2670064316410"></a><a name="image2670064316410"></a><span><img class="" id="image2670064316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809362008.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p1757432116410"><a name="p1757432116410"></a><a name="p1757432116410"></a>Indicates a high-level risk hazard that, if not avoided, will result in death or serious injury.</p>
</td>
</tr>
<tr id="row466863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1432579516410"><a name="p1432579516410"></a><a name="p1432579516410"></a><a name="image4895582316410"></a><a name="image4895582316410"></a><span><img class="" id="image4895582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001856160661.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p959197916410"><a name="p959197916410"></a><a name="p959197916410"></a>Indicates a medium-level risk hazard that, if not avoided, could result in death or serious injury.</p>
</td>
</tr>
<tr id="row123863216410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p1232579516410"><a name="p1232579516410"></a><a name="p1232579516410"></a><a name="image1235582316410"></a><a name="image1235582316410"></a><span><img class="" id="image1235582316410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809362012.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p123197916410"><a name="p123197916410"></a><a name="p123197916410"></a>Indicates a low-level risk hazard that, if not avoided, could result in minor or moderate injury.</p>
</td>
</tr>
<tr id="row5786682116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p2204984716410"><a name="p2204984716410"></a><a name="p2204984716410"></a><a name="image4504446716410"></a><a name="image4504446716410"></a><span><img class="" id="image4504446716410" height="25.270000000000003" width="55.9265" src="figures/en_image_0000001809521868.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4388861916410"><a name="p4388861916410"></a><a name="p4388861916410"></a>Used to convey device or environment safety warning information. If not avoided, it may result in device damage, data loss, degraded device performance, or other unpredictable consequences.</p>
<p id="p1238861916410"><a name="p1238861916410"></a><a name="p1238861916410"></a>"Caution" does not involve personal injury.</p>
</td>
</tr>
<tr id="row2856923116410"><td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.1.3.1.1 "><p id="p5555360116410"><a name="p5555360116410"></a><a name="p5555360116410"></a><a name="image799324016410"></a><a name="image799324016410"></a><span><img class="" id="image799324016410" height="15.96" width="47.88" src="figures/en_image_0000001856240665.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="79.42%" headers="mcps1.1.3.1.2 "><p id="p4612588116410"><a name="p4612588116410"></a><a name="p4612588116410"></a>Supplementary explanation of key information in the main text.</p>
<p id="p1232588116410"><a name="p1232588116410"></a><a name="p1232588116410"></a>"Note" is not a safety warning and does not involve injury to persons, devices, or the environment.</p>
</td>
</tr>
</tbody>
</table>

**Revision History<a name="section2467512116410"></a>**

<a name="table1557726816410"></a>
<table><thead align="left"><tr id="row2942532716410"><th class="cellrowborder" valign="top" width="20.8%" id="mcps1.1.4.1.1"><p id="p3778275416410"><a name="p3778275416410"></a><a name="p3778275416410"></a><strong id="b5687322716410"><a name="b5687322716410"></a><a name="b5687322716410"></a>Document Version</strong></p>
</th>
<th class="cellrowborder" valign="top" width="26.040000000000003%" id="mcps1.1.4.1.2"><p id="p5627845516410"><a name="p5627845516410"></a><a name="p5627845516410"></a><strong id="b5800814916410"><a name="b5800814916410"></a><a name="b5800814916410"></a>Release Date</strong></p>
</th>
<th class="cellrowborder" valign="top" width="53.16%" id="mcps1.1.4.1.3"><p id="p2382284816410"><a name="p2382284816410"></a><a name="p2382284816410"></a><strong id="b3316380216410"><a name="b3316380216410"></a><a name="b3316380216410"></a>Change Description</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row18423161573717"><td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.1.4.1.1 "><p id="p0424121523719"><a name="p0424121523719"></a><a name="p0424121523719"></a>04</p>
</td>
<td class="cellrowborder" valign="top" width="26.040000000000003%" headers="mcps1.1.4.1.2 "><p id="p11424171553719"><a name="p11424171553719"></a><a name="p11424171553719"></a>2025-02-28</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1257615581576"><a name="p1257615581576"></a><a name="p1257615581576"></a>Updated the content of the "<a href="source_code_download.md">Source Code Download</a>" section.</p>
</td>
</tr>
<tr id="row560713441118"><td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.1.4.1.1 "><p id="p136071534151116"><a name="p136071534151116"></a><a name="p136071534151116"></a>03</p>
</td>
<td class="cellrowborder" valign="top" width="26.040000000000003%" headers="mcps1.1.4.1.2 "><p id="p116072034121119"><a name="p116072034121119"></a><a name="p116072034121119"></a>2024-10-12</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><a name="ul858283411219"></a><a name="ul858283411219"></a><ul id="ul858283411219"><li>Updated the content of the "<a href="subscription_example_code.md">Subscription Example Code</a>" section.</li></ul>
</td>
</tr>
<tr id="row13603174220218"><td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.1.4.1.1 "><p id="p3603124232114"><a name="p3603124232114"></a><a name="p3603124232114"></a>02</p>
</td>
<td class="cellrowborder" valign="top" width="26.040000000000003%" headers="mcps1.1.4.1.2 "><p id="p360311421214"><a name="p360311421214"></a><a name="p360311421214"></a>2024-06-27</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><a name="ul596614255229"></a><a name="ul596614255229"></a><ul id="ul596614255229"><li>Updated the content of the "<a href="subscription_example_code.md">Subscription Example Code</a>" section.</li><li>Updated the content of the "<a href="publish_example_code.md">Publish Example Code</a>" section.</li><li>Updated the content of the "<a href="supporting_encrypted_channels.md">Supporting Encrypted Channels</a>" section.</li></ul>
</td>
</tr>
<tr id="row543416518117"><td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.1.4.1.1 "><p id="p13477159577"><a name="p13477159577"></a><a name="p13477159577"></a>01</p>
</td>
<td class="cellrowborder" valign="top" width="26.040000000000003%" headers="mcps1.1.4.1.2 "><p id="p7347191514575"><a name="p7347191514575"></a><a name="p7347191514575"></a>2024-04-10</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p663512312573"><a name="p663512312573"></a><a name="p663512312573"></a>First official version release.</p>
</td>
</tr>
<tr id="row5947359616410"><td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.1.4.1.1 "><p id="p2149706016410"><a name="p2149706016410"></a><a name="p2149706016410"></a>00B01</p>
</td>
<td class="cellrowborder" valign="top" width="26.040000000000003%" headers="mcps1.1.4.1.2 "><p id="p648803616410"><a name="p648803616410"></a><a name="p648803616410"></a>2024-03-15</p>
</td>
<td class="cellrowborder" valign="top" width="53.16%" headers="mcps1.1.4.1.3 "><p id="p1946537916410"><a name="p1946537916410"></a><a name="p1946537916410"></a>First interim version release.</p>
</td>
</tr>
</tbody>
</table>

# API Interface Description<a name="ZH-CN_TOPIC_0000001809362004"></a>




## Structure Description<a name="ZH-CN_TOPIC_0000001809521856"></a>

For detailed structure descriptions of paho.mqtt.c, refer to the official documentation: [https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/annotated.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/annotated.html)

## API List<a name="ZH-CN_TOPIC_0000001809362000"></a>

For detailed API descriptions of paho.mqtt.c, refer to the official documentation: [https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/globals\_func.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/globals_func.html)

## Configuration Description<a name="ZH-CN_TOPIC_0000001809521852"></a>

For detailed configuration descriptions of paho.mqtt.c, refer to the official documentation: [https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/globals\_defs.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/globals_defs.html)

# Development Guide<a name="ZH-CN_TOPIC_0000001856240657"></a>





## Development Process<a name="ZH-CN_TOPIC_0000001856240661"></a>

Applications using paho.mqtt.c typically use a similar structure:

-   Create a client object.
-   Set the options to connect to the MQTT server.
-   If multithreaded (asynchronous mode) operations are being used, set the callback functions (see the official documentation "[https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/async.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/async.html)").
-   Subscribe to any topics the client needs to receive.
-   Repeat until complete:
    -   Publish all the messages the client needs to publish.
    -   Handle any incoming messages.

-   Disconnect the client.
-   Release all memory used by the client.

For specific implementations, refer to the examples in the official documentation:

-   Synchronous publication example: [https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/pubsync.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/pubsync.html)

-   Asynchronous publication example: [https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/pubasync.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/pubasync.html)

-   Asynchronous subscription example: [https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/subasync.html](https://www.eclipse.org/paho/files/mqttdoc/MQTTClient/html/subasync.html)

## Source Code Download<a name="ZH-CN_TOPIC_0000002173234886"></a>

In the SDK build framework, the paho.mqtt.c source code is located in the open\_source/mqtt/paho.mqtt.c directory. The SDK does not include the paho.mqtt.c source code by default. If the product needs to use it:

1.  First, download "paho.mqtt.c v1.3.12" from the official website

    cd open\_source/mqtt

    git clone -b v1.3.12 https://github.com/eclipse-paho/paho.mqtt.c.git

2.  Apply the "open\_source/mqtt/mqtt\_v1.3.12.patch" file.

    cd paho.mqtt.c

    patch -p1 < ../mqtt\_v1.3.12.patch

3.  Add the MQTT component.

    Modify the build/config/target\_config/ws63/config.py script, and add the 'mqtt' element to the 'ram\_componect' list in the 'ws63-liteos-app' set.

## Subscription Example Code<a name="ZH-CN_TOPIC_0000001856160649"></a>

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#include "MQTTClient.h"
#include "MQTTClientPersistence.h"
#include "osal_debug.h"
#include "MQTTClient.h"
#include "los_memory.h"
#include "los_task.h"

#define CLIENTID_SUB    "ExampleClientSub"
#define QOS         1
#define TIMEOUT     10000L
#define KEEPALIVEINTERVAL 20
#define CLEANSESSION      1

volatile MQTTClient_deliveryToken deliveredtoken;
volatile char g_subEnd = 0;
extern int MQTTClient_init(void);
void delivered(void *context, MQTTClient_deliveryToken dt)
{
    (void)context;
    osal_printk("Message with token value %d delivery confirmed\r\n", dt);
    deliveredtoken = dt;
}

int msgarrvd(void *context, char *topicName, int topicLen, MQTTClient_message *message)
{
    int i;
    char *payloadptr = NULL;
    (void)context;
    (void)topicLen;
    osal_printk("Message arrived\r\n");
    osal_printk("     topic: %s\r\n", topicName);
    osal_printk("   message: ");

    payloadptr = message->payload;
    for (i = 0; i < message->payloadlen; i++) {
        osal_printk("%c", payloadptr[i]);
    }
    osal_printk("\r\n");

    if(memcmp(message->payload, "byebye", message->payloadlen) == 0) {
        g_subEnd = 1;
        osal_printk("g_subEnd = %d\r\n",g_subEnd);
    }
    MQTTClient_freeMessage(&message);
    MQTTClient_free(topicName);
    return 1;
}

void connlost(void *context, char *cause)
{
    (void)context;
    osal_printk("\nConnection lost\r\n");
    osal_printk("     cause: %s\r\n", cause);
}

int mqtt_002(char *addr, char *topic, char *user_name, char *password)
{
    osal_printk("start mqtt sync subscribe...\r\n");
    MQTTClient client;
    MQTTClient_connectOptions conn_opts = MQTTClient_connectOptions_initializer;
    int rc = 0;

    MQTTClient_init();
    MQTTClient_create(&client, addr, CLIENTID_SUB, MQTTCLIENT_PERSISTENCE_NONE, NULL);
    conn_opts.keepAliveInterval = KEEPALIVEINTERVAL;
    conn_opts.cleansession = CLEANSESSION;
    if (user_name != NULL) {
        conn_opts.username = user_name;
        conn_opts.password = password;
    }

    MQTTClient_setCallbacks(client, NULL, connlost, msgarrvd, delivered);

    if ((rc = MQTTClient_connect(client, &conn_opts)) != MQTTCLIENT_SUCCESS) {
        osal_printk("Failed to connect, return code %d\r\n", rc);
        return rc;
    }
    g_subEnd = 0;
    osal_printk("Subscribing to topic %s\nfor client %s using QoS%d\r\n\n"
           "wait for msg \" byebye\"\r\n\n", topic, CLIENTID_SUB, QOS);
    MQTTClient_subscribe(client, topic, QOS);
    do {
        LOS_TaskDelay(10);
    } while((g_subEnd == 0));
    osal_printk("Subscribing End\r\n", rc);
    MQTTClient_unsubscribe(client, topic);
    MQTTClient_disconnect(client, TIMEOUT);
    MQTTClient_destroy(&client);
    return rc;
}
```

## Publish Example Code<a name="ZH-CN_TOPIC_0000001856240653"></a>

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#include "MQTTClient.h"
#include "MQTTClientPersistence.h"
#include "osal_debug.h"
#include "MQTTClient.h"
#include "los_memory.h"
#include "los_task.h"

#define CLIENTID_PUB    "ExampleClientPub"
#define QOS         1
#define TIMEOUT     10000L
#define KEEPALIVEINTERVAL 20
#define CLEANSESSION      1
extern int MQTTClient_init(void);
int mqtt_001(char *addr, char *topic, char *msg, char *user_name, char *password)
{
    osal_printk("start mqtt publish...\r\n");

    MQTTClient client;
    MQTTClient_connectOptions conn_opts = MQTTClient_connectOptions_initializer;
    MQTTClient_message pubmsg = MQTTClient_message_initializer;
    MQTTClient_deliveryToken token;
    int rc = 0;

    MQTTClient_init();
    MQTTClient_create(&client, addr, CLIENTID_PUB, MQTTCLIENT_PERSISTENCE_NONE, NULL);
    conn_opts.keepAliveInterval = KEEPALIVEINTERVAL;
    conn_opts.cleansession = CLEANSESSION;
    if (user_name != NULL) {
        conn_opts.username = user_name;
        conn_opts.password = password;
    }

    if ((rc = MQTTClient_connect(client, &conn_opts)) != MQTTCLIENT_SUCCESS) {
        osal_printk("Failed to connect, return code %d\r\n", rc);
        return -1;
    }

    pubmsg.payload = msg;
    pubmsg.payloadlen = (int)strlen(msg);
    pubmsg.qos = QOS;
    pubmsg.retained = 0;
    MQTTClient_publishMessage(client, topic, &pubmsg, &token);
    osal_printk("Waiting for up to %d seconds for publication of %s\r\n"
            "on topic %s for client with ClientID: %s\r\n",
            (int)(TIMEOUT/1000), msg, topic, CLIENTID_PUB);
    rc = MQTTClient_waitForCompletion(client, token, TIMEOUT);
    osal_printk("Message with delivery token %d delivered\r\n", token);
    MQTTClient_disconnect(client, TIMEOUT);
    MQTTClient_destroy(&client);
    return rc;
}
```

# Precautions<a name="ZH-CN_TOPIC_0000001809521860"></a>


## Supporting Encrypted Channels<a name="ZH-CN_TOPIC_0000001856160657"></a>

-   To implement encrypted MQTT transmission, SSL parameters need to be set in the MQTT configuration items. When performing one-way authentication (the client authenticates the server), the root CA certificate used to authenticate the server must be provided; when performing two-way authentication (the client and the server authenticate each other), in addition to the root CA certificate, the client certificate and private key must also be provided. For encrypted publishing, refer to the following code example:

    >![](public_sys-resources/icon-note.gif) **Note:** 
    >It is recommended to use TLS version 1.2, with a certificate key length of at least 2048 bits.

    ```
    #include <stdio.h>
    #include <stdlib.h>
    #include <string.h>
    
    #include "MQTTClient.h"
    #include "MQTTClientPersistence.h"
    #include "osal_debug.h"
    #include "MQTTClient.h"
    #include "los_memory.h"
    #include "los_task.h"
    
    #define CLIENTID_PUB    "ExampleClientPub"
    #define QOS         1
    #define TIMEOUT     10000L
    #define KEEPALIVEINTERVAL 20
    #define CLEANSESSION      1
    
    /* Client certificate, fill it in by yourself */
    unsigned char client_crt[] = "\
    -----BEGIN CERTIFICATE-----\r\n\
    ****************************************************************\r\n\
    ****************************************************************\r\n\
    -----END CERTIFICATE-----\r\n\
    ";
    /* Client private key, fill it in by yourself */
    unsigned char client_key[] = "\
    -----BEGIN RSA PRIVATE KEY-----\r\n\
    ****************************************************************\r\n\
    ****************************************************************\r\n\
    -----END RSA PRIVATE KEY-----\r\n\
    ";
    /* Root CA certificate, fill it in by yourself */
    unsigned char ca_crt[] = "\
    -----BEGIN CERTIFICATE-----\r\n\
    ****************************************************************\r\n\
    ****************************************************************\r\n\
    -----END CERTIFICATE-----\r\n\
    ";
    extern int MQTTClient_init(void);
    int mqtt_005(char *addr, char *topic, char *msg, char *user_name, char *password)
    {
        osal_printk("start mqtt ssl publish...\r\n");
        MQTTClient_SSLOptions ssl_opts = MQTTClient_SSLOptions_initializer;
        MQTTClient client;
        MQTTClient_connectOptions conn_opts = MQTTClient_connectOptions_initializer;
        MQTTClient_message pubmsg = MQTTClient_message_initializer;
        MQTTClient_deliveryToken token;
        int rc = 0;
    
        MQTTClient_init();
        cert_string keyStore = {client_crt, sizeof(client_crt)};
        cert_string trustStore = {ca_crt, sizeof(ca_crt)};
        key_string privateKey = {client_key, sizeof(client_key)};
        ssl_opts.los_keyStore = &keyStore;
        ssl_opts.los_trustStore = &trustStore;
        ssl_opts.los_privateKey = &privateKey;
        ssl_opts.sslVersion = MQTT_SSL_VERSION_TLS_1_2;
    
        MQTTClient_create(&client, addr, CLIENTID_PUB, MQTTCLIENT_PERSISTENCE_NONE, NULL);
        conn_opts.keepAliveInterval = KEEPALIVEINTERVAL;
        conn_opts.cleansession = CLEANSESSION;
        conn_opts.ssl = &ssl_opts;
        if (user_name != NULL) {
            conn_opts.username = user_name;
            conn_opts.password = password;
        }
    
        if ((rc = MQTTClient_connect(client, &conn_opts)) != MQTTCLIENT_SUCCESS) {
            osal_printk("Failed to connect, return code %d\r\n", rc);
            return -1;
        }
        pubmsg.payload = msg;
        pubmsg.payloadlen = (int)strlen(msg);
        pubmsg.qos = QOS;
        pubmsg.retained = 0;
        MQTTClient_publishMessage(client, topic, &pubmsg, &token);
        osal_printk("Waiting for up to %d seconds for publication of %s\r\n"
                "on topic %s for client with ClientID: %s\r\n",
                (int)(TIMEOUT/1000), msg, topic, CLIENTID_PUB);
        rc = MQTTClient_waitForCompletion(client, token, TIMEOUT);
        osal_printk("Message with delivery token %d delivered\r\n", token);
        MQTTClient_disconnect(client, TIMEOUT);
        MQTTClient_destroy(&client);
        return rc;
    }
    ```

