# Namespaces

A Linux namespace is an abstraction over resources in the operating system. At a high level, they allow for isolation of global system resources between independent processes. We can think of a namespace as a box. Inside this box are these system resources, which ones exactly depend on the box’s (namespace’s) type. There are currently 7 types of namespaces:

* Mount - isolate filesystem mount points
* UTS - isolate hostname and domainname
* IPC - isolate interprocess communication
* PID - isolate the PID number space
* Network - isolate network interfaces
* User - isolate GID / UID number spaces
* Cgroup - isolate cgroup root directory

Namespaces aren’t some addon feature or library that you need to apt install, they are provided by the Linux kernel itself and already are a prerequisite to run any process on the system.

# Links

* [Demystifying Containers - Part I: Kernel Space](https://medium.com/@saschagrunert/demystifying-containers-part-i-kernel-space-2c53d6979504)
* [Demystifying Containers - Part II: Container Runtimes](https://medium.com/@saschagrunert/demystifying-containers-part-ii-container-runtimes-e363aa378f25)
* [Demystifying Containers – Part III: Container Images](https://www.suse.com/c/demystifying-containers-part-iii-container-images/)

## Linux manpages

* [exec(3)](http://man7.org/linux/man-pages/man3/exec.3.html)
* [fork(2)](http://man7.org/linux/man-pages/man2/fork.2.html)
* [clone(2)](http://man7.org/linux/man-pages/man2/clone.2.html)
* [setns(2)](http://man7.org/linux/man-pages/man2/setns.2.html)
* [unshare(2)](http://man7.org/linux/man-pages/man2/unshare.2.html)
* [user_namespaces(7)](http://man7.org/linux/man-pages/man7/user_namespaces.7.html)

## Linux namespaces

* A deep dive into Linux namespaces
  * [Part 1](http://ifeanyi.co/posts/linux-namespaces-part-1/)
  * [Part 2 - User namespace](http://ifeanyi.co/posts/linux-namespaces-part-2/)
  * [Part 3 - Mount points](http://ifeanyi.co/posts/linux-namespaces-part-3/)
  * [Part 4 - Network namespace](http://ifeanyi.co/posts/linux-namespaces-part-4/)


* [Linux Namespaces](https://medium.com/@teddyking/linux-namespaces-850489d3ccf)
  * [Namespaces in Go - Basics](https://medium.com/@teddyking/namespaces-in-go-basics-e3f0fc1ff69a)
  * [Namespaces in Go - User](https://medium.com/@teddyking/namespaces-in-go-user-a54ef9476f2a)
  * [Namespaces in Go - reexec](https://medium.com/@teddyking/namespaces-in-go-reexec-3d1295b91af8)
  * [Namespaces in Go - Mount](https://medium.com/@teddyking/namespaces-in-go-mount-e4c04fe9fb29)
  * [Namespaces in Go - Network](https://medium.com/@teddyking/namespaces-in-go-network-fdcf63e76100)
  * [Namespaces in Go - UTS](https://medium.com/@teddyking/namespaces-in-go-uts-d47aebcdf00e)

* Videos, talks
  * [Cgroups, namespaces, and beyond: what are containers made from?](https://www.youtube.com/watch?v=sK5i-N34im8)
  * [Building a container from scratch in Go - Liz Rice (Microscaling Systems](https://www.youtube.com/watch?v=Utf-A4rODH8)

## What the heck is...

* [...the inode number](https://tecadmin.net/what-is-inode-number-in-linux/)
* [...the RootFS](https://kernelnewbies.org/RootFileSystem)
* [...the /proc filesystem](https://www.geeksforgeeks.org/proc-file-system-linux/)
* ...the pseudo filesystem [1](https://superuser.com/questions/1198292/what-is-a-pseudo-file-system-in-linux) [2](http://www.tldp.org/LDP/sag/html/proc-fs.html) [3](http://www.olsr.org/docs/report_html/node75.html) [4](https://www.tecmint.com/exploring-proc-file-system-in-linux/)
