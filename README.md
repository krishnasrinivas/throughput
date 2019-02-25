# throughput

To just test network througput:

Run server as:
```
throughput server --port 8000 --devnull
```

Run client as: (100 threads)
```
throughput client --server http://serverip:8000 --duration 20 /randomfile{1..100}
```

To test network and disk throughput:

Run server as:
```
throughput server --port 8000
```

Run client as:
```
throughput client --server http://serverip:8000 --duration 20 /mnt/disk{1..12}/file{1..10}
```

This runs IO on 10 files on each of 12 disks.
