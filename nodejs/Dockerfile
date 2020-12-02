FROM jenkins/agent:latest
USER root
ENV NODE_VERSION 14.15.0
RUN wget -O node-v$NODE_VERSION-linux-x64.tar.gz "https://npm.taobao.org/mirrors/node/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.gz" \
	&& tar -xzvf node-v$NODE_VERSION-linux-x64.tar.gz -C /usr/share \
	&& echo "export PATH=/usr/share/node-v$NODE_VERSION-linux-x64/bin:$PATH" >> /etc/profile \
	&& source /etc/profile
ENTRYPOINT ["java", "-jar", "/usr/share/jenkins/agent.jar"]