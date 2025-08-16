FROM nvidia/cuda:12.4.1-cudnn-runtime-ubuntu22.04
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y \
    python3 python3-pip python3-venv git curl ca-certificates \
    && rm -rf /var/lib/apt/lists/*
RUN python3 -m pip install --upgrade pip
RUN pip install --no-cache-dir \
    kaggle jupyterlab ipykernel \
    numpy pandas scipy scikit-learn \
    matplotlib seaborn plotly lightgbm xgboost catboost \
    torch torchvision --index-url https://download.pytorch.org/whl/cu124