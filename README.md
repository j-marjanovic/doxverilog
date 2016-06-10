# doxverilog
Fork of: Eric's branch of Doxverilog (doxygen + doxverilog patch)

This was created for two reasons:
* Make a stable branch of Doxverilog that compiles on Windows
    - This is now complete, but a new patch needs to be made.
* Support mixed-language projects that contain both Verilog and VHDL
    - Status: Currently working!

##TODO
* There are still a lot of calls to VHDL-specific functions spread around (a majority in vhdldocgen.cpp) that need to either become generic "HDL" functions, or need to have Verilog-specific versions created.
* <del>Layout.cpp does not have the proper checks to handle a mixed-language environment.  Need to check language specifically, rather than the boolean flags for optimized VHDL/Verilog output.  At least the generated strings for VHDL are properly formatted now!</del>
* New patches need to be made for these fixes
* <del>Investigate what the whole image/icon changes were about - large amount of code I have ignored so far</del> These icons are put in the class listing for designating what each member is - there are specific icons for wires, regs, always blocks, etc.
* Add icons (see previous point) to VHDL code!

##Future
* Look into supporting newer versions of Doxygen
    - 1.8.7 introduces a new VHDL parser, so will likely require big changes.  1.8.6 might be possible with much less work.
    - http://sndegroot.blogspot.nl/2014/04/doxverilog-has-been-updated.html
    - http://sndegroot.blogspot.com/2011/08/documenting-verilog-ams-using.html
