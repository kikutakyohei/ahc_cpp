markdown# ahc_cpp

AtCoder Heuristic Contest (AHC) 向けの C++ + AtCoder Library + pahcer 開発環境を Docker で再現します。
VS Code Dev Containers / Docker Compose でそのまま使えます。

特徴
C++ (gcc/clang) ビルド環境完備
AtCoder Library (ACL) を /usr/local/include/atcoder に配置済み → #include <atcoder/all>
pahcer（提出用展開ツール）導入済み
Python3/pip など補助ツールも同梱（不要なら削除可）
すべて root ユーザー前提のシンプル構成
想定ディレクトリ構成
ahc_cpp/
├── .devcontainer/
│   ├── Dockerfile
│   └── docker-compose.yml
└── work/
    └── ahc000/
        ├── main.cpp
        ├── pahcer_config.toml
        ├── pacher/
        │   └── summary.md  # テスト結果など
        └── tools/
            ├── src/
            └── in/
work/ 以下は自由に増やしてください（ahc001, abc300 など）。

使い方
0. 前提
Docker / Docker Compose v2
（任意）VS Code + Dev Containers 拡張機能
1. ビルド
bash
cd ahc_cpp
docker compose -f .devcontainer/docker-compose.yml build
2. 実行（シェルに入る）
bash
docker compose -f .devcontainer/docker-compose.yml run --rm dev bash

# コンテナ内で:
g++ -std=gnu++17 -O2 -Wall main.cpp && ./a.out
3. VS Code Dev Container で開く
VS Code でこのリポジトリを開く
コマンドパレットから "Dev Containers: Reopen in Container"
.devcontainer/ の設定に従って自動でビルド＆起動されます
4. pahcer の例
bash
# 設定ファイル pahcer_config.toml を置いておく
pahcer path/to/main.cpp --config pahcer_config.toml
詳細は pahcer の README を参照。

