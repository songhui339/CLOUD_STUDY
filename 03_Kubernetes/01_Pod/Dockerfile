FROM tomcat:8.5.72-jdk8
WORKDIR /usr/local/tomcat/webapps
RUN pwd
# 작업 디렉터리에 ROOT 디렉터리 생성
RUN mkdir ./ROOT
ADD index.jsp ./ROOT
ENV TZ=Asia/Seoul
EXPOSE 8080
CMD [ "catalina.sh", "run" ]