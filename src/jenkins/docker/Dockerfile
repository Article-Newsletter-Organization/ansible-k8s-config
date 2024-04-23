FROM jenkins/jenkins:lts-alpine-jdk17

USER root

ENV JENKINS_HOME="/jenkins"

# Pulando a configuração inicial
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

# Definindo fuso horário do Brasil
RUN apk add --no-cache tzdata jq
ENV TZ=America/Sao_Paulo

# Atualizando e limpando cache do Alpine Linux
RUN apk update
RUN apk upgrade
RUN rm -rf /var/cache/apk/*

# Instalação prévia de plugins do Jenkins
COPY plugins.txt /jenkins/plugins.txt
RUN jenkins-plugin-cli -f /jenkins/plugins.txt

EXPOSE 8080 50000