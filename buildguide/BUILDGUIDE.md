# Introdution
This is the buildguide for the Skyline Keyboard.
There are different versions of the keyboard for different budgets and needs.
All costs are in € and I'm from germany, so I don't have much choice in vendors.
Some parts can be bought from aliexpress or other vendors from china, longer waittimes, but sometimes way cheaper.
**All config files in this repo are for nice nanos used with ZMK**.
If you decide on using a pro micro, or other controller, you'll have to do the config files yourself.
Also **this build requires soldering and sometimes glueing**, I don't add these costs to my estimation, because it can vary very much, depending which equipment you're using.

## Preface
All the pricings of the builds are **without your prefered choice of switches and keycaps.**
You have to add the cost of them to my estimated cost of the build.
**The cost also assumes that you print the files yourself**, keep that in mind. 
If you buy the prints the price could be 25€ to 50€ more.
**Also you will need cables, diodes, rubber anti-slip pads, screws and screw inserts.**
These will be same for every build. I compiled a list of everything you need in the [prerequisites](PREREQUISITES.md)

## The versions
**The cheapest version** you can build is with a promicro controller from an asian vendor (preferably bought in bulk) and a wired connection between both halves.
It won't look as cool as the wireless version and you are stuck with the switches you have chosen. 
You don't need batteries, "on/off" switches and you'll save a lot of time and maybe stress.
**Estimated Cost:**
**Pro Micro: 5€**

**Upgrade No.1:**
Instead of using a pro micro contoller you can use the nice nano v2.
This will allow you to fork my repo and use the ZMK config I have provided. 
For the cheaper build you can still only use one controller and wire both sides together. You'll save some money on another controller and battery, but you pay the price in looks.
**Estimated Upgrade Cost per keyboard side:**

**Nice Nano V2: 25€**

**Battery:5€**

**On/Off Switch: 3€**

**~33€ per side**

**Upgrade No.2:**
We will use hot-swap-sockets to make your choice of switches more flexible for future use. Hot-swap-sockts allow you to remove the switches from the keyboard without much hassle and insert other ones.

**This won't up the cost too much, but will make the printing and building harder**

**Estimated Upgrade Cost per keyboard side:**

**Hotswap sockets: 5€**

**Glue (I used glue for plastics, but you can use hot glue I think): 5€**

**Time: Much**

**Upgrade No.3:**
We use displays to show the battery life, connection status, layers and cool art.
**Keep in mind that you have to use 2 Nice Nanos, if you want to use 1 Display, because of the limited pins on the controller**
I used the nice view displays, you can use other displays that fit.


**Estimated Upgrade Cost per keyboard side:**
**Nice View Display: 25€**

## What now?
Now you have to choose what you want to build. 
Print what you have chosen and go to building.
As mentioned in the [prerequisites](PREREQUISITES.md) I'd recommend to print the [print helper](../stls/print_helper.stl) first to check your settings and test if everything works the way you want it to.

### Preparing while printing

For the next step it depends if you use hot-swap-sockets or not.

**With hot-swap-sockets**
I added a [stl file](../stls/hot_socket_helper.stl) that you can print, which helps you soldering the hot-swap sockets to the diodes. Just insert the hot-swap-socket into the frame.
Now you have to solder the diode. Prepare it like [this] and solder it to the right side of the hot-swap-socket like [this] (the arrow shows the side where the diode has to be soldered on).
**Be sure that every Diode has the same orientation**
Do that with every socket you have (so 34 times)
For the other side you need easily bendable wire like the one on the diodes. If you have enough of them, so you can sacrifice some, you can just clip it off the wire on the diodes and use it. You can also buy wire like [this] if you don't want to destroy your diodes.
Solder it like this. 
When you're done you have to wait for your prints to finish.

**Without hot-swap-sockets**
Prepare the diodes like [this].
We will solder them directly on the switch and we do it, when the switch is already in the case, so we have to wait on the prints to finish.


### When the prints are ready

#### Test the prints
First off you should put every switch in to see if the print was successful. Do the same with the prepared hot-swap-sockets. Test if the sockets fit in with the switch. 
If they don't you can try to fix the print with a blade or clipper. If you can't solve the problem, please let me know, so I know that my file has an error, or we can look over your printing settings. 

#### Start with the screw inserts
Nothing is more annoying then soldering the board, seeing that everything works and then screwing up the screw inserts. Now you have a functional board without plates on the bottom, a rather unfortunate situation.
Do yourself a favor and start with putting in the screwinserts. Just put them on your soldering iron and slowly push them into the holes. 
**Test every screw insert and try to put the plates on before you start soldering the rest.**

#### Glue the hot-swap-sockets
When you're sure that everything fits and works you can glue in the hot-swap-sockets. This process takes some time, because the sockets should be atleast a little bit dried before you start soldering. Wait an appropriate time, depending on the glue you used. 
When you have waited enough you can begin to solder.

#### Soldering the components
We will be soldering a Matrix. This means, that we wont connect every single switch to the controller, but connect them in columns and rows to reduce the pins we need on the controller. You can read more about how and why we do switch matrix [here](https://www.crackedthecode.co/a-complete-guide-to-building-a-hand-wired-keyboard/#key-switch-diode-installationhttps://www.crackedthecode.co/a-complete-guide-to-building-a-hand-wired-keyboard/#key-switch-diode-installation
).

BTW: You don't have to do the soldering like I do in this guide, you're free to do it the way you like. I just found my pretty easy for soldering the sockets without too much measuring and still keeping it clean.

**With hot-swap-sockets**

Now solder the Diodes together and try to stuff them in the [cutout] I have prepared for them. These are our Columns.
Now solder together the rows. Just connect every Socket like [this]. 

**Without hot-swap-sockets**

Put the diodes on the right side of the switch and solder them to the switch. 
Solder the diodes together, now we have our [Columns].
After that solder the [Rows] of the switches together.

**Connect everything to the Controller**

Now that we have our Rows and Columns together we have to connect them to the controller. [Here's] a picture of the pinout of the nice nano. I marked which col and row have to be connected to which pin. When you do it like this, you can use my config right off the bat. You can make changes how you prefere, but have to change the mapping in the overlay file.

We use insulated wires for this step, so we don't run into short circuts. 

**If you use Batteries**

After that you can solder the batteries. You will have to connect one wire of the battery to the controller and the other to the on/off switch. Then connect the on/off switch to the controller.

**If you use the display**

Solder 5 insulated wires to the pins of the display. Put the display in place and solder the wires to the controller. 

**Testing your build**
You can flash the firmware on the controller and see if the displays work.
You can test every switch and the on/off switch too. 
Glue the display to the case and fix the on/off switch if everything works.
Be sure to wait the appropriate amount of time for your glue too harden before you insert the switches. 


