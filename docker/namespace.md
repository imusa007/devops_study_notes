# Namespaces

In the context of Docker, namespaces are a feature of the Linux kernel that provide isolated workspaces called namespaces, which Docker uses to provide isolation between containers. Each namespace provides a layer of isolation, so what happens in one namespace is not directly visible in another namespace. Docker leverages several types of namespaces to isolate different aspects of containers from each other and from the host system. Here are the main types of namespaces used by Docker:

1. **PID (Process ID) Namespace:**
   - Each PID namespace has its own set of process IDs. When you create a new container, Docker creates a new PID namespace for that container. This means that processes within a container can have the same PID as processes in another container or on the host, but they are completely isolated from each other.
   - This isolation ensures that processes in one container cannot directly interact with processes in another container or the host system. For example, a `kill` command issued within a container cannot affect processes outside of that container.

2. **NET (Network) Namespace:**
   - The NET namespace provides each container with its own network stack. This means that each container has its own network devices, IP addresses, port numbers, and routing tables.
   - Because each container has its own network namespace, it operates as though it is running on a separate physical machine from other containers and the host, in terms of networking.

3. **IPC (Inter-Process Communication) Namespace:**
   - IPC namespaces isolate certain inter-process communication resources, such as message queues, semaphore sets, and shared memory segments. This means that processes in different IPC namespaces cannot directly communicate with each other using these IPC mechanisms.
   - This ensures that processes in one container cannot eavesdrop on or interfere with IPC communications from another container.

4. **MNT (Mount) Namespace:**
   - The MNT namespace provides isolation for the file system mount points seen by the processes in a namespace. Each container has its own mount namespace, so it has its own file system hierarchy that is separate from other containers and the host system.
   - This means that changes to the file system hierarchy (such as mounting or unmounting file systems) in one container do not affect other containers or the host.

5. **UTS (UNIX Time-sharing System) Namespace:**
   - The UTS namespace allows each container to have its own hostname and domain name. This is what allows you to set a container-specific hostname that is isolated from the host and from other containers.

6. **User Namespace:**
   - User namespaces isolate the user and group ID number spaces. This means that a process's user and group IDs can be different inside and outside a user namespace. This is key for securely mapping host user and group IDs to container user and group IDs.
   - It allows for the root user in a container to be mapped to a non-root user on the host, which is a significant security improvement.

7. **Cgroup Namespace (Linux 4.6 and later):**
   - Cgroup namespaces virtualize the view of the cgroup hierarchy. With cgroup namespaces, each namespace can have its own set of cgroup roots, which isolates its view of the cgroup hierarchies.

These namespaces are fundamental to Docker’s ability to create isolated containers. They allow containers to run in isolation from each other and from the host system, providing security and efficiency. 

It's worth noting that Docker manages these namespaces for you, so most of the time you don't need to interact with or think about them directly. However, understanding how they work can be very useful when you are working on advanced container configurations, troubleshooting issues, or considering security implications.