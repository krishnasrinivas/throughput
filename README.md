# throughput

If a server has 12 disks mounted at /mnt/disk1, /mnt/disk2 ... /mnt/disk12

On the server do:
```
throughput server --port 8000
```

On the client do:
```
throughput client --server http://serverip:8000 --duration 30 /mnt/disk{1..12}/file
```

To run multiple threads per disk, do:
```
throughput client --server http://serverip:8000 --duration 30 /mnt/disk{1..12}/file{1..100}
```

