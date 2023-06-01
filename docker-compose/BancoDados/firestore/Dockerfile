FROM google/cloud-sdk:alpine

RUN apk --no-cache update && \
    apk --no-cache add openjdk11-jre && \
    rm -rf /var/cache/apk/*

RUN gcloud components install --quiet beta cloud-firestore-emulator && \
    gcloud components update
#
EXPOSE 8105

#VOLUME /data

ENTRYPOINT ["gcloud", "beta", "emulators", "firestore"]
CMD ["start", "--host-port=0.0.0.0:8105"]