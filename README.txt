################################################################################
#
# PUPPETMASTER
#
# various snippets based on package puppet-server 
#
################################################################################


PREFACE

If you haven't heard about puppet yet: its a kind of configuration and resource
management system which scales up to typical data centers.

for more information about puppet, please check their homepage at:

http://www.puppetlabs.com/


PROJECT GOAL

Actually there is just one goal: I wanted to get used to puppet and its
usage in various scenarios (from small home setups to large grids).

TESTING ENVIRONMENT

Actually I use a Fedora 13 (livecd) setup, because this distribution can
find and install git and puppet-server automatically without any changes to 
default setup (yum repositories).

A 3-liner after installation does the job (fetch packages git and puppet-server)

# become root
su -
yum -y install git
yum -y install puppet-server

.... UNDER CONSTRUCTION ....

