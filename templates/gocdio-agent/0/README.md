# STCL-TECH GoCD Agent

### Info:

 To be used only with the [SkeltonThatcher Rancher/GoCD Terraform plan](https://github.com/SkeltonThatcher/aws-terraform-rancher-single-node-ha-gocd)

 This template creates and configures GoCD agent(s).

### Usage:

 Obtain the auto-registration key from config XML in the GoCD server.

 Add the GoCD agent stack, specifying the **gocdio-server service**, the number of agents required, and inputting the registration key.

 Upgrade the GoCD agent stack, creating a named host scheduling rule for **gocdagt_hst**.

 Launch the GoCD agent stack.
