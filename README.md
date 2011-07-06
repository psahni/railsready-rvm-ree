#Rails Ready
###Ruby and Rails setup script for Linux systems
###Distros supported:
 * Ubuntu 10.04 LTS and 10.10
 * CentOS 5.5 (utilizes the Fedora EPEL repo)

# 
###Run this on a fresh install. It WILL update your system!

###This is an unofficial fork. It WILL install RVM and it WILL install REE 1.8.7.

###To run:
  * `wget --no-check-certificate https://github.com/philtr/railsready-rvm-ree/raw/master/railsready.sh && bash railsready.sh`
  * The script will ask if you want to build Ruby from source or install RVM

###What this gives you:
  * An updated system
  * RVM running 1.8.7
  * Imagemagick
  * libs needed to run Rails (sqlite, mysql, etc)
  * Bundler, Passenger, and Rails gems
  * Git

Just install either NGINX or Apache, run passenger-install-nginx-module or passenger-install-apache-module, upload your app, point your vhost config to your apps public dir and go!

Please note: If you are running on a super slow connection your sudo session may timeout and you'll have to enter your password again. If you're running this on an EC2 or RS instance it shouldn't be problem.

# 
####Rails Ready now supports a "plugin" type system. The distro is detected and a corresponding "recipe" file is pulled down to run the distro specific setup steps. Check the recipes dir to see if your distro is supported. If you would like to add support for a system fork the repo, write a recipe, and submit a pull request. Take a look at recipes/ubuntu.sh for an idea of what to model your recipe after.

Thanks to Josh Frye ([@joshfng](https://github.com/joshfng)) for creating this handy script.
