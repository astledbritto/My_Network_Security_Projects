### My Network Security Projects
I have design and developed  different network topologies with the help of Cisco Packet Tracer 8.0.0.0212. 
## Projet Discription
I have created some basic working of network topologis. To do this I have used Cisco Packet Tracer Application. And all the networking devices which are used in developing a small scale or large scale network topology. 
So, what is Cisco Packet Tracer it's a sumulation software which is used to test and simulate abstract networking concepts. It's mainly used to explore your networking concepts and experince which is very close to what we see in computer networks.
## Installation 
We have to download the software from offical CCNA website. The link will be provided below, we do required a registration before downloading the software. After that we required to accept the tearms and conditions. Once all the steps are copleted the application will be install in your local machine. 
https://www.netacad.com/courses/packet-tracer
## Table Of Contents

1. Cisco Simple Network Topology 
2. Cisco Static Routing
3. Cisco RIP Routing 
4. Cisco OSPF Routing
5. Cisco EIGRP Routing 
6. Cisco VLAN and STP Topology 
7. Cisco Packet Filtering Firewall
8. Cisco (Outbound) Overloading NAT (ASA) And (Inbound) Static NAT (ASA)
9. Cisco (Outbound) Overloading NAT (IOS) And (Inbound) Static NAT (IOS)
10. Cisco IPSec VPN Topology
11. Cisco Remot Access VPN IPSec Topology

