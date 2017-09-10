# How to use steps :

Install Rally on your Box 

 Instalation Steps : 

   wget -q -O- https://raw.githubusercontent.com/openstack/rally/master/install_rally.sh | bash
   
   or using curl:
   
   curl https://raw.githubusercontent.com/openstack/rally/master/install_rally.sh | bash

Source OpenRC:

     $ . openrc admin admin

Create New deployment for this cloud:

    $ rally deployment create --fromenv --name=existing
 
Check for Environment status:

    $ rally deployment check

Start Rally Test by cloning this repo:

    $ git clone https://github.comcast.com/cdodda/rally.git

Edit variables file as per your use case:

    $ vim variables.yaml

Start Rally test:

    $ rally task start openstack.yaml --task-args-file variables.yaml

Get HTML output:

    $ rally task report --out=report1.html --open

