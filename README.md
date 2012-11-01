nagios-plugins
==============

Various Nagios / Icinga plugins I created or changed

pmp-check-pt-table-checksum-freshness
-------------------------------------

Checks how 'fresh' your checksum table is on your MySQL slave. Based on and similar to [`pmp-check-pt-table-checksum`](http://www.percona.com/doc/percona-monitoring-plugins/nagios/pmp-check-pt-table-checksum.html) (version 1.0.1).

For example, run it with the options `-w 24 -c 72` to raise a WARNing if one or more tables haven't been checksummed within 24 hours, or, to raise a CRITical-level warning if more than 72 hours have passed.

Other behavioural changes compared to `pmp-check-pt-table-checksum`:
* If the checksum table doesn't exists, it raises an UNKnown error (instead of OK).
* Use `/bin/bash` as interpreter (instead of `/bin/sh`). See [LP #1071802](https://bugs.launchpad.net/percona-monitoring-plugins/+bug/1071802).

Tested with Icinga 1.8.1 on Ubunu 12.04.
