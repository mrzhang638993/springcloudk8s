FROM openjdk:8
MAINTAINER allen xcp.email@gmail.com

VOLUME /tmp
ADD target/eureka-1.0-SNAPSHOT.jar app.jar

# 设置时区
ENV JAVA_OPTS="-Duser.timezone=Asia/Shanghai -Djava.security.egd=file:/dev/./urandom"
EXPOSE 7000
ENV APP_OPTS=""
# ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar /app.jar $APP_OPTS"]