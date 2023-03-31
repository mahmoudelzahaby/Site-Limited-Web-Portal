### Controlled Access Web Interface
The Controlled Access Web Interface is a secure web application that provides access to authorized users, sites, or IP addresses only. This web interface is designed to help organizations protect sensitive or confidential information by restricting access to authorized users only.

The web application is deployed using Kubernetes deployment service and ingress, which enables efficient management and scaling of the application. The ingress service provides routing rules and load balancing to ensure that the application is highly available and accessible.

To use the Controlled Access Web Interface, users must be authorized and granted access credentials by the organization's administrators. The web interface provides a clean and intuitive interface that enables users to access the authorized content and features easily and efficiently.

Features
Restricted access to authorized users, sites, or IP addresses
Kubernetes deployment service and ingress for efficient management and scaling
Intuitive and easy-to-use web interface

-----
This repository contains a simple Java Gradle application that can be used to build and deploy a Docker image to a Kubernetes cluster.

### Prerequisites
In order to build and deploy the application, you'll need the following tools installed on your local machine:

Java 11
Gradle 6.x
Docker
Kubernetes CLI (kubectl)

###Getting Started
To get started with this application, you'll need to follow these steps:


1 - Clone this repository: git clone [https://github.com/mahmouddahaby/App-repo-grad1.git](https://github.com/mahmouddahaby/Site-Limited-Web-Portal)
2- cd into the Site-Limited-Web-Portal directory
3- Build the Docker image: docker build -t my-app .
4- Run the Docker container: docker run -p 8080:8080 my-app
5- Open your web browser and navigate to http://localhost:8080 to see the "Hello World" message.

### Building the application
To build the application, navigate to the root directory of the project and run the following command:

 ```
./gradlew build
 ```
This will compile the Java code, run the tests, and produce an executable JAR file located in the build/libs/ directory.

### Building the Docker image
To build a Docker image of the application, run the following command from the root directory of the project:

 ```
docker build -t <image-name> .
 ```
Replace <image-name> with a name for your Docker image. This command will create a Docker image with the specified name, based on the Dockerfile in the root directory of the project.

### Running the Docker image
To run the Docker image locally, run the following command:

 ```
docker run -p 8080:8080 <image-name>
 ```
Replace <image-name> with the name of the Docker image you built in the previous step. This will start a container running the application, which will be accessible at http://localhost:8080.

### Deploying the application to Kubernetes
To deploy the application to a Kubernetes cluster, you'll need to have a running Kubernetes cluster and the kubectl CLI tool installed.

First, create a Kubernetes deployment by running the following command:

 ```
kubectl apply -f app-k8s/deployment.yaml
 ```
This will create a deployment with one replica of the Docker image you built earlier. To scale up the number of replicas, modify the replicas field in the deployment.yaml file and re-run the above command.

Next, create a Kubernetes service for the deployment by running the following command:

 ```
kubectl apply -f app-k8s/service.yaml
 ```
This will create a service that exposes the deployment on a cluster-internal IP address.

### Contributing
If you'd like to contribute to this project, feel free to open a pull request.
