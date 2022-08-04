# if you get error: 
# "pull access denied for sha256, repository does not exist or may require 'docker login' : denied: requested access to the resource is denied"
# when opening the project, this may mean that base SDK container has been deleted 
# or that the project has been moved to a different machine where such container does not exist, 
# you can re-build it by pressing F1 in Visual Studio Code and selecting:
# "Torizon: Rebuild SDK and reload in container"
# after this operation you should be able to re-open your project inside a container
FROM qtcore_arm32v7-qt5-wayland-no-ssh_bullseye_debug_d3f48de8-b79a-4ae4-92b8-4a5bc6168352_sdk_image

# This is required to allow regular user inside the container to access docker socket
RUN addgroup docker && groupmod --non-unique --gid 135 docker && adduser torizon docker
