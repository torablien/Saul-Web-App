Create a blank C9 workspace 

Option 1: Start from scratch

```
git clone https://github.com/IllinoisCogComp/saul.git
```

Option 2: Pull from this repository

```
git init
git clean -f -d
git pull git@github.com:torablien/Saul-Web-App.git
```

After doing either option, do the following (while still in default workspace):

```
sudo apt-get update
sudo apt-get install apt-transport-https

echo "deb https://dl.bintray.com/sbt/debian /" | sudo tee -a /etc/apt/sources.list.d/sbt.list
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823
sudo add-apt-repository ppa:webupd8team/java

sudo apt-get update
sudo apt-get install sbt
sudo apt-get install oracle-java8-installer

cd saul

sbt
format
project saulWebapp
format
run 8080
```

You can find the Saul Visualization Web App at:
http://saul-YOURUSERNAME.c9users.io/