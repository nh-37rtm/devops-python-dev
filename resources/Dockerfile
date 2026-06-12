FROM devops-base as devops-python-dev

ENV VIRTUAL_ENV=/opt/python/venv

# tools for debug
RUN apt-get install -y --no-install-recommends \
    sudo curl iputils-ping iproute2

RUN apt-get install -y --no-install-recommends \
    python3 python3-venv python3-pip

RUN mkdir -p ${VIRTUAL_ENV} && \
    chown -R ${APP_USER}:${APP_USER} ${VIRTUAL_ENV}

RUN usermod -aG sudo ${APP_USER} && \
    passwd --delete ${APP_USER}

USER ${APP_USER}:${APP_USER}

RUN python3 --version && \
    python3 -m venv ${VIRTUAL_ENV}
