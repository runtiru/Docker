FROM alpine:3 As Tiru
ARG DOWNLOAD_URL="https://github.com/nopSolutions/nopCommerce/releases/download/release-4.60.4/nopCommerce_4.60.4_NoSource_linux_x64.zip"
ADD ${DOWNLOAD_URL} /jai/nopCommerce_4.60.4_NoSource_linux_x64.zip
RUN apk update && \
    apk add unzip && \
    cd /jai && \
    unzip nopCommerce_4.60.4_NoSource_linux_x64.zip && \
    mkdir bin logs && \
    rm nopCommerce_4.60.4_NoSource_linux_x64.zip

FROM mcr.microsoft.com/dotnet/runtime:7.0
LABEL author="tiru" organization="runner"
COPY --from=Tiru /jai /baby
ENV ASPNETCORE_URLS="http://0.0.0.0:5000"
EXPOSE 5000
WORKDIR /baby
CMD [ "dotnet", "Nop.Web.dll"]