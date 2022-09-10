# Actionscript-3.0-battery-percentage-reader

Parts list instructions:
Computer: ESP32 Wrover

Dock: ESP32 WROVER programmer dock

component: "voltage sensor (vcc<25v)" 

description: The voltage sensor has a screwable section to add a battery for reading, and 3 header pins that go to your microcontroller.

Batteries used: (add your own battery and modify 876 in the "battery percent.fla")

"3.7v 100mah lipo" is set to have a 100% value when the microcontroller outputs: 876

Wiring instructions for sensor side (3 pins):

voltage sensor(Data) = IO33 esp32

voltage sensor (+) = NOT CONNECTED / NC

voltage sensor(-) = gnd esp32

Wiring instructions for sensor side (2 pins):

battery(+) = (VCC) sensor

sensor GND(-) = (GND) esp32

Wiring instructions for battery:

battery(-) = (IO13) esp32


Software instructions:
1.) Connect the esp32 to the usb port & open "battery_percentage/battery_percentage.ino" in the arduino IDE & click upload to program the board.

2.) Start "usb pipe 57600 baud.exe"

3.) Start "battery percent.fla" in the Actionscript 3.0 IDE & it should trace connected if the COM port of the esp32 is 11 for this line: "sock.connect("127.0.0.1",45055+11);"

4.) The microcontroller should update the "battery percent.swf" graphic along with the textfield that displays the remaining percentage of the battery.
