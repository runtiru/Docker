FROM amazoncorretto:11-alpine3.17
LABEL author="Runner"
LABEL organization="gamezoneworld"
ARG HOME_DIR=/spc
ARG uid=1001
ARG user=spring
ARG group=spring
RUN adduser -h ${HOME_DIR} -s /bin/sh -D -u ${uid} ${user}
USER ${user}
WORKDIR ${HOME_DIR}
ADD --chown=${user}:${group} https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/spring-petclinic-2.4.2.jar ${HOME_DIR}/spring-petclinic-2.4.2.jar
EXPOSE 8080
CMD ["java", "-jar", "spring-petclinic-2.4.2.jar"]

