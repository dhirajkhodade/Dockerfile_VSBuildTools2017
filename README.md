# Dockerfile_VSBuildTools2017
Docker file to create docker image with Visual Studio Build Tools installed. This can be used as build environment with AWS Code Build.

Steps to create docker image (You will need windows platform to create this image)

1] mkdir C:\BuildTools
2] cd C:\BuildTools
3] Save this file "Dockerfile" to C:\BuildTools\  (File should be without extension)
4] docker build -t buildtools2017:latest -m 2GB .

Above steps will create docker image. 
Hit below command to run and test docker image

5] docker run -it buildtools2017



