# Important Docker concepts

__1. Docker Engine__
    1. [[Architecture]]
    2. [[Daemon]]
    .  3. [[Namespaces]]
    4. Control Groups (cgroups)
    5. OCI (Open Container Initiative) Standards
    6. Swarm Mode
    7. Container Lifecycle
    8. Storage Drivers
    9. Networking Drivers
    10. Plugins
    11. Runtime
---------------------------------------------------
 
__2. Docker Images__
    1. Creation
    2. Layers
    3. Tags
    4. Base Image
    5. Child Image
    6. Image Repository
    7. Image Registry (e.g., Docker Hub)
    8. Push/Pull Images
    9. Inspect Images
    10. Remove Images
    11. Image Size Optimization
    12. Image Security Scanning
    13. Image Signing and Verification
    14. Export/Import Images
    15. Image Build Context
---------------------------------------------------

__3. Docker Containers__
    1. Creation
    2. Lifecycle (start, stop, restart)
    3. Management (ps, inspect, rm, etc.)
    4. Logs
    5. Executing Commands
    6. Port Mapping
    7. Volume Mounting
    8. Networking
    9. Environment Variables
    10. Health Checks
    11. Resource Limits (CPU, memory, etc.)
    12. Security (user, privileges)
    13. Inter-container Communication
    14. Container Isolation
    15. Export/Import Containers
    16. Attaching to Running Containers
------------------------------------------
__4. Dockerfile__
    1. Format and Syntax
    2. FROM (Base Image)
    3. RUN (Execute Commands)
    4. CMD (Default Command)
    5. ENTRYPOINT (Executable)
    6. COPY (Copy Files)
    7. ADD (Add Files)
    8. ENV (Environment Variables)
    9. ARG (Build Arguments)
    10. WORKDIR (Working Directory)
    11. EXPOSE (Ports)
    12. VOLUME (Mount Points)
    13. USER (Set User)
    14. LABEL (Metadata)
    15. ONBUILD (Triggers)
    16. Multi-Stage Builds
    17. Best Practices (Optimization, Security)
    18. Build Context
    19. Docker Build Command
    20. dockerignore File
--------------------------------
__5. Docker Compose__
    1. Compose File (docker-compose.yml)
    2. Version Specification
    3. Services Definition
    4. Build Configuration
    5. Container Dependencies
    6. Networking Configuration
    7. Volume Configuration
    8. Environment Variables
    9. Overrides (extends, docker-compose.override.yml)
    10. Command-Line Interface (CLI) Commands (up, down, ps, logs, etc.)
    11. Port Mapping
    12. Scaling Services
    13. Compose Project Name
    14. Health Checks
    15. Resource Limits (CPU, memory, etc.)
    16. Secrets Management
    17. Running in Background (Detached Mode)
    18. Compose Profiles
    19. Compose in Production Environments
    20. Best Practices (File Organization, Security)
--------------------------------------
__6. Docker Hub__
    1. Repositories
    2. Pushing Images
    3. Pulling Images
    4. Image Tags
    5. Public and Private Repositories
    6. Automated Builds
    7. Webhooks
    8. Organizations and Teams
    9. Access Control (permissions)
    10. Official Images
    11. Docker Hub Pricing Plans
    12. Rate Limiting
    13. Security Scanning
    14. Signing Images (Docker Content Trust)
    15. Docker Hub API
    16. Integration with GitHub/GitLab
    17. Image Versioning
    18. Repository Description and Documentation
----------------------------
__7. Docker Networking__
    1. Network Drivers (bridge, host, overlay, macvlan, none)
    2. Bridge Network
    3. Host Network
    4. Overlay Network
    5. Custom User-Defined Networks
    6. Network Isolation
    7. Network Creation and Deletion
    8. Network Inspection
    9. Port Mapping and Exposure
    10. DNS and Service Discovery
    11. Networking in Swarm Mode
    12. Network Security (Firewalls, Encryption)
    13. Network Troubleshooting
    14. Inter-Container Communication
    15. External Communication
    16. Connecting Containers to Multiple Networks
    17. IPv6 in Docker
    18. IP Address Management (IPAM)
    19. Network Performance Tuning
------------------------------------------
__8. Docker Volumes__
    1. Volume Creation and Deletion
    2. Mounting Volumes
    3. Named Volumes
    4. Anonymous Volumes
    5. Host Volumes (Bind Mounts)
    6. Volume Drivers (local, NFS, third-party plugins)
    7. Volume Inspection
    8. Volume Backup and Restore
    9. Volume Sharing between Containers
    10. Volume Pruning
    11. Volume Scope (local, global)
    12. Read-Only Volumes
    13. Volume Options and Configuration
    14. Data Persistence
    15. Data Migration
    16. Security and Permissions
    17. Volume Performance Tuning
---------------------------------
__9. Docker Security__
    1. Container Isolation
    2. Security Profiles (AppArmor, SELinux)
    3. User Namespaces
    4. Capabilities
    5. Secure Computing Mode (seccomp)
    6. Signed Images (Docker Content Trust)
    7. Rootless Mode
    8. Read-Only Containers
    9. Image Scanning and Vulnerability Analysis
    10. Using Minimal Base Images
    11. Network Security (Firewall Rules, Encryption)
    12. Secrets Management
    13. Access Control (RBAC, User Management)
    14. Docker Daemon Security (TLS, Socket, Authorization Plugins)
    15. Audit Logging
    16. Secure Build Pipeline
    17. Host Security Best Practices
    18. Docker Bench for Security
    19. System Call Filtering
    20. Avoid Running Containers as Root
