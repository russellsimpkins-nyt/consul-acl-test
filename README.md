## consul-test

This is a rather barebones set up of vagrant files to test the functionality of consul clusters and agents while implementing ACLs. You may have to point to another vagrant box. These Vagrantfiles are pointing to centos66 boxes.

Issue your vagrant up in consul1, 2 and 3. Then on each box you can start the nodes with

```
vagrant ssh
sudo su -
cd /vagrant
./start
```

It could be more elegant, but this way you get to watch the logs. All boxes have the consul ui running

http://192.168.33.10:8500/ui
http://192.168.33.11:8500/ui
http://192.168.33.12:8500/ui
http://192.168.33.13:8500/ui

You can't simply configure the cluster to have ACLs. To add ACLs you can use the UI on .11 or you can use this tool

http://github.com/russellsimpkins/consul-acl-mgr



