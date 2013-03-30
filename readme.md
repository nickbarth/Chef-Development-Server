Development Server Kitchen
==========================

Chef recipes to serve up a Node.js development environment.

## Requirements

Ruby and RubyGems
    
    yum install ruby
    apt-get install ruby
    brew install ruby
    
[Chef Solo Gem](http://wiki.opscode.com/display/chef/Installing+Chef+Client+and+Chef+Solo)
    
    gem install chef --no-ri --no-rdoc
    
[Knife Solo Gem](https://github.com/matschaffer/knife-solo)
    
    gem install knife-solo --no-ri --no-rdoc
    
[Librarian Chef](https://github.com/applicationsonline/librarian)
    
    gem install librarian --no-ri --no-rdoc
    

## Usage

Download this kitchen
    
    git clone git://github.com/nickbarth/Development-Server-Kitchen.git
    
Download cookbooks
    
    librarian-chef install
    
Setup your connection (Optional)
    
    # vim ~/.ssh/config
    Host matrix
      User root
      Hostname x
      port 22
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
