Run TiddlyWiki 5 via docker.

## Prerequisites

Install docker.

## Quickstart

    sudo docker -e TW_PASS=mypassword -e TW_USER=myusername run -d -p 8080:8080 forgottentea/tiddlywiki

Now TiddlyWiki should be running on [http://localhost:8080](http://localhost:8080).

## Keeping the data

The container uses a Docker volume to save the wiki data. In order not
to lose sight of that, I recommend using a local folder for the volume.

    sudo docker -e TW_PASS=mypassword -e TW_USER=myusername run -d -p 8080:8080 -v $(pwd)/.tiddlywiki:/var/lib/tiddlywiki forgottentea/tiddlywiki

In this example, the folder `$(pwd)/.tiddlywiki` is used for the data.
