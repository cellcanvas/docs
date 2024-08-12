# Tutorial: Remote Workflow

Step 1: Follow the [quick start](../../quick_start/)

Step 2: Install the server on the worker: 
```
album install cellcanvas:server:0.0.4
```

Step 3: Make a tunnel to the worker: 
```
ssh -L 8080:worker-host:8000 user.name@login-host -N -f
ssh -L 2222:login-host:22 user.name@login-host -N -f
```

Step 4: Launch the server on the worker: 
```
album run cellcanvas:server:0.0.4
```

Step 5: Install the config file fetecher on your local machine: 
```
album install cellcanvas:fetch-config:0.0.1 --filepath <my_path>
```

Step 6: Run the config file fetcher: 
```
album run cellcanvas:fetch-config:0.0.1 --localhost localhost --port
8080 --overlay_remote True --static_remote True --filepath
~/Data/copick/cellcanvas_server/local_sshOverlay_sshStatic.json
```

Step 7: Install the client on your local machine: 
```
album install
cellcanvas:napari-cellcanvas:0.0.1
```

Step 8: Launch the client on your local machine: 
```
album run cellcanvas:napari-cellcanvas:0.0.1 --hostname localhost --port 8080 --copick_config_path /Users/kharrington/Data/copick/cellcanvas_server/local_sshOverlay_sshStatic.json 
```