------------------------------
__10. Docker CLI Commands__
    1. `docker run`
    2. `docker build`
    3. `docker ps` (and `docker container ls`)
    4. `docker images` (and `docker image ls`)
    5. `docker exec`
    6. `docker pull`
    7. `docker push`
    8. `docker tag`
    9. `docker rm` (and `docker container rm`)
    10. `docker rmi` (and `docker image rm`)
    11. `docker logs`
    12. `docker volume`
    13. `docker network`
    14. `docker compose`
    15. `docker info`
    16. `docker inspect`
    17. `docker stop` (and `docker start`, `docker restart`)
    18. `docker login` (and `docker logout`)
    19. `docker prune`
    20. `docker top`
    21. `docker cp`
    22. `docker stats`
    23. `docker kill`
    24. `docker update`
    25. `docker swarm`
    26. `docker service`
    27. `docker stack`
    28. `docker node`
    29. `docker secret`
    30. `docker config`
    31. Command Options (e.g., `-d`, `--name`, `--rm`, `--env`, etc.)
-----------------------------------
__11. Building Images__
    1. Dockerfile
    2. `docker build` Command
    3. Build Context
    4. Build Arguments (`ARG`)
    5. Multi-Stage Builds
    6. Build Cache
    7. BuildKit
    8. Image Layers
    9. Image Tags
    10. Base Image Selection
    11. `RUN` Instruction Optimization
    12. Minimizing Image Size
    13. Security Hardening (e.g., Non-Root User)
    14. `.dockerignore` File
    15. Build Secrets
    16. Build Output Formats (OCI, etc.)
    17. Docker Buildx (Extended Build Features)
    18. Remote Build Cache
    19. Building for Different Architectures (e.g., ARM)
    20. Troubleshooting Build Errors
-------------------------------
__12. Managing Containers__
    1. `docker run` Command
    2. Container Lifecycle (start, stop, pause, unpause, restart)
    3. `docker ps` (List Containers)
    4. `docker exec` (Execute Commands in Container)
    5. `docker logs` (View Container Logs)
    6. `docker stop` (and `docker start`, `docker restart`)
    7. `docker rm` (Remove Container)
    8. `docker kill` (Force Stop Container)
    9. `docker inspect` (View Container Metadata)
    10. Port Mapping
    11. Volume Mounting
    12. Environment Variables
    13. `docker stats` (Monitor Container Resources)
    14. `docker top` (View Running Processes in Container)
    15. `docker cp` (Copy Files to/from Container)
    16. Resource Limits (CPU, memory, etc.)
    17. Health Checks
    18. Networking Configuration
    19. Inter-container Communication
    20. Security Options (User, Capabilities, Seccomp, etc.)
    21. Container Isolation
    22. Troubleshooting and Debugging
    23. Attaching to Running Containers
    24. `docker update` (Update Container Configuration)
    25. Container Pruning (`docker container prune`)
    26. Export/Import Containers
    27. Read-Only Containers
----------------------------------------------------
__13. Docker Registry__
    1. Image Storage
    2. Pushing Images
    3. Pulling Images
    4. Authentication and Authorization
    5. Security (TLS, Image Signing)
    6. Docker Hub
    7. Private Registry
    8. Self-Hosted Registry (e.g., Docker Registry 2.0)
    9. Third-Party Registry (e.g., AWS ECR, GCR, Azure ACR, Quay.io)
    10. Image Tags and Versioning
    11. Image Scanning and Vulnerability Detection
    12. Rate Limiting
    13. Webhooks and Notifications
    14. Garbage Collection
    15. Storage Drivers (e.g., S3, Azure Blob Storage)
    16. Catalog API
    17. Registry Configuration and Deployment
    18. Registry Mirroring and Caching
    19. Multi-tenancy Support
    20. Audit Logging and Monitoring
--------------------------------------
__14. Optimizing Dockerfiles__
    1. Multi-Stage Builds
    2. Minimizing Number of Layers
    3. `COPY` and `ADD` Best Practices
    4. Efficient `RUN` Instructions
    5. Build Cache Utilization
    6. `.dockerignore` File
    7. Reducing Image Size
    8. Base Image Selection (e.g., Alpine)
    9. Removing Unnecessary Files
    10. Avoiding Installation of Unnecessary Packages
    11. Combining Commands
    12. Ordering Instructions Effectively
    13. BuildKit and Advanced Build Features
    14. Security Optimization (Non-Root User, No SUID Binaries)
    15. Setting `HEALTHCHECK`
    16. Managing Build Arguments and Environment Variables
    17. Lean and Focused Containers (One Process Per Container)
    18. Compressing Resources
    19. Optimizing for Startup Time
    20. Analyzing and Auditing Images (e.g., using `dive` or other tools)
-------------------------------------
__15. Docker Logging and Monitoring__
    1. Logging Drivers (json-file, syslog, journald, gelf, fluentd, etc.)
    2. `docker logs` Command
    3. Log Rotation and Retention Policies
    4. Centralized Logging Solutions (e.g., ELK Stack, Splunk)
    5. Container Monitoring
    6. `docker stats` Command
    7. Performance Metrics (CPU, Memory, Network, I/O, etc.)
    8. Monitoring Solutions (e.g., Prometheus, Grafana, Datadog)
    9. Docker Swarm and Kubernetes Monitoring
    10. Health Checks (`HEALTHCHECK` instruction)
    11. Alerting and Notifications
    12. Troubleshooting and Debugging
    13. Distributed Tracing (e.g., Jaeger, Zipkin)
    14. Application Performance Monitoring (APM)
    15. Log Aggregation and Analysis
    16. Security Monitoring and Auditing
    17. Custom Metrics
    18. Resource Quotas and Limits
    19. Monitoring APIs and Endpoints
    20. Visualizing Docker Metrics
------------------------------------