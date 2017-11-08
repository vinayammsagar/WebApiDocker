# You can use the .NET Core SDK Docker image as a build and runtime environment. It's a useful image for iterative development 
#and the easiest way to get started using .NET Core with Docker.
# https://hub.docker.com/r/microsoft/dotnet/
FROM microsoft/dotnet:latest

# Copy everything into api folder
COPY . /api

# Set api folder as the working folder
WORKDIR /api
 
# Restore all the project dependencies into the working folder
RUN ["dotnet", "restore"]

# Build the project
RUN ["dotnet", "build"]

#RUN dotnet publish -c Release -o /publish

 
ENV ASPNETCORE_URLS http://*:8091


#EXPOSE 9000/tcp

# Runs the project which is in the current director
ENTRYPOINT ["dotnet", "run"]
 
