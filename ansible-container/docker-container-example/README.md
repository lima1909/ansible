# ansible-container-example

A simple ansible-container-example. Create a nginx image with a simple HTML-page (hello.html)

	# Start Container
	$ docker run --privileged -d --name ac lima1909/ansible-container:1.0

	# Go into the container
	$ docker exec -it ac bash
