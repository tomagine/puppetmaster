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

----------------------------------------------------------
.... UNDER CONSTRUCTION ....
----------------------------------------------------------

CPU type goodies:

grep "vmx" /proc/cpuinfo   ... if output is non-empty -> CPU supports Intel-VT 
grep "svm" /proc/cpuinfo   ... if output is non-empty -> CPU supports AMD-V
grep " lm " /proc/cpuinfo  ... if output is non-empty -> CPU supports 64-bit


KSM (Kernel Same Page Merging) goodies:

grep KSM /boot/config-`uname -r`  ... if output is 'CONFIG_KSM=y' -> KSM is supported
cat /sys/kernel/mm/ksm/run        ... checks if KSM is active (output==0|1)
echo 1 > /sys/kernel/mm/ksm/run   ... turns on KSM
echo 2 > /sys/kernel/mm/ksm/run   ... turns off KSM

(*) put the 'echo 1>/sys/kernel/mm/ksm/run' in /etc/rc.local to keep the setting after reboot

KVM installation:

# as root:
yum install qemu-kvm qemu-kvm-extras

