# Docker Command Helper

...




## Features:

 * Simplation some docker commands
 * Perform complex actions with simple commands
 * Easy to underestand and memorize
 * Use them in less than a minute!

<b>Note : </b>This commands only supported for unix based systems.

## Usage :

1 - Clone and register commands an terminal startup

```

# Go to the user home or other location 

cd ~

# Get source with git

git clone https://github.com/mrtdeh/docker-command-helper.git

# Then register this commands in .bashrc (or .bash_profile in mac)

echo "source ~/docker-command-helper/commands" >> ~/.bashrc

```
2 - Reopen the terminal or open new terminal window

3 - Enjoy that....


## Commands :

<b> Note : </b> All commands listed in the below started with <b>dkr</b> prefix.


 #### dkrps
 
 List of all containers whether running or exited

Translated to :
```
docker ps -a
```

 
 #### dkrrmall
 
 Remove all containers whether running or exited

Translated to :
```
docker rm -f $(docker ps -aq)
```

 
 
 
 #### dkrrmexited
 
 Remove only exited containers

Translated to :
```
docker rm $(docker ps -q -f status=exited)
```

 
 
 
 #### dkrstartall
 
 Start all exited containers

Translated to :
```
docker start $(docker ps -a -f status=exited --format "{{.Names}}")
```

 
 
 
 
 
 
 
 #### dkrimgs
 
 List of images

Translated to :
```
docker images
```

 
 
 
 
 #### dkrstats
 
 Show the status of all running containers

Translated to :
```
docker stats $(docker ps -a --format "{{.Names}}")
```

 
  
 
 
 
 #### dkrup
 
 Up the docker-compose.yaml file

Translated to :
```
docker-compose up
```

 
  
 #### dkrupd
 
 Up the docker-compose.yaml file in background

Translated to :
```
docker-compose up -d
```
 
   
 
 
 
 #### dkrdown
 
 Down the docker-compose.yaml file

Translated to :
```
docker-compose down
```

 
 
 
 
 ## Contributing
 
 Contributions are always welcome, no matter how large or small
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
.
.
