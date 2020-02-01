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

After testing this image we will push this to aws ecr repository
(considering you have aws cli configured on your machine)

6] aws ecr get-login

Above step will create credintianls for aws ecr repo 

7] docker tag buildtools2017:latest [YOUR ACCOUNT #].dkr.ecr.[YOUR REGION].amazonaws.com/ buildtools2017:latest
8] docker push [YOUR ACCOUNT #].dkr.ecr.[YOUR REGION].amazonaws.com/buildtools2017:latest

and now you have your VS build tools image ready in your aws ecr repository.

Reference- https://aws.amazon.com/blogs/devops/extending-aws-codebuild-with-custom-build-environments-for-the-net-framework/ 


