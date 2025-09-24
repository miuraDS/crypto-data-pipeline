FROM python:3.10-slim

# タイムゾーン設定
ENV TZ=Asia/Tokyo
RUN apt-get update && apt-get install -y tzdata && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリを /app に設定
WORKDIR /app

# 必要なパッケージをインストール
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# バージョン固定スクリプトだけコピー（差し替えやすい）
COPY backtest_ETH_Bot_0529_v67_bestparams_v2.py .

# デフォルトコマンド（docker-compose.yml の command: が上書きするのでここでは任意）
CMD ["python", "backtest_ETH_Bot_0529_v67_bestparams_v2.py"]
