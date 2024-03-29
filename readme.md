Chef Server Kitchen
===================

A [Chef Solo](http://docs.opscode.com/chef_client.html) kitchen for setting up a 
[Node.js](http://community.opscode.com/cookbooks/nodejs), [Nginx](http://community.opscode.com/cookbooks/nginx),
and [MongoDB](http://community.opscode.com/cookbooks/mongodb) development server.

## Requirements

Ruby and RubyGems
    
    # Red Hat / CentOS - http://wiki.opscode.com/display/chef/Installing+Chef+Client+on+CentOS
    yum install ruby ruby-devel ruby-ri ruby-rdoc ruby-shadow gcc gcc-c++ automake autoconf make curl dmidecode -y

    # Ubuntu / Debian - http://wiki.opscode.com/display/chef/Installing+Chef+Client+on+Ubuntu+or+Debian
    apt-get install ruby ruby-dev libopenssl-ruby rdoc ri irb build-essential wget ssl-cert curl -y
    
[Chef Solo Gem](http://wiki.opscode.com/display/chef/Installing+Chef+Client+and+Chef+Solo)
    
    gem install chef --no-ri --no-rdoc
    
[Knife Solo Gem](https://github.com/matschaffer/knife-solo)
    
    gem install knife-solo --no-ri --no-rdoc
    
[Librarian Chef](https://github.com/applicationsonline/librarian)
    
    gem install librarian --no-ri --no-rdoc
    

## Usage

### Download this kitchen
    
    git clone git://github.com/nickbarth/Development-Server-Kitchen.git
    
### Download cookbooks
    
    librarian-chef install
    
### Setup your connection (Optional)
    
    # vim ~/.ssh/config
    Host server
      User root
      Hostname x
      port 22

    # setup password-less ssh logins
    ssh-keygen
    ssh-copy-id -i ~/.ssh/id_rsa.pub root@server

### Prepare server and install cookbooks

    knife solo bootstrap server

### Debug cookbooks (if needed)
    
    ssh server
    cd /tmp/chef-solo/
    chef-solo -c /tmp/chef-solo/solo.rb -j /tmp/chef-solo/nodes/server.json

### Setup complete

You should now have a fully functional server setup with all specified [cookbooks](http://community.opscode.com/). 



