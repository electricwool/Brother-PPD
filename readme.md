brother PPD. traced from an original ppd. 

awaiting verification with production unit.

  unit detects an infinite number of pattern 907 from eeprom. unable to read the pattern. error 37 This Pattern Data Cannot be loaded. FRAM gives "improper cartridge is inserted in slot of CB-1" error 36. most importantly does not damage the CB-1. signal timing, routing optimization likely cause of the issue.
  Although marketted and repeatedly stated through documentation that FRAM is a drop in pin compatible replacement for SRAM designs, it is fundamentally incompatible due to, 
  "When designing with F-RAM for the first time, users of SRAM will
recognize a few minor differences. First, bytewide F-RAM
memories latch each address on the falling edge of chip enable.
This allows the address bus to change after starting the memory
access. Since every access latches the memory address on the
falling edge of CE, users cannot ground it as they might with
SRAM." 

The original uses 27C256 but this circuit was modified to use the 28C256 EEPROM. This is because the market is poluted with used chips and 27C256 OTP can be erased with X-ray or the windowed units with UV. This results in unreliable old OTP chips with high failure rates entering the supply chain. EEPROM can be old as well but can be rapidly erased and written to verify wheras a OTP can fail due to poor connection with the ZIF socket leaving you without recourse should a dodgy seller sell you a fried OTP PROM. 

the backup SRAM battery and power is eliminated by substituting a cypress FRAM that was relatively cheap at the time of making this but JLCPCB only had 5 in stock. alternatives could be Nvram but that is quite expensive and various chinese sites sell the cypress FRAM chips. 

a DIP eeprom is used because the edge connector is not keyed and it needs the case to have a wing out to the side anyway for mechanically keying the chip. 

These work perfectly well without the PROM installed as the SRAM was able to be formatted, store and load patterns with the PROM removed for firmware extraction. 
