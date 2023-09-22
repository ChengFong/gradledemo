FROM openjdk:17-jdk-alpine
VOLUME /tmp
ARG DEPENDENCY=target/dependency
COPY ${DEPENDENCY}/BOOT-INF/lib /app/lib
COPY ${DEPENDENCY}/META-INF /app/META-INF
COPY ${DEPENDENCY}/BOOT-INF/classes /app
# example com.sun.test.Application
ENTRYPOINT ["java","-Denv=prod","-cp","app:app/lib/*","com.atguigu.demo.DemoApplication",">","/tmp/console.log"]