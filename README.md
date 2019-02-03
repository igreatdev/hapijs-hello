# HapiJs-hello
Sample HapiJs Example to run on a docker container

## Build docker image
After cloning this repo, run the below docker command in the project dir.

<code> $ docker build -t <your-username>/hapijs-hello . </code>

To confrim that the image was built successfully, run the code below: 

<code> $ docker images </code>

This will give you the list of images. If your build was successful you should see <your-username>/hapijs-hello in the list.

## Run the docker image
Run the following code to start your docker image:

<code> $ docker run -d -p 3000:3000 <your username>/hapijs-hello </code>

## Test the app
You can get the port of your app with the following code:

<code> 
$ docker ps 

# Example

ID            IMAGE                                COMMAND    ...   PORTS
ecce33b30ebf  <your-username>/hapijs-hello:latest  npm start  ...   3000->3000
</code> 

Now you can call your app using curl

<code> $ curl -i 0.0.0.0:3000 </code>

If everything works out well, you should get a 200 Ok response with Hello world!
