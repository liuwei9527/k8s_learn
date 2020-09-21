FROM python:3.6.8-slim

RUN echo "deb http://mirrors.aliyun.com/debian/ buster main non-free contrib" > /etc/apt/sources.list \
    && apt update \
    && apt-get install -y gcc python3-dev \
    && python -m pip install --upgrade pip \
    && pip install bzt -i https://pypi.tuna.tsinghua.edu.cn/simple \
    && apt install -y apt-transport-https ca-certificates wget dirmngr gnupg software-properties-common \
    && wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | apt-key add - \
    && add-apt-repository --yes https://adoptopenjdk.jfrog.io/adoptopenjdk/deb/ \
    && apt-get update \
    && apt-get install -y adoptopenjdk-8-hotspot