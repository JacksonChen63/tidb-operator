FROM ghcr.io/pingcap-qe/bases/pingcap-base:v1.9.2

ARG TARGETARCH
RUN dnf install -y tzdata bind-utils && dnf clean all
RUN dnf install -y pam-1.5.1-22.el9_5 openssl-1:3.2.2-6.el9_5.1 && dnf update -y pam openssl
ADD bin/${TARGETARCH}/tidb-scheduler /usr/local/bin/tidb-scheduler
ADD bin/${TARGETARCH}/tidb-discovery /usr/local/bin/tidb-discovery
ADD bin/${TARGETARCH}/tidb-controller-manager /usr/local/bin/tidb-controller-manager
ADD bin/${TARGETARCH}/tidb-admission-webhook /usr/local/bin/tidb-admission-webhook
