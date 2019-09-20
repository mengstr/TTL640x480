# TTL640x480

I had been thinking for a while about making a TTL-based VGA video card when a post in the Z80-group on Facebook triggered me into action of actually realizing my design.

The ultimate goal is of course to make this circuit into a 80x25 character "video card" that uses only plain TTLs, a Character ROM and some RAM.  But as a start I decicded to focus on the counters for rows and columns as well as the generation of sync and blanking pulses.

There was at least one other implementation of this idea - the *Masochist's Video Card* by Pyroelectro but it used 30+ chips to basically do the sam thing as I wanted.

I went for a more minimalistic approach, while still maintaining full compliance with the 640x480 VGA standard.

I got it down to 3 counter ICs and 6 logic gates ICs for a total of 9 ICs, but I also use 3 diodes and a pulldown resistor as a discrete NOR (cheating a bit - so really it should be a total of 10 ICs to be fair) 

![The design on a breadboard](https://raw.githubusercontent.com/SmallRoomLabs/TTL640x480/master/Images/TTL640x480-breadboard-small.png)

All of this was back in Januari 2019, and then in July 2019 the ever so excellent Ben Eater published his own version of "The world's worst video card" https://eater.net/vga.  He made it with 20 ICs. I must admit I'm secretly happy that he didn't beat my chip count, but on the other hand his goal was not to make the lowest chip count but rather to make something educational.

### Schematics
![Schematics](https://raw.githubusercontent.com/SmallRoomLabs/TTL640x480/master/Images/TTL640x480-schematics.png)

### Part list
 3	×	74HCT393 Dual 4-bit counters  
 2	×	74HCT00 Quad 2-input NAND  
 1	×	74HCT10 Triple 3-input NAND  
 2	×	74HCT20 Dual 4-input NAND  
 1	×	74HCT04 Hex inverter  
 3	×	1N4148 Diodes   
 1	×	2K2 Resistor  
 1	×	25.175 MHz clock generator  

### Links
- My project at hackaday.io - https://hackaday.io/project/163298-ttl640x480
- Masochist's Video Card - http://www.pyroelectro.com/projects/masochists_video_card/
- Ben Eater's project - https://eater.net/vga
