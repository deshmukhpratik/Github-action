FROM calantic-docker-release-local.artifactory.bayer.com/calantic-java-base
WORKDIR /home

ARG ARTIFACT_NAME=orchestrator-service
ARG VERSION=*
ENV revision=$VERSION
ENV artifact_name=$ARTIFACT_NAME
# Need revision variable to be set as this is being used in other Java Application logging


COPY service/target/$ARTIFACT_NAME-$VERSION.jar  /home/app/$ARTIFACT_NAME.jar



EXPOSE 8080
ENTRYPOINT  ["/home/app/entrypoint.sh"]
