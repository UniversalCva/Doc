# install Hadoop

**Step1** : Install Java

```
sudo apt update
sudo apt install default-jdk
```

**Step2**: Install Hadoop

```
wget https://dlcdn.apache.org/hadoop/common/hadoop-3.3.1/hadoop-3.3.1.tar.gz
wget https://downloads.apache.org/hadoop/common/hadoop-3.3.1/hadoop-3.3.1.tar.gz.sha512
shasum -a 512 hadoop-3.3.1.tar.gz
cat hadoop-3.3.1.tar.gz.sha512
tar -xzvf hadoop-3.3.1.tar.gz
sudo mv hadoop-3.3.1 /usr/local/hadoop
```

**Step3**: Configure Hadoop's Java Home

```
readlink -f /usr/bin/java | sed "s:bin/java::"
sudo nano /usr/local/hadoop/etc/hadoop/hadoop-env.sh
        #Option 1: Set a Static Value
                . . .
                #export JAVA_HOME=
                export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64/
                . . .
        #Option 2: Use Readlink to Set the Value Dynamically
                . . .
                #export JAVA_HOME=
                export JAVA_HOME=$(readlink -f /usr/bin/java | sed "s:bin/java::")
                . . .
        #Step4: Running Hadoop
/usr/local/hadoop/bin/hadoop
mkdir ~/input
cp /usr/local/hadoop/etc/hadoop/*.xml ~/input
/usr/local/hadoop/bin/hadoop jar /usr/local/hadoop/share/hadoop/mapreduce/hadoop-mapreduce-examples-3.3.1.jar grep ~/input ~/grep_example 'allowed[.]*'
cat ~/grep
```
