FROM openjdk:11
LABEL maintainer="shchoi<shchoi@iei.or.kr>"
LABEL version="1.0"
# /root 디렉터리에 05_SpringBoot_MVC-0.0.1-SNAPSHOT.jar 파일을 복사
ADD 05_SpringBoot_MVC-0.0.1-SNAPSHOT.jar /root
# docker build 명령어 실행 시 값을 전달 받을 수 있는 변수 선언(기본값 dev)
ARG PROFILE=dev
# docker build 명령어 실행 시 값을 전달 받을 수 있는 PORT 변수 선언 (기본값 8088)
ARG PORT=8088
ENV TZ = Asia/Seoul
# ARG는 이미지 빌드 시에만 적용되고 실제 컨테이너에서는 사용할 수 없기 때문에 입력 받은 값을 ENV를 통해서 전달한다.
ENV PROFILE=${PROFILE}
# 작업 디렉터리를 /root로 변경
WORKDIR /root
# PORT 변수의 값으로 컨테이너에서 사용할 포트를 지정한다
EXPOSE ${PORT}
# 컨테이너 생성 시 05_SpringBoot_MVC-0.0.1-SNAPSHOT.jar 파일을 자동으로 실행 
CMD ["java", "-jar", "05_SpringBoot_MVC-0.0.1-SNAPSHOT.jar", "--srping.profiles.active=${PROFILE}"]