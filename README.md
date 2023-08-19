# docker-networking-assignment2-part1

### Step 1: Created a new Docker network named "my_network" 
```
docker network create my_network
```
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/f5881756-4571-425f-bf4b-2006aa13270c)

![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/95c8c2f7-1d66-4a9c-9778-54e697310e30)

### Step 2: Created a new Docker container "nginx_container" using the "nginx" image and connect it to the "my_network" network.
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/1f43492b-e8f4-4c94-a7b6-e3ccfc7bddd5)

### Step 3: Verify that the "nginx" default page is accessible on your host machine at http://localhost:8080.
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/af34d39e-ea6d-4002-85ea-1ecf4209db77)

### Step 4: Created a new Docker container "httpd_container" using the "httpd" image and connect it to the "my_network" network.
```
docker run -d --name httpd_container --network my_network -p 8081:80 httpd
```
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/bb04c864-8913-488f-9b1b-2d3c8b5bdcb0)

### Step 5: Verify that the "httpd" default page is accessible on your host machine at http://localhost:8081.
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/fa713721-581b-4383-9d8a-aaa2f703dcff)

### Step 6: Use the "docker network inspect" command to display information about the "my_network" network. Document your findings in the README.md file.
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/b1effa36-5e9f-4585-8d40-6e0a6b4c708b)

### Step 7: Stop and remove the "nginx_container" container.
```
docker stop nginx_container
docker rm nginx_container
```
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/f4de5637-2cee-4a6e-bd84-5f460ac4e673)

### Step 8: Create a new Docker container "nginx_container_2" using the "nginx" image and connect it to the "my_network" network.


### Step 9: Verify that the "nginx" default page is accessible on your host machine at http://localhost:8082.

### Step 10: Use the "docker container ls" command to display information about all running containers. Document your findings in the README.md file.

### Step 11: Stop and remove all containers.

### Step 12: Cleanup: Remove the "my_network" network.




