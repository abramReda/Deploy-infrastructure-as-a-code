## Deploy high avilable web app using cloud formation
see it work [http://udagr-webap-18o8zs2mcv3xv-1815303022.us-west-2.elb.amazonaws.com/](http://udagr-webap-18o8zs2mcv3xv-1815303022.us-west-2.elb.amazonaws.com/)
## install Stacks
To create Required infrastructure (i.e VPC, Subnets, Getway , Elastic IPs and Route tables) we have `UdagramNetwork.yml` templete ,just run the following command
```
create.bat UdagramNetwork UdagramNetwork.yml UdagramNetworkParameters.json
```
after creating network stack we will create servers stack ( autoscalling group , Security gruoups , load balancers)
```
create.bat UdagramServers UdagramServer.yml UdagramServerParameters.json
```

## side infotmation
- For debugging purposes we should create, and download key pair called `private-ec2-devops` this will be used through jump box to debug the ec2 instances

- we can change the size of instance by change the parameter `InstanseType`  in `UdagramServerParameters.json`

## Diagrams 
Network Digram
![network](Diagrams/UdagramInfrastructure.jpeg)