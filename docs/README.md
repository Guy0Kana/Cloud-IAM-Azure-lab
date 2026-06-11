## Let's Start
### Phase 1: Resource Group Creation
Resource Group Creation
A Resource Group acts as a logical container for all Azure resources used in this project. One resource group makes monitoring and management easier during the lifecycle of the system.

<pre>
Component       |     Setting
Resource Group  |    rg-gkltd
Region          |    South Africa North
</pre>

After deployment of the Resource Group, ensure that it appears on the Azure Portal and is ready to host project resources.

<img width="1528" height="349" alt="image" src="https://github.com/user-attachments/assets/623f88f1-1ee8-42b5-8db8-58d8f68f2ed0" />

### Phase 2: Virtual Network Deployment
The Active Directory environment requires a private network where servers and workstations can communicate securely. A Virtual Network (VNet) provides this isolated network infrastructure.

<pre>
Setting         |   Value
Name            |  vnet-gkltd
Address Space   |  10.0.0.0/16
Subnet          |  snet-server
Subnet Range    |  10.0.1.0/24
</pre>

Architecture

<pre>
rg-gktld-iam
│
└── vnet-gktld (10.0.0.0/16)
     │
     └── snet-server (10.0.1.0/24)
</pre>
