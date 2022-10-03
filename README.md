This project contains docker compose file that will provision two services rates app and db

Instructions:

clone this repository using git clone
CD into the repository
run docker-compose up or docker compose up depending on your avaliable command if it is not installed install it from here https://docs.docker.com/compose/install

A new two containers will be built if it's your first time running it otherwise they will be created from previous image.
reates app will expose its port 3000 to the host machine

You can test the application using command: curl "http://localhost:3000/rates?date_from=2021-01-01&date_to=2021-01-31&orig_code=CNGGZ&dest_code=EETLL"

Rates app was configured to use environment variables for database connitions instead of configs.py file, docker compose will inject the variables in the contianer from dev.env file
If you need to chnage database user, password or db name please do so in the dev.env file and do docker compose build, new variables will be used by db and rates services from the same file to reduce redundancy