## 1. Cisco Simple Network Topology
![image](https://user-images.githubusercontent.com/60734787/147476393-68488bdc-6463-443b-8a8e-9289c61e2d09.png)

Its a Simple network topology with following IP address 10.200.10.0.Where one device can communicate with each other in the same network. 
The Password is 'Secret55'.I have also configure SSH (Secure Shell) on our network devices, which can be used for a secure remote connection.It can be done using following command 'ssh -l AS-6903 <ip address>'. The username will be 'AS-6903' and the password will be 'Secret55'.
  
 ## 2. Cisco Static Routing
 ![image](https://user-images.githubusercontent.com/60734787/147477433-fe71af54-640d-46ae-83da-fac013bbce37.png)
In this topology I have given all the static routes in the network devices.There is a Multilayer switch 3650-24PS with two 2811 routers.The network which is beeing used is 10.200.2.0/29.
We can check the configuration by using 'Show Run'. And all the passwords will be 'Secret55'.
  
## 3. Cisco RIP Routing
  ![image](https://user-images.githubusercontent.com/60734787/147478161-3498199a-6844-4a3e-8317-b7af939358e5.png)
  In this topology I have configured RIP protocol on two 2811 routers. The networ that I am using in this topology is 172.18.5.0/24. To configure RIP protocol we do required to enter 'router rip' into the configuration mode. Then we do required to use rip version 2 with no auto-summary. Once all the set-up is completed we do required to add the networks, like 'network ip <ip address>'.We can check the ip routing protocol by using 'show ip route rip'.
  
## 4. Cisco OSPF Routing
  ![image](https://user-images.githubusercontent.com/60734787/147479684-d7c09aa1-b7ef-4a81-ad9f-46a22d25311f.png)
In this topology we first required to configured and authenticate MD5 on different router interfaces. Then we have to configure it with a key 'ip ospf message-digest-key 1 md5 Secret55'. And the authentication will be done with following connamd 'ip ospf authentication message-digest'. We are required to define the routing networks with the network ip its wild mask and area.The netwok assing for the OSPF topology is 172.18.5.0/24.
 
## 5. Cisco EIGRP Routing
  ![image](https://user-images.githubusercontent.com/60734787/147480313-0e45404b-5513-4fe5-828e-5a98793a3123.png)
In EIGRP there is two netwok topology beeing used those are WAN 172.100.104.0/30 and for LAN 192.168.104.0/27. First we have to loopback addresses on each of our routers. Then we have to start the EIGRP configuration using following command 'router eigrp 1'. Then we have to joine the networks with its corresponding interface.

## 6. Cisco VLAN and STP Topology
  ![image](https://user-images.githubusercontent.com/60734787/147481114-e49195ca-e1b3-4be9-812c-320306f1b3e9.png)
In this topology we are going to use two different network address for WAN 172.20.90.0/30 and for LAN 10.200.6.0/29. Then for routing we do required to configure EIGRP protocol and add the networks.Once the topology is set up we are ready to configure VLAN. We are going to use 'switchport access Vlan<number>'. Then we do required to perform truncking protocol. Then we have to configure encapsulation dot 1Q 5, after that we need to implement the spamming tree protocol with its priority number.
  
## 7. Cisco Packet Filtering Firewall
  ![image](https://user-images.githubusercontent.com/60734787/147506864-7d45cb23-e7d4-424a-887c-64c57ce2ee20.png)
In this topology I have configured two different networks those are LAN and WAN. with their respective IP address.I have also used EIGRP for routing connectivity. I have configured an Access List to allow the required network traffic.The ACL will be an standerd ACL which will either allow or denie the inbound traffic.
  
 ## 8. Cisco (Outbound) Overloading NAT (ASA) And (Inbound) Static NAT (ASA)
![image](https://user-images.githubusercontent.com/60734787/147507352-75a3c3bf-417c-4cc7-b87e-c013c476eefb.png)
In this topology we are going to use an network of 10.100.141.0/24 and 172.30.25.0/29 respectively. We are going to perform Network Address Translation (NAT).I have configured an trusted and untrusted interfaces on the router and to do the routing I have used static routing method. To the NAT translation we have to creat an access list that will our internal network address will be get translated while going into the untrusted network. So to do that we have to creat an pool of address which will have IP address of untrusted networks. After that I have also configure a set of NAT which will only include TCP port 80. So the translation will only include the specific port nummber 80's request to be translated.
  
## 9. Cisco (Outbound) Overloading NAT (IOS) And (Inbound) Static NAT (IOS)
![image](https://user-images.githubusercontent.com/60734787/147507968-57b2c631-ee73-4d58-a072-435bce768890.png)
In this topology first I have set up all the interfaces either outside or inside. Then I have set up the security level which is 0 for outside interface and 100 for incide interface. Then I set up the network objects which will have the subnets of trusted and untrusted networks. Then I did created an access list which will only permit ICMP and TCP packets. Then an access group was created which will append that list to which was created the access group.Later I have also added an DMZ server too it which will have an security level of 50.
  
## 10. Cisco IPSec VPN Topology
![image](https://user-images.githubusercontent.com/60734787/147508344-cec14c34-661c-4059-b687-89782c9e831d.png)
I have configured the lab topology by giving the appropriate IP address and the static route.Then configure the static route for the workstations on both sides to communicate with each other. Then once that part was done, we moved to the configure the domain name itns-AS6903.local and then we created an isakmp policy with the given parameters.After that the pre-shared key was given to the IP address of the external router along with the key Secret55.Once the key was shared, the Access-list was created according to the incoming and outgoing traffic.Then IPSec was created with the transform-set of parameters.At the end, we have to map the crypto to all the resources created.The map will include the peer ip address, Access-list, and the IPsec transform-set created earlier.This map is to be implemented with the interface on a router.

## 11. Cisco Remot Access VPN IPSec Topology
![image](https://user-images.githubusercontent.com/60734787/147508905-5e2dabf3-1c38-4d80-9467-a905f7b74c8e.png)
First, I have configured the topology, then I assign the ip address and the naming convention.Later assign the IP address to all the networking devices along with the static route for their communication.After that we need to configure the remote gateway.First, the DNS domain name was created.Then the pool was created with the ip address from a range of 10.174.131.100 to 10.174.131.150. Later on an aaa model was created along with the authorization and authentication list.Then ISAKMP policy was created along with the given parameters.As well as the IPSec Transform-set was created.This also includes the dynamic crypto map and the reverse route.Later on the They all were mapped together with the crypto map.
- The group name is ITNS_AS6903
- The group key is Secret55
- Server IP 10.174.133.2
- Username AS6903
- Password Secret55.
  
  ## It Was Really Fun Developing and Configuring Network Topologies

  

