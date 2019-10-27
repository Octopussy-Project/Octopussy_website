# Troubleshooting

### I can't get logged in, what's the problem ?

Do you have that in your 'users' file ?
(by default */var/lib/octopussy/conf/users.xml*)

	<?xml version='1.0' encoding='UTF-8'?>
  	<Octopussy_users>
  	<user language="EN"
        login="admin"
        menu_mode="ICONS_AND_TEXT"
        password="$1$OP$DS01VEfxN0orlyWumUTfE1"
        restrictions=""
        role="admin"
        status="Enabled"
        theme="DEFAULT"
        type="local" />
  	</Octopussy_users>


If yes, the login/pwd is **admin/admin**...

Check also that you have the good owner/rights for this file:

	-rw-r--r-- 1 octopussy octopussy 493 2007-02-19 10:05 users.xml

and that your apache daemon is launched with octopussy user

	ps -edf | grep apache

### I get an 'Internal Server Error' page

Check your **/var/log/apache2/octopussy-error.log** file to check where the problem is.

### I have performance issues with XML::Simple

Take a look at the XML::Simple documentation [here](http://search.cpan.org/~grantm/XML-Simple-2.18/lib/XML/Simple.pm#ENVIRONMENT).
