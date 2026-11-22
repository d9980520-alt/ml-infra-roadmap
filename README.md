# ML Infra Roadmap

I'm 15. Building a complete foundation from high-load Go backend and cloud infrastructure to GPU clusters and ML inference/training systems.

## Base — Backend & Platform

### Go Internals & Concurrency
- GMP scheduler (`G`, `M`, `P`), work-stealing, `syscall`, `netpoller`
- Channels (buffered, unbuffered, `select`, `hchan`), worker pools
- `sync` primitives (`Mutex`, `RWMutex`, `WaitGroup`, `Once`, `atomic`, `sync.Pool`)
- Escape analysis, memory layout, Garbage Collector (tri-color mark-and-sweep, `GOGC`, `GOMEMLIMIT`)
- Profiling & benchmarking: `pprof` (CPU, heap, goroutine, block), `go test -bench` + `benchstat`, execution `trace`

### Databases & Caching
- PostgreSQL internals: MVCC, WAL, vacuum/autovacuum, isolation levels, locks (`FOR UPDATE SKIP LOCKED`)
- Indexing (B-Tree, Hash, GIN, BRIN, covering/partial indexes), query planning (`EXPLAIN ANALYZE`)
- Connection pooling (`pgx/v5`, PgBouncer), keyset pagination (`UUIDv7`), idempotency (`ON CONFLICT`), partitioning
- Redis internals: event loop, data structures, persistence (RDB/AOF), eviction policies, pipelining, distributed locks, cache patterns

### Messaging, RPC & Containers
- gRPC & Protobuf: HTTP/2 framing, unary & bidirectional streaming, interceptors, deadlines, load balancing
- Apache Kafka: partitions, consumer groups, offsets, ISR, replication, producer acks, Transactional Outbox
- Docker: multi-stage builds, distroless/scratch images, layer caching, networking, volumes

### System Design Basics
- Load balancing (L4/L7), reverse proxies, API gateways, rate limiting, circuit breakers, retries with jitter
- Caching strategies, sharding, replication (sync/async), CAP/PACELC theorems, consistent hashing

### Kubernetes & GitOps
- K8s architecture: control plane, kubelet, etcd, Pods, Deployments, StatefulSets, DaemonSets, Jobs
- Networking & scheduling: Services, Ingress, NetworkPolicies, HPA/VPA, PDB, taints/tolerations, affinity
- Helm charts, Kustomize, ArgoCD (GitOps), CI/CD pipelines (GitHub Actions)

### Observability
- Metrics: Prometheus, PromQL, RED/USE methodologies, Grafana dashboards & alerting
- Logging: structured logging (`slog`), log aggregation (Loki / ELK)
- Distributed tracing: OpenTelemetry, context propagation, Jaeger / Tempo

### Infrastructure as Code & Security
- Terraform / OpenTofu: state management, modules, workspaces, drift detection
- Secrets management (Vault, External Secrets), RBAC, mTLS, TLS/PKI, container image scanning, supply chain security

### Cloud, Networking & Storage
- Linux networking stack: TCP/IP, DNS, BGP, iptables/nftables, eBPF/XDP networking (Cilium), Envoy
- Storage systems: block vs object storage (S3/MinIO), NVMe-oF, distributed filesystems (Ceph, Lustre), CSI drivers
Repository: [backend-go](https://github.com)
---

## ML / AI Infrastructure

### Linux Kernel & eBPF Deep Dive
- Kernel architecture: syscalls, virtual memory, page cache, `mmap`, `io_uring`, `epoll`, cgroups v2, namespaces
- eBPF: verifier, maps, kprobes/uprobes, tracepoints, XDP, Cilium/Tetragon observability & security

### Container Runtime Internals
- OCI specifications, `runc`, `containerd`, `shim`, rootless containers, overlayfs, cgroups resource isolation
- NVIDIA Container Toolkit (`nvidia-container-runtime`), GPU device plugins in Kubernetes

### Distributed Systems Deep Dive
- Consensus algorithms (Raft, Paxos), distributed transactions (2PC, Saga), vector clocks, CRDTs
- Fault tolerance, leader election, distributed coordination (etcd), backpressure, tail-latency optimization

### Math & PyTorch Internals
- Linear algebra (tensors, matmul, GEMM, SVD, attention mechanics), calculus & optimization (SGD, AdamW, mixed precision FP16/BF16/FP8)
- PyTorch internals: Autograd, Dispatcher, ATen, `torch.compile` (TorchDynamo, AOTAutograd, TorchInductor), memory allocator

### GPU Programming (CUDA & Triton)
- GPU hardware architecture: SMs, warps, threads/blocks, global/shared/register memory, memory coalescing, bank conflicts
- CUDA C++ kernels, streams, async execution, cuBLAS/cuDNN, profiling with Nsight Systems & Nsight Compute
- OpenAI Triton: writing fused kernels (fused softmax, FlashAttention concepts) in Python

### LLM Inference & Serving
- Transformer inference mechanics: prefill vs decode phases, KV-cache, PagedAttention, continuous batching, speculative decoding
- Quantization (AWQ, GPTQ, FP8, INT8/INT4), tensor & pipeline parallelism for inference
- Serving engines: vLLM, TensorRT-LLM, NVIDIA Triton Inference Server, dynamic batching, prefix caching

### Distributed Training
- Parallelism strategies: Data Parallelism (DDP), Fully Sharded Data Parallel (FSDP / ZeRO-1/2/3), Tensor Parallelism (TP), Pipeline Parallelism (PP), Sequence/Context Parallelism
- Collective communication: NCCL, AllReduce, AllGather, ReduceScatter, All-to-All, NVLink, InfiniBand / RoCE

### GPU Clusters & MLOps
- GPU cluster management: DCGM metrics, GPU health checks, ECC errors, MIG, time-slicing
- Experiment tracking, model registries, feature stores, data versioning, automated training/evaluation pipelines

### ML Schedulers & Orchestration
- Batch & gang scheduling: Kueue, Volcano, YuniKorn, Slurm
- Fractional GPU sharing, topology-aware scheduling (NVLink/NUMA), spot instance preemption & checkpointing

### Advanced ML System Design & Open Source
- End-to-end ML platform architecture: multi-tenant inference gateways, token-based rate limiting, model routing, autoscaling on GPU/KV-cache metrics
- Contributing to open-source ML/Cloud infrastructure (Kubernetes, vLLM, Kueue, Cilium, PyTorch)

---

## Daily log

`docs/daily-log`
