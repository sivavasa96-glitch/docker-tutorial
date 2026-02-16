1) Your container is running but the application is not accessible. What will you check?
Spoken answer:
“First I check if the container is actually running using docker ps. Then I verify port mapping using docker port or docker ps output. After that I check application logs using docker logs. If it’s still not working, I go inside the container using docker exec and check whether the service is listening on the correct port.”

2) A container keeps restarting again and again. What does it mean?
Spoken answer:
“It usually means the main process inside the container is crashing. I check docker logs to see the error. Most common reasons are wrong CMD/ENTRYPOINT, missing environment variables, or the application failing to connect to DB.”

3) You updated code but container is still running old code. Why?
Spoken answer:
“This happens when we didn’t rebuild the Docker image. If the code is copied during build, we must run docker build again and then recreate the container. Also if volumes are mounted, I check whether old volume data is overriding the new code.”

4) Your Docker image size is too large. How do you reduce it?
Spoken answer:
“I use a lightweight base image like alpine or slim, remove unnecessary packages, and use multi-stage builds. Also I clean cache like apt lists and avoid copying unwanted files using a .dockerignore.”

5) You want container data to persist even after container deletion. What will you use?
Spoken answer:
“I will use Docker volumes. Because container storage is temporary, but volumes store data permanently even if the container is removed.”

6) Two containers need to communicate. How will you do it?
Spoken answer:
“I create a user-defined Docker network. Then both containers can communicate using container names as DNS. This is commonly done in docker compose.”

7) How do you troubleshoot a container in production?
Spoken answer:
“I start with docker ps, docker logs, and check container health. If needed, I use docker exec to enter the container. I also check CPU/memory usage using docker stats. Then I verify network connectivity and environment variables.”

8) Your container works locally but fails in server. Why?
Spoken answer:
“It could be due to missing environment variables, different OS dependencies, port conflicts, firewall rules, or file permission issues. I compare docker image, docker-compose file, and check logs on server.”

9) A container cannot connect to database container. What will you check?
Spoken answer:
“First I check whether both containers are on the same Docker network. Then I verify DB container is running and listening. In Compose, I ensure the service name is used as hostname, not localhost. Also I check credentials and ports.”

10) What happens if you stop a container? Will data be lost?
Spoken answer:
“If the data is stored inside the container filesystem, it can be lost when the container is removed. But if we use volumes, the data will not be lost.”

11) You want to automatically restart a container if it crashes. What do you use?
Spoken answer:
“I use Docker restart policies like --restart always or --restart unless-stopped. In production, we usually use orchestration like Kubernetes, but restart policies help in Docker.”

12) You need to pass sensitive data like DB password. How will you handle it?
Spoken answer:
“I avoid hardcoding in Dockerfile. I use environment variables or Docker secrets in Swarm/Kubernetes. In Azure, we can store secrets in Key Vault and inject them during deployment.”

13) One container is using too much memory. How will you handle it?
Spoken answer:
“I check docker stats to confirm. Then I can set memory limits using --memory option or in docker-compose. I also check if there is a memory leak in the application.”

14) What is the difference between COPY and Volume Mount in real-time?
Spoken answer:
“COPY is used while building the image, so the files become part of the image. Volume mount is runtime, it connects host files into the container. In development we use mounts, in production we usually use COPY.”

15) You want zero downtime deployment using Docker. How?
Spoken answer:
“I run a new container version on a different port, then switch traffic using a load balancer like Nginx. After confirming the new version is stable, I stop the old container. This is like blue-green deployment.”