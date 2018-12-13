# ds402_usbtin
How to access a CAN DS402 device with ubstin


Each command must be terminated with an CR!

setup the baudrate with e.g. 'S4' for 250 kBaud

open the channel 'O'

start every CAN node with 't00020100' (NMT message)

switch the node to read to switch on with 't27F20600'

switch the node on with 't27F20700'

enable the operation with 't27F20F00'

select position mode with 't67F52F60600001'; this means access of 0x6060 and writing an one into it. 

set target position with 't67F8237A6000401F2000"; write decimal 2105152 in 0x607A 
