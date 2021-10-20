FROM docker.io/fedora:34
RUN dnf install -y pandoc-pdf texlive-euenc texlive-fontspec texlive-mathspec texlive-mdwtools && dnf clean all
ENV HOME=/tmp
ENTRYPOINT ["/usr/bin/pandoc"]
