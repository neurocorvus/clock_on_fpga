# Simple clock on FPGA
This is a simple FPGA clock. They support 4-bit time output to a multiplexed display and full time setting.
## Module interface
```verilog
clock_top
(
    input           i_Clock,
    input           i_Button_Set,
    input           i_Button_Up,

    output  [7:0]   o_Segments,
    output  [3:0]   o_Digits
);
```
__Default connections:__
* Input clock: External Quartz 32768Hz or internal PLL
* Input button: Logic zero - gnd, unit - vcc. That is, an inverter is needed for the pull-up button
* Output display: common cathode indicators. Inverters are needed for the common anode
