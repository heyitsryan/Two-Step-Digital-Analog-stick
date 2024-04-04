# Two-Step- Digital Analog stick

![TWOSTEP4](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/eaff48ae-d409-4c92-9c5a-741cddcf45af)

An enclosure to add extra movement steps to arcade sticks to mimic analog controls for platform fighters and other games.

The Two Step is a new concept in video game movement tech. Utilizing standard arcade micro switches and joystick designs but adding an extra stage of inputs to mimic analog joystick controls. 

![image](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/8987d4dd-634b-4c4a-bb91-3b66d5c9fc73)

The design idea came from trying to play Super Smash bros Ultimate on a cheap usb arcade joystick controller I had bought to play some classic arcade games. It had a setting to mimic the analog stick but since it only had one switch per direction it was full run all the time. This got me thinking, what if there was a second switch and I could set them to different analog values like on an all button controller with modifier buttons?

To see the full write up of how I got to this point please see my other repository https://github.com/heyitsryan/2-stage-arcade-stick

The Two step is comprised of a 3d printed enclosure and a custom firmware that is forked from Haybox firmware

## Parts needed:

* 1 Sanwa JLF/JLX arcade joystick
* 8 arcade micro switches with .187 terminals (List of tested switches is below)
* 1 3d printed Two Step enclosure and 4 lids (.stl files attached to project for download)
* wire (your preferred gauge and style)
* .187 crimp terminals or optional simply solder to the terminal pins whichever you prefer.
* 1 Raspberry Pi Pico 
* An enclosure to put it in (See my Stickwich design page for my preferred option but feel free to design your own)

## Tools Needed:

* Fine point tweezers
* soldering iron

### before assembling we should discuss parts options.

The Two Step was designed to work with the Sanwa Jlf arcade stick. This stick is the industry standard when it comes to japanese style arcade levers and has been a proven and reliable option for decades in Japaese arcades as well as high level arcade stick controllers for fighting games.

The original JLF can be purchased from amazon or other arcade parts stores such as focusattack.com

The amazon link is https://www.amazon.com/Sanwa-Denshi-JLF-TP-8YTFAST-SHIPPING-Adjustable/dp/B01CRQMWEQ/

Another option is the EG Starts JLF clone. This is an identical copy of the JLF as far as the hardware is concerned however it comes with lesser quality microswitches.  The link for the EG starts stick is https://www.amazon.com/gp/product/B01N0DO631/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1

the last option is the newly released Sanwa JLX. This stick is very similar to the venerable JLF however it has a few subtle improvements, mainly the pivot is highly polished and smoother feeling than the JLF. These can be purchased from focusattack.com here https://focusattack.com/sanwa-jlx-tp-8yt-joystick/

### We will also need to choose which microswitches to use. 

I have tested several microswitches and will list the ones I know to work for the Two Step however feel free to try other .187 terminal microswitches to see which ones feel best for you.

Sanwa V-152-3A5. These are my recommended first switches to try. they offer extremely consistent and reliable actuation feel while not being too overly stiff. https://focusattack.com/sanwa-v-152-3a5-fastener-micro-switch/

Suzo Happ E-Switch 50g .187" Microswitch. These are a very low actuation force microswitch and are a decent option if you have issues with actuating both switches at the same time. the downside to them is that they offer less  pushback which can make your return to center less accurate as well as possibly adding in the possibility for snapback. I have however found these to be very good to use for your up direction switches as that direction can sometimes be harder to actuate due to human ergonomics https://focusattack.com/e-switch-50g-187-microswitch/

Gersung GSM-V1623A3. These are very similar in feel to the Sanwa switches listed above and can be considered as a second option for that feel of switch. https://focusattack.com/gersung-gsm-v1623a3-187-microswitch-4-pak/

The jlf/jlx/eg starts arcade stick will come with a pcb with 4 microswitches on it of excellent quality and feel but since they are not .187 terminal switches we will not be using them in this guide. The switch assemblies do fit in the two step but the signal pins do not. if you choose to use the switch assemblies from these switches to save some money you will need to desolder them from the pcb they come on and you will have to directly solder your wires to the pins. Another option is to buy some cheap microswitches from amazon and swap the leaf springs from these soldered microswitches onto the .187 switch assemblies of the cheap microswitches. I have had success doing this using these cheap microswitches. https://www.amazon.com/dp/B07CK4473G?psc=1&ref=ppx_yo2ov_dt_b_product_details 

