
### Traffic from 192.168.1.0/24 to 10.0.0.0/24

```mermaid
graph LR;
    Fiber-->R1;
    R1-->R2;
    R1-->10.0.0.210/32;
    R2-->192.168.1.10/32;
```

```mermaid
flowchart LR;
    id1[ICMP, SSH and HTTPS traffic from the 192.168.1.0/24 network can reach the 10.0.0.0/24 network]
```


```mermaid
graph LR;
    R2-->R1;
    R2-->192.168.1.10/32;
    R1-->10.0.0.210/32;
    Fiber-->R1;
```

```mermaid
graph LR;
    Fiber-->R1;
    R1-->R2
    R1-->10.0.0.210/32;
    R2-->192.168.1.10/32;
```