
### Traffic from 192.168.1.0/24 to 10.0.0.0/24 & Internet

```ICMP, SSH, HTTP and HTTPS traffic from the 192.168.1.0/24 network can reach the 10.0.0.0/24 network```

```mermaid
graph RL;
    192.168.1.10/32-->Tele2_Gw;
    id1[(R1)]
    Tele2_Gw-->id1;
    id1-->10.0.0.210/32;
    id1-->Fiber;
    Fiber-->Junet_Gw;
    id2[(Internet)]
    Junet_Gw-->id2
```



```mermaid
graph LR;
    id3[(Core_R)]
    id3-->Gw:10.0.0.1
    id3-->10.0.0.210/32
    Fiber-->id3;
    id4[(Tele2_R)]
    id3-->id4
    id4-->Gw:192.168.1.0-->192.168.1.10
    id4-->10.0.0.243-->id3
```

