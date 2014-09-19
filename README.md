Puppet Master Profile Script
============================

The puppet master profile script generates a .tz file that includes information
about how a master is running.

How to use
----------

Download the repository and place the `profile.rb` on the puppet master. Start
(or restart) your master with the `debug` and `profile` options enabled. You may
also need to specify a `logdest` for the puppet logs to be output into a file.
After running your puppet master like this for a few hours run the `profile.rb`
script and pass in the log file outputted by puppet master as an argument. Follow
the on screen prompts to generate the .tz file and email this file to
[britt@puppetlabs.com](mailto:britt@puppetlabs.com).

About the Information
---------------------

The information collected should not contain any identifiable information but
information about the system itself. The script collects this information using
Facter and Puppet.

The information collected is listed below.

  - Facter Facts Collected
    - architecture
    - facterversion
    - hardwareisa
    - hardwaremodel
    - is_virtual
    - kernel
    - kernelversion
    - memoryfree_mb
    - memorysize_mb
    - os
    - processors
    - puppetversion
    - rubyversion
    - sp_cpu_type
    - sp_l2_cache_core
    - sp_l3_cache
    - sp_machine_model
    - sp_machine_name
    - swapfree_mb
    - swapsize_mb
    - virtual
  - Puppet Module Count
  - Number of Certificates
  - Type of Node Classifier Used
  - Approximate Number of Nodes managed by Puppet Master
  - Puppet Master Profile Data