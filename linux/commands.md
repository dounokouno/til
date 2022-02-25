# コマンドを一定間隔で繰り返し実行する → `watch` コマンド

## e.g.

### コマンドを2秒間隔で繰り返し実行する

```console
$ watch コマンド
```

### コマンドを1秒間隔で繰り返し実行する

```console
$ watch -n 1 コマンド
```

参考: [【 watch 】コマンド――コマンドを一定間隔で繰り返し実行する：Linux基本コマンドTips（220） - ＠IT](https://atmarkit.itmedia.co.jp/ait/articles/1806/29/news037.html)

# マシンの OS 、 CPU 、メモリ、 HDD などの情報を調べる

## OS名 、バージョン

### CentOS

```console
$ cat /etc/redhat-release
```

### AlmaLinux 8

```console
$ cat /etc/almalinux-release
$ cat /etc/centos-release # almalinux-release のエイリアス
$ cat /etc/os-release # /usr/lib/os-release のエイリアス
$ cat /etc/redhat-release # almalinux-release のエイリアス
```

## CPU 情報

- TODO: この辺りを書いている途中
- TODO: モデル名は下記でわかる？要確認

```
$ cat /proc/cpuinfo
# 以下はさくらのVPSの512MBプランの情報
processor	: 0
vendor_id	: GenuineIntel
cpu family	: 6
model		: 61
model name	: Intel Core Processor (Broadwell)
stepping	: 2
microcode	: 0x1
cpu MHz		: 2199.996
cache size	: 4096 KB
physical id	: 0
siblings	: 1
core id		: 0
cpu cores	: 1
apicid		: 0
initial apicid	: 0
fpu		: yes
fpu_exception	: yes
cpuid level	: 13
wp		: yes
flags		: fpu de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm constant_tsc rep_good nopl cpuid tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx hypervisor lahf_lm 3dnowprefetch invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap xsaveopt
bugs		: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds swapgs itlb_multihit srbds
bogomips	: 4399.99
clflush size	: 64
cache_alignment	: 64
address sizes	: 46 bits physical, 48 bits virtual
power management:
```

## メモリ情報

- TODO: この辺りを書いている途中
- TODO: モデル名は下記でわかる？要確認

```
$ cat /proc/meminfo
# 以下はさくらのVPSの512MBプランの情報
MemTotal:         476428 kB
MemFree:          160272 kB
MemAvailable:     370196 kB
Buffers:           16288 kB
Cached:           189032 kB
SwapCached:            0 kB
Active:            96544 kB
Inactive:         153464 kB
Active(anon):      45368 kB
Inactive(anon):     5688 kB
Active(file):      51176 kB
Inactive(file):   147776 kB
Unevictable:           0 kB
Mlocked:               0 kB
SwapTotal:       4194300 kB
SwapFree:        4194300 kB
Dirty:                24 kB
Writeback:             0 kB
AnonPages:         44716 kB
Mapped:            75692 kB
Shmem:              6372 kB
KReclaimable:      23180 kB
Slab:              44480 kB
SReclaimable:      23180 kB
SUnreclaim:        21300 kB
KernelStack:        1440 kB
PageTables:         5288 kB
NFS_Unstable:          0 kB
Bounce:                0 kB
WritebackTmp:          0 kB
CommitLimit:     4432512 kB
Committed_AS:     238392 kB
VmallocTotal:   34359738367 kB
VmallocUsed:           0 kB
VmallocChunk:          0 kB
Percpu:              568 kB
HardwareCorrupted:     0 kB
AnonHugePages:         0 kB
ShmemHugePages:        0 kB
ShmemPmdMapped:        0 kB
HugePages_Total:       0
HugePages_Free:        0
HugePages_Rsvd:        0
HugePages_Surp:        0
Hugepagesize:       2048 kB
Hugetlb:               0 kB
DirectMap4k:       73704 kB
DirectMap2M:      450560 kB
```
