FROM ubuntu:20.04

# Install vscode
RUN apt-get update && apt-get install -y wget
RUN wget -O- https://aka.ms/install-vscode-server/setup.sh | sh

# Entrypoint
ENTRYPOINT  ["/usr/local/bin/code-server", "serve-local", "--accept-server-license-terms", "--host", "0.0.0.0", "--server-data-dir", "/srv/code-server", "--without-connection-token"]