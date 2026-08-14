<h1>Network Segmentation Project</h1>
<h3> Mapping the ISO27001 Segregation of network control to the protect function of the NIST CSF</h3>
<P>This document presents the technical design and implementation of a departmental network segmentation project, simulated entirely within an Oracle VirtualBox lab environment. The project demonstrates the application of subnetting (CIDR/VLSM) principles to divide a single network block into four logically and technically isolated departmental subnets:</P>
  <OL>
  <LI>Information Technology (IT)</LI>
  <LI>Finance</LI>
 <LI>audit</LI>
 <LI>Procurement.

<p>The base network 10.0.2.0/24 was subdivided into four equal-sized /26 subnets, each providing 62 usable host addresses — comfortably accommodating the lab's per-department device count while leaving headroom for future growth. Network isolation was implemented using VirtualBox's NATNetwork feature, creating four independent virtual networks, each acting as the equivalent of a separate VLAN or physical network segment in a production environment.</p>

<p>Twelve virtual machines were deployed across the four subnets — two employee workstation VMs and one server VM per department — for a total of 8 workstations and 4 servers. Each VM's network adapter was explicitly attached to its corresponding
