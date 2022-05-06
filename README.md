## Install Hadoop On Windows

- https://towardsdatascience.com/installing-hadoop-3-2-1-single-node-cluster-on-windows-10-ac258dd48aef
- https://brain-mentors.com/hadoopinstallation/
- https://medium.com/analytics-vidhya/hadoop-how-to-install-in-5-steps-in-windows-10-61b0e67342f8


## How to start Hadoop

- Open terminal as **administration role**
- Check out to path `E:/hadoop-3.2.2/sbin`
- `start-dfs.cmd`
- `start-yarn.cmd`

```
# %HADOOP_HOME%\bin\hadoop jar %HADOOP_HOME%\hadoop-streaming-3.2.2.jar -mapper C:\Users\ligunagyi\Desktop\hadoop_tutorial\mapper.py -reducer C:\Users\ligunagyi\Desktop\hadoop_tutorial\reducer.py -input /user/liguangyi/hello.txt -output /user/liguangyi/output
```

## How to run mapper.py, reducer.py

- Delete output folder: `hdfs dfs -rm -r -f /user/liguangyi/output`
- Run `%HADOOP_HOME%\bin\hadoop jar %HADOOP_HOME%\hadoop-streaming-3.2.2.jar -mapper "python C:/Users/liguangyi/Desktop/hadoop_tutorial/mapper.py" -reducer "python C:/Users/liguangyi/Desktop/hadoop_tutorial/reducer.py" -input /user/liguangyi/hello.txt -output /user/liguangyi/output`

