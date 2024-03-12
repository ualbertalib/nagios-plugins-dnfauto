# nagios-plugins-dnfauto

* Until now, we've been using monitoring of the CentOS7 kernel version as a proxy for whether automatic patching is working.
* Let's move in to a bright new CS9-flavoured future, where the version of the kernel doesn't matter nearly as much, as whether dnf-automatic is running without errors!

## This Nagios Plugin

* ... only runs `systemctl is-failed dnf-automatic`, and returns status based on the results!
* The idea is: if dnf-automatic is not failing, Nagios should report OK status.
* And if dnf-automatic is failing, Nagios should report NOT OK
