# Two-Step- Digital Analog stick

![TWOSTEP4](https://github.com/heyitsryan/Two-Step-arcade-switch/assets/2439341/eaff48ae-d409-4c92-9c5a-741cddcf45af)

An enclosure to add extra movement steps to arcade sticks to mimic analog controls for platform fighters and other games.

The design idea came from trying to play Super Smash bros Ultimate on a cheap usb arcade joystick controller I had bought to play some classic arcade games. It had a setting to mimic the analog stick but since it only had one switch per direction it was full run all the time. This got me thinking, what if there was a second switch and I could set them to different analog values like on an all button controller with modifier buttons?

To see the full write up of how I got to this point please see my other repository https://github.com/heyitsryan/2-stage-arcade-stick

### I have started a discord for any questions or issue's you may have building the Two Step. It is also where active development of performance tweaks of my designed components is being worked on with play testers as well. https://discord.gg/K8QTqZ74

## Parts needed:

4 Two Step choc pcb's (jlcpcb ordering instructions below)  
A 3d printed Two Step enclosure  
4 printed buttons  
4 printed lower lid's  
4 printed upper lid's  
8 Kaihl Choc V1 switches of your choosing    
8 Kaihl Choc V1 hotswap sockets  
11 female end dupont cables  (30mm length is recommended)  
1 Sanwa JLF or JLX arcade stick  
1 raspberry pi Pico microcontroller  
A controller enclosure to put it all in (may I suggest my printable Stickwich enclosure? Located here:   )  

## Tools Needed:
Soldering iron.

### before assembling we should discuss parts options.

The Two Step was designed to work with the Sanwa Jlf arcade stick. This stick is the industry standard when it comes to japanese style arcade levers and has been a proven and reliable option for decades in Japaese arcades as well as high level arcade stick controllers for fighting games.

The original JLF can be purchased from amazon or other arcade parts stores such as focusattack.com

The amazon link is https://www.amazon.com/Sanwa-Denshi-JLF-TP-8YTFAST-SHIPPING-Adjustable/dp/B01CRQMWEQ/

Another option is the EG Starts JLF clone. This is an identical copy of the JLF as far as the hardware is concerned however the quality control is not as good as the name brand so you may get a less polished feeling stick.  The link for the EG starts stick is https://www.amazon.com/gp/product/B01N0DO631/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1

the last option is the newly released Sanwa JLX. This stick is very similar to the venerable JLF however it has improvements, mainly the pivot is highly polished and smoother feeling than the JLF. I highly recommend using these as they do feel much better than a JLF for not much more money. These can be purchased from focusattack.com here https://focusattack.com/sanwa-jlx-tp-8yt-joystick/

## Low profile switch selection:  

There are 16 total varieties of Kaihl Choc V1 switches to choose from. Out of those I would suggest staying with switches that are 50gf or higher. The reason for this is that arcade microswitches which the JLF/JLX and all arcade sticks use are much higher resistance than what the Choc V1 switches offer and if you use too low of a resistance the stick can feel mushy and struggle to return to center quickly. I personnaly use the yellow 70GF linears but I have also used the light blue 70gf clicky switches which also feel great. In my testing the "tactile" switches are not very easily felt during gameplay and in my opinion do not offer much to the experience but feel free to experiment. The advantage to this system is that you can combine different switches to create your optimal stick. struggle with hitting consistent Up B's? You might put a lower force switch in the first switch socket of your up pcb as an example. The possibilities are vast.

## Assembly guide

Step 1:

Prepare the pcb's by soldering on the hotswap sockets onto the pcb's. This is very easy to do with even a beginner soldering iron. Simply place the socket into the holes on the backside of the pcb and heat up the socket with your soldering iron and feed solder into the socket end until it makes a connection between the socket and the pcb. repeat for both sides of the hotswap sockets and the pcb's are now complete.

Step 2: 

Place your Kaihl Choc V1 switch of your choosing into the sockets on the front side of the pcb's.

Step 3:

Slide the pcb's into the Tw Step enclosure making sure that the dupont pins are on the left side and pointing out with the switches on the inside.

Step 4:

Place the Buttons into the enclosure. 

Step 5:

Put on the lower lids by lining up the two pegs and placing them into the two holes.

Step 6: 

Slide on the upper lid. The upper lid uses sliding dovetails to hold the lid on securely while upside down in the controller. Line up the dovetail on the right side of the housing and slide it to the left until it lines up on the left side of the housing and clicks into place.

Step 7: 

Connect the dupont pins to the Two Step. The color diagram is below:

The other end of the dupont cables are soldered to the pico microcontroller 

A video of the full assembly process can be found below



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











 


