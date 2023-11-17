# SOC-design-of-an-Old-MOS-6502-CPU

Abstract- 

Microprocessor design and production have advanced significantly as a result of the computer industry's quick development. This article details a ground-breaking initiative to close the gap between traditional CPU design and cutting-edge Very Large-Scale Integration (VLSI) methods. This research shows how to construct and design a MOS 6502 CPU utilizing Cadence tools inside a VLSI architecture, focusing on the classic MOS 6502 CPU, a cornerstone of early computing.  By employing Cadence tools, the MOS 6502's architecture is systematically translated into Register Transfer Level (RTL) designs, which are synthesized into gate-level representations. In-depth coverage of synthesis, place and route, and verification sheds light on how the RTL design is converted into physical gates and their ideal placement on the chip. Timing studies and functional simulations verify the effectiveness and accuracy of the design. 


BACKGROUND-

A number of technical innovations have changed the landscape of contemporary computing, with the invention of the microprocessor serving as a turning point in the development of the field. Among these, the MOS 6502 CPU has a special position due to its ground-breaking architecture, which was essential in the development of personal computing. The MOS 6502, which debuted in the middle of the 1970s and powered enduring devices like the Commodore 64, Apple II, and Atari 2600, came to be identified with the microcomputing period. . The 6502 has a 16-bit address bus and an 8-bit little-endian CPU. The earliest versions had a die size of 3.9 mm x 4.3 mm (advertised as 153 mils x 168 mils), for a total area of 16.6 mm2, and were made using an 8 m process technology chip. [1]. The goal of this research is to bridge the gap between the early CPU era's simplicity and the present VLSI era's complexity. This research tries to combine the best of both worlds by trying to revive the MOS 6502 CPU within a VLSI architecture. The 6502-team had to create a digital design of instruction decoders, an arithmetic/logic unit (ALU), registers, and data paths (high-level register-centric design) that could be realized using individual gates made out of NMOS transistors and depletion loads (low-level circuit design) in order to reduce this to a working circuit design. The register structure and other components of the high-level architecture were worked out by Peddle, Orgill, Mathys, and Mensch, with Mathys converting a series of data transfers for each instruction into state diagrams and logic equations.[2] While Wil Mathys worked on other tasks, Mensch and Orgill finished converting the register-centric architecture from logic equations into a circuit schematic of the NMOS transistors and depletion loads (officially known as the "650X-C Microprocessor Logic Diagram"[3]).


METHODOLOGY-

To dsign an old mos 6502 CPU, initially, create a directory file in the open terminal. Then from there, source the physical design. The edit file, input file, and io file were all produced after the source, as can be seen. Modify the code for the circuit connection with the pad by going to the input file after that. After it is finished, I will enter the synthesis file and modify the settings as necessary. Execute the genus next.Check the error after the genus has been successfully run; if it reveals a problem with the pad and circuit connection, go to the input file and repair it. Genus then takes off again. If it works, go to source synthesis. If there is a mistake, I will correct it; if not, I'll check the gui display to make sure the connection is good. Next,import the design into the encounter by going to the encounter. Then launch the MMMC browser and configure everything as needed. Save and leave when finished. You can then see where the pins are positioned in the encounter window. I now have to make a corner cell. To do that, I'll open the cpu_wpad.io file and make the necessary modifications. They will be connected to the circuit in the manner of VDD, VSS, VDDIOR, and VSSIOR. The floorplane is the next item. Go to floorplan, then choose a specific floorplan, and set core utilization to 0.4. I'll also set the core to 10, in addition to the core to left, the core to right, the core to top, and the core to bottom. After that, I'll plan my power. Metal 6 will be assigned to metals in the horizontal direction and Metal 5 to metals in the vertical direction. I'll make a unique design once it is finished. The circuit will thus be linked to utilizing a bespoke layer, which will connect VDD and VSS. Physical verification should happen right away. Here, I'll look at the DRC, LVS, ARC, and ERC. I will correct any infractions if I get any. Two different kinds of infractions are present here. These are violations of geometry and connection. The final SoC design will be revealed once everything has been resolved.

![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/2850f33f-984b-4f26-bfef-006f25557549)

