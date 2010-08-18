################################################################################
#
# PUPPETMASTER
#
# various snippets based on package puppet-server 
#
################################################################################


PREFACE

If you haven't heard about puppet yet: its a kind of configuration and resource
management system which scales up from small home office installments to
data centers.

for more information about puppet, please check their homepage at:

http://www.puppetlabs.com/


PROJECT GOAL

Actually there is just one goal: I wanted to get used to puppet and its
usage in various usage scenarios.

TESTING ENVIRONMENT

Actually I use a Fedora 13 (livecd) setup, because this distribution can
find and install git and puppet-server automatically without any changes to 
to the default setup (no yum repositories tweaking necessary).

After a default installation the following 1-liner finishes the
required setup (an installed puppet-server package): 

# execute as root
yum -y install git wget puppet-server


.... UNDER CONSTRUCTION ....