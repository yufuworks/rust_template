# 初期設定は1.59-busterだがコンテナがコンパイルエラー
# FROM rust:1.59-buster
# latestだとコンパイルが通る。git使用不能。
# FROM rust:latest
# VSCodeのデフォルトイメージを移植、コンパイル成功。
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/rust:0-${VARIANT}

RUN apt-get update && \
    apt-get -y install git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
