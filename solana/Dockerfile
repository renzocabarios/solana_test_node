
# Build the image:
#   docker build . -t solana-validator-docker
# Run a basic container:
#   docker run --rm -it --init solana-validator-docker:latest
# Run the solana-test-validator and expose port 8899:
#   docker run --rm -it --init -p 8899:8899 solana-validator-docker:latest solana-test-validator
#
# Based on Ubuntu 22.04 LTS (Jammy)
FROM ubuntu:jammy
WORKDIR /root
RUN apt -y update && apt -y install curl bzip2
RUN sh -c "$(curl -sSfL https://release.solana.com/v1.18.17/install)"
RUN ls
ENV PATH="/root/.local/share/solana/install/active_release/bin:${PATH}"

EXPOSE 8899
EXPOSE 1024
EXPOSE 8900

CMD ["solana-test-validator"]

# TEST