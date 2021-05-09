# Complete-Intro-to-Containers
What started as a way to manage multiple servers on one system has grown into the way we develop, write code, ship applications, and coordinate large scale applications! Containers may have started as tools for the ops team, but now everyone needs to learn to build and use them. In this course you’ll learn what containers are, how to create containers from scratch, how to run containers from Dockerhub, how to create your own containers with Dockerfiles, best practices for front-end and Node.js code in containers, and how to create development environments with containers.
# What's inside the course... 👀

## Containers
Link: [🔗 Containers](https://github.com/Freivincampbell/Complete-Intro-to-Containers/tree/02-Containers)

Containers are probably simpler than you think they are. Before I took a deep dive into what they are, I was very intimidated by the concept of what containers were. I thought they were for one super-versed in Linux and sysadmin type activties. In reality, the core of what containers are is just a few features of the Linux kernel duct-taped together. Honestly, there's no single concept of a "container": it's just using a few features of Linux together to achieve isolation. That's it.
So how comfortable are you with the command line? This course doesn't assume wizardry with bash or zsh but this probably shouldn't be your first adventure with it. If it is, check out Jem's course on it. This course will give you more than we'll need to keep up with this course.

1. chroot
2. Namespaces
3. cgroups




## Docker
Link: [🔗 Docker](https://github.com/Freivincampbell/Complete-Intro-to-Containers/tree/03-Docker)

This is probably why you're here: Docker. Docker is a commandline tool that made creating, updating packaging, distributing, and running containers significantly easier which in turns allowed them become very popular with not just system administraters but the programming populace at large. At its heart, it's a command line to achieve what we were doing with cgroups, namespaces, and chroot but in a much more convenient way. Let's dive into the core concepts of Docker.

1. Docker Images without Docker
2. Docker Images with Docker
3. Node.js on Containers
4. Tags
5. Docker CLI

## The Dockerfile
Link: [🔗 Dockerfile](https://github.com/Freivincampbell/Complete-Intro-to-Containers/tree/04-Intro-to-Dockerfiles)

So far we've been focusing a lot on running containers and haven't much dug into building them. This is on purpose because most of benefit of containers for developers comes from the running of containers. If you learn one thing, it should be how to run them.

That said, let's learn to build our own containers. We'll again be using Docker for this though there are other ways to do this. Docker has a special file called a Dockerfile which allows you to outline how a container will be built. Each line in a Docker file is a new a directive of how to change your Docker container.

A big key with Docker container is that they're supposed to be disposable. You should be able to create them and throw them away as many times as necessary. In other words: adopt a mindset of making everything short-lived. There are other, better tools for long-running, custom containers.

Let's make the most basic Dockerfile ever. Let's make a new folder, maybe on your desktop. Put a file in there called Dockerfile (no extension.) In your file, put this.

1. The most basic Dockerfile-based Container
2. Build a Node.js App
3. A More Complicated Node.js App
4. EXPOSE
5. Layers
6. Docker Ignore

## Making Tiny Containers
Link: [🔗 Tiny Containers](https://github.com/Freivincampbell/Complete-Intro-to-Containers/tree/05-Making-Tiny-Containers)

Making your containers smaller is a good thing for a few reasons. For one, everything tends to get a bit cheaper. Moving containers across the Internet takes time and bits to do. If you can make those containers smaller, things will go faster and you'll require less space on your servers. Often private container registries (like personal Docker Hubs, Azure Container Registry is a good example) charge you by how much storage you're using.

Beyond that, having less things in your container means you're less susceptible to bugs. Let's say there's a Python exploit that's going around that allows hackers to get root access to your container. If you don't have Python in your container, you're not vulnerable! And obviously if you do have Python installed (even if you're not using it) you're vulnerable. So let's see how to make your container a bit smaller.

In your previous Dockerfile, change the first line (FROM)

1. Alpine Linux
2. Making our own Node.js Alpine container
3. Multi Stage Builds
4. Static Assets Project


## Features in Docker
Link: [🔗 Features in Docker](https://github.com/Freivincampbell/Complete-Intro-to-Containers/tree/06-Features-in-Docker)

1. Bind Mounts
2. Volumes
3. Using Containers for your Dev Environment
4. Hugo
5. Aside on Node.js and Native Dependencies
6. Networking with Docker
7. Connecting our Node.js App to MongoDB


## Multi Container Projects
Link: [🔗 Multi Container Projects](https://github.com/Freivincampbell/Complete-Intro-to-Containers/tree/07-Multi-Container-Projects)

This may be one of the most useful features you learn about Docker. We've been mixing various different facets of deploying your app to production and creating development environments. This feature in particular is geared much more for development environments. Many times when you're developing containers you're not in just a single container environment (though that does happen too.) When this happens, you need to coordinate multiple containers when you're doing local dev and you've seen in the previous chapter, networking, that it's possible if a bit annoying.

With Docker Compose we simplify this a lot. Docker Compose allows us the ability to coordinate multiple containers and do so with one YAML file. This is great if you're developing a Node.js app and it requires a database, caching, or even if you have two+ separate apps in two+ separate containers that depend on each other or all the above! Docker Compose makes it really simple to define the relationship between these containers and get them all running with one docker-compose up.

Do note that Docker does say that Docker Compose is suitable for production environments if you have a single instance running multiple containers. This is atypical for the most part: if you have multiple containers, typically you want the ability to have many instances.

In addition to working very well dev, Docker Compose is very useful in CI/CD scenarios when you want GitHub Actions or some CI/CD provider to spin up multiple environments to quickly run some tests.

1. Docker Compose
2. Kubernetes
3. Kompose
4. Kompose Convert


## OCI
1. Buildah
2. Buildah && Docker
3. Podman


## Course Documentation & Tutorial
Link: [🔗 Course Documentation & Tutorial](https://btholt.github.io/complete-intro-to-containers/)
