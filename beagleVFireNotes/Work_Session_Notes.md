# Work Logs

## October 26, 2024

Work logs:
- Last time installed the microchip tools from [Microchip FPGA Tools Installation Guide](https://docs.beagleboard.org/boards/beaglev/fire/demos-and-tutorials/mchp-fpga-tools-installation-guide.html#beaglev-fire-mchp-fpga-tools-installation-guide) and finished the tutorial [Customize BeagleV-Fire Cape Gateware Using Verilog](https://docs.beagleboard.org/boards/beaglev/fire/demos-and-tutorials/gateware/customize-cape-gateware-verilog.html).
- Today, following tutorial at this location [Exploring Gateware Design with Libero](https://docs.beagleboard.org/boards/beaglev/fire/demos-and-tutorials/gateware/exploring-gateware-design-libero.html)
- Installed python and microchip requirement 
- sourced setup script `source ~/Microchip/setup-microchip-tools.sh`
- Cloned the gateware repo `git clone https://openbeagle.org/beaglev-fire/gateware.git`
- Error when running `python build-bitstream.py ./build-options/default.yaml # exploring the default gateware`



## October 28, 2024

Work logs:
- Trying to figure out the error from last time where the scripts cannot find synplify_pro:
```
Info: Active implementation is 'synthesis'
Starting Synplify Pro ME...
Error:  Failed to execute: '/home/media/microchip/Libero_SoC_v2024.1/SynplifyPro/bin/synplify_pro'.
        Executable cannot be found, you may need to reinstall this tool.
        Error:  Unable to start Synplify Pro ME.
                From the Project menu, select 'Tool Profiles...' and change the Synplify Pro ME profile.
                Error:  Synthesis failed.
                Error:  The command 'run_tool' failed.
                Error:  Failure when executing Tcl script. [ Line 272 ]
                Error:  The Execute Script command failed.
                The BVF_GATEWARE_025T project was closed.
                Finished
```
-  Looks like the issue is because the script is looking under `/microchip` and not under `/Microchip`, created a symbolic link for one to the other to test
- fixed it by moving the Synplify pro installation script to the correct microchip foler. When I have time I should probably reinstall all the tools with a clean path


## October 29, 2024

- Connected to the BeagleboneV fire via ttyACM0 on the Ubuntu Machine
- Local ip 172.21.8.233
- Next step is to continue the [Exploring Gateware Design with Libero Tutorial](https://docs.beagleboard.org/boards/beaglev/fire/demos-and-tutorials/gateware/exploring-gateware-design-libero.html#exploring-gateware-design-with-libero)
