FROM alpine:3
ADD https://github.com/nopSolutions/nopCommerce/releases/download/release-4.60.4/nopCommerce_4.60.4_NoSource_linux_x64.zip /jai/
RUN apk update && \
    apk add unzip && \
    cd /jai && \
    unzip nopCommerce_4.60.4_NoSource_linux_x64.zip && \
    mkdir bin logs && \
    rm nopCommerce_4.60.4_NoSource_linux_x64.zip
