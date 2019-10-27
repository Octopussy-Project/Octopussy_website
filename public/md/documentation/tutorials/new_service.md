# Tutorial: New Service Creation

When you go to the 'Logs Wizard' page, you can see devices with unknown messages.

![Device with Unknown Messages in Logs Wizard](/img/tutorials/tutorial_new_service01.png "Device with Unknown Messages in Logs Wizard")

Click on the Device to show the unknown messages.

![Unknown Messages for one Device in Logs Wizard](/img/tutorials/tutorial_new_service02.png "Unknown Messages for one Device in Logs Wizard")

If these messages are not related with known services, you need to create a new one.
Here, we know that the unknown messages are from a Squid proxy...

Let's create a new service '*Squid*' !


## 1 - Service Creation

Go to the **'Services'** page, enter a name and a description for this new service.

![Service Creation](/img/tutorials/tutorial_new_service03.png "Service Creation")

Here we create the service '*Squid*' with the description '*Squid Service*'.


## 2 - Table Creation

Then go to **'Tables'** page, enter a name and a description for this new table.

![Table Creation](/img/tutorials/tutorial_new_service04.png "Table Creation")

Here we create the table '*Squid_Traffic*' with the description '*Squid Traffic Table*'.

**Note:** You can create more than one table for one service. (ex: Cisco_Router_msg & Cisco_Router_traffic tables for Cisco_Router service)

Then you can add fields you want to use:

![Table Edition](/img/tutorials/tutorial_new_service05.png "Table Edition")

Here we add '*duration*', '*client_ip*', '*squid_code*'... fields to '*Squid Traffic Table*'.


## 3 - Add Service to Device

Now you have created our new Service and our new Table(s), let's add this new Service to the Device !

Return to **'Logs Wizard'** page, select the device you want to add the new service, then select the 'Add New service' link.
You will be redirected to the **'Device Services'** page. Add the new service to this device.

**Note:** You can also go to '*Devices*' page, and click on the link of the device you want to add the new service.

![Add Service to Device](/img/tutorials/tutorial_new_service06.png "Add Service to Device")

Here we add the service '*Squid*' to the device '*mediabox*'.


## 4 - Add Message to Service

Return to **'Logs Wizard'** page, select the device which have the new service.
Then you can select the new Service as Service, the Log Level, the Taxonomy and the new Table as Table for this unknown message.

![Set new Service & new Table to unknown message](/img/tutorials/tutorial_new_service07.png "Set new Service & new Table to unknown message")

Here we set the service to '*Squid*', the Log Level to '*Information*', the Taxonomy to '*Traffic*' and the Table to '*Squid_Traffic*'.


Then click the '*Select this message*' button.

Octopussy Wizard detect simple types (datetime, number...), then you add to set the new table fields to this message fields.
If one type is detected and you don't want to set table field for this message field, let the message field original value (by default).

![New Message Selection Fields](/img/tutorials/tutorial_new_service08.png "New Message Selection Fields")

Here we set, the table field '*datetime*' to message field '*DATE_TIME_SYSLOG*', the table field '*device*' to message field '*WORD*', the table field '*client_ip*' to message field '*IP_ADDR*' and the table field '*http_code*' to the second message field '*NUMBER*'.
The message field '*FLOAT_NUMBER*' is not modified, you will modify it on the next page, and the first message field '*NUMBER*' is set to '*NULL*'.

Then click the '*Edit*' button.

You will see the new message with the message fields you have just set.

![New Message Edition](/img/tutorials/tutorial_new_service09.png "New Message Edition")

Finish the creation of this new message by editing manually.
Each message field is written like this: 

**<@FIELD_TYPE:table_field_name@>**

ex: <@NUMBER:duration@>

If you want to define a complicated field, you can use, the REGEXP field:

**<@REGEXP("your regexp field"):table_field_name@>**

ex: <@REGEXP(".+ Password for \S+ was changed"):msg@> in '*Linux_System:password_was_changed*' message.

Set an explicit message_id for this message and click on the '*Finish*' button.

![New Message Edition](/img/tutorials/tutorial_new_service10.png "New Message Edition")

Here we manually add the table fields which were not detected on the previous step ('*duration*', '*squid_code*', '*bytes*', ...)

Finally, you will be redirected on the **'Services'** page of your device with your new message added !

![New Message added to New Service](/img/tutorials/tutorial_new_service11.png "New Message added to New Service")
