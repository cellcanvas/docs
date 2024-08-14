# Tutorial: Local Workflow

Step 1: Install the client on your local machine: 
```
album install cellcanvas:napari-cellcanvas:0.0.5
```

Step 2: Install the server on your local machine: 
```
album install cellcanvas:server:0.0.11
```

Step 3: Launch the server on your local machine: 
```
album run cellcanvas:server:0.0.11 --copick_config_path <path_to_your_copick_config> --models_json_path <path_to_your_models_json>
```

Step 4: Launch the client on your local machine: 
```
album run cellcanvas:napari-cellcanvas:0.0.5 --hostname localhost --port 8000 --copick_config_path <path_to_your_copick_config> --fetch_config False
```
Make sure to replace `<path_to_your_copick_config>` and `<path_to_your_models_json>` with the appropriate file paths specific to your setup.
