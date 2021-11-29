# m4b-tool as a daemon
This container is mostly based on m4b-tool.
https://github.com/sandreas/m4b-tool
sandreas made a really good job there.

## What's it' intend?
This docker was made to make it even easier to follow this guide:
https://github.com/seanap/Plex-Audiobook-Guide

I think the guide is great, but it's a kind of hassle to set, especially the conversion system, up.
To make this even easier and improve the way it works, I made this container.

## What does it?
I slightly improved the above already available auto-m4b-tool.sh to make it an ease to convert your whole library.

Besides this, it was fun to learn something new.
For me it was using docker to build software and afterwards run it.
This docker itself is a kind of huge, but it is what it is and does for me a good job.

## Set up the Container
As I think only compose files make sense only those are here :D.

## Variables
If you are curious what are those $DOCKERDIR and so on are for, it uses an .env file.
So you can define a .env besides your compose file, it will use those variables.

### docker-compose.yml
~~~
version: '3.7'
services:
  m4b-tool:
    image: 9madmax5/m4b-tool
    container_name: m4b-tool
    volumes:
      - /path/to/config:/config
      - /path/to/temp:/temp
      - /path/to/original:/original
      - /path/to/backup:/backup
~~~
