# docker-networking-assignment2-part1

### Step 1: Created a new Docker network named "my_network" 
```
docker network create my_network
```
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/f5881756-4571-425f-bf4b-2006aa13270c)

![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/95c8c2f7-1d66-4a9c-9778-54e697310e30)

### Step 2: Created a new Docker container "nginx_container" using the "nginx" image and connect it to the "my_network" network.
```
docker run -d --name nginx_container --network my_network -p 8080:80 nginx
```
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
```
docker run -d --name nginx_container_2 --network my_network -p 8082:80 nginx
```
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/84f2becc-73c3-4d76-9687-d09b61b50ac4)

### Step 9: Verify that the "nginx" default page is accessible on your host machine at http://localhost:8082.
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/3d453de8-4631-4fc7-b934-74d0e121c946)

### Step 10: Use the "docker container ls" command to display information about all running containers. Document your findings in the README.md file.
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/7fa2aca8-8563-4cae-8add-6934af9bd839)

### Step 11: Stop and remove all containers.
```
docker stop nginx_container_2
docker rm nginx_container_2
docker stop httpd_container
docker rm httpd_container
```
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/a4a1d798-241a-4634-abc7-a314c5256afb)

### Step 12: Cleanup: Remove the "my_network" network.
```
docker network rm my_network
```
![image](https://github.com/zahydakhan/docker-networking-assignment2-part1/assets/45081511/92d2390d-de07-477e-8d1a-74e61c2646ba)

### Step 13: Done: Create a README.md file and document your findings for each command.
### Step 14: Pushed the codebase
