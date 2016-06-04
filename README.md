# doxverilog
Fork of: Eric's branch of Doxverilog (doxygen + doxverilog patch)

This was created for two reasons:
* Make a stable branch of Doxverilog that compiles on Windows
* Support mixed-language projects that contain both Verilog and VHDL

As to the second point, currently the VHDL parser is "repurposed" when the 
verilog flag is set in the config file, and does not generate valid VHDL output
when supplied VHDL files.
