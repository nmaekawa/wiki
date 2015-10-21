## vagrant

### vagrant package a vm that has private-ips

from https://github.com/mitchellh/vagrant/issues/1777

    To my point of view and what i do for my CentOS box is:

    --Each MAC should be unique, so if you have HWADDR or UUID in your box/template ifcfg-eth0 your clones will obtain the same. So you have to delete them for your box before packaging.
    --70-persistent-net.rules keeps persistent rules for net interfaces, so it should be deleted.
    --ifcfg-eth1 will be created by vagrant for every new clone, so it should be deleted from the box too.

    before packaging:
    rm -rf /etc/udev/rules.d/70-persistent-net.rules
    sed -i '/HWADDR/d' /etc/sysconfig/network-scripts/ifcfg-eth0
    sed -i '/UUID/d' /etc/sysconfig/network-scripts/ifcfg-eth0
    rm -rf /etc/sysconfig/network-scripts/ifcfg-eth1

    You create the box with "vagrant package" and you should have any issues while create new hosts based on that box

