# Use the latest Ubuntu image
FROM ubuntu:22.04

# Run as root user
USER root

#to install open jdk

RUN apt-get update -qq
RUN apt install -y openjdk-11-jdk

# install ssh server 
RUN apt update
RUN apt-get install -y openssh-server
RUN service ssh start


# adding jenkins user
RUN useradd -ms /bin/bash jenkins

#to install docker
RUN apt-get update -qq
RUN apt-get install \ 
    ca-certificates \
    curl \
    gnupg \
    lsb-release -qq
RUN mkdir -m 0755 -p /etc/apt/keyrings
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /etc/apt/keyrings/docker.gpg -qq
RUN echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
RUN apt-get update -qq
RUN apt-get install -y docker-ce 
RUN usermod -aG docker jenkins 

#install git
RUN apt install git

#extra tools for manual testing

# COPY ./root/* /root/.ssh/
USER jenkins
# Set the working directory
WORKDIR /home/jenkins/jenkins_home
# Run a command to print a message
RUN echo "Ubuntu image running as root user with some packages installed!"

# Run a command to start the bash shell
CMD ["/bin/bash"]
