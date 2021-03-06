# Introduction to Software Defined Networking (SDN):
You don't need human (and even network automation tools which use CLI)
to configure the entire network; you create a virtual machine, and the
entire network behind the scene will be configured for us.

With SDN, we use a central controller for the control plane. Depending
on the vendor’s SDN solution, this could mean that the SDN controller
takes over the control plane 100% or that it only has insight in the
control plane of all network devices in the network. The SDN controller
could be a physical hardware device or a virtual machine.

There are some advantages and disadvantages of having a distributed vs
a central control plane. One of the advantages of having a central
controller is that we can configure the entire network from a single
device. This controller has full access and insight of everything that
is happening in our network.

The SDN controller uses two special interfaces:
* **Southbound interface (SBI):** The SDN controller has to communicate with
our network devices in order to program the data plane. This is done
through the southbound interface. This is not a physical interface but
a software interface, often an API (Application Programming Interface).
Some popular southbound interfaces are:
    * OpenFlow: Open source
    * Cisco OpFlex: Open source
    * CLI: Cisco offers APIC-EM which is an SDN solution for the current
    generation of routers and switches. It uses protocols that are
    available on current generation hardware like telnet, SSH, and SNMP

* **Northbound interface (NBI):** This allows a network administrator to
access the SDN to configure it or to retrieve information from it.
This could be done through a GUI but it also offers an API which allows
other applications access to the SDN controller.  You can use NBI to
write scripts and automate your network administration.

SDN controllers typically use a REST API(Representational State
Transfer).
The REST API uses HTTP messages to send and receive information between
the SDN controller and another application. The two most used data
formats are JSON and XML.
<img src="https://user-images.githubusercontent.com/31813625/32898743-f7cb7b38-cab6-11e7-887f-f76b4730a23f.png" width="430" height="446" />
