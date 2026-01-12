# What should i learn in docker for understand this
##
| Part                       | Explanation                                | What to Learn                                                     |
| -------------------------- | ------------------------------------------ | ----------------------------------------------------------------- |
| `docker run`               | Run a container                            | **Docker CLI basics**: run, stop, ps, rm                          |
| `-d`                       | Detached mode (run in background)          | Linux shell: understanding **foreground vs background processes** |
| `--name mongodb`           | Assign a name to the container             | Docker container management                                       |
| `-p 27017:27017`           | Map host port to container port            | Networking basics: **ports, localhost, host vs container**        |
| `-v mongodb-data:/data/db` | Mount a Docker volume (persistent storage) | Linux **filesystem paths**, volumes, persistence concepts         |
| `mongo`                    | The Docker image to use                    | Docker images, pulling, and understanding **official images**     |
