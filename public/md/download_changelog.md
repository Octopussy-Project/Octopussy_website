### Octopussy 1.0.16 ###
*release date: Sat, 03 Jun 2017*

  * Major Security fixes:
    * [Protection against CSRF attacks](https://github.com/sebthebert/Octopussy/issues/636)
    * [Cookie Security](https://github.com/sebthebert/Octopussy/issues/637)
    * [Password Policy Rules](https://github.com/sebthebert/Octopussy/issues/635#issuecomment-246844717) added
  * [Apache::ASP with Apache 2.4 issue (remote_ip)](https://github.com/sebthebert/Octopussy/commit/287342bd8a5a9388d2450a2380e6c2bbe2db5440) fixed
  * Code cleaning
  * Debian package and installation script updated

### Octopussy 1.0.14 ###
*release date: Tue, 15 Apr 2014*

  * Bugfix [#586](https://github.com/sebthebert/Octopussy/issues/586), [#587](https://github.com/sebthebert/Octopussy/issues/587) & [#588](https://github.com/sebthebert/Octopussy/issues/588): Fixing read_dir issues
  * Code cleaning
  * Services 'ARPWatch' & 'Ntp' updated

### Octopussy 1.0.13 ###
*release date: Wed, 26 Mar 2014*

  * Bugfix [#583](https://github.com/sebthebert/Octopussy/issues/583): Fixing octo_parser bugs introduced in Octopussy 1.0.12

### Octopussy 1.0.12 ###
*release date: Sat, 22 Mar 2014*

  * Major performance improvement when a lot of octo_parser start at the same time (Issue [#576](https://github.com/sebthebert/Octopussy/issues/576))
  * Small security fix on login page
  * Huge code cleaning & rebuilding to prepare CPAN integration
  * Service 'Nagios' updated to handle Nagios3 logs

### Octopussy 1.0.11 ###
*release date: Sun, 16 Feb 2014*

  * Bugfix [#554](https://github.com/sebthebert/Octopussy/issues/554): Problem with the 'mysql --exec' in postinstall scripts
  * Bugfix [#557](https://github.com/sebthebert/Octopussy/issues/557): Fixing the Report Editing issues with columns & columns_name
  * Bugfix [#565](https://github.com/sebthebert/Octopussy/issues/565): Add Zulu Time Zone in ISO8601 Datetime regex
  * Feature Request [#558](https://github.com/sebthebert/Octopussy/issues/558): Ability to configure a delay between octo_parser starts
  * Feature Request #134: Possibility to set only City in Device Location
  * Feature Request [#576](https://github.com/sebthebert/Octopussy/issues/576): Big work on reducing IO usage when octo_parser starts
  * Turkish translation added
  * Work to migrate from Date::Manip to Time::Piece reducing memory usage of
    octo_logrotate, octo_reporter & octo_scheduler of 3.5 MBytes
  * Code cleaning
  * Services 'Ansible', 'DragonFly_Mail_Agent' added
  * Services 'Cisco_Switch' & 'Keepalived' updated

### Octopussy 1.0.10 ###
*release date: Thu, 18 Jul 2013*

  * [Bugfix #358](https://sourceforge.net/p/syslog-analyzer/bugs/358/): no NSCA alerts and octo_parser crash (Can't store REGEXP bug)
  * [Bugfix #359](https://sourceforge.net/p/syslog-analyzer/bugs/359/): Report Edition is not working with 'ofc type' report
  * [Feature Request #128](https://sourceforge.net/p/syslog-analyzer/feature-requests/128/): One message only for every Jabber alert
  * [Support Request #77](https://sourceforge.net/p/syslog-analyzer/support-requests/70/): Fixing Device::Valid_Name function to handle hostname starting with digit(s) (RFC 1123)
  * Minor improvement in octo_sender
  * octo_tool backup before installation also for INSTALL.sh now
  * Start using [Devel::Cover](https://metacpan.org/module/Devel::Cover) reporting to improve test suite

### Octopussy 1.0.9 ###
*release date: Fri, 24 May 2013*

  * [Bugfix #347](https://sourceforge.net/p/syslog-analyzer/bugs/347/): Cannot create messages for logs with bad mail dir
  * [Bugfix #353](https://sourceforge.net/p/syslog-analyzer/bugs/353/): Problem running reports on more than one device
  * Bugfixing log compression issues
  * Bugfixing Web Interface issues reported on [Google+](https://plus.google.com/113385322268951381996/posts/jKcDgysHBic)
  * Minor bugfixes on octo_parser and Octopussy::Alert
  * Fixing major security issues in Web interface
  * Improving Web Interface
  * Invalid Devicename are not created anymore by octo_dispatcher

### Octopussy 1.0.8 ###
*release date: Tue, 26 Feb 2013*

  * [Bugfix #314](https://sourceforge.net/p/syslog-analyzer/bugs/314/): Fixing the LDAP Users authentication
  * [Bugfix #320](https://sourceforge.net/p/syslog-analyzer/bugs/320/): Logs Viewer issues
  * [Feature Request #119](https://sourceforge.net/p/syslog-analyzer/feature-requests/119/): No space in msgid
  * [Feature Request #120](https://sourceforge.net/p/syslog-analyzer/feature-requests/120/): You can click on devicename in 'Last minute messages box' to go to 'Device Dashboard' page
  * [Support Request #70](https://sourceforge.net/p/syslog-analyzer/support-requests/70/): Fixing Maps plugin documentation link
  * Bugfixing new Octopussy version checker
  * Bugfixing AAT::LDAP minor issue
  * LDAP Request now only on user defined fields

### Octopussy 1.0.7 ###
*release date: Sun, 20 Jan 2013*

  * 4 Services updated
  * New Service 'IBM_Cognos' created
  * Adding no_trans parameter to AAT:Label (1/2)
  * Working on Testing Suite
  * Now, you can set Contacts fields from LDAP Contacts fields
  * Bugfix #3574577: 500 Internal server error because of unknown translation
  * Bugfix #3574616: '500 Internal server error' because of invalid devicename
    in Device::Parse_Status
  * Bugfix #3580468: Alert edition broken
  * Bugfix #3584230: Alerts are not sent by XMPP anymore
  * [Bugfix #328](https://sourceforge.net/p/syslog-analyzer/bugs/328/): Report can not be deleted
  * [Bugfix #179](https://sourceforge.net/p/syslog-analyzer/bugs/179/): types.xml updated
  * [Bugfix #267](https://sourceforge.net/p/syslog-analyzer/bugs/267/): Name 'Win32::Locale::Lexicon' used only once error messages
  * [Bugfix #332](https://sourceforge.net/p/syslog-analyzer/bugs/332/): Dispatcher stopped
  * [Bugfix #314](https://sourceforge.net/p/syslog-analyzer/bugs/314/): Fixing various LDAP problems
  * [Bugfix #275](https://sourceforge.net/p/syslog-analyzer/bugs/275/): Can't Save Search Templates
  * Bugfixing Servicegroup adding in device_services.asp page
  * Fixing minor issues in octo_reporter & octo_scheduler
  * Fixing 'white column' when there wasn't Service in device_services.asp page
  * Feature Request #1831840: Hide unused Services in Services selector
  * Feature Request #3513127: Now you can specify timestamp to start from a
    specific date in Logs Wizard and also add a new pattern to a service by
    copy/pasting it
  * Feature Request #3517497: Better NET_INTERFACE type

### Octopussy 1.0.6 ###
*release date: Thu, 06 Sep 2012*

  * octo_tool program updated to handle backups
  * References to 8pussy.org have been replaced by octopussy.pm
  * Services & Tables updates
  * [Feature Request #3538049](https://sourceforge.net/tracker/?func=detail&aid=3538049&group_id=154314&atid=791287): Ability to change banner image
  * [Feature Request #3560370](https://sourceforge.net/tracker/?func=detail&aid=3560370&group_id=154314&atid=791287): Move and copy of patterns between Services
  * [Feature Request #3510112](https://sourceforge.net/tracker/?func=detail&aid=3510112&group_id=154314&atid=791287): Now LDAP Users have the same preferences/roles than local users
  * Bugfixes on Debian packaging update
  * Bugfixes for LDAP Contacts & Users
  * Bugfix Loglevel/Taxonomy unknown parameter for octo_extractor
  * [Bugfix #3541753](https://sourceforge.net/tracker/?func=detail&aid=3541753&group_id=154314&atid=791284): Removes RRD error messages
  * [Bugfix #3519341](https://sourceforge.net/tracker/?func=detail&aid=3519341&group_id=154314&atid=791284): msgid & taxo stats not in cache anymore when stats are disabled
  * [Bugfix #3555337](https://sourceforge.net/tracker/?func=detail&aid=3555337&group_id=154314&atid=791284): Allow dots in devicename and devicegroupname

### Octopussy 1.0.5 ###
*release date: Mon, 25 Jun 2012*

  * [Bugfix #3537131](https://sourceforge.net/tracker/?func=detail&aid=3537131&group_id=154314&atid=791284): Problem with Device with only ip address after Octopussy 1.0.4 update
  * Updates on 'Valid_Name' functions and Test Suite

### Octopussy 1.0.4 ###
*release date: Thu, 21 Jun 2012*

  * Fixing minor WebUI bugs for ReadOnly users
  * Cache clearing feature added to octo_tool program
  * Filtering Web pages entries to avoid XSS attacks
  * [Feature Request #3528557](https://sourceforge.net/tracker/?func=detail&aid=3528557&group_id=154314&atid=791287): Bigger Device & Service selector in Alert Creation/Edition Web pages

### Octopussy 1.0.3 ###
*release date: Wed, 04 Apr 2012*

  * New program octo_tool added to do simple tasks
    (for now, service_clone & table_clone)
  * [Feature Request #3477812](https://sourceforge.net/tracker/?func=detail&aid=3477812&group_id=154314&atid=791287): Ability to create an alert when Octopussy receives new unknown logs
  * [Feature Request #3477752](https://sourceforge.net/tracker/?func=detail&aid=3477752&group_id=154314&atid=791287): You can now be redirected to Wizard page or Service page after Message pattern creation
  * [Feature Request #3428757](https://sourceforge.net/tracker/?func=detail&aid=3428757&group_id=154314&atid=791287): You can now enable/disable logs compression in 'Device Services' web page
  * [Feature Request #3416032](https://sourceforge.net/tracker/?func=detail&aid=3416032&group_id=154314&atid=791287) (1/2): Fixing the ordering of the status in 'Alerts Viewer' page
  * [Feature Request #3416032](https://sourceforge.net/tracker/?func=detail&aid=3416032&group_id=154314&atid=791287) (2/2): 'Delete from Database' button added to 'Alerts Viewer' page
  * [Feature Request #3488473](https://sourceforge.net/tracker/?func=detail&aid=3488473&group_id=154314&atid=791287): Virtual Hosts added for Device Types/Models
  * [Feature Request #3416018](https://sourceforge.net/tracker/?func=detail&aid=3416018&group_id=154314&atid=791287): Now, you can set mimimum delay between 2 alerts
  * [Feature Request #3492003](https://sourceforge.net/tracker/?func=detail&aid=3492003&group_id=154314&atid=791287): Edit option for contacts
  * [Bugfix #3485331](https://sourceforge.net/tracker/?func=detail&aid=3485331&group_id=154314&atid=791284): Handling invalid Octopussy plugin
  * [Bugfix #3506010](https://sourceforge.net/tracker/?func=detail&aid=3506010&group_id=154314&atid=791284): Manual pages for Octopussy Perl modules were generated with incorrect filename by 'packaging_from_svn.pl' script
  * Bugfixing the unrefreshed date in 'Selector_date'
  * Bugfixing the missing 'use AAT::Syslog;' in Octopussy/Plugin.pm

### Octopussy 1.0.2 ###
*release date: Mon, 19 Dec 2011*

  * Translation updates to fix 'Internal Server Error'
  * [Bugfix #3439106](https://sourceforge.net/tracker/?func=detail&aid=3439106&group_id=154314&atid=791284): Many bugs in Restricted Logs Viewer
  * [Bugfix #3455262](https://sourceforge.net/tracker/?func=detail&aid=3455262&group_id=154314&atid=791284): Fixing octo_logrotate issues
  * [Bugfix #3452230](https://sourceforge.net/tracker/?func=detail&aid=3452230&group_id=154314&atid=791284): Services are now correctly selected in 'user_restrictions.asp' page

### Octopussy 1.0.1 ###
*release date: Tue, 15 Nov 2011*

  * Cisco_ASA & MySQL Services updates
  * [Bugfix #3433578](https://sourceforge.net/tracker/?func=detail&aid=3433578&group_id=154314&atid=791284): octo_uparser didn't work since release 1.0rc6
  * Bugfixing Translations issues
  * Bugfixing missing 'favicon.ico' in apache logs

### Octopussy 1.0 ###
*release date: Fri, 11 Nov 2011*

  * Mac OS X related Services updates
  * 'Octopussy restart from Web Interface' feature has been disabled because it was buggy
  * Bugfixing '-- ANY --' selection in 'logs_viewer.asp' page
  * [Bugfix #3432668](https://sourceforge.net/tracker/?func=detail&aid=3432668&group_id=154314&atid=791284): Unable to enable/disable statistics in 'device_services.asp' page
  * [Bugfix #3434572](https://sourceforge.net/tracker/?func=detail&aid=3434572&group_id=154314&atid=791284): Bug in Waiting_For_Process_Already_Running function
  * [Bugfix #3435120](https://sourceforge.net/tracker/?func=detail&aid=3435120&group_id=154314&atid=791284): Dispatcher now drops line (and don't create a new invalid device) if the device name is not valid

### Octopussy 1.0rc6 ###
*release date: Wed, 02 Nov 2011*

  * Many Services added and updated
  * [Feature Request #3391894](https://sourceforge.net/tracker/?func=detail&aid=3391894&group_id=154314&atid=791284): You can now add a 'Device Filtering Regexp' to handle only devices you really want
  * [Feature Request #3428291](https://sourceforge.net/tracker/?func=detail&aid=3428291&group_id=154314&atid=791287): Sort Contacts by 'id' by default
  * [Feature Request #3421855](https://sourceforge.net/tracker/?func=detail&aid=3421855&group_id=154314&atid=791287): Dynamic DeviceGroup configuration displayed in tooltip when the mouse is over 'Dynamic' type
  * [Bugfix #3411747](https://sourceforge.net/tracker/?func=detail&aid=3411747&group_id=154314&atid=791284): Plugin check-octopussy missing use statement
  * [Bugfix #3418377](https://sourceforge.net/tracker/?func=detail&aid=3418377&group_id=154314&atid=791284): Fixing security issues in 'index.asp', 'alerts.asp', 'devices.asp', 'storages.asp', 'alerts_viewer.asp' & 'world_statistics.asp' web pages
  * [Bugfix #3414351](https://sourceforge.net/tracker/?func=detail&aid=3414351&group_id=154314&atid=791284): fixing 'invalid dirhandle' messages in octo_logrotate when directory is missing
  * [Bugfix #3140040](https://sourceforge.net/tracker/?func=detail&aid=3140040&group_id=154314&atid=791284): GTalk/XMPP issues
  * Bugfix: Fixing XMPP test message sent twice
  * [Bugfix #3431929](https://sourceforge.net/tracker/?func=detail&aid=3431929&group_id=154314&atid=791284): Wrong order between lower/uppercase in Services list
  * [Bugfix #3412966](https://sourceforge.net/tracker/?func=detail&aid=3412966&group_id=154314&atid=791284): Octopussy can now handle Regexp::Assemble failures

### Octopussy 1.0rc5 ###
*release date: Sat, 10 Sep 2011*

  * Starting JQueryfication of the Web Interface
  * Modification of Debian/Ubuntu apache2.conf file to use Snakeoil SSL Certificate in order to simplify Octopussy installation
  * [Bugfix #3402213](https://sourceforge.net/tracker/?func=detail&aid=3402213&group_id=154314&atid=791284): Fix error message in octo_world_stats
  * [Bugfix #3391894](https://sourceforge.net/tracker/?func=detail&aid=3391894&group_id=154314&atid=791284): Ability to enable/disable 'Automatic Device Creation'
  * [Feature Request #3402215](https://sourceforge.net/tracker/?func=detail&aid=3402215&group_id=154314&atid=791287): Option to quiet cron tasks
  * Minor Bugfixes
  * Fixing Debian FHS policy
  * Fixing lintian issues

### Octopussy 1.0rc4 ###
*release date: Wed, 06 Jul 2011*

  * Now you can choose between Rsyslog and Syslog-ng to receive your logs
  * DateTime::Format::Strptime & Term::ProgressBar added to Perl Module Requirements
  * Restricted Logs Viewer display bug fixed
  * Better octo_pusher
  * Now, there is also a form to Create a New Service at the top of the services.asp page
  * Updates on 8pussy.org are now daily updated from Subversion repository
  * Homepage link added to 'Top Menu' in WebGUI
  * Fixing Debian 6 installation problem

  * [Bugfix #3184249](https://sourceforge.net/tracker/?func=detail&aid=3184249&group_id=154314&atid=791284): prototype.js added for OpenFlashChart
  * [Bugfix #3184259](https://sourceforge.net/tracker/?func=detail&aid=3184259&group_id=154314&atid=791284): AAT::Schedule::Match replaced by Octopussy::Schedule::Match
  * [Bugfix #3188874](https://sourceforge.net/tracker/?func=detail&aid=3188874&group_id=154314&atid=791284): Sending alerts to multiple recipients or with empty subect/body failed
  * Bugfix <del>#3285704</del>: Translations issues with undefined msgid in .po files
  * [Bugfix #3303598](https://sourceforge.net/tracker/?func=detail&aid=3303598&group_id=154314&atid=791284): Msgid statistics in Service divided by 2 because of total
  * [Bugfix #3087438](https://sourceforge.net/tracker/?func=detail&aid=3087438&group_id=154314&atid=791284): Missing _MSG_DEVICEGROUP_ALREADY_EXISTS
  * [Bugfix #3309458](https://sourceforge.net/tracker/?func=detail&aid=3309458&group_id=154314&atid=791284): Filtering in logs viewer is not working with 'Unknown'

### Octopussy 1.0rc3 ###
*release date: Tue, 15 Feb 2011*

  * Better Test Suite
  * Code cleanning

  * [Bugfix #3166138](https://sourceforge.net/tracker/?func=detail&aid=3166138&group_id=154314&atid=791284): Fixing major problems with old syslog datetime format
  * [Bugfix #3176376](https://sourceforge.net/tracker/?func=detail&aid=3176376&group_id=154314&atid=791284) & [Support Request #3078102](https://sourceforge.net/tracker/?func=detail&aid=3078102&group_id=154314&atid=791285): Specific sysctl conf added to raise 'fs.inotify.max_user_instances'

### Octopussy 1.0rc2 ###
*release date: Wed, 26 Jan 2011*

  * Rsyslog UDP/TCP reception now forced in installation scripts
  * Now 'export APACHE_RUN_DIR' in /usr/sbin/directory (needed for Apache2 configuration in some distribs)

  * [Bugfix #3160987](https://sourceforge.net/tracker2/?func=detail&aid=3160987&group_id=154314&atid=791284): Fixing major issue on ISO8601 DateTime Regexp
  * [Bugfix #3067657](https://sourceforge.net/tracker2/?func=detail&aid=3067657&group_id=154314&atid=791284): Wrong scheduling matching fixed and Test Suite updated
  * Minor Bugfixes

### Octopussy 1.0rc1 ###
*release date: Fri, 14 Jan 2011*

  * WARNING: ISO8601 DateTime format migration ! (see '[ISO8601 DateTime Format Migration](/documentation/howtos/iso8601migration)')
  * Alerts name are now limited to [-_a-zA-Z0-9] characters
  * Contacts id are now limited to [-_a-zA-Z0-9] characters
  * Services name are now limited to [-_a-zA-Z0-9] characters
  * Better Test Suite
  * Minor modifications to fix Debian Lintian errors

  * Bugfix: Fixing file rights problems in Debian installation
  * Bugfix: Missing translation fixed in AAT_Selector_DateTime_Simple.inc
  * [Bugfix #3061992](https://sourceforge.net/tracker2/?func=detail&aid=3061992&group_id=154314&atid=791284): 0GIN% missing in Octopussy logs
  * [Bugfix #3065906](https://sourceforge.net/tracker2/?func=detail&aid=3065906&group_id=154314&atid=791284): Bug in Get_Mail_Addresses function in octo_sender
  * [Bugfix #3064879](https://sourceforge.net/tracker2/?func=detail&aid=3064879&group_id=154314&atid=791284): Authentication problems after user preferences changes
  * [Bugfix #3109566](https://sourceforge.net/tracker2/?func=detail&aid=3109566&group_id=154314&atid=791284): Rsyslog configuration filename changed from 'octopussy.conf' to '10-octopussy.conf'

### Octopussy 0.9.9.9.9 ###
*release date: Fri, 03 Sep 2010*

  * Bugfix in octo_scheduler
  * Bugfix on Octopussy::FS::Flie_Ext
  * [Bugfix #3014851](https://sourceforge.net/tracker2/?func=detail&aid=3014851&group_id=154314&atid=791284) & [Bugfix #3036766](https://sourceforge.net/tracker2/?func=detail&aid=3036766&group_id=154314&atid=791284): Octopussy::Create_Directory -> Octopussy::FS::Create_Directory
  * [Bugfix #3015810](https://sourceforge.net/tracker2/?func=detail&aid=3015810&group_id=154314&atid=791284): Problem in 'System Configuration' & 'Updater' page
  * [Bugfix #3018897](https://sourceforge.net/tracker2/?func=detail&aid=3018897&group_id=154314&atid=791284): chown cannot access '2' problem
  * [Bugfix #3057572](https://sourceforge.net/tracker2/?func=detail&aid=3057572&group_id=154314&atid=791284): problem with devicename with '_' in octo_rrd

  * Timeout added in AAT::Download::File
  * You can now modify user configuration and a user can now be enabled/disabled
  * Test suite hugely updated
  * Installation of Octopussy on other linux systems has been greatly improved.
  * Installation Documentation has been updated (Debian/Ubuntu/CentOS/Fedora).

### Octopussy 0.9.9.9.8 ###
*release date: Fri, 04 Jun 2010*

  * A lot of work has been done to reduce memory usage (-40% for parsers)
  * A huge Services & Tables update
  * Faster Reports for Reports with Plugins
  * Better octo_extractor (with Device, Service, Loglevel & Taxonomy validation)
  * ProgressBar added for octo_reporter in command line
  * Alerts are now sent by octo_sender instead of octo_parser
  * Some little changes in Web Interface to improve speed
  * Translation files are now in .po format
  * Huge Test Suite (280+ tests) has been created to reduce 'stupid bugs'
  * Code cleaning
  * [Bugfix #2960273](https://sourceforge.net/tracker2/?func=detail&aid=2960273&group_id=154314&atid=791284): Parses stops due some perl subs missing
  * [Support Request #2967444](https://sourceforge.net/tracker/?func=detail&aid=2967444&group_id=154314&atid=791285): Device Models/Types problem
  * Bugfix: Wizard title with '[]' problem
  * [Bugfix #2976415](https://sourceforge.net/tracker2/?func=detail&aid=2976415&group_id=154314&atid=791284): Cisco_Pix Service problem
  * [Bugfix #2991712](https://sourceforge.net/tracker2/?func=detail&aid=2991712&group_id=154314&atid=791284): Device hasn't send any logs every 2 seconds


### Octopussy 0.9.9.9.6 ###
*release date: Thu, 25 Feb 2010*

  * Bugfix: 'undefined value within %re_type or olor in Message.pm' messages
  * Bugfix: 'change service rank - internal server error msg'
  * Bugfix: 'use strict in Plugin.pm' & 'pid_param' error messages
  * Bugfix: minor changes in DeviceGroup, Message & Report modules
  * Bugfix: octo_parser
  * Bugfix: '\r\n' in message creation with Wizard
  * Bugfix: 2 minor changes in Web Interface
  * Bugfix: missing status in Running Reports in Reports Viewer
  * [Bugfix #2946434](https://sourceforge.net/tracker2/?func=detail&aid=2946434&group_id=154314&atid=791284) & [Bugfix #2946818](https://sourceforge.net/tracker2/?func=detail&aid=2946818&group_id=154314&atid=791284|2946818]]: 'sort uniq' problem
  * Bugfix: Major fix for XML Caching when reading just after writing in AAT::XML.pm
  * Bugfix: Remove verbose tar in Octopussy::Configuration.pm
  * [Bugfix #2948940](https://sourceforge.net/tracker2/?func=detail&aid=2948940&group_id=154314&atid=791284): Fixes the missing servicename for the 1st message of a service
  * Bugfix: '\' character problem with DAY, DAY_HOUR, DAY_HOUR_MIN, UNIX_TIMESTAMP in Report SQL functions

  * Faster Wizard when there is a lot of 'unknown files'
  * Reduce the memory used by octopussy binaries
  * Test suite created with more than 120 tests
  * MobilePhone list updates
  * Major Services updates


### Octopussy 0.9.9.9.2 ###
*release date: Tue, 19 Jan 2010*

  * A lot of bugs have been introduced in the last releases (logs viewer/octo_ex
tractor), this release should fix that !

### Octopussy 0.9.9.9 ###
*release date: Tue, 12 Jan 2010*

  * Bugfix 'adding locations does not update' ([Bugfix #2920425](https://sourceforge.net/tracker2/?func=detail&aid=2920425&group_id=154314&atid=791284))
  * Bugfix 'User properties are not updated' ([Bugfix #2921789](https://sourceforge.net/tracker2/?func=detail&aid=2921789&group_id=154314&atid=791284))
  * Bugfixes on Alerts


### Octopussy 0.9.9.8 ###
*release date: Wed, 23 Dec 2009*

  * Major Bufixes in octo_extractor/octo_reporter ([Bugfix #2906742](https://sourceforge.net/tracker2/?func=detail&aid=2906742&group_id=154314&atid=791284),[Bugfix #2907323](https://sourceforge.net/tracker2/?func=detail&aid=2907323&group_id=154314&atid=791284),[Bugfix #2915014](https://sourceforge.net/tracker2/?func=detail&aid=2915014&group_id=154314&atid=791284))
  * Bugfix in Alert Creation ([Bugfix #2903747](https://sourceforge.net/tracker2/?func=detail&aid=2903747&group_id=154314&atid=791284) & [Bugfix #2906983](https://sourceforge.net/tracker2/?func=detail&aid=2906983&group_id=154314&atid=791284))
  * Code cleaning (Perl Best Practices)


### Octopussy 0.9.9.7 ###
*release date: Tue, 24 Nov 2009*

  * Better Logs Wizard (unmatched part of log is now in red) ([Feature Request #2901173](http://sourceforge.net/tracker/?func=detail&aid=2901173&group_id=154314&atid=791287))
  * Minor bugfixes
  * Code cleaning (Perl Best Practices)

### Octopussy 0.9.9.6 ###
*release date: Wed, 21 Oct 2009*

  * Major speed improvement (4X-5X) for octo_parser & octo_uparser !
  * Major Code Cleaning (Perltidy & Perl Best Practices)
  * You can now Disable/Enable statistics by Device/Service
  * Zabbix_sender available to send Alerts
  * You can now specify Host & Service for Nagios NSCA & Zabbix_sender Alerts
  * Better Wizard Search Service
  * Unclosed file in octo_parser bug fixed ([Bugfix #2798302](https://sourceforge.net/tracker2/?func=detail&aid=2798302&group_id=154314&atid=791284))
  * Authenticated LDAP are now supported ([Bugfix #2808664](https://sourceforge.net/tracker2/?func=detail&aid=2808664&group_id=154314&atid=791284))
  * Invalid Regexp messages are logged in octo_parser
  * Invalid Regexp messages are showed in Service Messages list
  * Service Message Statistics are now in this format (xx.x%)

### Octopussy 0.9.9.4 ###
*release date: Mon, 18 May 2009*

  * dispatcher bugs fixed ([Bugfix #2787361](https://sourceforge.net/tracker2/?func=detail&aid=2787361&group_id=154314&atid=791284), [Bugfix #2791070](https://sourceforge.net/tracker2/?func=detail&aid=2791070&group_id=154314&atid=791284), [Bugfix #2792199](https://sourceforge.net/tracker2/?func=detail&aid=2792199&group_id=154314&atid=791284))
  * cron.daily logrotate bug fixed ([Bugfix #2790071](https://sourceforge.net/tracker2/?func=detail&aid=2790071&group_id=154314&atid=791284))
  * Apache2 Installation bug fixed ([Bugfix #2790082](https://sourceforge.net/tracker2/?func=detail&aid=2790082&group_id=154314&atid=791284))
  * Rsyslog Installation bug fixed ([Bugfix #2790769](https://sourceforge.net/tracker2/?func=detail&aid=2790769&group_id=154314&atid=791284))

### Octopussy 0.9.9.3 ###
*release date: Tue, 28 Apr 2009*

  * Syslog-ng replaced by Rsyslog
  * /etc/init.d/octopussy is now [LSB compliant](http://wiki.debian.org/LSBInitScripts)
  * Better Debian installation
  * Minor Bugfixes/Improvements

### Octopussy 0.9.9.2 ###
*release date: Mon, 20 Apr 2009*

  * Better reports with [Open Flash Chart](http://teethgrinder.co.uk/open-flash-chart-2/) !
  * RRD taxonomy bug fixed ([Bugfix #2659959](https://sourceforge.net/tracker2/?func=detail&aid=2659959&group_id=154314&atid=791284))
  * Minor Bugfixes/Improvements


### Octopussy 0.9.9.1 ###
*release date: Wed, 25 Feb 2009*

  * Major Bug discovered & fixed in octo_dispatcher (no more logs were handled by Octopussy ! :()

### Octopussy 0.9.9 ###
*release date: Mon, 23 Feb 2009*

  * New feature: Logs Availability Viewer
  * Now, you can 'replay' logs with octo_replay !
  * Before, you can only set log retention duration by Device, now, you can set it by Device/Service
  * Logs Viewer now with Loglevel, Taxonomy & MsgID filtering
  * [Bugfix #2509315](https://sourceforge.net/tracker2/?func=detail&aid=2509315&group_id=154314&atid=791284): now /usr/sbin/octo_* require to be launched by Octopussy user
  * So Many Bugfixes...

### Octopussy 0.9.8.8 ###
*release date: Tue, 02 Dec 2008*

  * Major bugfix on octo_dispatcher ! ([Bugfix #2343806](https://sourceforge.net/tracker2/?func=detail&aid=2343806&group_id=154314&atid=791284))
  * Bugfix the apache2 restart bug ([Bugfix #2304276](https://sourceforge.net/tracker2/?func=detail&aid=2304276&group_id=154314&atid=791284))
  * You can now limit the number of minutes to search for restricted users
  * Minor WebUI improvements

### Octopussy 0.9.8.7 ###
*release date: Tue, 25 Nov 2008*

  * Wget replaced by LWP
  * Major Bugfixes in octo_parser & octo_uparser
  * Bugfixes all the bugs introduced in the last 2 releases (Taxonomy::List)
  * Bugfixes for Perl 5.10 support
  * IT & PT Translations updated


### Octopussy 0.9.8.6 ###
*release date: Mon, 17 Nov 2008*

  * Bugfix the RRDTool bug ([Bugfix #2293036](https://sourceforge.net/tracker2/?func=detail&aid=2293036&group_id=154314&atid=791284)) introduced in last release
  * Bugfix 'the number of alerts always 0' bug (SR ID: 2272569)
  * 'REGEXP' reserved word is now 100% Perl Regexp ( () [] are working now) ([Bugfix #2284493](https://sourceforge.net/tracker2/?func=detail&aid=2284493&group_id=154314&atid=791284))
  * Services updates in order to work with the updated 'REGEXP' reserved word

### Octopussy 0.9.8.5 ###
*release date: Thu, 13 Nov 2008*

  * Loglevel added in Logs Viewer & Reporter
  * Selector for Services, Loglevel & Taxonomy are fully dynamic now
  * Better/Easier Report SQL Query Configurator (except for WHERE clause)
  * Minor bugfix on octo_world_stats
  * Code cleaning



### Octopussy 0.9.8.4 ###
*release date: Wed, 29 Oct 2008*

  * Octopussy World Stats
  * New type PID (NUMBER type with no MIN,MAX,AVG,SUM functions)
  * Bugfix on Report Edition ([Bugfix #1835898](https://sourceforge.net/tracker2/?func=detail&aid=1835898&group_id=154314&atid=791284))
  * Lot of major & minor bugfixes
  * Code cleaning

### Octopussy 0.9.8.1 ###
*release date: Thu, 04 Sep 2008*

  * Fixes bugs introduced by 0.9.8
  * Code cleaning

### Octopussy 0.9.8 ###
*release date: Wed, 03 Sep 2008*

  * Possibility to move to First/Last Service in Device Services List
  * Possibility to move to First/Last Message in Service Messages List
  * '10 seconds step' logging feature added
  * Dispatcher doesn't update RRD files anymore, a new process has been created for that, octo_rrd
  * Major Bugfixes ([Bugfix #2033700](https://sourceforge.net/tracker2/?func=detail&aid=2033700&group_id=154314&atid=791284), [Bugfix #2033938](https://sourceforge.net/tracker2/?func=detail&aid=2033938&group_id=154314&atid=791284))
  * Bugfixes in Logs Viewer ([Bugfix #2067498](https://sourceforge.net/tracker2/?func=detail&aid=2067498&group_id=154314&atid=791284))
  * Services updates

### Octopussy 0.9.7.6 ###
*release date: Thu, 24 Jul 2008*

  * 'Running Reports List' feature added
  * Minor Bugfixes

### Octopussy 0.9.7.4 ###
*release date: Wed, 16 Jul 2008*

  * Really better communication between WebUI & octo_reporter & octo_extractor
  * Minor Bugfixes

### Octopussy 0.9.7 ###
*release date: Mon, 07 Jul 2008*

  * Major Bugfix on AAT::XML module
  * Taxonomy selection added in Logs Viewer
  * Linux Inotify 'feature' added to octo_parser ! (no more waste of time between dispatcher & parser)
  * Italian translation (not complete) added (thanks to Giuliano Natali)


### Octopussy 0.9.6.6 ###
*release date: Wed, 28 May 2008*

  * 'Devices list filtering' feature added ([Feature Request #1841748](https://sourceforge.net/tracker2/?func=detail&aid=1841748&group_id=154314&atid=791287))
  * 'check new Octopussy version' feature added ([Feature Request #1732808](https://sourceforge.net/tracker2/?func=detail&aid=1732808&group_id=154314&atid=791287))
  * 'octo_extractor uses too much memory' bug fixed ([Bugfix #1968031](https://sourceforge.net/tracker2/?func=detail&aid=1968031&group_id=154314&atid=791284))
  * Major Bugfixes on dynamic selector for Devices/Services
  * Some work on Web Interface
  * So many bugfixes

### Octopussy 0.9.6.2 ###
*release date: Mon, 28 Apr 2008*

  * Major Bugfixes on Logs Viewer
  * Major Bugfixes on Backup
  * Bugfix the wizard bug ([Bugfix #1951515](https://sourceforge.net/tracker2/?func=detail&aid=1951515&group_id=154314&atid=791284))
  * 'Search Templates administration' feature added
  * 'Search Templates removing in Logs Viewer' feature added

### Octopussy 0.9.6 ###
*release date: Mon, 21 Apr 2008*

  * ServiceGroup feature added (you can now add a list of services to one device in one shot)
  * Bugfix to disable deletion of last admin user
  * Bugfix on Selector_DateTime_Simple (for hour & min < 10)
  * Bugfixes on Logs Viewer

### Octopussy 0.9.5.8 ###
*release date: Thu, 10 Apr 2008*

  * 'Reload Required' feature added (Parser are not reloaded anymore when you move Service or Message)
  * Really Better Logs Viewer
  * Parsers now stop cleanly
  * Bugfix on Logs sort (with unsorted month)
  * Lot of Bugfixes
  * Major Security fix !

### Octopussy 0.9.5.4 ###
*release date: Tue, 11 Mar 2008*

  * Alerts with Regexp(Include/Exclude)
  * Backup/Restore configuration feature added
  * Menu Configuration added (Icons&Text, IconsOnly, TextOnly)
  * New Types: Bytes & User_Agent (with specific plugins)
  * **Russian translation** (not complete) added (thanks to Andrew Pantyukhin)
  * Lot of Bugfixes

### Octopussy 0.9.5 ###
*release date: Tue, 12 Feb 2008*

  * Migration to Apache2
  * Better Logs Viewer with Ajax
  * Included Help/Documentation
  * Reducing number of Tables -> Global report easier
  * Min & Max SQL functions added to Reports
  * Yearly Stats added
  * Services Added/Updated
  * Report ProgressBar in Ajax now
  * A lot of Minor Bugfixes

### Octopussy 0.9.4.8 ###
*release date: Wed, 19 Dec 2007*

  * Report XML output added
  * In Wizard, now you can check if unknown logs match Service that don't belong to Device
  * Device Type is no more used for Logs Directories (Code Cleaner)
  * Bugfix for specific chars in Alerts msgs, Contacts & Wizard msgs
  * Bugfixes in Report Scheduler
  * Bugfixes in octo_logrotate
  * Code Cleaning

### Octopussy 0.9.4.4 ###
*release date: Wed, 21 Nov 2007*

  * You can now specify type (line or stack) and step (N minutes) to RRD Graph
  * RRD Taxonomy Graph for each device are now generated only when needed (lower load from octo_logrotate)
  * Code Cleaning (All AAT data is now in /usr/share/aat/ directory)
  * Bugfix on RRD Graph Report Edition
  * Lot of Bugfixes in installation scripts & documentation

### Octopussy 0.9.4 ###
*release date: Wed, 14 Nov 2007*

  * Storages used space now on main page
  * Handling User Restrictions (by Device/Service/ALert/Report)
  * Detection of Devices that don't send logs for n minutes
  * Simple Datetime Selector (current/last hour/day/week/month/year) added
  * Code cleaning and documentation

### Octopussy 0.9.3.8 ###
*release date: Wed, 24 Oct 2007*

  * Bugfix of device with status 'Stopped' that restarted after Octopussy restart
  * Major Bugfix on Report Scheduler
  * Global Performance improvment by 'nicing' Octopussy programs (pusher, scheduler, uparser, rrdgraph)
  * Message fields can now be inserted in Alert messages
  * WebUI - Service logos added in Services list
  * First Mac OS X System/Kernel messages created

### Octopussy 0.9.3.4 ###
*release date: Wed, 17 Oct 2007*

  * Major BugFixes on Alerts Viewer
  * Major Bugfix on octo_alerter introduced in last release
  * Reports now in PDF (with htmldoc)

### Octopussy 0.9.3.1 ###
*release date: Wed, 03 Oct 2007*

  * Portuguese translation added (thanks to Rafael Henrique Vieira)
  * Bugfix on 'Total Events on Last minute'
  * Bugfix on Report Scheduler
  * Bugfix for Creation of Report with only one field

### Octopussy 0.9.3 ###
*release date: Mon, 01 Oct 2007*

  * 'Storages' feature added (you can now decide where to store logs by Device/Service)
  * Categories added in Report Viwer
  * Possibility to Remove Reports for 1 month
  * RRD files removed after Device/Service removed
  * Tooltip in Reports Viewer to show an abstract of the Report

### Octopussy 0.9.2.4 ###
*release date: Fri, 14 Sep 2007*

  * Improvements of octo_parser/octo_uparser (faster & lower load)
  * Change Reserved Word 'CONSTANT' by 'REGEXP'
  * Migration Apache::ASP Toolkit continued (all system stuff is now handled by AAT)
  * Cleaned last release debugging messages
  * Add 'Check Connection' feature to the System Configuration Panel
  * Lot of Bugfixes


### Octopussy 0.9.2 ###
*release date: Mon, 13 Aug 2007*

  * Start Apache::ASP Toolkit migration
  * Better WebUI with new Icons (mix of Tango, Futurosoft & Crystal Project)
  * Live syntax checker on Wizard
  * Lot of Bugfixes on alerts handling
  * Add choise of DB Type in System COnfiguration
  * Fix the bug of the Unknown messages not reparsed in Wizard
  * Minor Bugfixes ([Bugfix #1721184](https://sourceforge.net/tracker2/?func=detail&aid=1721184&group_id=154314&atid=791284), [Bugfix #1757568](https://sourceforge.net/tracker2/?func=detail&aid=1757568&group_id=154314&atid=791284))
  * Now users.xml are not overwritten anymore in Debian installation


### Octopussy 0.9.1.3 ###
*release date: Thu, 10 May 2007*

  * Fix 3 bugs in non-debian installation
  * Fix the Logs Wizard problem again ([Bugfix #1712057](https://sourceforge.net/tracker2/?func=detail&aid=1712057&group_id=154314&atid=791284))
  * Minor WebUI improvements


### Octopussy 0.9.1.2 ###
*release date: Wed, 09 May 2007*

  * Fix the Logs Wizard problem ([Bugfix #1712057](https://sourceforge.net/tracker2/?func=detail&aid=1712057&group_id=154314&atid=791284))

### Octopussy 0.9.1.1 ###
*release date: Wed, 02 May 2007*

  * Fix the librrd0 problem on Debian Etch

### Octopussy 0.9.1 ###
*release date: Fri, 27 Apr 2007*

  * Bugs with XML/utf8 fixed ([Bugfix #1708864](https://sourceforge.net/tracker2/?func=detail&aid=1708864&group_id=154314&atid=791284)), Octopussy is now fully utf8 !
  * WebUI improvements
  * Bugfixes on logs viewer, updater, reporter & scheduler
  * Device Dashboard Page with Device Taxonomy RRD Graph

### Octopussy 0.9.0.8 ###
*release date: Wed, 04 Apr 2007*

  * Alerts handle Repetition/Duration
  * Online Update for Translations added.

### Octopussy 0.9.0.6 ###
*release date: Tue, 27 Mar 2007*

  * RRDTool Graph used for Reports !
  * Basic Reports are now available
  * Online Update for Basic Reports added.
  * Minor Bugfixes

### Octopussy 0.9.0.2 ###
*release date: Tue, 06 Mar 2007*

  * Improve 'LogsFiles' function which improve extractor/reporter speed
  * Add Proxy Configuration to get Octopussy updates
  * Bugfix on Sending Alerts
  * Bugfix on New Device Detection

### Octopussy 0.9 ###
*release date: Wed, 28 Feb 2007*

  * Lot of Minor Bugfixes
  * Code Cleaning
  * You can now submit your Service/Table to support directly from the WebUI
  * Stop/Start/Pause device functionality
  * Tooltips

### Octopussy 0.8.9.9 ###
*release date: Fri, 05 Jan 2007*

  * Major Bugfix on Report SQL Request creation
  * Bugfix on sending Alerts vi email/IM
  * Spanish translation updated (thanks to Victor Barahona)

### Octopussy 0.8.9.8 ###
*release date: Wed, 03 Jan 2007*

  * Major Bugfix on installation script ([Forum Question #1622659](https://sourceforge.net/forum/forum.php?thread_id=1622659&forum_id=629149))
  * Major Bugfixes on memory usage which improve global performance
  * In Wizard, now you can delete one minute of unknown logs in one click

### Octopussy 0.8.9.6 ###
*release date: Wed, 29 Nov 2006*

  * Web Interface Enhancements
  * Minor Bugfixes
  * Code Cleaning

### Octopussy 0.8.9.5 ###
*release date: Fri, 24 Nov 2006*

  * Web Interface Enhancements
  * Lots of minor bugfixes/features enhancements
  * Code Cleaning

### Octopussy 0.8.9 ###
*release date: Tue, 07 Nov 2006*

  * Device Footprint functionality added (Octopussy can now determine Device Type & Model, and set Services with New Device log lines)
  * Plugins can now be applied in Input (before SQL insert) or Output (after SQL query)
  * RRDTool integration
  * Lot of Bugfixes/Enhancements

### Octopussy 0.8.8 ###
*release date: Wed, 20 Sep 2006*

  * Online Update (on 8pussy.org) for Octopussy Services & Tables added !
  * octo_pusher (octo_dispatcher for non-syslog devices) added !
  * Updated Web Interface buttons with The Tango Desktop Project icons
  * Many Minor Bugfixes

### Octopussy 0.8.7.4 ###
*release date: Thu, 31 Aug 2006*

  * Minor Bugfixes & Feature enhancements

### Octopussy 0.8.7 ###
*release date: Wed, 09 Aug 2006*

  * Lot of Bugfixes on installation !

### Octopussy 0.8.6.2 ###
*release date: Fri, 04 Aug 2006*

  * Dynamic Alerts edition added.
  * Disabled OpenDocument Export because installation problems in v0.8.6

### Octopussy 0.8.6 ###
*release date: Wed, 02 Aug 2006*

  * Reports exporting methods (mail/ftp/scp) added to Scheduler
  * Remove empty directories with octo_logrotate
  * Remove logfiles exceeding logrotate limit with octo_logrotate
  * Handling logs directories & files when changing device type fixed
  * Code Cleaning
  * Minor Bugfixes

### Octopussy 0.8.5 ###
*release date: Fri, 21 Jul 2006*

  * Version 0.8.4 was completely buggy, this is the fixed version !
  * Modified Plugin Architecture (see '[Plugin Howto](/documentation/howtos/plugin)')
  * Minor bugfixes

### Octopussy 0.8.4 ###
*release date: Wed, 19 Jul 2006*

  * Bugfix on octo_dispatcher when no NTP sync !
  * TimePeriods functionality added
  * Dynamic Alerts with TimePeriod added
  * Reports exporting methods added (by mail/ftp/scp)
  * Dispatcher & Parser improvments
  * Bugfix (Headers fields in Report)

### Octopussy 0.8.2 ###
*release date: Tue, 11 Jul 2006*

  * Bugfixes (removing logs in wizard & empty msgs for alerts)
  * Data from reports can now be handled by external plugins !

### Octopussy 0.8 ###
*release date: Wed, 05 Jul 2006*

  * Bugfixes
  * Add 'date_time' fields in Alerts -> Better sort in Alerts Tracker Interface
  * Export logs in 'txt' & 'csv' file format

### Octopussy 0.7.9.9 ###
*release date: Fri, 30 Jun 2006*

  * "System Configuration" Interface for DB, LDAP, Jabber, SMTP configuration
  * "Message Matching Statictics" in Service
  * Users LDAP Authentication is now working

### Octopussy 0.7.9.8 ###
*release date: Thu, 22 Jun 2006*

  * LDAP powered for contacts & users (users can't connect with LDAP yet)
  * Alerts Notifications can be sent via sendxmpp (Jabber)

### Octopussy 0.7.9.6 ###
*release date: Mon, 19 Jun 2006*

  * Web Page for Messages filtering (Service, Log Level, Taxonomy, Table)

### Octopussy 0.7.9.4 ###
*release date: Thu, 15 Jun 2006*

  * Alerts Creation via Web Interface

### Octopussy 0.7.9.2 ###
*release date: Fri, 09 Jun 2006*

  * Modification for SMTP & Alerts configuration

### Octopussy 0.7.9 ###
*release date: Tue, 06 Jun 2006*

  * Bugfixes in octo_reporter
  * Bugfixes in octo_scheduler
  * Clear empty directories with octo_logrotate
  * Dynamic Devicegroups

### Octopussy 0.7.8 ###

  * Bugfixes
  * Code cleaning
  * Logs Viewer & Reporter faster
  * New Services

### Octopussy 0.7.75 ###
*release date: Fri, 28 Apr 2006*

  * Bugfixes
  * WebUI really faster than before
  * First Debian Packaging

### Octopussy 0.7.7 ###

  * Now works with syslog-ng ! (should fix logrotate problems)

### Octopussy 0.7.6 ###

  * Bugfixes & improvements

### Octopussy 0.7.5 ###

  * Added checks for table & fields in message when creating/modifying message
  * Added checks for space in tablenames (substituted by '_')
  * Added checks for uniq msgids
  * Maps can redirect to alerts

### Octopussy 0.7.4 ###

  * Bugfixes
  * Added Maps functionality

### Octopussy 0.7.2 ###

  * Explicit msg_id for service messages
  * Added "LIMIT" functionality in Report
  * Added Predefined Taxonomy in Report
  * Added "versioning" (yyyymmddxxxx) in services

### Octopussy 0.7 ###

  * Bugfixes/WebUI improvements
  * Lot of new Services/messages
  * Enabled "message removing" in Wizard
  * Added "Report sort order (ascending/descending)"
  * Bugfix for "nested quantifiers errors" in Wizard
  * Incoming & Unknown messages now divided in 2 specific directories

### Octopussy 0.6.4 ###
*release date: Mon, 23 Jan 2006*

  * Bugfixes
  * Calendar added
  * Locations added

### Octopussy 0.6 ###
*release date: Mon, 16 Jan 2006*

  * Logrotate & Scheduler full functionality
  * javascript code for dynamic device/service selector

### Octopussy 0.5.6 ###
*release date: Wed, 11 Jan 2006*

  * A lot of bugfixes
  * Logrotate functionality added

### Octopussy 0.5.2 ###
*release date: Thu, 29 Dec 2005*

  * Some code cleaning
  * Some minor changes on File Hierarchy
  * Added user rights checkings before any Add/Modify/Remove action
  * Added Dialog Boxes !

### Octopussy 0.5 ###
*release date: Wed, 28 Dec 2005*

  * A lot of improvements & new features since 0.4 version !

### Octopussy 0.4 ###
*release date: Wed, 14 Dec 2005*

  * First Public Release