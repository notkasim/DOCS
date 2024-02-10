
### Traffic from 192.168.1.0/24 to 10.0.0.0/24

```mermaid
graph LR;
    Fiber-->R1;
    R1-->Tele2_Gw;
    R1-->10.0.0.210/32;
    Tele2_Gw-->192.168.1.10/32;
```

```mermaid
flowchart LR;
    id1[ICMP, SSH and HTTPS traffic from the 192.168.1.0/24 network can reach the 10.0.0.0/24 network]
```

```mermaid
graph RL;
    192.168.1.10/32-->Tele2_Gw;
    Tele2_Gw-->R1;
    R1-->10.0.0.210/32;
    R1-->Fiber;
    Fiber-->Junet_Gw;
    id2[(Internet)]
    Junet_Gw-->id2
```