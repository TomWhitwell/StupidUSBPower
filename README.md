![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr2.jpg)  

# StupidUSBPower

This is a USB Stick Eurorack Power supply. 

- It takes +5v from USB power, and turns it into +/-12v and also passes along the 5v. 
- The key component is a IR0512S DC-DC Converter from XP Power - [Farnell Link](http://uk.farnell.com/xp-power/ir0512s/dc-dc-converter-semi-reg-dual/dp/1860988) which costs about £8.50 and gives 125mA of power on both rails.  This is a standard SIP package, so other dual output DC-DC converters may work in the same spot. I just chose the one with a good output. 
- The board also includes a simple passive headphone output; the 3.5mm mono socket goes through a 50k Volume Pot into the stereo headphone socket. This didn't work well with three-connector iphone earbuds, but was fine with normal stereo headphones. 
- Seems to work well with portable USB batteries. 
- The IR0512S is rated 125mA on +12v and -12v, but that seems quite conservative. The Dixie+Turing+Radio Music in the photo below ran quite happily, with an expected current draw of 160mA on +12v, 52mA on -12v. The converter module was warm but certainly not hot. The whole thing was drawing 600mA from the USB port. 

##Reasons why this is stupid: 
3. There are no fuses or protection devices anywhere in the circuit. If you plug this plus $800 worth of modules into a $2000 laptop, you're taking a risk. 
4. There is no filtering in the system, so there will be clock noise from the converter on the rails. The datasheet and my measurements suggest it's in the 60-85khz range.  
2. 125mA isn't very much power. Just because the module seems to run above that rating doesn't mean it's safe or reliable.  
1. Designing this as a memory stick is conceptually strong, but it would be much safer and easier to use with a female USB socket and a short cable.
2. Keyed headers are not reverse power protection. 

![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr3-main.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr1.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr4.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr5.jpg)  
![](https://raw.githubusercontent.com/TomWhitwell/StupidUSBPower/master/Collateral/usbpwr6.jpg)  