See the video below that shows how to assemble a disassembled switch assembly to do this mod.

There are so many microswitch options out there. I have only had the time and resources to test a few but feel free to try your own combinations. 

This enclosure is designed for .187 terminal microswitches and cannot guarantee that other terminal size switches will work.

## Assembly guide


To assemble the Two Step we will need to disassemble the microswitches and harvest the internal components. Most micro switches come apart in two pieces, the body and the lid, however some switches have a rivet that secures these pieces together and the body plastic is brittle and cracks apart when you pry the lid up. This is fine as we do not need to keep the factory enclosures. Don't worry if you break the switch plastic during this process.

Begin by taking your fine point tweezers and place them along the seam of the body and the lid and push in. You may need to do that at a couple different places along the seam until the lid lifts up and then pull on the lid until it comes off.

See video of this here: https://youtu.be/2ONEnv9Hk40

Now we can see the contents of the switch. The pieces we will need to keep are the metal contact pins on the end (if the switch you are using has 2 pins we will only need one but keep the extra’s as spares) the plastic actuator pin and the spring assembly. 

### The spring assembly is made up of 4 metal parts:

* The ground pin
* The lever arm
* the contact arm
* The leaf spring

![image](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/d8a05791-8db0-46ad-a3ce-e6b1f7fddbbf)


Take the back of your tweezers and use the flat surface to pull up on the ground pin to pull it out of the enclosure. I like to stop pulling once its almost out and then use my fingers the rest of the way.

Once you have the assembly loose put your thumb below the leaf spring/contact arm and your fingers on the ground pin to keep the assembly together.

* Note: When pulling the assembly out its very easy to keep them all together but sometimes you might lose your grip on the bottom and it will fall apart. This is ok! It’s easy enough to put the assembly back together. Watch this video here for instructions: https://youtu.be/dY3N_1uZfwE

Once you have the assembly out we will take it over to our Two Step housing and line up the upright piece of the ground pin with the pin slot on the first step housing. Also make sure the bottom end of the ground pin is lined up with the pin slot on the bottom of the first step housing. Once that is lined up press down until the assembly is fully seated.

see video here: https://youtu.be/kioZvGeRnSY

Now we will pull out the signal pin from the factory switch housing and making sure that the round contact patch is facing down, slide the pin into the pin slot on the housing. Finally we will take the plastic actuator pin and while lifting up slightly on the lever arm slide the pin into the slot on the bottom of the switch housing. 

Repeat this step for all 4 inner stage switches.

For the outer stage switches the instructions are identical only that we will need to flip the assembly horizontally 180 degrees and then slide the assembly into place just like the first stage switches you completed. Complete this for all outer stage switches and congratulations you are done!

The final step is the test each direction with your thumb to make sure both stages are clicking and then releasing separately. If they both actuate at the same time the switches are too close and you need to slide the outer stage switch towards to outside slightly until you get the right spacing. I tried my best to make this step not necessary however different switch manufacturers use ever so slightly different assemblies and so this step will need to be done for each direction.

### note

If you are having issues getting the second stage to actuate correctly or if you want to change the spacing timing between the stages you can try adding some thin shims of plastic above the second stage plastic actuator pin

see video here:https://youtu.be/UNOzQDCdHXk

Once the switches are actuating individually in both directions an optional step to make sure everything stays that way is to put a small drop of super glue on the pin slots (making sure to not glue in your plastic actuator pins) and allowing that to dry for 10 minutes or if you have super glue accelerant use that to speed up the process.

Now we simply snap on the lids. The lid pins are slightly undersized to allow you to remove the lids for maintenance without snapping them off so if they don’t feel 100% secure that is totally fine as the gate will hold them on securely.

Now we will need to prepare the sanwa JLF arcade stick.

## Installation onto the sanwa JLF

Begin by taking off the stick gate. This is a clear and yellow plastic piece that is on the bottom of the JLF.  There are 4 retaining tabs around the gate that you will need to push in until you can lift off the gate.

We can reuse this gate or you can use the 3d printable gate attached to this project. If you choose to use the factory gate we will need to slightly modify it by removing the inner yellow piece. This can be done by pushing the piece up and rotating it to the left until it lines up with the slot that allows you to pull it out of the clear gate. Watch this video if you need clarification: videourlhere Now we can just use the clear gate piece. We need to do this to allow for enough stick travel to actuate both stages. 

