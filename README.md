# Project

### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly secure, in addition to restricting public to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_
- It allows for better control of the Nwtwork while also only allowing those with the propper ssh information to conntect the network.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log inforamtion and traffic.
- _TODO: What does Filebeat watch for?
-   Collects, monitors, and centralizes log inforamtion.
- _TODO: What does Metricbeat record? Monitors metrics such as CPU ussage on the system.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| RedWeb1  | Server   | 10.0.0.3   | Linux            |
| RedWeb2  | Server   | 10.0.0.4   | Linux            |
| Elk      | LogServer| 10.0.0.X   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the RedJumpBox machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- My personal IP

Machines within the network can only be accessed by RedJumpBox.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address? 
- RedJumpBox 10.0.0.1

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | My personal IP       |
| RedWeb1  | No                  | 10.0.0.4             |
| RedWeb2  | No                  | 10.0.0.4             |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?
- Reduces and maintains the network on a consistant bases without human error.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- Install the docker service.
- Run docker.
- Launch the docker countainer.

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

Note: My Azure account is curently not working. Working with the technical team now. If problem please contact me on Slack.

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- RedWeb1 -10.0.0.3
- RedWeb2 -10.0.0.4
- RedJumpBox -10.0.0.1

We have installed the following Beats on these machines:
- Filebeat and Metricbeat.

These Beats allow us to collect the following information from each machine:
- _TODO: Log and chanages made to the virtual network.

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the ansible file to proper virtual machine.
- Update the yml file to include the virtual machines on the network.
- Run the playbook, and navigate to the desired virtual machine to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
-Which file is the playbook? Where do you copy it? 
  The playbook is a yml file and needs to be copied to any virtual machine that is on the network. 
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on? Update the file on the Elk machine and also install filbebeat/metric beat on the Elk server.
- _Which URL do you navigate to in order to check that the ELK server is running?
  Not sure.
_As a **Bonus**, provide the specific commands the user will need to run to down
