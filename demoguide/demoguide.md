[comment]: <> (please keep all comment items at the top of the markdown file)
[comment]: <> (please do not change the ***, as well as <div> placeholders for Note and Tip layout)
[comment]: <> (please keep the ### 1. and 2. titles as is for consistency across all demoguides)
[comment]: <> (section 1 provides a bullet list of resources + clarifying screenshots of the key resources details)
[comment]: <> (section 2 provides summarized step-by-step instructions on what to demo)


[comment]: <> (this is the section for the Note: item; please do not make any changes here)
***
### Utilize Private Link to access apps on networks with overlapping address spaces

<div style="background: lightgreen; 
            font-size: 14px; 
            color: black;
            padding: 5px; 
            border: 1px solid lightgray; 
            margin: 5px;">

**Note:** Below demo steps should be used **as a guideline** for doing your own demos. Please consider contributing to add additional demo steps.
</div>

[comment]: <> (this is the section for the Tip: item; consider adding a Tip, or remove the section between <div> and </div> if there is no tip)

***
### 1. What Resources are getting deployed

This scenario is aligned with the Az-104 and Az-700 path and provides a demo solution for managing overlapping IP address spaces with Azure Private Link.

Overlapping IP address spaces often happens when networks from different customers or companies are connected, especially when there’s no centralized IP address management. 

This scenario guides how to make applications running in one Azure virtual network accessible to users in another virtual network with an overlapping IP address space.

Resources deployed: 

 - VMConsumerOsDisk: Virtual Machine Disk
 - myVM0OsDisk: Virtual Machine Disk
 - myVM1OsDisk: Virtual Machine Disk
 - myILB: Internal Load Balancer
 - VMConsumer-nic: Virtual Machine network interface
 - myPLS.nic.d2543340-e40e-434f-bb7c-ab8997cd7180: Network Interface
 - myPrivateEndpoint.nic.1a0ace1e-74eb-4055-926c-bca971fae1b8: Network Interface
 - myVM-nic0: Network Interface
 - myVM-nic1: Network Interface
 - myPrivateEndpoint: Private endpoint
 - myPLS: Private link service
 - VMConsumerPublicIP: Public IP address
 - VMConsumer: Virtual machine
 - myVM0: Virtual Machine 
 - myVM1: Virtual Machine 
 - NetworkA-PrivateEndpoint: Virtual network
 - NetworkB-PrivateLink: Virtual network

<img src="https://raw.githubusercontent.com/daverendon/azd-private-link/refs/heads/main/demoguide/rg-private-link.png" alt="Intersite connectivity" style="width:70%;">
<br></br>
<br></br>



### 2. What can I demo from this scenario after deployment

<img src="https://raw.githubusercontent.com/daverendon/azd-private-link/refs/heads/main/demoguide/diagram-private-link.png" alt="Intersite connectivity diagram" style="width:70%;">
<br></br>
<br></br>

Once you deploy the environment, you should be able to RDP to the VMConsumer virtual machine.

Then, open a browser in your VMConsumer machine and, using a browser, access the private IP address of the Private Endpoint, like 10.0.0.5. You should be able to access VM0 and VM1.



[comment]: <> (this is the closing section of the demo steps. Please do not change anything here to keep the layout consistant with the other demoguides.)
<br></br>
***
<div style="background: lightgray; 
            font-size: 14px; 
            color: black;
            padding: 5px; 
            border: 1px solid lightgray; 
            margin: 5px;">

**Note:** This is the end of the current demo guide instructions.
</div>


