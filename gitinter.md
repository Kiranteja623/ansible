difference b/w git merge and rebase
-------------------------------------
[Referhere] (https://www.atlassian.com/git/tutorials/merging-vs-rebasing)
for git understanding [Referhere](https://www.atlassian.com/git/tutorials/what-is-version-control)
git branching strategies
----------------------------
[Referhere](https://gitential.com/git-branching-strategies-for-your-team-how-to-choose-the-best/)
* jenkins backup [Referhere](https://devopscube.com/jenkins-backup-data-configurations/)

Packaging tag
-------------
```
In DevOps, packaging refers to the process of bundling an application or software component along with all its dependencies and configuration files into a distributable format, which can be easily deployed to a target environment.

A packaging tag in DevOps typically refers to a version number or label assigned to a packaged software component or artifact, such as a Docker image or a compiled binary, to help identify and track changes and updates to that component over time.

Packaging tags can be used to facilitate the management and deployment of software components in various stages of the DevOps pipeline, including development, testing, and production. By using standardized packaging tags, DevOps teams can easily track and manage changes to software components, maintain version control, and ensure consistency across multiple environments and deployments.
```
post block in jenkins
----------------------
```
In Jenkins, a post block is a section of the pipeline script that allows you to define steps that should be executed after a stage or the entire pipeline is completed.
```
Docker compose
------------------
```
Docker Compose is a tool for defining and running multi-container Docker applications. It allows you to define the services, networks, and volumes required for your application in a single YAML file, which can then be used to create and run the application with a single command.
```
docker volumes
--------------
```
In Docker, a volume is a persistent data storage mechanism that can be used to share data between containers or to persist data even after a container is deleted or recreated. Volumes can be managed using the Docker CLI or Docker Compose.

When a container is deleted, any data stored inside the container's filesystem is also deleted. However, if you use a volume to store the data, the data will persist even if the container is deleted or recreated. Volumes can also be used to share data between containers, allowing you to create a shared data storage space that can be accessed by multiple containers.
```
Docker ignore:
-----------------
examples:
```
# Ignore all files with the .log extension
*.log

# Ignore the entire logs directory
logs/

# Ignore the file named secrets.txt
secrets.txt

# Ignore all files with the .tmp extension, except for file.tmp
!file.tmp
```
In the example above, the first line specifies that any files with the .log extension should be excluded from the build context. The second line specifies that the entire logs directory should be excluded. The third line specifies that the secrets.txt file should be excluded. The fourth line specifies that any files with the .tmp extension should be excluded, except for file.tmp.
When you run the docker build command, Docker reads the .dockerignore file and excludes any files or directories that match the patterns specified in the file.

It's important to note that the .dockerignore file only affects the build context, and not the contents of the Dockerfile. If you want to exclude files or directories from the image itself, you should use the appropriate Dockerfile commands, such as RUN rm or COPY --from.

