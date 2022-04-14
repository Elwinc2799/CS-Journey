# Greenplum and Hadoop

| Application | Username | Password    |
| ----------- | -------- | ----------- |
| Greenplum   | gpadmin  | Ch@ngeM3N0w |
| Hadoop      | hdp      | Ch@ngeM3N0w | 

### Steps to access Greenplum:
1. Connect to Greenplum server
```
ssh gpadmin@192.168.2.30
```

2. Check if Greenplum server is running
```
gpstate
```

3. If no service is running or this is the first time accessing the server, run
```
gpstart -a
```

4. Connect to xxxx database and start the Greenplum environment
```
psql xxxx
```

5. List the available databases
```
\l
```

6. List the available schemas in the current database
```
\dn
```

7. List the available tables in the current database
```
\dt
```

5. Quit the environment
```
\q
```

### Steps to access Hadoop
1. Connect to Hadoop server
```
ssh hdp@192.168.2.20
```

2. If this is the first time accessing the server, run
```
./start-all.sh
```

3. Check if the NameNode, DataNode, ResourceManager, and NodeManager are started and running
```
jps
```