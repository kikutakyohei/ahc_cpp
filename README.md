# ahc_cpp

AtCoder Heuristic Contest (AHC) 向けの C++ + AtCoder Library + pahcer 開発環境を Docker で再現します。  
VS Code Dev Containers / Docker Compose でそのまま使えます。

あとでoptunaとかも入れたいですね

---

## 特徴

- **C++ (gcc/clang)** ビルド環境完備  
- **AtCoder Library (ACL)** を `/usr/local/include/atcoder` に配置済み → `#include <atcoder/all>`  
- **pahcer**（提出用展開ツール）導入済み  
- Python3 / pip など補助ツールも同梱
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
```

### 2. 起動
```bash
docker compose -f .devcontainer/docker-compose.yml run --rm dev bash
```

### 3. pahcerの設定
詳細はpahcerのREADMEを参照してください。
(https://github.com/terry-u16/pahcer/blob/main/README.md)


