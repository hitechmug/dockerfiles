FROM openjdk:8u102-jdk


# Installs Android SDK  
ENV ANDROID_SDK_URL http://dl.google.com/android/android-sdk_r24.4.1-linux.tgz
ENV ANDROID_API_LEVELS android-23,android-24
ENV ANDROID_XTRAS extra-android-m2repository,extra-google-m2repository
ENV ANDROID_BUILD_TOOLS_VERSION 21.1.0
ENV ANDROID_HOME /opt/android-sdk-linux
ENV PATH ${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/platform-tools

RUN cd /opt && \
 curl ${ANDROID_SDK_URL} | tar xz  && \
 echo y | android update sdk --no-ui -a --filter tools,platform-tools,${ANDROID_API_LEVELS},${ANDROID_XTRAS},build-tools-${ANDROID_BUILD_TOOLS_VERSION} --no-https 

