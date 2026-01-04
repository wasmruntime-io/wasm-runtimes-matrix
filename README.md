# Awesome WebAssembly Runtimes

[![English](https://img.shields.io/badge/Language-English-blue)](#) [![Chinese](https://img.shields.io/badge/Language-中文-gray)](README.zh.md)

> **Note**: This repository maintains a static feature matrix. For real-time performance benchmarks (Cold Start, Memory, Throughput) and interactive filtering, please visit the **[WasmRuntime.com Dashboard](https://wasmruntime.com)**.

---

## Runtime Matrix (Top 5)

A curated list of the most popular WebAssembly runtimes.

| Runtime | Language | License | Key Features | Best For... |
| :--- | :---: | :---: | :--- | :--- |
| **[Wasmtime](https://wasmtime.dev/)** | Rust | Apache-2.0 | • WASI Preview 2<br>• Component Model | **Standard Compliance**<br>Security, Server-side |
| **[Wasmer](https://wasmer.io/)** | Rust | MIT | • WASIX Standard<br>• Pluggable Engines | **Universal Usage**<br>Running "Anything" anywhere |
| **[WasmEdge](https://wasmedge.org/)** | C++ | Apache-2.0 | • AI Plugins (TF/PyTorch)<br>• Kubernetes Compatible | **AI Inference & Edge**<br>High-perf Edge Computing |
| **[wazero](https://wazero.io/)** | Go | Apache-2.0 | • Zero CGO<br>• Pure Go Implementation | **Go Integration**<br>Cross-platform Go Apps |
| **[WAMR](https://github.com/bytecodealliance/wasm-micro-runtime)** | C | Apache-2.0 | • Intel SGX Support<br>• Multiple Execution Modes | **IoT & Embedded**<br>Minimum footprint |

[View full 15+ runtime leaderboard with performance data →](https://wasmruntime.com)

---

## Quick Selection Guide

### Go Developers
*   **Recommendation**: **wazero**
*   **Why**: It is the only mature runtime that requires **Zero CGO**, solving cross-compilation pain points. [Compare compilation speeds here](https://wasmruntime.com).

### Python Developers
*   **Recommendation**: **Wasmer** (General) or **WasmEdge** (AI)
*   **Why**: Wasmer has the easiest pip install; WasmEdge supports native AI hardware acceleration for [lower inference latency](https://wasmruntime.com).

### Rust Developers
*   **Recommendation**: **Wasmtime**
*   **Why**: The gold standard for WASI Preview 2 and Component Model support.

---

## Top Use Cases

### Serverless
WebAssembly cold starts are significantly faster than Docker containers.
*   **Recommendation**: **Spin (by Fermyon)**
*   **Feature**: Sub-millisecond cold starts. [See benchmarks vs AWS Lambda](https://wasmruntime.com).

### AI Inference
Run LLMs and ML models with portable binaries.
*   **Recommendation**: **WasmEdge**
*   **Feature**: Direct GPU/NPU access via plugins.

---

## Comparison Summary

Based on [WasmRuntime.com benchmarks](https://wasmruntime.com):
*   **Cold Start**: Wasm is 10-50x faster than Docker.
*   **Density**: Wasm allows 50x more instances per server.
*   **Security**: Process-level sandboxing (Capability-based).

---

## Contribution

Maintained by the **WasmRuntime.com** team.
Found a mistake? Submit a PR or check the site for the latest data.
