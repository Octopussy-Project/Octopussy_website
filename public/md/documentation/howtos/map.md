# Octopussy Map Howto

In Octopussy, a Map is just a picture where you define clickable area in order to be redirected to Device Dashboard page.

The Maps files are stored in **/var/lib/octopussy/conf/maps/** directory.


Here is an example of xml map file:

	<opt name="global_map"
		description="Global Map"
     	filename="global.gif">
		<area aid="building1"
			map="building1"
			x1="170" y1="0"
			x2="295" y2="175" />
		<area aid="building2"
        	map="building2"
        	x1="585" y1="0"
        	x2="715" y2="175" />
		<area aid="Device1"
        	device="device1"
        	x1="345" y1="280"
        	x2="415" y2="390" />
		<area aid="Device2"
        	device="device2"
        	x1="480" y1="280"
        	x2="550" y2="390" />
	</opt>

In this file, we indicate the Map Picture with *filename* (here */var/lib/octopussy/conf/maps/global.gif*) and 4 clickable area (2 'Device' area & 2 'Map' area) in this picture.

Each area is defined by Top-Left/Bottom-Right coordinates (x1,y1,x2,y2) and the device or the map you will be redirected if you click on it.

If you click on a 'Device' area, you will be redirected to the **Device DashBoard Page**.

If you click on a 'Map' area, you will be redirected to this Map.
