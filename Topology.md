
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
    id3[(R1)]
    Fiber-->id3;
    id3-->Tele2_Gw
    id3-->10.0.0.210/32
    Tele2_Gw-->192.168.1.10/32
```

