# wireshark-filters

- ICMP Errors

```bash
icmp.type eq 3 || icmp.type eq 4 || icmp.type eq 5 || icmp.type eq 11 || icmpv6.type eq 1 || icmpv6.type eq 2 || icmpv6.type eq 3 || icmpv6.type eq 4
```

- TCP SYN Only

```bash
tcp.flags.syn==1 && tcp.flags.ack==0
```
