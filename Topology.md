
### Traffic from 192.168.1.0/24 to 10.0.0.0/24

```test
graph LR;
    Fiber-->R1;
    R1-->R2
    R1-->Server(10.0.0.210)
    R2-->pi(192.168.1.10)
```