# dperf log
## client-cps.conf
```bash
mode            client
cpu             0
packet_size     1500
duration        60s
cps             32k
cc              64k
keepalive       10s
port            0000:02:00.0      192.168.8.110   192.168.8.120
client          192.168.8.110     1
server          192.168.8.120     1
listen          80                1
tx_burst        10
launch_num      10


```

## server_cps.conf
```bash
mode        server
cpu         1
tx_burst    10
duration    60s
packet_size 1500
keepalive   10s
port        0000:01:00.0    192.168.8.120   192.168.8.110
client      192.168.8.110       1
server      192.168.8.120       1
listen      80                  1


```



```bash
root@test-Super-Server:/home/test/zjzhe/f-stack/app/dperf# ./build/dperf -c ./test/http/client-cps.conf 
EAL: Detected CPU lcores: 16
EAL: Detected NUMA nodes: 1
EAL: Detected shared linkage of DPDK
EAL: Multi-process socket /var/run/dpdk/rte/mp_socket
EAL: Selected IOVA mode 'PA'
EAL: No available 1048576 kB hugepages reported
EAL: VFIO support initialized
EAL: Probe PCI driver: mlx5_pci (15b3:a2d6) device: 0000:02:00.0 (socket 0)
TELEMETRY: No legacy callbacks, legacy socket not created
socket allocation succeeded, size 0.01GB num 65535
Get gateway's MAC address successfully

seconds 0                  cpuUsage 0   
pktRx   8                  pktTx    4                  bitsRx   8,064              bitsTx  1,632              dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    2                  udpTx   0                 
arpRx   6                  arpTx    4                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    0                  finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  2                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 1                  cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    0                  finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 2                  cpuUsage 0   
pktRx   1                  pktTx    10                 bitsRx   2,592              bitsTx  4,960              dropTx  0                 
tcpRx   0                  tcpTx    10                 udpRx    1                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    10                 finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  1                 
skOpen  10                 skClose  0                  skCon    10                 skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 3                  cpuUsage 0   
pktRx   2                  pktTx    4,260              bitsRx   960                bitsTx  2,112,960          dropTx  0                 
tcpRx   0                  tcpTx    4,260              udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    4,260              finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  4,260              skClose  0                  skCon    4,270              skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 4                  cpuUsage 0   
pktRx   2                  pktTx    5,340              bitsRx   960                bitsTx  2,648,640          dropTx  0                 
tcpRx   0                  tcpTx    5,340              udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    5,340              finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   10                 finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  5,330              skClose  0                  skCon    9,600              skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 5                  cpuUsage 0   
pktRx   2                  pktTx    10,660             bitsRx   960                bitsTx  5,287,360          dropTx  0                 
tcpRx   0                  tcpTx    10,660             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    10,660             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   4,260              finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  6,400              skClose  0                  skCon    16,000             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 6                  cpuUsage 0   
pktRx   2                  pktTx    12,800             bitsRx   960                bitsTx  6,348,800          dropTx  0                 
tcpRx   0                  tcpTx    12,800             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    12,800             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   5,340              finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  7,460              skClose  0                  skCon    23,460             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 7                  cpuUsage 0   
pktRx   2                  pktTx    19,180             bitsRx   960                bitsTx  9,513,280          dropTx  0                 
tcpRx   0                  tcpTx    19,180             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    19,180             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   10,660             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  8,520              skClose  0                  skCon    31,980             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 8                  cpuUsage 0   
pktRx   2                  pktTx    22,400             bitsRx   960                bitsTx  11,110,400         dropTx  0                 
tcpRx   0                  tcpTx    22,400             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    22,400             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   12,800             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  9,600              skClose  0                  skCon    41,580             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 9                  cpuUsage 0   
pktRx   2                  pktTx    29,840             bitsRx   960                bitsTx  14,800,640         dropTx  0                 
tcpRx   0                  tcpTx    29,840             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,840             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   19,180             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  10,660             skClose  0                  skCon    52,240             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 10                 cpuUsage 0   
pktRx   2                  pktTx    34,110             bitsRx   960                bitsTx  16,918,560         dropTx  0                 
tcpRx   0                  tcpTx    34,110             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    34,110             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   22,390             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  11,720             skClose  10                 skCon    63,950             skErr   10                
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 11                 cpuUsage 0   
pktRx   2                  pktTx    29,890             bitsRx   960                bitsTx  14,825,440         dropTx  0                 
tcpRx   0                  tcpTx    29,890             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,890             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   25,580             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  4,310              skClose  4,260              skCon    64,000             skErr   4,260             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 12                 cpuUsage 0   
pktRx   2                  pktTx    34,110             bitsRx   960                bitsTx  16,918,560         dropTx  0                 
tcpRx   0                  tcpTx    34,110             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    34,110             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   28,780             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  5,330              skClose  5,330              skCon    64,000             skErr   5,330             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 13                 cpuUsage 0   
pktRx   2                  pktTx    29,870             bitsRx   960                bitsTx  14,815,520         dropTx  0                 
tcpRx   0                  tcpTx    29,870             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,870             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   23,480             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  6,390              skClose  6,390              skCon    64,000             skErr   6,390             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 14                 cpuUsage 0   
pktRx   2                  pktTx    34,110             bitsRx   960                bitsTx  16,918,560         dropTx  0                 
tcpRx   0                  tcpTx    34,110             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    34,110             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   26,650             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  7,460              skClose  7,460              skCon    64,000             skErr   7,460             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 15                 cpuUsage 0   
pktRx   2                  pktTx    29,890             bitsRx   960                bitsTx  14,825,440         dropTx  0                 
tcpRx   0                  tcpTx    29,890             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,890             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   21,360             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  8,530              skClose  8,530              skCon    64,000             skErr   8,530             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 16                 cpuUsage 0   
pktRx   2                  pktTx    34,110             bitsRx   960                bitsTx  16,918,560         dropTx  0                 
tcpRx   0                  tcpTx    34,110             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    34,110             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   24,520             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  9,590              skClose  9,590              skCon    64,000             skErr   9,590             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 17                 cpuUsage 0   
pktRx   2                  pktTx    29,890             bitsRx   960                bitsTx  14,825,440         dropTx  0                 
tcpRx   0                  tcpTx    29,890             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,890             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   19,230             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  10,660             skClose  10,660             skCon    64,000             skErr   10,660            
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 18                 cpuUsage 0   
pktRx   2                  pktTx    34,100             bitsRx   960                bitsTx  16,913,600         dropTx  0                 
tcpRx   0                  tcpTx    34,100             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    34,100             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   22,380             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  11,720             skClose  11,730             skCon    63,990             skErr   11,730            
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 19                 cpuUsage 0   
pktRx   2                  pktTx    29,900             bitsRx   960                bitsTx  14,830,400         dropTx  0                 
tcpRx   0                  tcpTx    29,900             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,900             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   25,580             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  4,320              skClose  4,310              skCon    64,000             skErr   4,310             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 20                 cpuUsage 0   
pktRx   2                  pktTx    34,090             bitsRx   960                bitsTx  16,908,640         dropTx  0                 
tcpRx   0                  tcpTx    34,090             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    34,090             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   28,770             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  5,320              skClose  5,330              skCon    63,990             skErr   5,330             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 21                 cpuUsage 0   
pktRx   2                  pktTx    29,910             bitsRx   960                bitsTx  14,835,360         dropTx  0                 
tcpRx   0                  tcpTx    29,910             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,910             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   23,510             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  6,400              skClose  6,390              skCon    64,000             skErr   6,390             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 22                 cpuUsage 0   
pktRx   2                  pktTx    34,090             bitsRx   960                bitsTx  16,908,640         dropTx  0                 
tcpRx   0                  tcpTx    34,090             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    34,090             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   26,630             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  7,460              skClose  7,460              skCon    64,000             skErr   7,460             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 23                 cpuUsage 0   
pktRx   2                  pktTx    29,910             bitsRx   960                bitsTx  14,835,360         dropTx  0                 
tcpRx   0                  tcpTx    29,910             udpRx    0                  udpTx   0                 
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    29,910             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   21,380             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  8,530              skClose  8,530              skCon    64,000             skErr   8,530             
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 

```



