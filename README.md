#### Get it up and run
##### Setup Environment
- Install Vagrant
- Install Virtualbox
- Download [simple-magento-vagrant](https://github.com/ehudthelefthand/simple-magento-vagrant/archive/master.zip). You will get the file name "simple-magento-vagrant-master.zip". Just unzip and rename it as you wish. In this case I will call it "simple-magento-vagrant".
```
$ cd ./simple-magento-vagrant
$ vim Vagrantfile
// On line 5. change sample_data = "true" to sample_data = "false" or leave it incase you need sample data
// Save changed
$ vagrant up
```

##### Install this module using modman
  * Don't have modman yet? Don't worry open your termial and put this in.
```
bash < <(wget -q --no-check-certificate -O - https://raw.github.com/colinmollenhour/modman/master/modman-installer)
```
or
```
bash < <(curl -s -L https://raw.github.com/colinmollenhour/modman/master/modman-installer)
source ~/.profile
```

  * Then...

```
cd [Your Magento Directory] // If you use "simple-magento-vagrant". It should be in ./simple-magento-vagrant/httpdocs
modman init
modman clone https://github.com/ehudthelefthand/odbgift-shop-base.git
```

##### Restore data
Extract the this file >> httpdocs/.modman/odbgift-shop-base/data/media-20150727072348.tgz

You will get 2 folders.
- media : Copy this folder and replace it in the magento root directory
- var : You will get 1437981828_db.gz file inside. Just extract it and run the SQL file against your magento database. If you use 'simple-magento-vagrant', the database name should be 'magentodb'


Done!
