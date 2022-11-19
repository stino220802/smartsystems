# **smartsystems**
This repo contains information on how to create python apps on fly.io

## **getting started**
First you need to install the flyctl cmd tool. To do this follow [this](https://fly.io/docs/hands-on/install-flyctl/) guide. For windows it is important to use windows powershell and not cmd. Now create an account and login, follow [this](https://fly.io/docs/getting-started/log-in-to-fly/) guide. Now your setup is complete and you can follow through with the guide.

## **python flask app**
First create a path on your computer where you want to store the app. Then copy the main.py file found [here](https://github.com/stino220802/smartsystems/blob/main/flaskpython/main.py). Also you need to copy the requirements file found [here](https://github.com/stino220802/smartsystems/blob/main/flaskpython/requirements.txt). Then we need to create a Procfile, [example](https://github.com/stino220802/smartsystems/blob/main/flaskpython/Procfile). In this Procfile you see you need to specify web: gunicorn server:app . app Stands for the function you created in your main.py file. As you can see in my example on line 23 it says app.run(), this is where app comes from.

### **flyctl launch**
![image](https://github.com/stino220802/smartsystems/blob/main/pictures/launch.PNG)

Now open a command prompt window and cd in the folder where you created your files. Type flyctl launch this, this will ask you to specify a few things. First it will ask you if it can overwrite the Procfile, say yes. Then it will ask you to give your app a name, don't use special characters, numbers or capital letters. This will crash the launch sequence. After that you need to specify a region with the arrow keys, choose amsterdam(ams). And finally it will ask you to create a postgresql database, choose no because it won't allow you to make one because you have the free plan. Now if you look into your folder a fly.toml file has appeared. In this file you to change the build package. 

![image](https://github.com/stino220802/smartsystems/blob/main/pictures/flytoml.PNG) 

Under [build], you see a variable builder. Change that to "paketobuildpacks/builder:base" as shown in the image above.

### **flyctl deploy**
Now in the same cmd window type flyctl deploy, this upload your app to fly. This will take a while!!! 

![image](https://github.com/stino220802/smartsystems/blob/main/pictures/deploy.PNG)

### **result**
Now if you open fly.io in your browser you can go to your app.




