FROM ubuntu:22.04
RUN apt update
RUN apt install openjdk-17-jdk -y
RUN apt install curl -y
RUN curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
RUN echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | tee /etc/apt/sources.list.d/jenkins.list > /dev/null 
RUN apt-get update
RUN apt-get install jenkins -y
RUN apt install software-properties-common -y
RUN add-apt-repository --yes --update ppa:ansible/ansible 
RUN apt install ansible -y
RUN java -version
CMD ["/usr/bin/jenkins","run"] 
