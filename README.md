# geodjango environment

* adapted from https://github.com/caffeinehit/chef-geodjango Thank you guys!

Out of the box environment for
[Geo Django](https://docs.djangoproject.com/en/1.3/ref/contrib/gis/)

Using
[Chef](http://wiki.opscode.com/display/chef/Home)
[Vagrant](http://vagrantup.com/)


What it builds/prepares:
apt - updates
apt-upgrade upgrades vm packages
build-essential
database - postgres + postgis
geos - installs
proj4 - installs
git - installs
nginx - installs
python-pip - installs
python-virtualenv - installs
virtualenvwrapper - installs and adds virtualenvwrapper to profile
screen - installs
vim - installs
virtualbox-guesttools - installs guest tools so that shared folders work

Make sure you customize `cookbooks/database/attributes/default.rb`
to use your actual database user and database name.

To try the setup out, do:

	$ git clone https://github.com/eamonnfaherty/geodjango-env.git
	$ cd chef-geodjango
	$ vagrant up

That'll give you a virtual machine with a database ready to go.