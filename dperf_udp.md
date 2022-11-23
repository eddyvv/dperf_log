# dperf udp

## server_cps.conf
```bash
mode        server
cpu         1
tx_burst    10
protocol    udp
duration    60s
packet_size 1500
keepalive   1s
port        0000:01:00.0    192.168.8.120   192.168.8.110
client      192.168.8.110       1
server      192.168.8.120       1
listen      80                  1


```

## client_cps.conf
```bash
mode            client
cpu             0
protocol        udp
packet_size     1500
duration        60s
cps             100
cc              8k
keepalive       1ms
port            0000:02:00.0      192.168.8.110   192.168.8.120
client          192.168.8.110     1
server          192.168.8.120     1
listen          80                1
tx_burst        10
launch_num      10


```

## client log

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
pktRx   6                  pktTx    4                  bitsRx   2,880              bitsTx  1,632              dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   6                  arpTx    4                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 1                  cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 2                  cpuUsage 0   
pktRx   0                  pktTx    30                 bitsRx   0                  bitsTx  360,000            dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   30                
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   20                 udpDrop  0                  tcpDrop  0                 
skOpen  10                 skClose  0                  skCon    10                 skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 3                  cpuUsage 0   
pktRx   0                  pktTx    10,030             bitsRx   0                  bitsTx  120,360,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   10,030            
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   10,020             udpDrop  0                  tcpDrop  0                 
skOpen  10                 skClose  0                  skCon    20                 skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 4                  cpuUsage 0   
pktRx   0                  pktTx    21,690             bitsRx   0                  bitsTx  260,280,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   21,690            
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   21,680             udpDrop  0                  tcpDrop  0                 
skOpen  10                 skClose  0                  skCon    30                 skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 5                  cpuUsage 0   
pktRx   0                  pktTx    35,000             bitsRx   0                  bitsTx  420,000,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   35,000            
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   34,990             udpDrop  0                  tcpDrop  0                 
skOpen  10                 skClose  0                  skCon    40                 skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 6                  cpuUsage 0   
pktRx   0                  pktTx    54,180             bitsRx   0                  bitsTx  650,160,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   54,180            
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   54,160             udpDrop  0                  tcpDrop  0                 
skOpen  20                 skClose  0                  skCon    60                 skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 7                  cpuUsage 0   
pktRx   0                  pktTx    77,320             bitsRx   0                  bitsTx  927,840,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   77,320            
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   77,290             udpDrop  0                  tcpDrop  0                 
skOpen  30                 skClose  0                  skCon    90                 skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 8                  cpuUsage 1   
pktRx   1                  pktTx    101,190            bitsRx   480                bitsTx  1,214,280,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   101,190           
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   101,160            udpDrop  0                  tcpDrop  0                 
skOpen  30                 skClose  0                  skCon    120                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 9                  cpuUsage 1   
pktRx   1                  pktTx    129,320            bitsRx   480                bitsTx  1,551,840,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   129,320           
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   129,301            udpDrop  0                  tcpDrop  0                 
skOpen  20                 skClose  0                  skCon    140                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 10                 cpuUsage 1   
pktRx   1                  pktTx    160,430            bitsRx   480                bitsTx  1,925,160,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   160,430           
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   160,389            udpDrop  0                  tcpDrop  0                 
skOpen  40                 skClose  0                  skCon    180                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 11                 cpuUsage 2   
pktRx   1                  pktTx    194,270            bitsRx   2,592              bitsTx  2,331,240,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   194,270           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   194,240            udpDrop  1                  tcpDrop  0                 
skOpen  30                 skClose  0                  skCon    210                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 12                 cpuUsage 2   
pktRx   2                  pktTx    231,360            bitsRx   960                bitsTx  2,776,320,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   231,360           
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   231,320            udpDrop  0                  tcpDrop  0                 
skOpen  40                 skClose  0                  skCon    250                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 13                 cpuUsage 2   
pktRx   2                  pktTx    271,420            bitsRx   960                bitsTx  3,257,040,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   271,420           
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   271,380            udpDrop  0                  tcpDrop  0                 
skOpen  40                 skClose  0                  skCon    290                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 14                 cpuUsage 3   
pktRx   4                  pktTx    314,830            bitsRx   6,144              bitsTx  3,777,960,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    2                  udpTx   314,830           
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   314,780            udpDrop  2                  tcpDrop  0                 
skOpen  50                 skClose  0                  skCon    340                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 15                 cpuUsage 3   
pktRx   1                  pktTx    360,640            bitsRx   2,592              bitsTx  4,327,680,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   360,640           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   360,600            udpDrop  1                  tcpDrop  0                 
skOpen  40                 skClose  0                  skCon    380                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 16                 cpuUsage 3   
pktRx   2                  pktTx    410,270            bitsRx   960                bitsTx  4,923,240,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   410,270           
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   410,210            udpDrop  0                  tcpDrop  0                 
skOpen  60                 skClose  0                  skCon    440                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 17                 cpuUsage 4   
pktRx   2                  pktTx    462,390            bitsRx   960                bitsTx  5,548,680,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   462,390           
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   462,340            udpDrop  0                  tcpDrop  0                 
skOpen  50                 skClose  0                  skCon    490                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 18                 cpuUsage 4   
pktRx   3                  pktTx    517,200            bitsRx   3,552              bitsTx  6,206,400,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   517,200           
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   517,140            udpDrop  1                  tcpDrop  0                 
skOpen  60                 skClose  0                  skCon    550                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 19                 cpuUsage 5   
pktRx   1                  pktTx    575,350            bitsRx   2,592              bitsTx  6,904,200,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   575,350           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   575,290            udpDrop  1                  tcpDrop  0                 
skOpen  60                 skClose  0                  skCon    610                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 20                 cpuUsage 6   
pktRx   1                  pktTx    636,440            bitsRx   480                bitsTx  7,637,280,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   636,440           
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   636,380            udpDrop  0                  tcpDrop  0                 
skOpen  60                 skClose  0                  skCon    670                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 21                 cpuUsage 6   
pktRx   1                  pktTx    700,330            bitsRx   480                bitsTx  8,403,960,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   700,330           
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   700,270            udpDrop  0                  tcpDrop  0                 
skOpen  60                 skClose  0                  skCon    730                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 22                 cpuUsage 7   
pktRx   1                  pktTx    767,980            bitsRx   480                bitsTx  9,215,760,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   767,980           
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   767,910            udpDrop  0                  tcpDrop  0                 
skOpen  70                 skClose  0                  skCon    800                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 23                 cpuUsage 7   
pktRx   0                  pktTx    838,120            bitsRx   0                  bitsTx  10,057,440,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   838,120           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   838,050            udpDrop  0                  tcpDrop  0                 
skOpen  70                 skClose  0                  skCon    870                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 24                 cpuUsage 8   
pktRx   1                  pktTx    911,630            bitsRx   480                bitsTx  10,939,560,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   911,630           
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   911,550            udpDrop  0                  tcpDrop  0                 
skOpen  80                 skClose  0                  skCon    950                skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 25                 cpuUsage 8   
pktRx   2                  pktTx    987,780            bitsRx   960                bitsTx  11,853,360,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   987,780           
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   987,700            udpDrop  0                  tcpDrop  0                 
skOpen  80                 skClose  0                  skCon    1,030              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 26                 cpuUsage 8   
pktRx   2                  pktTx    1,067,080          bitsRx   960                bitsTx  12,804,960,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,067,080         
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,067,000          udpDrop  0                  tcpDrop  0                 
skOpen  80                 skClose  0                  skCon    1,110              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 27                 cpuUsage 8   
pktRx   0                  pktTx    1,148,977          bitsRx   0                  bitsTx  13,787,724,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,148,978         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,148,899          udpDrop  0                  tcpDrop  0                 
skOpen  80                 skClose  0                  skCon    1,190              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 28                 cpuUsage 9   
pktRx   1                  pktTx    1,234,473          bitsRx   480                bitsTx  14,813,676,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,234,472         
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,234,381          udpDrop  0                  tcpDrop  0                 
skOpen  90                 skClose  0                  skCon    1,280              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 29                 cpuUsage 10  
pktRx   1                  pktTx    1,322,810          bitsRx   480                bitsTx  15,873,720,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,322,810         
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,322,720          udpDrop  0                  tcpDrop  0                 
skOpen  90                 skClose  0                  skCon    1,370              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 30                 cpuUsage 10  
pktRx   2                  pktTx    1,416,730          bitsRx   960                bitsTx  17,000,760,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,416,730         
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,416,630          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    1,470              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 31                 cpuUsage 11  
pktRx   0                  pktTx    1,516,590          bitsRx   0                  bitsTx  18,199,080,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,516,590         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,516,490          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    1,570              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 32                 cpuUsage 12  
pktRx   1                  pktTx    1,616,910          bitsRx   480                bitsTx  19,402,920,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,616,910         
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,616,810          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    1,670              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 33                 cpuUsage 13  
pktRx   1                  pktTx    1,716,510          bitsRx   480                bitsTx  20,598,120,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,716,510         
arpRx   1                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,716,410          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    1,770              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 34                 cpuUsage 14  
pktRx   2                  pktTx    1,816,310          bitsRx   960                bitsTx  21,795,720,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,816,310         
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,816,210          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    1,870              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 35                 cpuUsage 15  
pktRx   0                  pktTx    1,916,680          bitsRx   0                  bitsTx  23,000,160,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   1,916,680         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   1,916,580          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    1,970              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 36                 cpuUsage 16  
pktRx   0                  pktTx    2,016,292          bitsRx   0                  bitsTx  24,195,504,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,016,292         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,016,193          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,070              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 37                 cpuUsage 19  
pktRx   0                  pktTx    2,116,078          bitsRx   0                  bitsTx  25,392,936,000     dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,116,078         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,115,977          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,170              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 38                 cpuUsage 24  
pktRx   0                  pktTx    2,216,482          bitsRx   0                  bitsTx  26,597,784,000     dropTx  54,316            
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,216,482         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,216,383          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,270              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 39                 cpuUsage 32  
pktRx   0                  pktTx    2,313,283          bitsRx   0                  bitsTx  27,759,396,000     dropTx  153,896           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,313,285         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,313,184          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,370              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 40                 cpuUsage 35  
pktRx   0                  pktTx    2,413,995          bitsRx   0                  bitsTx  28,967,940,000     dropTx  254,684           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,413,993         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,413,893          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,470              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 41                 cpuUsage 42  
pktRx   0                  pktTx    2,515,198          bitsRx   0                  bitsTx  30,182,376,000     dropTx  356,418           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,515,198         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,515,098          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,570              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 42                 cpuUsage 41  
pktRx   2                  pktTx    2,613,172          bitsRx   960                bitsTx  31,358,064,000     dropTx  478,680           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,613,172         
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,613,072          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,670              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 43                 cpuUsage 46  
pktRx   0                  pktTx    2,714,574          bitsRx   0                  bitsTx  32,574,888,000     dropTx  611,392           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,714,576         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,714,476          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,770              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 44                 cpuUsage 47  
pktRx   0                  pktTx    2,813,096          bitsRx   0                  bitsTx  33,757,152,000     dropTx  711,804           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,813,094         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,812,994          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,870              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 45                 cpuUsage 50  
pktRx   0                  pktTx    2,911,778          bitsRx   0                  bitsTx  34,941,336,000     dropTx  809,308           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   2,911,778         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   2,911,678          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    2,970              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 46                 cpuUsage 52  
pktRx   0                  pktTx    3,012,712          bitsRx   0                  bitsTx  36,152,544,000     dropTx  913,908           
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,012,712         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,012,612          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,070              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 47                 cpuUsage 55  
pktRx   0                  pktTx    3,111,790          bitsRx   0                  bitsTx  37,341,480,000     dropTx  1,008,718         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,111,791         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,111,692          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,170              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 48                 cpuUsage 57  
pktRx   0                  pktTx    3,211,468          bitsRx   0                  bitsTx  38,537,616,000     dropTx  1,107,904         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,211,468         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,211,368          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,270              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 49                 cpuUsage 59  
pktRx   0                  pktTx    3,310,492          bitsRx   0                  bitsTx  39,725,904,000     dropTx  1,209,814         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,310,491         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,310,390          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,370              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 50                 cpuUsage 62  
pktRx   0                  pktTx    3,406,230          bitsRx   0                  bitsTx  40,874,760,000     dropTx  1,304,234         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,406,230         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,406,130          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,470              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 51                 cpuUsage 63  
pktRx   0                  pktTx    3,505,860          bitsRx   0                  bitsTx  42,070,320,000     dropTx  1,399,340         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,505,860         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,505,760          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,570              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 52                 cpuUsage 66  
pktRx   0                  pktTx    3,460,340          bitsRx   0                  bitsTx  41,524,080,000     dropTx  1,396,322         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,460,340         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,460,240          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,670              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 53                 cpuUsage 74  
pktRx   2                  pktTx    3,714,438          bitsRx   960                bitsTx  44,573,256,000     dropTx  1,572,940         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,714,439         
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,714,340          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,770              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 54                 cpuUsage 74  
pktRx   0                  pktTx    3,794,127          bitsRx   0                  bitsTx  45,529,524,000     dropTx  1,648,668         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,794,126         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,794,026          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,870              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 55                 cpuUsage 78  
pktRx   0                  pktTx    3,906,055          bitsRx   0                  bitsTx  46,872,660,000     dropTx  1,757,568         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,906,055         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,905,954          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    3,970              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 56                 cpuUsage 75  
pktRx   0                  pktTx    3,987,970          bitsRx   0                  bitsTx  47,855,640,000     dropTx  1,839,602         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,987,970         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,987,871          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,070              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 57                 cpuUsage 76  
pktRx   0                  pktTx    4,077,262          bitsRx   0                  bitsTx  48,927,144,000     dropTx  1,930,286         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   4,077,262         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   4,077,161          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,170              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 58                 cpuUsage 78  
pktRx   0                  pktTx    4,170,263          bitsRx   0                  bitsTx  50,043,156,000     dropTx  2,018,596         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   4,170,264         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   4,170,165          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,270              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 59                 cpuUsage 84  
pktRx   0                  pktTx    3,996,827          bitsRx   0                  bitsTx  47,961,924,000     dropTx  1,913,500         
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   3,996,826         
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   3,996,726          udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,370              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 60                 cpuUsage 91  
pktRx   2                  pktTx    7,498              bitsRx   960                bitsTx  89,976,000         dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   7,498             
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   7,397              udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,470              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 61                 cpuUsage 0   
pktRx   2                  pktTx    100                bitsRx   960                bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,570              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 62                 cpuUsage 0   
pktRx   2                  pktTx    100                bitsRx   960                bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,670              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 63                 cpuUsage 0   
pktRx   2                  pktTx    100                bitsRx   960                bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   2                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,770              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 64                 cpuUsage 0   
pktRx   6                  pktTx    100                bitsRx   28,320             bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   6                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,870              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 65                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    4,970              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 66                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,070              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 67                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,170              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 68                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,270              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 69                 cpuUsage 0   
pktRx   3                  pktTx    101                bitsRx   9,920              bitsTx  1,200,480          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   1                  arpTx    1                  icmpRx   2                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,370              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 70                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,470              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 71                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,570              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 72                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,670              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 73                 cpuUsage 0   
pktRx   2                  pktTx    100                bitsRx   5,280              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  1                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,770              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 74                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,870              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 75                 cpuUsage 0   
pktRx   3                  pktTx    100                bitsRx   12,032             bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   2                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    5,970              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 76                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,070              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 77                 cpuUsage 0   
pktRx   2                  pktTx    100                bitsRx   9,440              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   2                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,170              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 78                 cpuUsage 0   
pktRx   3                  pktTx    100                bitsRx   12,032             bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   2                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,270              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 79                 cpuUsage 0   
pktRx   3                  pktTx    100                bitsRx   9,904              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    2                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  2                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,370              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 80                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,470              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 81                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,570              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 82                 cpuUsage 0   
pktRx   4                  pktTx    90                 bitsRx   8,432              bitsTx  1,080,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   90                
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  2                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  90                 skClose  0                  skCon    6,660              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 83                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,760              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 84                 cpuUsage 0   
pktRx   3                  pktTx    100                bitsRx   12,032             bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    1                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   2                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,860              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 85                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    6,960              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 86                 cpuUsage 0   
pktRx   2                  pktTx    100                bitsRx   9,440              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   2                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    7,060              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 87                 cpuUsage 0   
pktRx   2                  pktTx    100                bitsRx   5,280              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  1                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    7,160              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 88                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    7,260              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 89                 cpuUsage 0   
pktRx   1                  pktTx    100                bitsRx   4,720              bitsTx  1,200,000          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   100               
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  100                skClose  0                  skCon    7,360              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 90                 cpuUsage 0   
pktRx   2                  pktTx    1                  bitsRx   1,040              bitsTx  480                dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  1                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    7,360              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 91                 cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    7,360              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 92                 cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    7,360              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 93                 cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    7,360              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


