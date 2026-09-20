 ROADMAP

Detailed plan for each list.

## List 1 — Go internals
- GMP, escape analysis, GC, hchan
- pprof, benchmark, trace, sync.Pool
- Project: my own goroutine scheduler

## List 2 — databases and caching
- PostgreSQL: indexes, EXPLAIN, MVCC
- Redis, cache-aside
- Project: service with cache

## List 3 — architecture and infra
- gRPC streaming, interceptors
- Kafka, Docker, Kubernetes, Helm
- CI/CD, ArgoCD

## List 4 — Triton and GPU kernels
- Triton, CUDA C
- shared memory, warp primitives

## List 5 — performance
- pprof (CPU, heap, trace)
- benchstat, vegeta, wrk, k6

## List 6 — PyTorch internals
- autograd, tensor, backprop
- CUDA integration

## List 7 — observability
- Prometheus, Grafana, OTel
- Jaeger, Tempo, Loki
- SLI/SLO/SLA

## List 8 — data engine
- Arrow, Parquet, Iceberg
- Feature Store, Feast
- Kafka Streams, Flink, Spark

## List 9 — GPU orchestration
- K8s GPU, device plugin, MIG
- Triton Inference Server, vLLM
- KServe, Seldon

## List 10 — ML scheduler
- Go + Python + gRPC + Kafka + K8s + CUDA
- Flagship project

## List 11 — Nsight and GPU profiling
- Nsight Compute, Nsight Systems
- Bottleneck analysis

## List 12 — Ray
- Ray, Ray Data, Ray Train, Ray Serve

## List 13 — CUDA / Triton
- CUDA, cuBLAS, cuDNN
- Kernel optimization

## List 14 — distributed training
- DDP, FSDP, DeepSpeed, Megatron-LM
- NCCL, NVLink, InfiniBand

## List 15 — LLM inference
- vLLM, TensorRT-LLM, SGLang
- PagedAttention, quantization

## List 16 — MLOps
- MLflow, Kubeflow, Feast

## List 17 — TensorRT, ONNX
- Graph optimization, quantization

## List 18 — open-source
- PRs to vLLM, PyTorch, Triton, Ray

## Flagships

### ML Scheduler
Combines lists 1–15: Go + Python + gRPC + K8s + CUDA.

### Mini Runtime
My own container runtime.
