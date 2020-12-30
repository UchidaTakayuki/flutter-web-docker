# flutter-web-docker
Prepare the flutter web environment with docker.

# Preparation
Specify the name of the application to be developed as APPLICATION_NAME in the .env file.
```
APPLICATION_NAME=myapp
```

If you already have a git repository under development, specify the repository name as FLUTTER_WEB_GIT_REPOSITORY in the .env file.
```
APPLICATION_NAME=myapp
FLUTTER_WEB_GIT_REPOSITORY=UchidaTakayuki/myapp
```

If you want to change the domain from localhost, change FLUTTER_NGINX_SERVER_NAME in the .env file.
```
FLUTTER_NGINX_SERVER_NAME=myapp.com
```
# Command
Build the docker compose
```
$ docker-compose build
```

After Success building image
```
$ docker-compose up -d
```

How to initialize an application project
```
$ docker exec -i flutter-web-{APPLICATION_NAME} bash /usr/local/script/flutter-web-init.sh
```

How to build the application
```
$ docker exec -i flutter-web-{APPLICATION_NAME} bash /usr/local/script/flutter-web-build.sh
```

# Workspace
The development workspace will be under the src directory.
After modifying the code, you can run the build command to reflect the changes.