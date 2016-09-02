![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr2.jpg)  

# StupidUSBPower

This is a USB Stick Eurorack Power supply. 

- It takes +5v from USB power, and turns it into +/-12v and also passes along the 5v. 
- The key component is a IR0512S DC-DC Converter from XP Power which [costs about £8.50 from Farnell](http://uk.farnell.com/xp-power/ir0512s/dc-dc-converter-semi-reg-dual/dp/1860988) and gives 125mA of power on both rails.  This is a standard SIP package, so other dual output DC-DC converters may work in the same spot. I just chose the one with a good output. 
- The board also includes a simple passive headphone output; the 3.5mm mono socket goes through a 50k Volume Pot into the stereo headphone socket. This didn't work well with three-connector iphone earbuds, but was fine with normal stereo headphones. 
- Seems to work well with portable USB batteries. 
- The IR0512S is rated 125mA on +12v and -12v, but that seems quite conservative. The Dixie+Turing+Radio Music in the photo below ran quite happily, with an expected current draw of 160mA on +12v, 52mA on -12v. The converter module was warm but certainly not hot. The whole thing was drawing 600mA from the USB port. 

##Updates 
- This project has taken off a little bit! [C1T1ZEN](https://www.instagram.com/p/BEDGNGCOpEv/?taken-by=c1t1zen) has been building incredibly cool lunchbox euro boxes powered with his improved version. 
- Just got a [Re:Load2](http://www.arachnidlabs.com/reload-2/) so I've been trying to destroy my USB power prototype. With the IR0512S...
    - 250ma on +12v: Seems to work quite happily, pulling 710ma from the USB port. 
    - 350ma: It appears to work OK. The lights are on, but I'm making no no claims on the power stability, ripple etc, pulling about 1amp from USB, the converter is definitely HOT, but ran for an afternoon without death. 
    - 460ma: Seems to be the absolute max. Really hot. Above that, when you try to pull more current, all the lights blink and it says goodbye. The IR0512S seems to have an internal fuse, so recovers after it's cooled down. 
    - I initially had a 1a Polyfuse on the USB line (short circuited for this test) - that certainly seems sensible in the light of this - maybe 750ma would be safer. So: no actual magic smoke but definitely some warm plastic smells. 
    - Conclusions: This was a raw test: power to load, so can't draw any conclusions about what makes a good/stable/safe PSU for your modules, but it explains why I was able to power more than 125ma worth of modules with this thing.

##Reasons why this is stupid: 
3. There are no fuses or protection devices anywhere in the circuit. If you plug this plus $800 worth of modules into a $2000 laptop, you're taking a risk. NB: Do not do this. 
4. There is no filtering in the system, so there will be clock noise from the converter on the rails. The datasheet and my measurements suggest it's in the 60-85khz range. Do not use this to play live or record your new album. 
2. 125mA isn't very much power. Just because the module seems to run above that rating doesn't mean it's safe or reliable.  
1. Designing this as a memory stick is conceptually strong, but it would be much safer and easier to use with a female USB socket and a short cable.
2. Keyed headers are not reverse power protection. 
 
##Status 
- Eagle files and Gerbers (optimised for [OSH Park](https://oshpark.com/)) are in this repository. 
- These are Rev1.1 boards. The prototype below is Rev 1, which had the -12v LED reversed and needed a bit of trimming to get the USB socket on. I haven't built any 1.1 boards, but I'd be very confident that they'll work. 
- This project is Creative Commmons Licensed [CC-BY-SA](https://creativecommons.org/licenses/by-sa/3.0/). If you like the idea, why not develop it a little and submit your changes here? 
- I haven't exported a formal BOM. The only non-obvious bits aside from the DC-DC converter are: 
    - [USB Socket Type A, Through Hole](http://uk.farnell.com/multicomp/mc32603/usb-2-0-type-a-plug-th/dp/1696544)  
    - [Lumberg  150309 Stereo Socket](http://uk.farnell.com/lumberg/1503-09/connector-rca-jack-3-5mm-3way/dp/1243244)
    - [Amphenol  T821116A1S100CEU  Shrouded headers](http://uk.farnell.com/amphenol/t821116a1s100ceu/header-vertical-2-54mm-16way/dp/2215308)  
    - [Thonkiconn](http://www.thonk.co.uk/shop/thonkiconn-3-5mm-jack-sockets-x50/) mono jack socket, [Alpha](http://www.thonk.co.uk/shop/ttpots/) Pot, 3mm LEDs, 2k LED Resistors, 47uF 16v capacitor on the 5v line. 

![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr3-main.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr1.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr4.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr5.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr6.jpg)  
