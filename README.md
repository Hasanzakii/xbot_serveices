# xbot  Project with Docker 🚀

This repository contains a Laravel project configured to run with Docker. It consists of two services: Laravel and MySQL

## Prerequisites - Grab Your Popcorn 🍿

Make sure you have the following tools installed on your machine:

- [Docker](https://www.docker.com/) - It's like having a magic wand for your code.
- [Docker Compose](https://docs.docker.com/compose/) - Because one compose is never enough, right?

## Configure Application 🎪
1.Clone this repository in a folder call **xbot**:
```ocaml
git clone https://gitlab.com/witelgroup/xbot.v2.git -b master
```
2.Navigate to the `xbot.v2` directory:
```bash
cd path/to/xbot/xbot.v2
```
3.Create a copy of the .env.example file and name it *.env* ny running this:
```bash
cp .env.example .env
```
4.update **.env** file by expected configuration(ask backend team lead for that).  

**Note**: Your MySQL database *host name* should be `mysql`, **not** `localhost`.  


## Configure Docker 🐳
1.Clone the repository in xbot folder which you had created it before:
```ocaml
git clone https://gitlab.com/x1450442/xbot_services.git -b master
```
2.Navigate to the `xbot_services` directory:
```ocaml
cd path/to/xbot/xbot_services
```
4.Create a copy of the **.env.example** file and name it *.env*:
```ocaml
cp .env.example .env
```
Update the .env file by expected configurations.  

**Note**: Your **project_path** should be the path of **xbot.v2** repo `path/to/xbot/xbot.v2`.  

The name of the project is optional, but it is recomended to set it as xbot .  

For the rest of the value ask the back team cause it's secret information.  

## Start the project 
As i said before we have 2 services:

- **laravel**
- **mysql**

1.First of all , we start mysql service as its the persitence layer of our project by just run a simple command:  

- **Start MySQL service**  🦑
```ocaml
docker compose --profile mysql up
```  
**Note**: To ensure that the mysql service is runnig successfully you should see this log `ready to accept connection` in the last line  

Now it's Laravel service turn to run 
- **Start Laravel service** 
```ocaml
docker compose --profile backend up --build
```
- **What it does**: Starts the container that make your Laravel project run. The `up` run the servie," and `--build` ensures everything is fresh and up to date.  

**Time to shine**
Open your browser and head to ` http://localhost:8003` If the sun isn't shining there, something might be wrong 🤸
