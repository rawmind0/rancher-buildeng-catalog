# STCL-TECH GoCD server

### Info:

 To be used only with the [SkeltonThatcher Rancher/GoCD Terraform plan](https://github.com/SkeltonThatcher/aws-terraform-rancher-single-node-ha-gocd)

 Creates and configures a GoCD server instance with data HA.

 Utilises an AWS EC2 EBS volume for /godata.

### Usage:

 Install the Rancher EBS plugin stack first.

 Using the Rancher storage option, create an EBS volume named ebs.

 Set the volume size and type pairs, e.g:

 ```
 volumeType = gp2
 size = 10
 ```

 Add the GoCD server stack.

 Upgrade the GoCD server stack, creating a named host scheduling rule for **gocdsrv_hst**

 Launch the stack.

 The GoCD server will be available at http://<HOST_IP>:8153

### Optional:

 Install the Rancher AWS Route 53 plugin to provide DNS HA in the event of a host or service failure.

 Once installed, create a Route 53 CNAME entry to the dynamic A record for the GoCD server service.

### Notes:

 JVM options are fixed at default, e.g:

 ```
 Xms512m
 Xmx1024m
 ```
