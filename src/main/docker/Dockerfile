FROM java
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
COPY dockermvn-0.0.1-SNAPSHOT.jar /dockermvn.jar
COPY boot.sh /boot.sh
RUN sed -i 's/\r$//' /boot.sh
RUN chmod +x /boot.sh
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "/boot.sh" ]