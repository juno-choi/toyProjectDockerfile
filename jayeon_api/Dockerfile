FROM openjdk:11-ea-27-jdk

# 개발자 정보
MAINTAINER "ililil9482@naver.com"

# 컨테이너 실행시 실행할 멸령어
RUN mkdir project
RUN wget https://services.gradle.org/distributions/gradle-7.4-rc-2-bin.zip -P /tmp
RUN unzip -d /opt/gradle /tmp/gradle-*.zip

# 작업 데렉터리 변경
WORKDIR /project

RUN git clone https://github.com/juno-choi/jayeon-api.git

WORKDIR /project/jayeon-api
RUN /opt/gradle/gradle-7.4-rc-2/bin/gradle build
WORKDIR /project/jayeon-api/build/libs

ENTRYPOINT ["java"]
CMD ["-jar", "jayeon-0.0.1-SNAPSHOT.jar"]

