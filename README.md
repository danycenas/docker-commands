## Docker Images

**How to use a imagen?**
```java
docker images
/* List all images */

docker pull debian
/* Download a imagen */

docker pull debian:8
/* Download a imagen with specific tag */
```

## Docker Containers

**How to create a container?**
```java
docker container ps -a
/* List all container (initiated or detained)  */

docker run -it ubuntu
/* Created container name by default */

docker run -it --name containerUbuntu ubuntu
/* Created container name assigned */

docker run -it --name containerUbuntu -d ubuntu
/* Start a container in detached mode */
```

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
