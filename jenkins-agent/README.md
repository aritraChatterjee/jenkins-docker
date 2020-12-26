#### To build the customized agent container image:

````sh
[wnode@localhost ~]docker build -t jenkins-agent-docker .
````



#### To start an agent:

```sh
[wnode@localhost ~]$docker run -d --group-add $(stat -c '%g' /var/run/docker.sock) --security-opt label:disable -v /var/run/docker.sock:/var/run/docker.sock jenkins-agent-docker -url http://host:8080 secret agent-name
```

Here, ***host*** is the hostname/ip of the jenkins-master and ***secret*** can be found from the page of the corresponding node under nodes in jenkins-master

![image-20201226145411007](D:\tech\projects\infra-projects\jenkins-docker\jenkins-agent\secret_config.png)