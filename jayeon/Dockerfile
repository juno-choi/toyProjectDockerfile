FROM node

# 개발자 정보
MAINTAINER "ililil9482@naver.com"

# 컨테이너 실행시 실행할 멸령어
RUN mkdir project
RUN npm install -g pm2
# 작업 데렉터리 변경
WORKDIR /project

RUN git clone https://github.com/juno-choi/jayeon-front.git

WORKDIR /project/jayeon-front
RUN npm install
WORKDIR /project/jayeon-front/bin
ENTRYPOINT ["pm2"]
CMD ["start", "--no-daemon", "www"]

