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
* Link code : https://github.com/salesagility/SuiteCRM-Core/releases
8. Install Vietnamese language
    ```
    Bước 1: Download file install tại đây:
        https://github.com/luudinhkiet/VNS-CR-vnm
    Bước 2: Đăng nhập vào VNS-CRM, chọn mục " Quản trị viên"
        ![1](https://user-images.githubusercontent.com/71433332/198084966-ad5a3716-d24c-42c6-9a62-2a7f67f6569a.png)
    Bước 3: Chọn bộ nạp mô-đun tại phần công cụ quản trị:
        ![2](https://user-images.githubusercontent.com/71433332/198085681-a6167627-0d55-41df-9de4-59ee81a2c782.png)
    Bước 4: Upload file vừa tải về :
        ![3](https://user-images.githubusercontent.com/71433332/198086243-e12c1fc6-5f78-4bfa-8de9-9f8e1653c79e.png)
        4.1 : chọn Tải lên :
           ![3](https://user-images.githubusercontent.com/71433332/198086466-9dca6e64-5e2c-4d21-b7f3-66244fc8c275.png)
        4.2 : chọn Cài đặt :
            ![4](https://user-images.githubusercontent.com/71433332/198087111-930ea0f2-fa16-4a3a-b15c-4fd2c5ae5bf0.png)
    Bước 5: đi đến Quản trị -> chọn Sửa chữa -> chọn Nhanh chóng sửa chữa và xây dựng lại.
    Bước 6: log out.
     ```
