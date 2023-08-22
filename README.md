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

When you run the script with the mlflow instance, a mlrun folder will be created with
- saved model.pkl
- model configuration
- conda environment configuration
- metadata file
- tracking experiment files

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

# MLflow integrated with 
## Dagshub:
Imagine you're baking a cake with your friends. You have a recipe book (DAGsHub) that everyone can write in. This book keeps track of all the changes and updates to the recipe as you experiment and improve it over time.

Now, MLflow is like a magical baking assistant. Whenever you try a new version of the cake, MLflow takes a picture and notes down all the ingredients and steps you used. It even records how the cake turned out and how people liked it.

Here's how they work together in MLOps:

1. Collaboration with DAGsHub:
You and your friends work on the cake recipe together. You use DAGsHub to keep everything organized.
You create a timeline of changes, like adding more chocolate or using different flour. Everyone can see what each person did and why.
DAGsHub helps you avoid confusion by showing a clear history of your cake-making journey.

2. Tracking with MLflow:
Every time you bake a cake (train a machine learning model), MLflow takes a snapshot of the process.
It notes the recipe (model code), ingredients (data), and baking time (parameters). This helps you remember how you made that delicious cake (achieved a good model) later on.
If the cake turns out great (model performs well), MLflow remembers the details, so you can replicate it in the future.

3. Improving with Both:
As you keep baking and improving the cake, DAGsHub keeps track of the changes you make, like adding frosting or changing the baking temperature.
MLflow continues taking pictures and notes, helping you compare different versions of the cake (model iterations) to see which one is the tastiest (best-performing).

Together, DAGsHub and MLflow make MLOps sweet and efficient. DAGsHub helps you work together smoothly, while MLflow captures the magic of each cake-baking session (model training) so you can keep making delicious cakes (building great models) over and over again.

## AWS services (S3 & EC2):
Imagine you're a chef in a big kitchen, and you're baking special cakes (machine learning models) to serve to your customers. You have a smart way of doing it using three important tools:

- AWS S3 (Simple Storage Service):
This is like your pantry, where you keep all your ingredients, baking tools, and finished cakes.
You store your important stuff, like your recipes (machine learning code), fresh ingredients (datasets), and even your beautiful cakes (trained models) in S3.
It's a secure and organized way to keep everything you need for baking.

- Amazon EC2 (Elastic Compute Cloud):
Imagine this as your magical oven that can bake multiple cakes at once.
EC2 lets you create virtual ovens (computers) in the cloud that can handle heavy-duty baking (model training).
You can start or stop these ovens as needed, depending on how many cakes you're baking (scaling your resources).

- MLflow:
MLflow is like your assistant chef who keeps a detailed record of each cake you bake.
When you start baking a cake (training a model), MLflow takes notes of the recipe (code and parameters), measures the ingredients (data), and even takes pictures of the cake (model performance).
It helps you remember how you baked that delicious cake (created a great model) and lets you compare different cake versions (model iterations).

- Now, let's see how they all work together for MLOps:

1. Preparing the Baking:
You store your recipes (code) and fresh ingredients (data) in your pantry (S3).
When you're ready to bake, you set the right temperature and settings for your magical ovens (EC2 instances).

2. Baking the Cakes:
You put your cake into the oven (train your model on EC2) and let it work its magic.
While baking, your assistant chef (MLflow) takes notes and pictures of the process.

3. Checking the Results:
Once the cake is baked (model is trained), you take it out and check how it turned out.
MLflow shows you the pictures, notes, and details of each cake (model), so you can decide which one is the tastiest (best-performing).

4. Sharing and Enjoying:
You can share your yummy cakes (models) with others by storing them in the pantry (S3). Others can see your amazing creations and even taste them (use the models) for their own cooking (projects).

In MLOps, this setup makes baking (model training) efficient, organized, and scalable. You have a well-stocked pantry (S3) with all your ingredients, magical ovens (EC2) that can handle any baking task, and your assistant chef (MLflow) who helps you bake and keep track of your delicious creations (models).

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
