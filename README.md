# Installation Vinorsoft CRM
1. Install Docker Compose
    ```
    1. sudo curl -L https://github.com/docker/compose/releases/download/1.29.2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
    2. sudo chmod +x /usr/local/bin/docker-compose
    3. docker-compose --version
    ```
2. Install groupadd docker
    ```
    1. sudo groupadd docker
    2. sudo usermod -aG docker $USER
    3. newgrp docker 
    4. systemctl status docker.service
    ```
3. Clone project
    ```
    git clone https://github.com/doansangg/vns-crm.git
    ```
4. Creat network deploy from server
    ```
    docker network create my-network
    ```
5. Install CRM
    ```
    1. cd vns-crm
    2. docker-compose up -d
    ```
6. Go to link in client
    * ##### Go to link with http: http://117.4.247.68:10709/#/Login
    * ##### Go to link with https: https://117.4.247.68:10713/#/Login
7. Note
    ```
    If you want deploy to other port. Edit line 15-16 with
    '10709:8080': http - 8080(port within docker) - 10709 (port public) 
    '10713:8443': https - 8443(port within docker) - 10713 (port public)
    ```

* Link issues slove : https://serverfault.com/questions/1076500/docker-create-two-container-got-two-different-network-id-instead-of-using-defa