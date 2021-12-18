**Simple Explanation**

```
Before i create something, i first ask myself what i require and i come
up with a list.

Once i have a list its the one i use to generate instances of what i
require.


(a)A docker file creates a docker image.

(b)A docker image is not a running instance but
   it is used in creating a container.

docker file ---->docker image----->docker container.


My Docker file will specifies the number of things needed to run my application.


```

**Advantages of Docker**

```
(a)It makes running of the application easy especially when working with teams.

Without docker while working on a team, the running of
my application is dependent on what is installed in the System.

While using docker, my container has got everything that is needed to run my application.

Within my container i am going to install allmy dependecies and the advantage of that is that it is completely isolated from my computer.

There will be no issue of unmarching dependencies from computer A to computer B.

Woow, Containers are very much isolated from my operating
System!

Therefore regardless of the Operating system that i am using, i am able to run my app since it runs from my container.


(b)It Produces a very Similar development and Production environment.

We run our application based on our image (whether we are on production or in development)

(c)It integrates well with continuous integration or continuous delivery practices.


```

**Docker Structure**

```

(a)Docker File->Instructions needed to build our Image


(b)Docker Image


(c)Docker Container.


Explaining FIle

(a)FROM node:alpine

(b)WORKDIR /usr/app

(c)COPY . .

(d)RUN npm install

(e)CMD [ "npm","run","start" ]


Explanation

(a)I want to go and build my image based on Node JS.I can get various images for various programming Languages in docker hub.

When we specify alpine we get the bare minimum of the image in a certain programming language.

We do not get any extra configuration.

 (b) and (c)

 WORKDIR /usr/app

 COPY . .

 Copies our project and other files in from working directory to the container.

 in short i am putting my projects into the working directory where there are no collisions whatsoever.


(d)Installs the npm packages into the container.

 Remember the node modules is always git ignored.

 In my container which is completely isolated from my local environment i must npm install.


 .dockerignore-These are all files and folders that we do not want copied into our image.

  as a rule of thumb node modules should always be dockerignore, so that your container runs its own node modules.

(e)Whenever we Spin up a container from Our Image,It is going to run our application.

  CMD [ "npm","run","start" ]


```

**How do i Build an Image**

```


```

**Notes By**

```
MbuguaCaleb

```
