Create a blank C9 workspace 

git clone https://github.com/IllinoisCogComp/saul.git

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