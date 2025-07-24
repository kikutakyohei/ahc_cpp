# ahc_cpp

AtCoder Heuristic Contest (AHC) 向けの **C++ + AtCoder Library + pahcer** 開発環境を Docker で再現します。  
VS Code Dev Containers / Docker Compose でそのまま使えます。

---

## 特徴

- **C++ (gcc/clang)** ビルド環境完備  
- **AtCoder Library (ACL)** を `/usr/local/include/atcoder` に配置済み → `#include <atcoder/all>`  
- **pahcer**（提出用展開ツール）導入済み  
- Python3 / pip など補助ツールも同梱（不要なら削除可）  
- すべて root ユーザー前提のシンプル構成

---

## 使い方

### 0. 前提

- Docker / Docker Compose v2  
- （任意）VS Code + Dev Containers 拡張機能

### 1. ビルド

```bash
cd ahc_cpp
docker compose -f .devcontainer/docker-compose.yml build
