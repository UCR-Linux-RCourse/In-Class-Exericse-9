# In-Class Exericse 09
## Tasks
1. Make sure docker is working using `docker run hello-world`
2. Start a docker container using the nginx image and name the container webtest
    + `docker run -d -p 8080:80 --name webtest nginx`
3. Connect to the website and make sure it shows the default nginx page
4. Use the interactive mode to explore the docker container and find where that webpage is stored.
    + `docker exec -it bash`
    + Look in /usr/share/nginx/html
5. Exit the container by typing `exit` into the terminal
6. Stop and remove the webtest container
    + `docker stop webtest`
    + `docker rm webtest`
7. Start the container but this time mount the website folder in the current directory to the html folder in the nginx container
    + `docker run -d -p 8080:80 -v ./website:/usr/share/nginx/html --name webtest nginx`
8. Navigate to the website again and notice a new webpage! (You may need to refresh)
9. Stop and remove the webtest container
    + `docker stop webtest`
    + `docker rm webtest`
10. Remove the nginx image.
    + `docker rmi nginx`