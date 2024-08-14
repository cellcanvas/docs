# Tutorial: Remote Workflow

Step 1: Follow the [quick start](../../quick_start/)

Step 2: Install the server on the worker: 
```
album install cellcanvas:server:0.0.7
```

Step 3: Make a tunnel to the worker: 
```
ssh -L 8080:worker-host:8000 user.name@login-host -N -f
ssh -L 2222:login-host:22 user.name@login-host -N -f
```

Step 4: Launch the server on the worker: 
```
album run cellcanvas:server:0.0.7 --copick_config_path remote_localOverlay_localStatic.json 
```

Step 5: Install the client on your local machine: 
```
album install cellcanvas:napari-cellcanvas:0.0.5
```

Step 6: Launch the client on your local machine: 
```
album run cellcanvas:napari-cellcanvas:0.0.5 --hostname localhost
--port 8080 --copick_config_path local_sshOverlay_sshStatic.json
--fetch_config True --overlay_remote True --static_remote True
```

