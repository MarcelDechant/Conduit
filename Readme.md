
# Conduit

## Containerization of an Frontend and Backend application

This repository serves as a guide for containerizing a simple [Frontend](https://github.com/MarcelDechant/conduit-frontend) and associated [Backend](https://github.com/MarcelDechant/conduit-backend) application using **Docker Compose**.  
  
This Repository was created as part of my training at the **Developer Academy**.  

## Table of Contents

1. [Prerequisites](#prerequisites)   
2. [Description](#description)
3. [Quickstart](#quickstart) 

## Prerequisites

* **Docker** 24.0.7
  * **Compose** v2.32.4 (module to install, [More Information](https://docs.docker.com/compose/))

## Description

### The Conduit-Project

**Conduit** was created to demonstrate a fully fledged application built with Angular that interacts with an actual backend server including CRUD operations, authentication, routing, pagination, and more.  
  
It is a complete full-stack blogging system that serves as a reference implementation for various frontend and backend technologies. It is often used for educational purposes to show developers how a real application is built using modern technologies.  

It is provided free by [Thinkster](https://thinkster.io/) and is also known as the **RealWorld Example App**.

> [!TIP]
> If you want to learn more about the [Frontend](https://github.com/MarcelDechant/conduit-frontend) and [Backend](https://github.com/MarcelDechant/conduit-backend) app or try them both individually, check out their repositories.

### Conduit combined in a container

Often the frontend and backend are hosted on different servers. A clear option is to host both together in a container. Here is a way to make it work.

## Quickstart

This section provides a fast and **minimal setup guide** for using the tools in this repository. For a more **in-depth understanding** and additional options, please refer to the [Usage](#usage) section.

1. [Clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) the project to your platform manually:
    * Example: Clone the repo e.g. using an SSH-Key:  

    ```bash
    git clone git@github.com:MarcelDechant/Conduit.git
    ```

2. Init and update the **submodules**:

    ```bash
    git submodule init
    git submodule update
    ```

3. Configure the **environment variables**:
    * Copy the content of the [`example.env`](example.env) file into an .env file.

    * The new `.env` file should contain all the environment variables - **all of them are required** to run the frontend and backend application!

4. **Build and start the containers** in the background (detached mode):

    ```bash
    docker compose up --build -d
    ```

5. Check whether the **containers are running** correctly:

* Browse to your **IP_ADDRESS:8282** to open the `Frontend`, you should see something like this:
    ![conduit-frontend](frontend.png)

* Browse to your **IP_ADDRESS:8383/admin** to open the `Backend`, you should see this:
    ![conduit-backend](backend.png)
