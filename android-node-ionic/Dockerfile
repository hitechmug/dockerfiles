FROM android-node
RUN npm install -g cordova ionic && \
    cordova telemetry off
RUN apt-get install lib32stdc++6 lib32z1 -y
RUN mkdir /build
WORKDIR /build
ENTRYPOINT ["ionic", "build", "android"]