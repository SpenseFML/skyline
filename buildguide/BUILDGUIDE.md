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

