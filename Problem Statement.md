## Problem Statement

Create a docker container from the httpd image. The new container needs to be accessible on port 8082 on the host. The conatiner should have the capbility of persisting the data even if the Docker Daemon goes down. The containers default page should show as "Welcome to docker training".

Hint: The default page of httpd image is located at `/usr/local/apache2/htdocs/`
