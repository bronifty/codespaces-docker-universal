FROM  mcr.microsoft.com/vscode/devcontainers/universal:1-linux
RUN sudo apt-get update && export DEBIAN_FRONTEND=noninteractive \
&& curl -sSL install.astronomer.io | sudo bash -s \
&& sudo pip install apache-airflow-providers-dbt-cloud==2.0.0

WORKDIR /workspace
COPY . .
# CMD astro dev start