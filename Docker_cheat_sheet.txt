**Docker Cheat Sheet**

**Concepts:**

* **Image:** A self-contained package with everything needed to run an application (code, runtime, libraries). Think of it as a blueprint.
* **Container:** A running instance of an image. Like building a house from the blueprint.
* **Registry:** A central location to store and share images (like Docker Hub).

**Basic Commands:**

* **List Images:** `docker images`
* **Pull an Image:** `docker pull <image_name>` (e.g., `docker pull ubuntu`)
* **Run a Container:** `docker run --name <container_name> <image_name>` (e.g., `docker run --name my_web_app nginx`)
  * `-d`: Run container in detached mode (background)
  * `-p`: Publish container port to host port (e.g., `-p 8080:80`)
* **See Running Containers:** `docker ps`
* **Stop a Container:** `docker stop <container_name>`
* **Start a Stopped Container:** `docker start <container_name>`
* **Enter a Running Container:** `docker exec -it <container_name> bash` (get terminal access)
* **Remove a Container:** `docker rm <container_name>` (**caution:** use with care!)
* **Remove all Unused Images:** `docker image prune`
* **Build an Image from Dockerfile:** `docker build -t <image_name> .` (builds from current directory)


**Intermediate Commands:**

* **Inspect an Image/Container:** `docker inspect <image/container_name>` (Detailed information)
* **Commit Changes from Container:** `docker commit <container_name> <new_image_name>` (Save modifications)
* **Tag an Image:** `docker tag <source_image> <target_image>` (Create an alias)
* **Search for Images:** `docker search <keyword>` (Find images on Docker Hub)
* **Manage Networks:** `docker network ls` (List networks), `docker network create/inspect/rm <network_name>` (Create/inspect/remove networks)
* **Manage Volumes:** `docker volume ls` (List volumes), `docker volume create/inspect/rm <volume_name>` (Create/inspect/remove volumes)
* **Attach to Running Container Logs:** `docker logs -f <container_name>` (Follow container logs)
* **Copy Files/Directories:** `docker cp <source>:<source_path> <container_name>:<destination_path>` (Copy between host and container)
* **Run Multiple Commands:** `docker run --name <container_name> <image_name> sh -c "<command1>; <command2>; ..."` (Chain commands)
* **Use Docker Compose:** `docker-compose up/down/ps` (Manage multi-container applications)

**Advanced Commands:**

* **Restart Policy:** `docker run --restart unless:stopped <image_name>` (Define container restart behavior)
* **Resource Limits:** `docker run --memory=512m --cpu-shares=256 <image_name>` (Set memory and CPU limits)
* **Environment Variables:** `docker run -e KEY=VALUE <image_name>` (Set environment variables for container)
* **Network Modes:** `docker run --network host <image_name>` (Share host network with container)
* **Build with Multi-Stage Builds:** Leverage multiple FROM statements in Dockerfile for optimized images

***************************************
***************************************
***************************************
***************************************
***************************************

**How to push your image to Docker Hub:**
**Prerequisites:**

1. **Docker Hub Account:** Sign up for a free account on [https://hub.docker.com/](https://hub.docker.com/) if you don't have one already.
2. **Built Image:** Make sure you have built the image you want to push using `docker build`.

**Steps:**

1. **Login to Docker Hub:**
   ```bash
   docker login
   ```
   Enter your Docker Hub username and password when prompted.

2. **Tag your Image (Optional):**
   * By default, Docker images are named `<repository_name>:<tag>`.
   * You can push with the default tag (usually `latest`) or create a specific tag for versioning.
   ```bash
   docker tag <your_image_name> <your_username>/<repository_name>:<tag>
   ```
   * Replace `<your_image_name>` with the name you assigned during the build process.
   * Replace `<your_username>` with your Docker Hub username.
   * Replace `<repository_name>` with the desired name for your repository on Docker Hub (create it beforehand if needed).
   * Replace `<tag>` with a specific version tag (optional, but recommended for version control).

3. **Push the Image:**
   ```bash
   docker push <your_username>/<repository_name>:<tag>
   ```
   * Use the same names you used in the tagging step (or omit the `<tag>` if using the default).

**Example:**

Let's say you built an image named `my-web-app` and want to push it to your Docker Hub username `johndoe` with the tag `v1.0`. Here are the commands:

```
docker login

docker tag my-web-app johndoe/my-web-app:v1.0

docker push johndoe/my-web-app:v1.0
```

This will push your `my-web-app` image to the `johndoe/my-web-app` repository on Docker Hub with the version tag `v1.0`.

**Additional Tips:**

* Make sure you're logged in with the correct Docker Hub account before pushing.
* Pushing images can take some time depending on the image size and your internet connection.
* Docker Hub offers public and private repositories. You can choose visibility during repository creation.


Remember, these are just a selection of useful commands.  The Docker documentation offers a comprehensive list and explanations [https://docs.docker.com/](https://docs.docker.com/).

**Additional Tips:**

* Use volumes (`-v`) to persist data outside the container.
* Link containers together (`--link`) for communication.
* Explore environment variables (`-e`) for configuration.
* Refer to the official Docker documentation for more details: [https://docs.docker.com/](https://docs.docker.com/)

**Learning Resources:**

* Get started with Docker tutorials: [https://docs.docker.com/get-started/](https://docs.docker.com/get-started/)
* Explore Docker Hub for pre-built images: [https://hub.docker.com/](https://hub.docker.com/)
* Practice with online interactive courses: [https://docs.docker.com/](https://docs.docker.com/)


