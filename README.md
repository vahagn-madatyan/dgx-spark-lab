# DGX Spark Lab

Hands-on machine learning lab built around the NVIDIA DGX Spark (GB10 Grace Blackwell). Training, fine-tuning, and deploying models locally — from first boot to production deployment pipelines.

> **Try it on Perplexity Computer:** [NVIDIA AI Certification Study](https://www.perplexity.ai/computer/a/dgx-spark-training-dashboard-WALc9ax0R4CDxBobo0Mhyg)

## What This Is

A structured, progressive curriculum for getting real hands-on experience with the DGX Spark. Each phase builds on the last, covering infrastructure setup, inference, fine-tuning, custom model training, and multi-node scaling.

## Training Phases

| Phase | Focus | Key Projects |
|-------|-------|-------------|
| **P0** | First Boot & Setup | DGX OS config, NVIDIA AI stack, container runtime |
| **P1** | Inference Basics | Run pre-trained models (Llama, Mistral) via vLLM and TRT-LLM |
| **P2** | Fine-Tuning | LoRA/PEFT fine-tuning, dataset preparation, evaluation |
| **P3** | Custom Training | Train models from scratch (nanochat-style), experiment tracking |
| **P4** | Trading Models | Market data ingestion, labeling, trading-specific model training |
| **P5** | Deployment | HuggingFace model registry → GCP Vertex AI / GKE serving |
| **P6** | Multi-Node | ConnectX-7 dual-Spark scaling, distributed training |

## Architecture

```
Market Data Sources → DGX Spark Lab → Model Registry (HF) → GCP Serving → SaaS & Trading Agents
```

End-to-end pipeline:
- **Data ingestion** — Alpaca, Finnhub, Alpha Vantage for live + historical market data
- **Training loop** — PyTorch, Transformers, TRL on Spark with experiment tracking
- **Model versioning** — Push checkpoints to HuggingFace Hub
- **Deployment** — Serve via vLLM/TRT-LLM on GCP, consume via LangChain in SaaS apps

## Hardware

- **NVIDIA DGX Spark** — GB10 Grace Blackwell superchip
- 128 GB unified LPDDR5x memory
- 6,144 CUDA cores, up to 1 PFLOP FP4
- 4 TB NVMe, ConnectX-7 NIC (200 Gbps)
- Models up to ~200B params (single unit), ~405B (dual linked)

## Certification Coverage

Projects are mapped to NVIDIA certification exam domains:
- **NCA-AIIO** — AI Infrastructure & Operations Associate
- **NCA-GENL** — Generative AI LLMs Associate
- **NCP-GENL** — Generative AI LLMs Professional (future)

## Stack

```
hardware     dgx spark · gb10 grace blackwell
frameworks   pytorch · transformers · trl · vllm · trt-llm
data         alpaca api · finnhub · alpha vantage
ml ops       huggingface hub · weights & biases · mlflow
deployment   gcp vertex ai · gke · langchain
tools        docker · nvidia-smi · nsight · cuda toolkit
```

## License

Apache 2.0
