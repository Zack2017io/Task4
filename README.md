Firewall Configuration Task
Task Overview:
In this task, I explored how to use the firewall to control and secure network traffic. The steps included:

Listing current firewall rules.

Adding a rule to block inbound traffic on a specific port (port 23 for Telnet).

Testing the rule using Telnet to ensure the block was effective.

Adding a rule to allow SSH (port 22).

Removing the test block rule restores the firewall to its original state.

Commands/Steps Used
For Windows: Used Windows Defender Firewall GUI (Control Panel → System and Security → Windows Defender Firewall → Advanced Settings).

For Linux (UFW):

bash
Copy
Edit
sudo ufw status numbered
sudo ufw deny 23/tcp
telnet 127.0.0.1 23
sudo ufw allow 22/tcp
sudo ufw delete deny 23/tcp
Key Concepts Learned
Firewalls filter network traffic based on rules (allow/deny).

Blocking a port prevents services from accepting external connections.

SSH (port 22) is commonly allowed for secure remote access.

Testing rules helps confirm firewall effectiveness.
