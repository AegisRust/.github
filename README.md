# AegisRust Project

**High-Performance, Rust-Powered DDoS Mitigation Stack for Minecraft & Beyond.**

AegisRustは、RustとeBPF(XDP)を駆使して構築された、次世代の分散型DDoS防御システムです。
L3/L4の高速フィルタリングから、Minecraftプロトコル(L7)の深い解析までを統合し、圧倒的なスループットと安定性を提供します。

---

## Our Architecture

AegisRustは、役割ごとに最適化された3つの主要コンポーネントで構成されています。

### [AegisRust-Edge (The Shield)](https://github.com/AegisRust/AegisRust-Edge)
- **Layer:** L3 / L4 (XDP/eBPF)
- **Role:** 最前線でのパケット爆撃をミリ秒以下の遅延で処理。
- **Tech:** Rust + Aya, XDP, eBPF Maps.

### [AegisRust-Gaze (The Eye)](https://github.com/AegisRust/AegisRust-Gaze)
- **Layer:** L7 (Minecraft Protocol)
- **Role:** パケットの中身を解析し、ログインボットやプロトコル攻撃を検知。
- **Tech:** Rust + Tokio, Zero-copy parsing.

### [AegisRust-Core (The Brain)](https://github.com/AegisRust/AegisRust-Core)
- **Role:** システム全体の司令塔。ノード管理、統計収集、BANポリシーの配信。
- **Tech:** Rust + Tonic (gRPC), PostgreSQL/ClickHouse.

---

## 🛠️ Technology Stack

| Category | Technology |
| :--- | :--- |
| **Language** | ![Rust](https://img.shields.io/badge/rust-%23E32F26.svg?style=flat&logo=rust&logoColor=white) |
| **Networking** | eBPF (XDP), gRPC, Tokio |
| **OS** | ![AlmaLinux](https://img.shields.io/badge/AlmaLinux-84D4E1?style=flat&logo=almalinux&logoColor=white) (RedHat family) |
| **Spec** | Protocol Buffers (Shared across all nodes) |

---

## 📅 Roadmap

- [x] **Phase 1: Foundation** - Define [AegisRust-Spec](https://github.com/AegisRust/AegisRust-Spec).
- [ ] **Phase 2: Core & Edge** - Implement basic gRPC signaling and XDP dropping.
- [ ] **Phase 3: Gaze** - Deep packet inspection for Minecraft Handshake.
- [ ] **Phase 4: Dashboard** - Real-time attack visualization.

---


<p align="center">  
  <i>"Building a shield that never rusts."</i>
</p>
