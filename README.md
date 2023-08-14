# MLP-88
MLOPS | MLflow project demo: tracking machine learning models.

#  What is MLflow?
MLflow is an open-source platform that helps manage the end-to-end machine learning lifecycle. It provides tools for tracking experiments, packaging and sharing code, and deploying machine learning models. In MLOps (Machine Learning Operations), MLflow plays a role in managing and streamlining the process of developing, deploying, and maintaining machine learning models in production.

**How MLflow is used in MLOps:**

1. Experiment Tracking: Imagine you're trying out different algorithms and parameters to build the best machine learning model. MLflow lets you log and compare these experiments. It keeps track of what you tried, what worked, and what didn't, helping you learn and make informed decisions.
2. Code Packaging: Once you have a successful model, MLflow helps you package your code, dependencies, and model files together. Think of it as putting your model in a nice, neat box so you can share it with others or deploy it easily.
3. Model Deployment: MLflow helps you deploy your packaged model to different environments, like cloud servers or data centers. It takes care of the technical details, so you don't have to worry about setting up servers or handling requests.
4. Monitoring and Updates: When your model is out in the real world, MLflow keeps an eye on its performance. If your model starts misbehaving or needs improvements, you can update it without causing disruptions.

In simple terms, MLflow is like a helpful assistant that keeps track of your machine learning experiments, makes it easy to share and deploy your models, and ensures they keep performing well even after they're out in the wild. It's a tool that helps data scientists and engineers work together to create and manage powerful machine learning applications.

#  What is Dagshub?
DAGsHub is a platform that helps you manage and collaborate on machine learning projects, making it easier to track, share, and reproduce your work. In MLOps (Machine Learning Operations), DAGsHub plays a role in improving collaboration and version control for machine learning projects.

**How DAGsHub is used in MLOps:**
1. Project Tracking: Imagine you're working on a complex machine learning project with multiple people. DAGsHub helps you organize your work by creating a timeline of what happened when, like a story of your project's development.
2. Version Control: Just like track changes in a document, DAGsHub keeps a record of all the changes you make to your machine learning code and models. This way, you can easily see what was done, who did it, and when.
3. Collaboration: DAGsHub makes it easy for different team members to work together on the same project. You can share your work, collaborate on code, and see each other's contributions.
4. Reproducibility: Ever had a "It worked on my computer" moment? DAGsHub helps avoid that. You can recreate someone else's results exactly, even if they used different tools or environments.
5. Model Sharing: When you've created a great machine learning model, you can package and share it on DAGsHub. Others can then use your model for their projects without having to start from scratch.

In simple terms, DAGsHub is like a magic book where you write down everything you do in your machine learning project. It helps you remember, share, and work together with others. It's a tool that helps keep your machine learning project organized, makes collaboration smoother, and ensures your work can be easily understood and reproduced.

#  What is AWS S3?
1. Imagine it as a big online storage room.
2. S3 is like a place where you can store your files, like photos, documents, and even data used for machine learning.
3. In MLOps, you might store your trained machine learning models or datasets in S3, making them easy to access and share.
4. You store your machine learning data and models in Amazon S3.

#  What is AWS EC2?
1. Think of it as a virtual computer you can rent.
2. EC2 lets you create and use virtual machines in the cloud. These machines can run your programs, websites, or even complex machine learning calculations.
3. In MLOps, you might use EC2 to train your machine learning models on powerful cloud computers.
4. When you want to do some heavy-duty machine learning, you rent virtual computers (EC2 instances) to do the work.

#  What is security groups 5000 port?
1. Security groups are like digital bouncers for your virtual machines.
2. They control who can talk to your virtual machine and what they can do. They're like setting up rules for who's allowed to enter your virtual space.
3. Port 5000 is like a specific entrance door.
4. In MLOps, you might configure a security group to allow only certain people or systems (like your team's computers) to access a virtual machine, and you could open a specific "door" (port 5000) to let data flow in and out.
5.  You use security groups to control who can access these instances and which "doors" (ports) they can use.
6. This helps you collaborate, share, and process machine learning tasks efficiently and securely.

# Steps
## For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/MLflow-Basic-Demo.mlflow \
MLFLOW_TRACKING_USERNAME=entbappy \
MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0 \
python script.py



```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/MLflow-Basic-Demo.mlflow

export MLFLOW_TRACKING_USERNAME=entbappy 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0


```


# MLflow on AWS

## MLflow on AWS Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000/
```

# Documentation
- https://mlflow.org/docs
