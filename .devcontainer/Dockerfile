# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.222.0/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version (use hirsuite or bionic on local arm64/Apple Silicon): hirsute, focal, bionic
ARG VARIANT="bionic"
FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
  && apt-get -y install --no-install-recommends gettext-base=0.19.8.1-6ubuntu0.3 \
  && apt-get -y install python3 nodejs npm \
  && rm -rf /var/lib/apt/lists/* \
  && python -m ensurepip --upgrade \
  && pip install --no-cache-dir urllib3==1.26.15