# dperf 服务端

```bash
root@test-Super-Server:/home/test/zjzhe/f-stack/app/dperf# ./build/dperf -c ./test/http/server-cps.conf 
EAL: Detected CPU lcores: 16
EAL: Detected NUMA nodes: 1
EAL: Detected shared linkage of DPDK
EAL: Multi-process socket /var/run/dpdk/rte/mp_socket
EAL: Selected IOVA mode 'VA'
EAL: No available 1048576 kB hugepages reported
EAL: VFIO support initialized
EAL: Probe PCI driver: mlx5_pci (15b3:a2d6) device: 0000:01:00.0 (socket 0)
TELEMETRY: No legacy callbacks, legacy socket not created
socket allocation succeeded, size 0.01GB num 65535
Get gateway's MAC address successfully

seconds 0                  cpuUsage 0   
pktRx   8                  pktTx    4                  bitsRx   8,064              bitsTx  1,632              dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    2                  udpTx   0                 
arpRx   6                  arpTx    4                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    0                  finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  2                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 1                  cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    0                  finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 2                  cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   0                  synTx    0                  finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 3                  cpuUsage 0   
pktRx   3,452              pktTx    3,451              bitsRx   1,714,272          bitsTx  1,711,680          dropTx  0                 
tcpRx   3,450              tcpTx    3,450              udpRx    1                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   3,450              synTx    3,450              finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  1                 
skOpen  3,450              skClose  0                  skCon    3,450              skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 4                  cpuUsage 0   
pktRx   5,121              pktTx    5,121              bitsRx   2,540,000          bitsTx  2,540,000          dropTx  0                 
tcpRx   5,120              tcpTx    5,120              udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   5,120              synTx    5,120              finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   0                  finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  5,120              skClose  0                  skCon    8,570              skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 5                  cpuUsage 0   
pktRx   9,641              pktTx    9,641              bitsRx   4,781,920          bitsTx  4,781,920          dropTx  0                 
tcpRx   9,640              tcpTx    9,640              udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   9,640              synTx    9,640              finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   3,450              finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  6,190              skClose  0                  skCon    14,760             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 6                  cpuUsage 0   
pktRx   12,381             pktTx    12,381             bitsRx   6,140,960          bitsTx  6,140,960          dropTx  0                 
tcpRx   12,380             tcpTx    12,380             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   12,380             synTx    12,380             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   5,120              finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  7,260              skClose  0                  skCon    22,020             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 7                  cpuUsage 0   
pktRx   17,961             pktTx    17,961             bitsRx   8,908,640          bitsTx  8,908,640          dropTx  0                 
tcpRx   17,960             tcpTx    17,960             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   17,960             synTx    17,960             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   9,640              finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  8,320              skClose  0                  skCon    30,340             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 8                  cpuUsage 0   
pktRx   21,771             pktTx    21,771             bitsRx   10,798,400         bitsTx  10,798,400         dropTx  0                 
tcpRx   21,770             tcpTx    21,770             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   21,770             synTx    21,770             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   12,380             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  9,390              skClose  0                  skCon    39,730             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 9                  cpuUsage 0   
pktRx   28,411             pktTx    28,411             bitsRx   14,091,840         bitsTx  14,091,840         dropTx  0                 
tcpRx   28,410             tcpTx    28,410             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   28,410             synTx    28,410             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   17,960             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  10,450             skClose  0                  skCon    50,180             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 10                 cpuUsage 0   
pktRx   33,291             pktTx    33,291             bitsRx   16,512,320         bitsTx  16,512,320         dropTx  0                 
tcpRx   33,290             tcpTx    33,290             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,290             synTx    33,290             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   21,770             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  11,520             skClose  0                  skCon    61,700             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 11                 cpuUsage 0   
pktRx   30,711             pktTx    31,396             bitsRx   15,232,640         bitsTx  15,572,400         dropTx  0                 
tcpRx   30,710             tcpTx    31,395             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,710             synTx    31,395             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   27,560             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  3,835              skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 12                 cpuUsage 0   
pktRx   33,291             pktTx    33,081             bitsRx   16,512,320         bitsTx  16,408,160         dropTx  0                 
tcpRx   33,290             tcpTx    33,080             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,290             synTx    33,080             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,080             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 13                 cpuUsage 0   
pktRx   30,711             pktTx    30,491             bitsRx   15,232,640         bitsTx  15,123,520         dropTx  0                 
tcpRx   30,710             tcpTx    30,490             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,710             synTx    30,490             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   30,490             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 14                 cpuUsage 0   
pktRx   33,271             pktTx    33,061             bitsRx   16,502,400         bitsTx  16,398,240         dropTx  0                 
tcpRx   33,270             tcpTx    33,060             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,270             synTx    33,060             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,060             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 15                 cpuUsage 0   
pktRx   30,721             pktTx    30,676             bitsRx   15,237,600         bitsTx  15,215,280         dropTx  0                 
tcpRx   30,720             tcpTx    30,675             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,720             synTx    30,675             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   30,675             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 16                 cpuUsage 0   
pktRx   33,281             pktTx    33,281             bitsRx   16,507,360         bitsTx  16,507,360         dropTx  0                 
tcpRx   33,280             tcpTx    33,280             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,280             synTx    33,280             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,280             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 17                 cpuUsage 0   
pktRx   30,721             pktTx    30,721             bitsRx   15,237,600         bitsTx  15,237,600         dropTx  0                 
tcpRx   30,720             tcpTx    30,720             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,720             synTx    30,720             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   30,720             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 18                 cpuUsage 0   
pktRx   33,271             pktTx    33,271             bitsRx   16,502,400         bitsTx  16,502,400         dropTx  0                 
tcpRx   33,270             tcpTx    33,270             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,270             synTx    33,270             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,270             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 19                 cpuUsage 0   
pktRx   30,731             pktTx    31,416             bitsRx   15,242,560         bitsTx  15,582,320         dropTx  0                 
tcpRx   30,730             tcpTx    31,415             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,730             synTx    31,415             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   31,415             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 20                 cpuUsage 0   
pktRx   33,271             pktTx    33,051             bitsRx   16,502,400         bitsTx  16,393,280         dropTx  0                 
tcpRx   33,270             tcpTx    33,050             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,270             synTx    33,050             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,050             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 21                 cpuUsage 0   
pktRx   30,701             pktTx    30,501             bitsRx   15,227,680         bitsTx  15,128,480         dropTx  0                 
tcpRx   30,700             tcpTx    30,500             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,700             synTx    30,500             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   30,500             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 22                 cpuUsage 0   
pktRx   33,291             pktTx    33,071             bitsRx   16,512,320         bitsTx  16,403,200         dropTx  0                 
tcpRx   33,290             tcpTx    33,070             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,290             synTx    33,070             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,070             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 23                 cpuUsage 0   
pktRx   30,711             pktTx    30,666             bitsRx   15,232,640         bitsTx  15,210,320         dropTx  0                 
tcpRx   30,710             tcpTx    30,665             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,710             synTx    30,665             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   30,665             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 24                 cpuUsage 0   
pktRx   33,291             pktTx    33,291             bitsRx   16,512,320         bitsTx  16,512,320         dropTx  0                 
tcpRx   33,290             tcpTx    33,290             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,290             synTx    33,290             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,290             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 25                 cpuUsage 0   
pktRx   30,711             pktTx    30,711             bitsRx   15,232,640         bitsTx  15,232,640         dropTx  0                 
tcpRx   30,710             tcpTx    30,710             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,710             synTx    30,710             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   30,710             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 26                 cpuUsage 0   
pktRx   33,271             pktTx    33,271             bitsRx   16,502,400         bitsTx  16,502,400         dropTx  0                 
tcpRx   33,270             tcpTx    33,270             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,270             synTx    33,270             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,270             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 27                 cpuUsage 0   
pktRx   30,731             pktTx    31,416             bitsRx   15,242,560         bitsTx  15,582,320         dropTx  0                 
tcpRx   30,730             tcpTx    31,415             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   30,730             synTx    31,415             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   31,415             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 28                 cpuUsage 0   
pktRx   33,271             pktTx    33,061             bitsRx   16,502,400         bitsTx  16,398,240         dropTx  0                 
tcpRx   33,270             tcpTx    33,060             udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
synRx   33,270             synTx    33,060             finRx    0                  finTx   0                  rstRx   0          rstTx 0         
synRt   33,060             finRt    0                  ackRt    0                  pushRt  0                 
tcpDrop 0                  udpDrop  0                 
skOpen  0                  skClose  0                  skCon    65,535             skErr   0                 
httpGet 0                  http2XX  0                  httpErr  0                 
ierrors 0                  oerrors  0                  imissed  0                 
```
