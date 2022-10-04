Dean Weiss
4 October 2022

# Compute Abstractions on AWS: A Visual Story

<p> A distinct line between Consumer Space (Managed bny Customer) and Provide Space (Managed by AWS). 
<br>
 Virtual Machine Abstraction: Easiest way to get started, retain responsibility of the guest operatin system and above and their life
 <br>
 Container Abstraction: <br> 
 A containers control plane that is responsible for exposing the API and interfaces to define, deploy, and lifecycle containers. This is also sometimes referred to as the container orchestration layer.
 <br>
 A containers data plane that is responsible for providing capacity (as in CPU/Memory/Network/Storage) so that those containers can actually run and connect to a network. From a practical perspective this is typically a Linux host or less often a Windows host where the containers get started and wired to the network.
 <br>
 Function Abstraction: <br>
 The key point about Lambda is that you don’t have to manage the infrastructure underneath the function you are running. No need to track the status of the physical hosts, no need to track the capacity of the fleet, no need to patch the OS where the function will be running. In a nutshell, no need to spend time and money on the undifferentiated heavy lifting.
 <br>
 Bare Metal Abstraction: <br>
 Direct access to the hardware.
 <br>
 Full Container Abstraction: <br>
  Enter AWS Fargate, a production-grade service that provides compute capacity to AWS containers control planes. Practically speaking, Fargate is making the containers data plane fall into the “Provider space” responsibility. This means the compute unit exposed to the user is the container abstraction, while AWS will manage transparently the data plane abstractions underneath. 
</p>

<image src ="https://user-images.githubusercontent.com/100364917/193865837-b7016e87-dc57-4ac1-b372-320e519513ea.png">

 
 Source: https://aws.amazon.com/blogs/architecture/compute-abstractions-on-aws-a-visual-story/
