nagios-plugins
==============

Various Nagios / Icinga plugins I created or changed

pmp-check-pt-table-checksum-freshness
-------------------------------------

Checks how 'fresh' your checksum table is. Based on and similar to [pmp-check-pt-table-checksum](http://www.percona.com/doc/percona-monitoring-plugins/nagios/pmp-check-pt-table-checksum.html).

By example, run it with the options `-w 24 -c 72` to raise a WARNing if one or more tables haven't been cheksummed within 24 hours, or, to raise a CRITical-level warning if more than 72 hours have passed.

Tested with Icinga 1.8.1 on Ubunu 12.04 and Percona Monitoring plugins 1.0.1.
