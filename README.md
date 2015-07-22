#### Get it up and run
##### Setup Environment
- Install Vagrant
- Install Virtualbox
```
git clone https://github.com/ehudthelefthand/simple-magento-vagrant.git
cd ./simple-magento-vagrant
vagrant up
```

##### Install this module using modman
  * Don't have modman yet? Don't worry open your termial and put this in.
```
bash << (curl -s -L https://raw.github.com/colinmollenhour/modman/master/modman-installer)
source ~/.profile
```

  * Then...

```
cd [Your Magento Directory] // If you use "simple-magento-vagrant". It should be in the ./simple-magento-vagrant/httpdocs
modman init
modman clone https://github.com/ehudthelefthand/odbgift-shop-base.git
```