-------------
Test Finished
-------------
pktRx   105                pktTx    98,862,446         bitsRx   233,024            bitsTx  1,186,349,282,592  dropTx  24,451,898        
tcpRx   0                  tcpTx    0                  udpRx    12                 udpTx   98,862,440        
arpRx   51                 arpTx    6                  icmpRx   37                 icmpTx  0                 
tosRx   0                  otherRx  5                  badRx    0                 
udpRt   98,855,080         udpDrop  12                 tcpDrop  0                 
skOpen  7,360              skClose  0                  skCon    7,360              skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 

root@test-Super-Server:/home/test/zjzhe/f-stack/app/dperf# 

```


## server log
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
pktRx   6                  pktTx    4                  bitsRx   2,880              bitsTx  1,632              dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   6                  arpTx    4                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 1                  cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 2                  cpuUsage 0   
pktRx   0                  pktTx    0                  bitsRx   0                  bitsTx  0                  dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    0                  udpTx   0                 
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 3                  cpuUsage 0   
pktRx   5,676              pktTx    5,670              bitsRx   68,068,320         bitsTx  68,040,000         dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    5,670              udpTx   5,670             
arpRx   0                  arpTx    0                  icmpRx   6                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 4                  cpuUsage 0   
pktRx   15,671             pktTx    15,670             bitsRx   188,044,720        bitsTx  188,040,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    15,670             udpTx   15,670            
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 5                  cpuUsage 1   
pktRx   27,971             pktTx    27,970             bitsRx   335,644,720        bitsTx  335,640,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    27,970             udpTx   27,970            
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 6                  cpuUsage 2   
pktRx   45,441             pktTx    45,440             bitsRx   545,284,720        bitsTx  545,280,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    45,440             udpTx   45,440            
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 7                  cpuUsage 2   
pktRx   66,949             pktTx    66,948             bitsRx   803,380,720        bitsTx  803,376,000        dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    66,948             udpTx   66,948            
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 8                  cpuUsage 4   
pktRx   90,274             pktTx    90,273             bitsRx   1,083,269,200      bitsTx  1,083,264,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    90,272             udpTx   90,272            
arpRx   1                  arpTx    1                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 9                  cpuUsage 4   
pktRx   116,913            pktTx    116,912            bitsRx   1,402,937,200      bitsTx  1,402,932,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    116,911            udpTx   116,911           
arpRx   1                  arpTx    1                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 10                 cpuUsage 6   
pktRx   146,101            pktTx    146,100            bitsRx   1,753,193,200      bitsTx  1,753,188,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    146,099            udpTx   146,099           
arpRx   1                  arpTx    1                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 11                 cpuUsage 7   
pktRx   178,839            pktTx    178,838            bitsRx   2,146,060,720      bitsTx  2,146,056,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    178,838            udpTx   178,838           
arpRx   0                  arpTx    0                  icmpRx   1                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 12                 cpuUsage 9   
pktRx   214,594            pktTx    214,593            bitsRx   2,575,107,072      bitsTx  2,575,104,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    214,593            udpTx   214,592           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 13                 cpuUsage 10  
pktRx   251,065            pktTx    251,065            bitsRx   3,012,768,480      bitsTx  3,012,768,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    251,064            udpTx   251,064           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 14                 cpuUsage 11  
pktRx   295,470            pktTx    295,469            bitsRx   3,545,619,072      bitsTx  3,545,616,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    295,469            udpTx   295,468           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 15                 cpuUsage 12  
pktRx   340,112            pktTx    340,111            bitsRx   4,081,334,592      bitsTx  4,081,332,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    340,112            udpTx   340,111           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 16                 cpuUsage 14  
pktRx   388,023            pktTx    388,022            bitsRx   4,656,255,072      bitsTx  4,656,252,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    388,022            udpTx   388,021           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 17                 cpuUsage 16  
pktRx   438,866            pktTx    438,866            bitsRx   5,266,380,480      bitsTx  5,266,380,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    438,865            udpTx   438,865           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 18                 cpuUsage 17  
pktRx   492,737            pktTx    492,736            bitsRx   5,912,823,072      bitsTx  5,912,820,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    492,736            udpTx   492,735           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  1                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 19                 cpuUsage 19  
pktRx   536,200            pktTx    536,200            bitsRx   6,434,400,000      bitsTx  6,434,400,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    536,200            udpTx   536,200           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 20                 cpuUsage 20  
pktRx   554,232            pktTx    554,232            bitsRx   6,650,784,000      bitsTx  6,650,784,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    554,232            udpTx   554,232           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 21                 cpuUsage 20  
pktRx   566,955            pktTx    566,955            bitsRx   6,803,460,000      bitsTx  6,803,460,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    566,955            udpTx   566,955           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 22                 cpuUsage 19  
pktRx   581,499            pktTx    581,499            bitsRx   6,977,976,480      bitsTx  6,977,976,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    581,498            udpTx   581,498           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 23                 cpuUsage 18  
pktRx   613,658            pktTx    613,658            bitsRx   7,363,896,000      bitsTx  7,363,896,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    613,658            udpTx   613,658           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 24                 cpuUsage 20  
pktRx   656,234            pktTx    656,234            bitsRx   7,874,808,000      bitsTx  7,874,808,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    656,234            udpTx   656,234           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 25                 cpuUsage 20  
pktRx   679,410            pktTx    679,410            bitsRx   8,152,908,480      bitsTx  8,152,908,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    679,409            udpTx   679,409           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 26                 cpuUsage 22  
pktRx   697,353            pktTx    697,353            bitsRx   8,368,224,480      bitsTx  8,368,224,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    697,352            udpTx   697,352           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 27                 cpuUsage 20  
pktRx   707,633            pktTx    707,633            bitsRx   8,491,596,000      bitsTx  8,491,596,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    707,633            udpTx   707,633           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 28                 cpuUsage 22  
pktRx   716,964            pktTx    716,964            bitsRx   8,603,568,000      bitsTx  8,603,568,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    716,964            udpTx   716,964           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 29                 cpuUsage 23  
pktRx   720,194            pktTx    720,194            bitsRx   8,642,316,480      bitsTx  8,642,316,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    720,193            udpTx   720,193           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 30                 cpuUsage 23  
pktRx   720,953            pktTx    720,953            bitsRx   8,651,424,480      bitsTx  8,651,424,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    720,952            udpTx   720,952           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 31                 cpuUsage 22  
pktRx   719,825            pktTx    719,825            bitsRx   8,637,900,000      bitsTx  8,637,900,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    719,825            udpTx   719,825           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 32                 cpuUsage 23  
pktRx   719,822            pktTx    719,822            bitsRx   8,637,852,480      bitsTx  8,637,852,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    719,821            udpTx   719,821           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 33                 cpuUsage 22  
pktRx   704,536            pktTx    704,535            bitsRx   8,454,420,560      bitsTx  8,454,420,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    704,535            udpTx   704,535           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  1                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 34                 cpuUsage 22  
pktRx   675,150            pktTx    675,150            bitsRx   8,101,788,480      bitsTx  8,101,788,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    675,149            udpTx   675,149           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 35                 cpuUsage 22  
pktRx   675,464            pktTx    675,464            bitsRx   8,105,568,000      bitsTx  8,105,568,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    675,464            udpTx   675,464           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 36                 cpuUsage 21  
pktRx   675,418            pktTx    675,418            bitsRx   8,105,016,000      bitsTx  8,105,016,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    675,418            udpTx   675,418           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 37                 cpuUsage 21  
pktRx   675,965            pktTx    675,965            bitsRx   8,111,568,480      bitsTx  8,111,568,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    675,964            udpTx   675,964           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 38                 cpuUsage 22  
pktRx   673,151            pktTx    673,151            bitsRx   8,077,812,000      bitsTx  8,077,812,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    673,151            udpTx   673,151           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 39                 cpuUsage 21  
pktRx   672,214            pktTx    672,214            bitsRx   8,066,568,000      bitsTx  8,066,568,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    672,214            udpTx   672,214           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 40                 cpuUsage 22  
pktRx   671,904            pktTx    671,904            bitsRx   8,062,848,000      bitsTx  8,062,848,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    671,904            udpTx   671,904           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 41                 cpuUsage 22  
pktRx   671,239            pktTx    671,239            bitsRx   8,054,868,000      bitsTx  8,054,868,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    671,239            udpTx   671,239           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 42                 cpuUsage 18  
pktRx   610,879            pktTx    610,879            bitsRx   7,330,536,480      bitsTx  7,330,536,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    610,878            udpTx   610,878           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 43                 cpuUsage 18  
pktRx   541,268            pktTx    541,268            bitsRx   6,495,216,000      bitsTx  6,495,216,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    541,268            udpTx   541,268           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 44                 cpuUsage 18  
pktRx   538,437            pktTx    538,437            bitsRx   6,461,244,000      bitsTx  6,461,244,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    538,437            udpTx   538,437           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 45                 cpuUsage 16  
pktRx   476,700            pktTx    476,700            bitsRx   5,720,388,480      bitsTx  5,720,388,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    476,699            udpTx   476,699           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 46                 cpuUsage 14  
pktRx   467,430            pktTx    467,430            bitsRx   5,609,160,000      bitsTx  5,609,160,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    467,430            udpTx   467,430           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 47                 cpuUsage 15  
pktRx   465,511            pktTx    465,511            bitsRx   5,586,132,000      bitsTx  5,586,132,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    465,511            udpTx   465,511           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 48                 cpuUsage 14  
pktRx   463,121            pktTx    463,121            bitsRx   5,557,452,000      bitsTx  5,557,452,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    463,121            udpTx   463,121           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 49                 cpuUsage 15  
pktRx   461,113            pktTx    461,113            bitsRx   5,533,356,000      bitsTx  5,533,356,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    461,113            udpTx   461,113           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 50                 cpuUsage 14  
pktRx   461,637            pktTx    461,637            bitsRx   5,539,644,000      bitsTx  5,539,644,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    461,637            udpTx   461,637           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 51                 cpuUsage 14  
pktRx   456,986            pktTx    456,986            bitsRx   5,483,832,000      bitsTx  5,483,832,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    456,986            udpTx   456,986           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 52                 cpuUsage 17  
pktRx   541,469            pktTx    541,469            bitsRx   6,497,628,000      bitsTx  6,497,628,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    541,469            udpTx   541,469           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 53                 cpuUsage 19  
pktRx   614,651            pktTx    614,650            bitsRx   7,375,789,040      bitsTx  7,375,788,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    614,649            udpTx   614,649           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  1                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 54                 cpuUsage 20  
pktRx   610,169            pktTx    610,169            bitsRx   7,322,016,480      bitsTx  7,322,016,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    610,168            udpTx   610,168           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 55                 cpuUsage 18  
pktRx   610,992            pktTx    610,991            bitsRx   7,331,904,000      bitsTx  7,331,892,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    610,992            udpTx   610,992           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 56                 cpuUsage 20  
pktRx   612,155            pktTx    612,156            bitsRx   7,345,848,480      bitsTx  7,345,860,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    612,154            udpTx   612,154           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 57                 cpuUsage 20  
pktRx   611,896            pktTx    611,896            bitsRx   7,342,752,000      bitsTx  7,342,752,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    611,896            udpTx   611,896           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 58                 cpuUsage 19  
pktRx   601,025            pktTx    601,025            bitsRx   7,212,300,000      bitsTx  7,212,300,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    601,025            udpTx   601,025           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 59                 cpuUsage 19  
pktRx   586,563            pktTx    586,563            bitsRx   7,038,756,000      bitsTx  7,038,756,000      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    586,564            udpTx   586,564           
arpRx   0                  arpTx    0                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 60                 cpuUsage 8   
pktRx   280,609            pktTx    280,609            bitsRx   3,367,296,480      bitsTx  3,367,296,480      dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    280,607            udpTx   280,607           
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 61                 cpuUsage 0   
pktRx   101                pktTx    101                bitsRx   1,200,480          bitsTx  1,200,480          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    100                udpTx   100               
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 62                 cpuUsage 0   
pktRx   101                pktTx    101                bitsRx   1,200,480          bitsTx  1,200,480          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    100                udpTx   100               
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


seconds 63                 cpuUsage 0   
pktRx   101                pktTx    101                bitsRx   1,200,480          bitsTx  1,200,480          dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    100                udpTx   100               
arpRx   1                  arpTx    1                  icmpRx   0                  icmpTx  0                 
tosRx   0                  otherRx  0                  badRx    0                 
udpRt   0                  udpDrop  0                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 


-------------
Test Finished
-------------
pktRx   28,413,695         pktTx    28,413,672         bitsRx   340,963,799,520    bitsTx  340,963,718,112    dropTx  0                 
tcpRx   0                  tcpTx    0                  udpRx    28,413,647         udpTx   28,413,642        
arpRx   32                 arpTx    30                 icmpRx   14                 icmpTx  0                 
tosRx   0                  otherRx  2                  badRx    0                 
udpRt   0                  udpDrop  5                  tcpDrop  0                 
skOpen  0                  skClose  0                  skCon    0                  skErr   0                 
ierrors 0                  oerrors  0                  imissed  0                 

root@test-Super-Server:/home/test/zjzhe/f-stack/app/dperf# 



```