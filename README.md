# Using Docker Swarm to run K6 tests
# Introduction
This template will help you to execute K6 tests with Docker Swarm.k6 is a popular load testing tool that provides testers a powerful and easy way to conduct load tests. On the other hand when we combine it with Docker Swarm, a container orchestration tool then it becomes even easier to distribute and scale load tests across multiple machines. In this blog, we will explore how to run k6 tests using Docker Swarm, enabling you to simulate realistic loads on your application.


# Technologies Used
Performance testing tool - K6

Containerisation - Docker

IDE - IntelliJ Idea


# Prerequisites
Docker : https://docs.docker.com/get-docker/

K6 : https://k6.io/docs/get-started/installation/


# Steps for execution
1. Clone the repository on your local system by using command : `git clone https://github.com/knoldus/k6-using-docker-swarm`

2. Open the cloned project in IDE

3. Modify **`test.js`** k6 script according to your requirement

4. Go to the terminal and execute the command to build dockerfile : `sudo docker build -t k6-test .`

5. Go to the terminal and execute the command to create Docker Swarm cluster : `sudo docker swarm init`

6. Go to the terminal and execute the command to deploy k6 test as a service in Docker Swarm cluster : `sudo docker service create --name k6-test --replicas 1 k6-test`

7. Go to the terminal and execute the command to view the logs of the running k6 service replicas and service logs : `sudo docker service logs k6-test`

That’s it! You now have a Docker Swarm setup running with k6 test script.



For a better understanding and changing this project according to you please refer to this blog based on same:-
https://blog.nashtechglobal.com/wp-admin/post.php?post=12530&action=edit
