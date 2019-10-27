# ISO8601 DateTime Format Migration

Since **Octopussy 1.0rc1**, Octopussy uses **ISO8601** DateTime Format.

## Changes

*RSYSLOG_TraditionalFileFormat* is now commented in */etc/rsyslog.conf*:

	#$ActionFileDefaultTemplate RSYSLOG_TraditionalFileFormat

Then, your logs will be now formated like this:

	2010-09-08T10:09:33.009922+01:00 <device> <message>

instead of 

	Sep  8 10:09:33 <device> <message>

In order to handle this new format:

  * a new type has been added in [types.xml](http://syslog-analyzer.svn.sourceforge.net/viewvc/syslog-analyzer/tags/Octopussy-1.0rc1/var/lib/octopussy/conf/types.xml?revision=428&view=markup)
  * message patterns in [all services](http://syslog-analyzer.svn.sourceforge.net/viewvc/syslog-analyzer/tags/Octopussy-1.0rc1/var/lib/octopussy/conf/services/) have been modified to match the new datetime format. (<@DATE_TIME_SYSLOG:datetime@> replaced by <@DATE_TIME_ISO:datetime@>) 


## Convert your old logs

You can convert your logs in old format with the **octo_syslog2iso8601.pl** program:

	octo_syslog2iso8601.pl --device <device> --service <service> --timezone <+/-HH:MM>
