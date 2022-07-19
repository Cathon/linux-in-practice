本项目内容为 [Linux 是怎样工作的 实验X图解 直击Linux核心工作原理](https://www.ituring.com.cn/book/2867) 的实验程序

# 说明

本项目中的代码以 Ubuntu 20.04 为运行环境，将书中所写的 C 程序移植到 Go 和 Python 中，同时对一部分代码进行了修改，使其也能进行图表绘制。

必须依赖的软件包如下所示：

binutils, build-essential, golang, python3-matplotlib, python3-pil, fonts-takao

## 第 2 章

- [hello.py](02-syscall-and-non-kernel-os/hello.py)
- [hello.go](02-syscall-and-non-kernel-os/misc/hello.go): 是 [hello.c](02-syscall-and-non-kernel-os/hello.c) 对应的 Go 语言实现，可以使用 `go build hello.go` 命令进行编译。
- [inf-loop](02-syscall-and-non-kernel-os/misc/inf-loop): 是 [loop.c](02-syscall-and-non-kernel-os/loop.c) 对应的 Python 程序。
- [syscall-inf-loop](02-syscall-and-non-kernel-os/misc/syscall-inf-loop): 是 [ppidloop.c](02-syscall-and-non-kernel-os/ppidloop.c) 对应的 Python 程序。

## 第 3 章

- [fork](03-process-management/misc/fork): 是 [fork.c](03-process-management/fork.c) 对应的 Python 程序。
- [fork-and-exec](03-process-management/misc/fork-and-exec): 是 [fork-and-exec.c](03-process-management/fork-and-exec.c) 对应的 Python 程序。

## 第 4 章

- [sched](04-process-scheduler/misc/sched): 是 [sched.c](04-process-scheduler/sched.c) 对应的 Python 程序，并将结果以 "sched-<并发数>.jpg" 的文件名保存。
- [sched_nice.c](04-process-scheduler/sched_nice.c)

以下是在单个 CPU 上运行 sched 程序并进行绘图的结果。分别是1个进程、2个进程并发、3个进程并发的结果。

- ![sched-1.jpg](04-process-scheduler/misc/sched-1.jpg)
- ![sched-2.jpg](04-process-scheduler/misc/sched-2.jpg)
- ![sched-3.jpg](04-process-scheduler/misc/sched-3.jpg)

## 第 5 章

- [cow](05-memory-management/misc/cow): 是 [cow.c](05-memory-management/cow.c) 对应的 Python 程序。
- [demand-paging](05-memory-management/misc/demand-paging): 是 [demand-paging.c](05-memory-management/demand-paging.c) 对应的 Python 程序。
- [mmap.go](05-memory-management/misc/mmap.go): 是 [mmap.c](05-memory-management/mmap.c) 对应的 Go 语言实现，可以使用 `go build mmap.go` 命令进行编译。
- [filemap.go](05-memory-management/misc/filemap.go): 是 [filemap.c](05-memory-management/filemap.c) 对应的 Go 语言实现，可以使用 `go build filemap.go` 命令进行编译。
- [segv.go](05-memory-management/misc/segv.go): 是 [segv.c](05-memory-management/segv.c) 对应的 Go 语言实现，可以使用 `go build segv.go` 命令进行编译。
- [vsz-rss.sh](05-memory-management/vsz-rss.sh)

## 第 6 章

- [cache.go](06-storage-hierarchy/misc/cache.go): 是 [cache.c](06-storage-hierarchy/cache.c) 对应的 Go 语言实现，可以使用 `go build cache.go` 命令进行编译。
- [read-twice.sh](06-storage-hierarchy/read-twice.sh)
- [write.sh](06-storage-hierarchy/write.sh)

以下是当 CPU 的 L1d、L2、L3 高速缓存容量分别为 32KB,512KB,4MB 时，cahe 程序运行结果的图表。

- ![cache.jpg](06-storage-hierarchy/misc/cache.jpg)

## 第 8 章

- [io.c](08-storage-device/io.c)

