# lab-mandaroty06

## Lab Instructions

### 1. Review Simulated CI/CD Pipeline Configuration:

* **Build Stage:**
  * **Code Commit:** Developers commit code to a version control system, triggering the CI pipeline.
  * **Docker Image Creation:** Dockerfiles define the environment and dependencies, and Docker builds an image which encapsulates the application and its runtime.

* **Test Stage:**
  * **Automated Testing:** Docker images are used to spin up containers where automated tests are conducted, ensuring that the application behaves as expected in an environment identical to production.

* **Deployment Stage:**

  * **Container Registry:** Successfully tested Docker images are tagged and pushed to a Docker registry.
  * **Orchestration and Deployment:** Tools like Kubernetes or Docker Swarm manage the deployment of these images into containers across different environments, handling scaling and load balancing.

### 2. Analyze Enhancements and Potential Issues:
  * **Enhancements:** We can add the validate commit phase prior to build, add the SAST/SCA, Publish and Deploy phases and I would combine the test phase with build
  * **Potential Issues:** Use a repository for generated artifacts and dependencies in the construction phase. The same case for built images, use a private registry

### 3. Write an Analysis Report:

Typically a CI/CD pipeline establish the phases **Validate commit, Build, SAST/SCA, Publish,Deploy** and transversal tasks such as monitoring, log collection and notifications about the phases.

The deploy phase can be used to deploy to a cloud, on-premise, or in microservices environments a new pod is deployed to a Kubernetes cluster.
