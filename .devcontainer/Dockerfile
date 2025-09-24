FROM mcr.microsoft.com/devcontainers/python:3.13-bookworm

# uv を入れる（root の ~/.local/bin に入るので、万人が使えるよう /usr/local/bin へ）
RUN curl -LsSf https://astral.sh/uv/install.sh | sh \
    && mv /root/.local/bin/uv /usr/local/bin/uv
