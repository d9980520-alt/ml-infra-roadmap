# Learning Plan

## Phase 1 — Backend / Platform

### List 1 — Go internals
GMP, escape analysis, GC, hchan
pprof, benchmark, trace, sync.Pool

### List 2 — Databases and caching
PostgreSQL: indexes, EXPLAIN, MVCC
Redis, cache-aside

### List 3 — Architecture and infra
gRPC streaming, interceptors
Kafka, Docker, Kubernetes, Helm
CI/CD, ArgoCD

### List 4 — Performance
pprof (CPU, heap, trace)
benchstat, vegeta, wrk, k6

### List 5 — Observability
Prometheus, Grafana, OTel
Jaeger, Tempo, Loki
SLI/SLO/SLA

### List 6 — Linux and eBPF
cgroups v2, namespaces
eBPF, bpftrace, XDP

### List 7 — Distributed systems
Raft, Paxos, CRDT
CAP, Saga, consistent hashing

### List 8 — IaC and security
Terraform, Pulumi, Ansible
TLS, mTLS, Vault, RBAC

### List 9 — Container runtime
namespaces, cgroups, overlayfs
runc-like runtime

## Phase 2 — ML / AI Infra

### List 10 — Triton and GPU kernels
Triton, CUDA C
Shared memory, warp primitives

### List 11 — PyTorch internals
autograd, tensor, backprop
CUDA integration

### List 12 — Data engine
Arrow, Parquet, Iceberg
Feature Store, Feast
Kafka Streams, Flink, Spark

### List 13 — GPU orchestration
K8s GPU, device plugin, MIG
Triton Inference Server, vLLM
KServe, Seldon

### List 14 — Nsight and GPU profiling
Nsight Compute, Nsight Systems
Bottleneck analysis

### List 15 — CUDA / Triton
CUDA, cuBLAS, cuDNN
Kernel optimization

### List 16 — Distributed training
DDP, FSDP, DeepSpeed, Megatron-LM
NCCL, NVLink, InfiniBand

### List 17 — LLM inference
vLLM, TensorRT-LLM, SGLang
PagedAttention, quantization

### List 18 — MLOps and open-source
MLflow, Kubeflow, Feast
TensorRT, ONNX
PRs to vLLM, PyTorch, Triton, Ray
