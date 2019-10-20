# spark-ubuntu-vm-setup


## Setup Environment
```
 java -version
 sudo apt-get update
 sudo apt-get install default-jre
 java -version
 sudo apt-get install default-jdk
 sudo add-apt-repository ppa:webupd8team/java
 sudo apt-get update
 sudo apt-get install oracle-java8-installer
 java -version
 sudo update-alternatives --config java
 sudo nano /etc/environment 
 echo $JAVA_HOME
 sudo update-alternatives --config java
 sudo nano /etc/environment 
 source /etc/environment 
 echo $JAVA_HOME
 java -version
```

## Setup Scala

1-  Download Scala


## Setup Apache Spark
  ```
  clear
  sudo apt install build-essential dkms
  clear
  tar -xvf scala-2.12.8.tgz 
  dir
  cd scala-2.12.8/
  cd bin/
  scala
  ./scala

  tar -xvf spark-2.4.0-bin-hadoop2.7.tgz 
  clear
  cd spark-2.4.0-bin-hadoop2.7/bin/
  clear
  ./spark-shell 
```   
## Setup Winutils (Trick the PC/VM into thinking Hadoop exists)

```
download the winutils and related files and setup HADOOP_HOME with values setup in PATH as well.
but still getting error
place all winutils inside SPARK_HOME/bin/
issue was resolved
```

## Setup Python and Jupyter Notebook

```
sudo apt install python3-pip --install python and pip
python -V --Capital V for python version
sudo apt-get install curl
sudo pip3 install jupyter
jupyter notebook --starts jupyter notebook
sudo pip3 install py4j
```

### Setup Environment vairables for Python and Jupyter

```
  cd spark-2.4.0-bin-hadoop2.7/
  clear
  pwd
  export SPARK_HOME='/home/digitalchemist/spark_vm/program_files/spark-2.4.0-bin-hadoop2.7
  export SPARK_HOME='/home/digitalchemist/spark_vm/program_files/spark-2.4.0-bin-hadoop2.7'
  echo $SPARK_HOME
  clear
  echo PATH=$SPARK_HOME:$PATH
  export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH
  export PYSPARK_DRIVER_PYTHON="jupyter"
  export PYSPARK_DRIVER_PYTHON=OPTS="notebook"
  export PYSPARK_PYTHON=python3
  
  NOTE:
  PYSPARK_DRIVER_PYTHON and PYSPARK_DRIVER_PYTHON_OPTS parameters are used to launch the PySpark shell in the Jupyter Notebook.
  
  pyspark --master local[2]
  The --master paramter is used for setting the master node address, here we luach spark locally on 2 cores for local testing.
  

 -- permissions
 
  sudo chmod 777 spark-2.4.0-bin-hadoop2.7
  cd spark-2.4.0-bin-hadoop2.7/
  clear
  cd python/
  clear
  python3
  sudo chmod 777 pyspark
  jupyter notebook
  sudo pip3 install findspark

```
