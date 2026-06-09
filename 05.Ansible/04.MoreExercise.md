Recommended to do after you've learned at least loops.

Run on 2 nodes:
1. Deploy nginx
2. Pass a Jinja template of nginx configuration file:
    1. Port as a group parameter
    2. root as a host parameter
3. Pass a different html file to each node/server
4. Check outside HTTP access* to the servers using the parameters you configured with - must be a part of the playbook!

* Notice - you may encounter a problem accessing your site due to firewall rules. Run the following commands on the two nodes:
systemctl stop firewalld; setenforce 0 
This will turn off the firewall service and SELinux. It is a not recommended temporary solution, but you will learn about it later on in Networking.

Be creative! Add error handling, roles and etc. enjoy!
