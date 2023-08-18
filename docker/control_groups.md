# Control group

In the context of Docker, Control Groups (or cgroups) are a Linux kernel feature that allows Docker to limit and isolate the resource usage (CPU, memory, disk I/O, network, etc.) of containers. When you run a container, Docker (or more accurately, the container runtime that Docker uses, such as runc) can use cgroups to control the amount of resources a container can use.

Here are some of the key functionalities provided by cgroups:

1. **Resource Limitation**: Cgroups allow Docker to specify a maximum and minimum for the system resources a set of processes in a container can use. For example, you can limit the percentage of CPU time a container can use or the amount of memory it can consume.

2. **Resource Isolation**: Cgroups can be used to ensure that a group of processes (in this case, a container) gets its fair share of specific system resources, which helps to prevent one container from starving other containers of those resources.

3. **Resource Monitoring**: Cgroups also provide a way to monitor the usage of various system resources by a set of processes (a container in Docker's case). This makes it possible to see how much CPU, memory, and other resources are being used by a container.

4. **Resource Accounting**: This feature of cgroups provides reporting that can be used for analyzing the resource usage patterns over time for processes and, in the context of Docker, for containers.

In Docker, you can specify these cgroup settings when you run a new container. For example, to limit a container to use a maximum of 512 megabytes of memory, you can run a command like this:

```bash
docker run -m 512m <image_name>
```

Or to limit a container to use no more than a specific amount of CPU time, you can use a command like this:

```bash
docker run --cpus="0.5" <image_name>
```

These settings then get translated by Docker into cgroup configurations that the Linux kernel enforces.

It's worth noting that cgroups are part of a broader set of features that Docker uses to isolate containers. The other big part of this is namespaces, which provide a different kind of isolation (isolating the process tree, network interfaces, mount points, etc.).

Cgroups have been a critical part of making containers a practical technology, as they allow for safe multi-tenancy on a shared host, where different containers can be prevented from interfering with each other’s resource usage.