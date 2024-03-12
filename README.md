# JavaMongoDBExplorer
Hey there! Welcome to our Java MongoDB Learning Project! 🚀 This project is aimed at Java enthusiasts who want to dive into the world of MongoDB, the popular NoSQL database, and integrate it seamlessly into their Java applications.

## Table of Contents

- [Installation](#installation)

## Installation

To understand MongoDB with java we need to first run MongoDB locally on system. There are 2 ways to do it.
1. [Running via Docker](#Running via Docker)
2. [Running directly by MongoSh](#Running directly by MongoSh)

### Running via Docker

1. Install Docker: Ensure Docker is installed on your system. You can download and install Docker Desktop from the official Docker website.
    - After successfully installing docker locally if you get error that hypervisor not found while running then you need to enable visualization in the BIOS and then run below command to enable it.

```console
bcdedit /set hypervisorlaunchtype auto 
```

2. Pull MongoDB Image: If you haven't already pulled the MongoDB Docker image, you can do so by running the following command in your terminal or command prompt:

```console
docker pull Mongo
```

3. Run MongoDB Container: Once the MongoDB image is downloaded, you can run a MongoDB container using the following command:


```console
docker run --name my-mongodb -d -p 27017:27017 mongo
```

- --name my-mongodb: This assigns a name to your container (in this case, my-mongodb). You can replace my-mongodb with any name you prefer.
- -d: This flag runs the container in detached mode, meaning it runs in the background.
- -p 27017:27017: This option maps port 27017 on your host machine to port 27017 in the Docker container. Port 27017 is the default port used by MongoDB.

4. After that from docker desktop terminal you can Mongo shell to create collection. Below are the same code to create some entries.

```console
use recipeManager
db.recipe
db.recipe.insertOne({"title": "Chicken Sandwiches","chief": "Rahul Khandelwal","timeRequired": "10 mins","foodType": ["breakfast","snack"],"ingredents": ["bread","chicken"],"rating": "3"});
db.recipe.insertOne({"title": "Prawn Sandwiches","chief": "Rahul Khandelwal","timeRequired": "10 mins","foodType": ["breakfast","snack"],"ingredents": ["bread","chicken"],"rating": "5"});
db.recipe.insertOne({"title": "Wrap","chief": "Rahul Khandelwal","timeRequired": "10 mins","foodType": ["breakfast","snack"],"ingredents": ["bread","chicken"],"rating": "3"});

```