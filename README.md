# MyApp

A basic Node.js application.

## Files Overview

- `app.js`: Main server or application logic.
- `Dockerfile`: Instructions to containerize the app using Docker.
- `package.json`: Defines dependencies and project metadata.
- `README.md`: Project documentation.

## Getting Started

### Prerequisites

- Node.js installed (version 14 or higher recommended)
- npm (comes with Node.js)
- Docker (optional, for running the app in a container)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/myapp.git
   cd myapp




<!-- <-----------------------------------Task 2-------------------------------------------> -->

```markdown
# Docker Commands - Results and Documentation

This document includes commonly used Docker commands along with their outputs and brief explanations. It serves as a quick reference guide for container management.

---

## 1. `docker ps`

**Command Used:**
```bash
docker ps
```

**Output:**
```
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

**Explanation:**
This command lists all **running containers**. It’s useful to check the status of your containers and verify if they are currently active.

---

## 2. `docker ps -a`

**Command Used:**
```bash
docker ps -a
```

**Output:**
```
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS                     PORTS     NAMES
b968becdbbba   my-node   "npm start"   5 hours ago   Exited (0) 2 hours ago             competent_kirch
```

**Explanation:**
Lists **all containers**, including those that are **stopped**. Useful for viewing history and debugging.

---

## 3. `docker images`

**Command Used:**
```bash
docker images
```

**Output:**
```
REPOSITORY             TAG         IMAGE ID       CREATED        SIZE
najwa006/my-node-app   latest      8ca5ccded98b   6 hours ago    1.36GB
my-node-app            latest      8ca5ccded98b   6 hours ago    1.36GB
```

**Explanation:**
Displays all the **Docker images** on your system. Useful for seeing which images you can use to start containers.

---

## 4. `docker stop`

**Command Used:**
```bash
docker stop b968becdbbba
```

**Output:**
```
b968becdbbba
```

**Explanation:**
Stops a **running container**. Helps you safely halt applications running in containers.

---

## 5. `docker logs`

**Command Used:**
```bash
docker logs b968becdbbba
```

**Output:**
```
> my-node-app@1.0.0 start
> node app.js

App running on port 3000
```

**Explanation:**
Shows the **log output** of a container. Helps with debugging and viewing app outputs.

---

## 6. `docker inspect`

**Command Used:**
```bash
docker inspect b968becdbbba
```

**Output:**  
(Too long to show here, it's a detailed JSON)

**Explanation:**
Provides detailed **JSON metadata** about the container. Useful for inspecting network settings, mounts, etc.

---

## 7. `docker exec`

**Command Used:**
```bash
docker exec -it b968becdbbba bash
```

**Output:**
```
root@b968becdbbba:/app#
```

**Explanation:**
Lets you **run commands inside a running container**. Helpful for troubleshooting or interacting directly with your container's OS.

---

## 8. `docker cp`

**Command Used:**
```bash
docker cp myfile.txt b968becdbbba:/app/
```

**Output:**
No output if successful.

**Explanation:**
Copies files **from host to container** (or vice versa). Useful for moving code, configs, etc.

---

## 9. `docker update`

**Command Used:**
```bash
docker update b968becdbbba --cpus=1.0 --memory=512m
```

**Output:**
```
b968becdbbba
```

**Explanation:**
Updates the container’s **CPU and memory limits**. Useful for managing resources and performance.

---

## 10. `docker restart`

**Command Used:**
```bash
docker restart b968becdbbba
```

**Output:**
```
b968becdbbba
```

**Explanation:**
Restarts the container (stop + start). Helps to apply changes or recover a stuck container.

---

## 11. `docker port`

**Command Used:**
```bash
docker port b968becdbbba
```

**Output:**
```
3000/tcp -> 0.0.0.0:3000
```

**Explanation:**
Shows **which port** on your local machine is connected to a container's internal port. Useful for accessing apps in the browser.

---

## 12. `docker stats`

**Command Used:**
```bash
docker stats
```

**Output:**
```
CONTAINER ID   NAME              CPU %     MEM USAGE / LIMIT   NET I/O     BLOCK I/O
b968becdbbba   competent_kirch   0.15%     50MiB / 512MiB       2kB / 2kB   0B / 0B
```

**Explanation:**
Gives real-time **CPU and memory usage** for running containers. Great for performance monitoring.

---

## 13. `docker rename`

**Command Used:**
```bash
docker rename competent_kirch my-node-app-container
```

**Output:**
No output if successful.

**Explanation:**
Changes the name of a container to something more readable.

---

## 14. `docker commit`

**Command Used:**
```bash
docker commit b968becdbbba my-node-app:v2
```

**Output:**
```
sha256:3b3bfa... (image ID)
```

**Explanation:**
Creates a **new image** from a container’s current state. Useful for saving progress or creating backups.

---

## 15. `docker attach`

**Command Used:**
```bash
docker attach b968becdbbba
```

**Output:**
(You’re attached to the running container’s output)

**Explanation:**
Connects your terminal to the container’s output stream (useful for debugging or interactive apps).

---

## 16. `docker top`

**Command Used:**
```bash
docker top b968becdbbba
```

**Output:**
```
UID       PID     CMD
root      1234    node app.js
```

**Explanation:**
Shows running **processes inside the container**, like the Linux `top` command.

---

## 17. `docker pause` and `docker unpause`

**Commands Used:**
```bash
docker pause b968becdbbba
docker unpause b968becdbbba
```

**Output:**
```
b968becdbbba
```

**Explanation:**
Pauses/resumes all processes inside a container. Useful for temporarily suspending container execution.

---

## 18. `docker wait`

**Command Used:**
```bash
docker wait b968becdbbba
```

**Output:**
```
0
```

**Explanation:**
Waits until the container stops and returns the **exit code**. Good for scripting and automation.

---

## Conclusion

This document summarizes the key Docker commands used for managing containers, with real examples and explanations to help understand their purpose.
```

---

Let me know if you want a version with screenshots or formatted for submission!