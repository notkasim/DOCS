
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
    core[(Core_R)]
    tele2[(Tele_R)]
    core_link{{10.0.0.242}}
    tele2_link{{10.0.0.243}}
    core_net[\10.0.0.0/24/]
    tele2_net[/192.168.1.0/24\]

    Fiber-->core;
    core_net-->core;
    core-->core_link;
    core_link-->tele2_link;
    tele2_link-->tele2;
    tele2-->tele2_net-->192.168.1.10;






```

