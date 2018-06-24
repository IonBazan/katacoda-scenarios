Now, we want to run things. Let's start with running a single nginx container.

To run the container we will need an image. To find one, use `docker search nginx`{{execute}} or browse [https://hub.docker.com/](https://hub.docker.com/).

You can use tags (visible only via Web Browser) to run a specific version of nginx or simply use `latest` (default):
`docker run -d --name my_nginx nginx`{{execute}}. You must add _-d_ flag to run container in the background. Otherwise it would run in your terminal.
You will get container's hash (ID) as output.

To verify it's running, run `docker ps`{{execute}}.`

You can find low-level details of many Docker objects (containers, images, networks) by running `docker inspect`.
Try inspecting your container: `docker inspect my_nginx`{{execute}} and the image you used: `docker inspect nginx`{{execute}}.

You can view it's processes by running `docker top my_nginx`{{execute}} and open bash by executing `docker exec -it my_nginx bash`. Feel free to navigate trough files in the container.
