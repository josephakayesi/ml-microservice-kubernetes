<p align="center" ><img src="https://res.cloudinary.com/tutcan/image/upload/v1657723371/general/machine-learning.png" width="100%" height="100%" alt="Design by Joseph Akayesi. Photo by Katarzyna Pe"></p>

<br>
<br>
<br>

[![josephakayesi](https://circleci.com/gh/josephakayesi/ml-microservice-kubernetes.svg?style=shield)](https://app.circleci.com/insights/github/josephakayesi/ml-microservice-kubernetes/workflows/workflow/jobs?branch=master)

## Project Summary

This project deploys a Machine Learning Microservice API using Docker and Kubernetes.
The Machine Learning Model is exposed by a python flask app via Web API.
The model is trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios.

## Files Overview
1. **.circleci**: It holds all CICD configurations for CircleCI build server.
2. **model_data**: It holds the prediction model library and the prediction model data used to train the model. 
3. **output_txt_files**: It holds the output logs for the deployed and running application for both docker and kubernetes.
4. **app.py**: The index file for starting the python flask application server. 
5. **Dockerfile**: Docker configurations for building and running the docker image based of the project. 
6. **requirements**.txt: The package dependencies for the python flask application.
7. **run_docker.sh**: Script to build and run docker image.
8. **run_kubernetes.sh**: Script to run docker image using kubernetes.
9. **upload_docker.sh**: Script to upload docker image to dockerhub. 

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this [link](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments) for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
