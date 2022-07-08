# Jupyterhub

## Installation

* Prerequisites

 * Anaconda3

 * `$JUPYTERHUB_HOME` server, pull `service-spawner` and set the location `service-spawner/jupyterhub` as the value for `JUPYTERHUB_HOME`

As root user, execute the following cmd

```
> conda install -c conda-forge jupyterhub
```


## Run Jupyterhub Server

```
> cd $JUPYTERHUB_HOME
> sh run.sh
```

Jupyterhub server will listen at port 8000
