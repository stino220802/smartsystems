# **smartsystems**
This repo contains information on how to create python apps on fly.io

## **getting started**
First you need to install the flyctl cmd tool. To do this follow [this](https://fly.io/docs/hands-on/install-flyctl/) guide. For windows it is important to use windows powershell and not cmd. Now create an account and login, follow [this](https://fly.io/docs/getting-started/log-in-to-fly/) guide. Now your setup is complete and you can follow through with the guide.

## **python flask app**
First create a path on your computer where you want to store the app. Then copy the main.py file found [here](https://github.com/stino220802/smartsystems/blob/main/flaskpython/main.py). Also you need to copy the requirements file found [here](https://github.com/stino220802/smartsystems/blob/main/flaskpython/requirements.txt). Then we need to create a Procfile, [example](https://github.com/stino220802/smartsystems/blob/main/flaskpython/Procfile). In this Procfile you see you need to specify web: gunicorn server:app . app Stands for the function you created in your main.py file. As you can see in my example on line 


