Using the Docker platform for application-level deployment, developers and users can leverage containers to efficiently create, distribute, execute, and oversee their apps. Containers offer programmers the capability to combine different components of their software into a unified instance, encompassing packages, tools, environments, libraries, and more. Consequently, this enables developers to seamlessly run their applications in diverse environments, without concerns about varying dependencies. Notably, Docker functions akin to a virtual machine, alleviating users from fretting over dependencies, packages, and numerous other complexities through the utilization of Docker features.

Installing Docker in Ubuntu 20.04
Docker Engine is compatible with x86_64(amd64), armfh, arm64 and s390x architectures. Before Installing the latest versions of Docker, uninstall older versions by the name of docker, docker.io, or docker-engine. If we want a clean installation, then clean up the existing data stored in /var/lib/docker.

# sudo apt-get remove docker docker-engine docker.io containerd runc

Set up repository
First, update the apt package and Install the necessary packages to enable apt to access an HTTPS repository: 
# sudo apt-get update
# sudo apt-get install ca-certificates curl gnupg lsb-release

Add Docker’s official GPG key
# sudo mkdir -p /etc/apt/keyrings
# curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

Run the below command to set up the repository
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

Install Docker Engine
Run the following command to install the docker
# sudo apt update
# sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

To verify the installation is successful we can run the hello-world image
# sudo docker run hello-world

It will give a message as shown below:
Hello from Docker!
This message shows that your installation appears to be working correctly.
To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.
To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash
Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/
For more examples and ideas, visit:
 https://docs.docker.com/get-started/
