# Awesome WebAssembly Runtimes

[![English](https://img.shields.io/badge/Language-English-gray)](README.md) [![Chinese](https://img.shields.io/badge/Language-中文-blue)](#)

> **说明**：本仓库维护主要运行时的静态功能列表。如需查看实时性能基准测试（冷启动时间、内存占用、吞吐量）和交互式筛选，请访问 **[WasmRuntime.com 仪表盘](https://wasmruntime.com)**。

---

## 运行时矩阵 (Top 5)

当前最主流的 WebAssembly 运行时精选。

| 运行时 | 语言 | 协议 | 关键特性 | 最佳场景 |
| :--- | :---: | :---: | :--- | :--- |
| **[Wasmtime](https://wasmtime.dev/)** | Rust | Apache-2.0 | • WASI Preview 2<br>• Component Model | **标准合规 & 安全**<br>服务端、云原生标准首选 |
| **[Wasmer](https://wasmer.io/)** | Rust | MIT | • WASIX 标准<br>• 可插拔引擎 | **通用性 & 多语言**<br>支持"随处运行" |
| **[WasmEdge](https://wasmedge.org/)** | C++ | Apache-2.0 | • AI 插件 (TF/PyTorch)<br>• Kubernetes 兼容 | **AI 推理 & 边缘计算**<br>高性能边缘计算场景 |
| **[wazero](https://wazero.io/)** | Go | Apache-2.0 | • 零 CGO<br>• 纯 Go 实现 | **Go 语言集成**<br>跨平台 Go 应用 |
| **[WAMR](https://github.com/bytecodealliance/wasm-micro-runtime)** | C | Apache-2.0 | • Intel SGX 支持<br>• 多种执行模式 | **IoT & 嵌入式**<br>极小体积，适合低配硬件 |

[查看包含 15+ 运行时的完整性能排行榜 →](https://wasmruntime.com)

---

## 语言选型指南

### Go 开发者
*   **推荐**: **wazero**
*   **理由**: 它是唯一成熟的 **零 CGO** 运行时，完美解决交叉编译痛点。[查看编译速度对比](https://wasmruntime.com)

### Python 开发者
*   **推荐**: **Wasmer** (通用) 或 **WasmEdge** (AI)
*   **理由**: Wasmer 安装最简单；WasmEdge 支持 AI 硬件加速，具有更低的 [AI 推理延迟](https://wasmruntime.com)。

### Rust 开发者
*   **推荐**: **Wasmtime**
*   **理由**: WASI Preview 2 和组件模型 (Component Model) 支持的黄金标准。

---

## 核心场景推荐

### Serverless (无服务器)
WebAssembly 冷启动速度远超 Docker 容器。
*   **推荐**: **Spin (by Fermyon)**
*   **特点**: 亚毫秒级冷启动。[查看 vs AWS Lambda 数据](https://wasmruntime.com)

### AI Inference (AI 推理)
使用可移植二进制运行 LLM 和 ML 模型。
*   **推荐**: **WasmEdge**
*   **特点**: 支持直接调用底层 GPU/NPU 资源。

---

## 对比总结

基于 [WasmRuntime.com 基准测试](https://wasmruntime.com) 的实测数据：
*   **冷启动**: Wasm 比 Docker 快 10-50 倍。
*   **密度**: Wasm 单机实例密度高 50 倍以上。
*   **安全**: 进程级沙箱 (基于 Capability 的安全模型)。

---

## 贡献与反馈

本列表由 **WasmRuntime.com** 团队维护。
发现错误？请提交 PR 或访问主站查看最新数据。
