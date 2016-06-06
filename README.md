# doxverilog
Fork of: Eric's branch of Doxverilog (doxygen + doxverilog patch)

This was created for two reasons:
* Make a stable branch of Doxverilog that compiles on Windows
    - This is now complete, but a new patch needs to be made.
* Support mixed-language projects that contain both Verilog and VHDL
    - In progress

As to the second point, currently the VHDL parser is "repurposed" when the 
verilog flag is set in the config file, and does not generate valid VHDL output
when supplied VHDL files.

##TODO
* There are still a lot of calls to VHDL-specific functions spread around (a majority in vhdldocgen.cpp) that need to either become generic "HDL" functions, or need to have Verilog-specific versions created.
* Layout.cpp does not have the proper checks to handle a mixed-language environment.  Need to check language specifically, rather than the boolean flags for optimized VHDL/Verilog output.  At least the generated strings for VHDL are properly formatted now!
* New patches need to be made for these fixes
* Investigate what the whole image/icon changes were about - large amount of code I have ignored so far

##Future
* Look into supporting newer versions of Doxygen
    - http://sndegroot.blogspot.nl/2014/04/doxverilog-has-been-updated.html
    - http://sndegroot.blogspot.com/2011/08/documenting-verilog-ams-using.html
    - 