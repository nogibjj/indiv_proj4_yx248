# indiv_proj4_yx248

## Description
This project is a Flask-based web application containerized using Docker. It demonstrates a basic web app with "Home" and "About" pages, which is deployed to Azure App Services.

## Project Setup

### Dependencies
* Python 3.x
* Flask
* Docker

### Local Deployment
To run this application locally, you will need Docker installed on your machine. Follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/nogibjj/indiv_proj4_yx248
    ```

2. Build the Docker image:
    ```bash
    docker build -t my-flask-app .
    ```

3. Run the Docker container:
    ```bash
    docker run -p 23333:23333 my-flask-app
    ```

### DockerHub Login and Push
To push the built image to DockerHub, use the following commands:

    docker login --username=yourusername
    docker build -t yourusername/reponame .
    docker push yourusername/reponame

You should have a DockerHub account.

Docker Build for DockerHub:
![Docker Build](/images/build-for-dockerhub.png)

Push to DockerHub:
![Push to DockerHub](/images/push-docker.png)

## Changing Ports
If you wish to use a different port:

1. Modify the port in `app.py` (main file).
2. Update the `EXPOSE` port in the Dockerfile.
3. When setting up the Azure Web App, ensure the `WEBSITES_PORT` is set to the new port you are using. Here it is set to `23333`.

## Web Page Preview

Below are the screenshots of the page preview:

Home Page:
![Home Page](/images/home-page.png)

About Page:
![About Page](/images/about-page.png)

## Azure Deployment
### Steps
1. Create Web App on Azure:
![Create Web App](/images/create-web-app.png)

2. Web App Settings on Azure:
![Web App Settings](/images/create-web-app-setting.png)

3. Web App Docker Settings on Azure:
![Web App Docker Settings](/images/create-web-app-docker-setting.png)

4. Add and Set WEBSITES_PORT on Azure:
![Set WEBSITES_PORT](/images/set-websites_port.png)

### Deployed Information on Azure App Services
The app is deployed on Azure App Services, accessible via the default domain provided by Azure. Here are the details for the deployed app:

* Default domain: [`my-simple-flask-web-app.azurewebsites.net`](my-simple-flask-web-app.azurewebsites.net)
* App Service Plan: `ASP-MySimpleFlaskWebAppgroup-85ce (P1v3: 1)`
* Operating System: Linux
* Health Check: Not Configured

![Azure Public URL](/images/Azure-web-app-public-url.png)

## Acknowledgments
* [Flask](https://flask.palletsprojects.com/)
* [Docker](https://www.docker.com/)
