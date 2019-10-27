# Octopussy Plugin Howto

In Octopussy, Plugins are modules that can modify Octopussy Reports input & output.
One Plugin is made of 2 files:

  * the Desciption file
  * the Code file

## Plugin Description File 

This file is located in plugins directory. (by default, it is */var/lib/octopussy/conf/plugins/*)
It defines the Plugin Name and its Functions.

Example for the NETWORK Plugin Description file (*/var/lib/octopussy/conf/plugins/Network.xml*):

	<octopussy_plugin name="NETWORK">
  		<function label="MASK_8"
            perl="Octopussy::Plugin::Network::Mask_8"
            source="OUTPUT">
    		<field_type>IP_ADDR</field_type>
  		</function>
  		<function label="MASK_16"
            perl="Octopussy::Plugin::Network::Mask_16"
            source="OUTPUT">
    		<field_type>IP_ADDR</field_type>
  		</function>
  		<function label="MASK_24"
            perl="Octopussy::Plugin::Network::Mask_24"
            source="OUTPUT">
    	<field_type>IP_ADDR</field_type>
  		</function>
  		<function label="RIPE_INFO"
            perl="Octopussy::Plugin::Network::Ripe_Info"
            source="OUTPUT">
    	<field_type>IP_ADDR</field_type>
  		</function>
	</octopussy_plugin>

For each functions, you can define 3 or 4 elements:

  * *label* the name that will be displayed in WebUI
  * *perl* the perl function to execute when this function is found
  * *field* or *field_type* respectively the field (ex: Netscreen_IDP:subcategory) or the type of field (ex: IP_ADDR, NUMBER...) on which you can apply this function
  * *source* indicates if the function works on input data (before SQL inserting) or output data (after SQL querying)

## Plugin Code File

This file is located in */usr/share/perl5/Octopussy/Plugin/* directory.
It defines perl code to treat the data.

Example for the NETWORK Plugin Code file (*/usr/share/perl5/Octopussy/Plugin/Network.pm*):

	=head1 NAME

	Octopussy::Plugin::Network - Octopussy Plugin Network

	=cut
	package Octopussy::Plugin::Network;

	use strict;
	use Octopussy;

	my %services = ();

	=head1 FUNCTIONS

	=head2 Init()

	=cut

	sub Init()
	{
  		my $conf_port = AAT::List::Configuration("AAT_Port");

  		foreach my $i (AAT::ARRAY($conf_port->{item}))
    		{ $services{$i->{value}} =  $i->{label}; }
	}

	=head2 Mask_8($addr)

	Only shows the first 8 bits of an IP address (--> 10.XXX.XXX.XXX)

	=cut

	sub Mask_8($)
	{
  		my $addr = shift;

  		$addr =~ s/(\d+)\.\d+\.\d+\.\d+/$1.XXX.XXX.XXX/;

  		return ($addr);
	}

	[...]

	=head2 Service($port)

	=cut
	
	sub Service($)
	{
  		my $port = shift;

  		return ($services{$port} || $port);
	}

	1;

	=head1 AUTHOR

	Sebastien Thebert <octo.devel@gmail.com>

	=cut

*Init* function is called before any 'data manipulation' function. It can be used to initialize data that can be used by any 'data manipulation' function.
