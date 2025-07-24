# ahc_cpp
pahcer、atcoder libraryを備えたc++環境構築のためのDockerコンテナです。

こんな感じのディレクトリ構成を想定しています

└── ahc_cpp
    ├── .devcontainer
    │   ├── Dockerfile
    │   └── docker-compose.yml
    └── work
        └── ahc000
            ├── main.py
            ├── pahcer_config.toml
            ├── pacher
            │   └── summary.mdなどテスト結果
            └── tools
                ├── src
                └── in


ビルド・起動コマンド

docker compose -f .devcontainer/docker-compose.yml build
docker compose -f .devcontainer/docker-compose.yml run --rm dev bash