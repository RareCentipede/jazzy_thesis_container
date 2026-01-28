# Image and container for ROS2 Jazzy with Gazebo harmonic and Nvidia driver support.

## Build the image:
```bash
docker build -t rarecentipede/jazzy_thesis:latest .
```

## Run the container with Gazebo support:
```bash
docker-compose run gazebo
```

# Alternatively
## Assemble a distrobox container:
This requires distrobox to be installed, and you must log in to docker using `docker login` first. This will pull the image from Docker Hub so you don't have to build anything locally.
```bash
distrobox-assemble create --root --file jazzy_nv_ubuntu24_harmonic.ini
```

Then enter the container with:
```bash
distrobox-enter --root jazzy_harmonic
```

# To do:
- [ ] Figure out how to make changes to the image and push to Docker Hub automatically.
- [ ] VSCode integration, it doesn't like runnign as root but docker requires root.