FROM devops-base as devops-python-dev

ENV VIRTUAL_ENV=/opt/python/venv

# tools for debug
RUN apt-get install -y --no-install-recommends \
    sudo curl iputils-ping iproute2

RUN apt-get install -y --no-install-recommends \
    python3 python3-venv python3-pip

RUN python3 --version && \
    python3 -m venv ${VIRTUAL_ENV}

RUN usermod -aG sudo ${APP_USER} && \
    passwd --delete ${APP_USER}

USER ${APP_USER}:${APP_USER}