see video here: https://youtu.be/bynt-vVpXo0

Once the gate is off you can pull off the factory microswitch pcb and now we are ready to put the jlf base into your preferred enclosure. Once the JLF is secured into your enclosure we can put on the Two Step. I like to take the gate and line it up with the holes on the lids of the Two Step and then place both the gate and the assembled Two Step onto the JLF at the same time. This will keep the lids in place and prevent the jlf actuator from accidentally pushing out one of the plastic actuator pins while pressing down. Once you get the gate to click into place and all 4 retainer tabs are locked into place you are finished!

Give the stick a test and make sure you can actuate both steps in all 4 directions. 

*Note: I prefer to use a larger actuator with the Two Step however the factory actuator also works fine. This is a preference issue and you may want to try different actuator sizes to see which ones work best for you. I have included some stl files of different actuator sizes for testing however due to the nature of fdm prints being stacked layers I cannot guarantee how well they will survive prolonged use. Otto DIY sells different Nylon actuators on amazon for not much money. https://www.amazon.com/gp/product/B0BVMT9CT9/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1

## Now we can connect it to the Raspberry pi Pico.

We will need to create a ground chain for the 8 ground pins. If you plan to use .187 crimp terminals for this I find it good to bend the crimp terminals and also the ground pins themselves for the first stage ground pins at an angle so that you can access the first stage signal pins and not cause a possible signal short with the other direction signal pins

See the photo below for the ground chain pins you will need to connect together as well as the signal pins

![twostep-pindiagram](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/ec17fa31-8d59-481e-921d-fa9627bb39cf)

As you can see the vertical directions are opposite of what you expect them to be however the horizontal directions are not. This is because we rotated the enclosure horizontally but not vertically. I find it useful to mark the directions on the inside of the enclosure so you don’t get confused as to which is which.

The wiring colors as shown are as follows. you do not need to use these wire colors I have just used these to show which pins are what.

black: ground chain
red: Down
orange: Down2
yellow: Right
green: right2
blue: Up
purple: Up2
pink: Left
white: Left2

Once these are wired to the switch pins and the ground loop is completed we will connect the wires to the raspberry pi pico

![twostep-pico-wiring](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/63119ae7-7b14-4cfc-b84a-8170ba06d82c)


For simplicity I used the same pins that the Haybox firmware uses for left, right, up and down for the first stage switches and then added 4 more inputs for left2, right2, up2 and down2. I would recommend using the same pins on the pi pico as the diagram above for simplicity so you do not need to modify the code.

Once connected it should look something like this:

![image](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/cbe30166-7686-45cd-a6df-1cea9e1e64df)

## Next step is to prepare the Raspberry pi Pico microcontroller board and load the firmware.

On the raspberry pi pico there is a white bootsel button. Hold that down while plugging in the micro usb cable into your pc. It should pop up in your file browser as a removable drive labeled "RPI-RP2"

Download the HayStick-2.4.0.tar.gz file and extract it. Inside the extracted directory find the .pio/build/pico/ directoiry. inside this directory is the firmware.uf2 file and drag it into the RPI-RP2 drive. This will then disconnect the Pi Pico and reboot. Once it disconnects you can unplug the micro usb cable from the pico and proceed to use the controller.

Currently I only have 2 working profiles, The Ultimate profile and the melee20button profile. If you are wiring your pico to use a gamecube cable the default profile will be the melee20button profile however you can use the Ultimate profile by holding down the A button while plugging in the controller. If you use the usb connection to the Nintendo switch you can use the Ultimate profile by holding down X while plugging in the controller.

Additional wiring diagrams:

If you wish to wire your controller to use a gamecube cable

![pico_gcc_cable - twostep](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/19181d15-9023-4d25-93cb-f111336d98c2)

If you want to connect to a usb-c breakout board

![pico_usbc_breakout-twostep](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/623597a9-34f9-4312-b8ce-998c4b17b645)

For all other pi pico related questions please refer to the build guide of the original Haybox firmware of which I have forked the Haystick firmware from. Their github page can be found here: https://github.com/JonnyHaystack/HayBox
Another amazing resource is the Crane's lab discord server: https://discord.gg/yTZnsx5e I would not have been able to complete this project without their help and support. Thank you so much.

## Now you can begin using your controller! 











 


