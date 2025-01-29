𝗔̲𝗪̲𝗦̲ ̲𝗩̲𝗣̲𝗖̲ ̲𝗜̲𝗻̲𝘁̲𝗲̲𝗿̲𝘃̲𝗶̲𝗲̲𝘄̲ ̲𝗤̲𝘂̲𝗲̲𝘀̲𝘁̲𝗶̲𝗼̲𝗻̲𝘀̲

1. 𝗛𝗼𝘄 𝗱𝗼𝗲𝘀 𝗩𝗣𝗖 𝗽𝗲𝗲𝗿𝗶𝗻𝗴 𝘄𝗼𝗿𝗸?
VPC peering connects two VPCs for communication using private IPs. Traffic stays within AWS without transiting the internet.

2. 𝗪𝗵𝗮𝘁 𝗮𝗿𝗲 𝗿𝗼𝘂𝘁𝗲 𝘁𝗮𝗯𝗹𝗲𝘀, 𝗮𝗻𝗱 𝘄𝗵𝘆 𝗮𝗿𝗲 𝘁𝗵𝗲𝘆 𝗶𝗺𝗽𝗼𝗿𝘁𝗮𝗻𝘁?
Route tables define paths for traffic within a VPC and to external destinations (e.g., IGW, NAT).

3. 𝗜𝗻𝘁𝗲𝗿𝗻𝗲𝘁 𝗚𝗮𝘁𝗲𝘄𝗮𝘆 𝘃𝘀. 𝗡𝗔𝗧 𝗚𝗮𝘁𝗲𝘄𝗮𝘆: 
- IGW: Enables internet access for public subnet instances. 
- NAT Gateway: Provides outbound internet access for private subnet instances.

4. 𝗣𝘂𝗿𝗽𝗼𝘀𝗲 𝗼𝗳 𝗦𝗲𝗰𝘂𝗿𝗶𝘁𝘆 𝗚𝗿𝗼𝘂𝗽𝘀 𝗮𝗻𝗱 𝗡𝗔𝗖𝗟𝘀: 
- Security Groups: Instance-level rules for inbound/outbound traffic. 
- NACLs: Subnet-level, stateless rules for traffic filtering.

5. 𝗥𝗲𝘀𝘁𝗿𝗶𝗰𝘁𝗶𝗻𝗴 𝘁𝗿𝗮𝗳𝗳𝗶𝗰 𝗯𝗲𝘁𝘄𝗲𝗲𝗻 𝘀𝘂𝗯𝗻𝗲𝘁𝘀: 
Use NACLs or security group rules to limit access based on IP ranges or ports.

6. 𝗗𝗲𝘀𝗶𝗴𝗻𝗶𝗻𝗴 𝗮 𝗺𝘂𝗹𝘁𝗶-𝗿𝗲𝗴𝗶𝗼𝗻 𝗩𝗣𝗖 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲: 
- Use Transit Gateway or VPC peering for inter-region connectivity. 
- Ensure redundancy, low latency, and compliance with regulations.

7. 𝗔𝗪𝗦 𝗧𝗿𝗮𝗻𝘀𝗶𝘁 𝗚𝗮𝘁𝗲𝘄𝗮𝘆 𝘃𝘀. 𝗩𝗣𝗖 𝗣𝗲𝗲𝗿𝗶𝗻𝗴: 
- Transit Gateway: Central hub for connecting multiple VPCs and on-prem networks. 
- VPC Peering: One-to-one connection between VPCs.

8. 𝗘𝗹𝗮𝘀𝘁𝗶𝗰 𝗟𝗼𝗮𝗱 𝗕𝗮𝗹𝗮𝗻𝗰𝗲𝗿 (𝗘𝗟𝗕) 𝘄𝗶𝘁𝗵 𝗩𝗣𝗖:
Distributes incoming traffic across instances in subnets and enhances scalability and fault tolerance.

9. 𝗘𝗻𝘀𝘂𝗿𝗶𝗻𝗴 𝗵𝗶𝗴𝗵 𝗮𝘃𝗮𝗶𝗹𝗮𝗯𝗶𝗹𝗶𝘁𝘆 𝗶𝗻 𝗮 𝗩𝗣𝗖 𝗱𝗲𝘀𝗶𝗴𝗻: 
- Deploy resources across multiple Availability Zones. 
- Use redundant IGWs, NAT Gateways, and load balancers.

10. 𝗩𝗣𝗖 𝗹𝗶𝗺𝗶𝘁𝘀: 
Default limits: 5 VPCs per region, 200 subnets per VPC. Limits can be increased via AWS Support.
