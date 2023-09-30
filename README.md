# wireshark-filters

- ICMP Errors

```bash
icmp.type eq 3 || icmp.type eq 4 || icmp.type eq 5 || icmp.type eq 11 || icmpv6.type eq 1 || icmpv6.type eq 2 || icmpv6.type eq 3 || icmpv6.type eq 4
```

- TCP SYN Only

```bash
tcp.flags.syn==1 && tcp.flags.ack==0
```

- TCP SYN/ACK only

```bash
tcp.flags.syn==1 && tcp.flags.ack==1
```

- TCP TCP SYN && SYN/ACK only

```bash
tcp.flags.syn==1
```

- TCP Reassembled Length

```bash
tcp.reassembled.data
```

- HTTP 80 Traffic Analysis

```bash
tcp.port == 80
```


- HTTP GET/POST Method

```bash
http.request.method == GET or http.request.method == POST
```

- HTTP Server Error

```bash
http.response.code < 600 and http.response.code >= 500
```

- HTTP Client Error

```bash
http.response.code < 500 and http.response.code >= 400
```



