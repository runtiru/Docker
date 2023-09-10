FROM mcr.microsoft.com/dotnet/sdk:7.0
LABEL author="nop"
ARG DOWNLOAD_LOCATION="https://github.com/nopSolutions/nopCommerce/releases/download/release-4.60.4/nopCommerce_4.60.4_NoSource_linux_x64.zip"
ADD ${DOWNLOAD_LOCATION} /tiru/nopCommerce_4.60.4_NoSource_linux_x64.zip
RUN apk update && \
    apk add unzip && \
    cd /tiru && \
    unzip /nopCommerce_4.60.4_NoSource_linux_x64.zip && \
    mkdir bin logs && \
    rm /nopCommerce_4.60.4_NoSource_linux_x64.zip
WORKDIR /tiru
EXPOSE 5000


