Rhel Subscription
=========

This role manages a script that checks if rhel subscription is registered. Also writes the info for prometheus to collect with textfile collector. The directory being assumed is */var/lib/node_exporter/*.

Requirements
------------

For everything to work correctly the **subscription-manager** needs to be installed. This role does not manage that, but only runs on machines that have that binary installed.

License
-------

BSD-2-CLAUSE

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
