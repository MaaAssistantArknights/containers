FROM node:lts as BUILD

USER root

# 移除不必要的提示
RUN rm -f /etc/update-motd.d/60-unminimize

# 安装必要的工具
RUN apt update
RUN DEBIAN_FRONTEND=noninteractive DEBIAN_PRIORITY=critical apt install -y -o "Dpkg::Options::=--force-confold" --no-install-recommends curl ca-certificates git
RUN curl https://dl.min.io/client/mc/release/linux-amd64/mc -o /root/mc && chmod +x /root/mc
RUN cd /root && git clone --depth 1 https://github.com/MaaAssistantArknights/MaaRelease.git
RUN cd /root/MaaRelease/scripts && npm run ciInCI


FROM node:lts-alpine

# 复制文件
COPY --from=BUILD /root/mc /root/mc
COPY --from=BUILD /root/MaaRelease/scripts /root/MaaRelease/scripts

# 安装必要的工具
RUN apk add --no-cache git uuidgen python3
RUN ls -lh /root/MaaRelease
RUN ls -lh /root/MaaRelease/scripts
