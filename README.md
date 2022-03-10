# GuitarDesignModeling

## Quick Start
1.  Pull the [Dolfinx Docker](https://hub.docker.com/u/dolfinx) Image
	```
	docker pull dolfinx/dolfinx
	```
2.  Build the customized Dolfinx Dockerfile
	 ```
	 cd CustomizedDolfinx
	 docker build -t customized-dolfinx .
	 ```

3. Run Jupyter Lab (and mount current directory to host container):
	```
	docker run -it -p 8888:8888 --mount type=bind,source="$(pwd)",target=/root  customized-dolfinx``` # on host machine
	```
	```
	jupyter lab --ip 0.0.0.0 --no-browser --allow-root``` # inside container
	```
	```
	http://127.0.0.1:8888/lab?token=… # Past into browser
	```
