FROM debian-base as base

RUN sudo apt-get install -y --no-install-recommends \
    python3 python3-venv python3-pip

RUN curl -fsSL https://astral.sh/uv/install.sh | sh
RUN ln -s /opt/scripts/uv.bashrc $HOME/.bashrc.d/uv.bashrc