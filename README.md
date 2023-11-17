# SOC-design-of-an-Old-MOS-6502-CPU

Abstract- 

Microprocessor design and production have advanced significantly as a result of the computer industry's quick development. This article details a ground-breaking initiative to close the gap between traditional CPU design and cutting-edge Very Large-Scale Integration (VLSI) methods. This research shows how to construct and design a MOS 6502 CPU utilizing Cadence tools inside a VLSI architecture, focusing on the classic MOS 6502 CPU, a cornerstone of early computing.  By employing Cadence tools, the MOS 6502's architecture is systematically translated into Register Transfer Level (RTL) designs, which are synthesized into gate-level representations. In-depth coverage of synthesis, place and route, and verification sheds light on how the RTL design is converted into physical gates and their ideal placement on the chip. Timing studies and functional simulations verify the effectiveness and accuracy of the design. 


BACKGROUND-

A number of technical innovations have changed the landscape of contemporary computing, with the invention of the microprocessor serving as a turning point in the development of the field. Among these, the MOS 6502 CPU has a special position due to its ground-breaking architecture, which was essential in the development of personal computing. The MOS 6502, which debuted in the middle of the 1970s and powered enduring devices like the Commodore 64, Apple II, and Atari 2600, came to be identified with the microcomputing period. . The 6502 has a 16-bit address bus and an 8-bit little-endian CPU. The earliest versions had a die size of 3.9 mm x 4.3 mm (advertised as 153 mils x 168 mils), for a total area of 16.6 mm2, and were made using an 8 m process technology chip. [1]. The goal of this research is to bridge the gap between the early CPU era's simplicity and the present VLSI era's complexity. This research tries to combine the best of both worlds by trying to revive the MOS 6502 CPU within a VLSI architecture. The 6502-team had to create a digital design of instruction decoders, an arithmetic/logic unit (ALU), registers, and data paths (high-level register-centric design) that could be realized using individual gates made out of NMOS transistors and depletion loads (low-level circuit design) in order to reduce this to a working circuit design. The register structure and other components of the high-level architecture were worked out by Peddle, Orgill, Mathys, and Mensch, with Mathys converting a series of data transfers for each instruction into state diagrams and logic equations.[2] While Wil Mathys worked on other tasks, Mensch and Orgill finished converting the register-centric architecture from logic equations into a circuit schematic of the NMOS transistors and depletion loads (officially known as the "650X-C Microprocessor Logic Diagram"[3]).


METHODOLOGY-

To dsign an old mos 6502 CPU, initially, create a directory file in the open terminal. Then from there, source the physical design. The edit file, input file, and io file were all produced after the source, as can be seen. Modify the code for the circuit connection with the pad by going to the input file after that. After it is finished, I will enter the synthesis file and modify the settings as necessary. Execute the genus next.Check the error after the genus has been successfully run; if it reveals a problem with the pad and circuit connection, go to the input file and repair it. Genus then takes off again. If it works, go to source synthesis. If there is a mistake, I will correct it; if not, I'll check the gui display to make sure the connection is good. Next,import the design into the encounter by going to the encounter. Then launch the MMMC browser and configure everything as needed. Save and leave when finished. You can then see where the pins are positioned in the encounter window. I now have to make a corner cell. To do that, I'll open the cpu_wpad.io file and make the necessary modifications. They will be connected to the circuit in the manner of VDD, VSS, VDDIOR, and VSSIOR. The floorplane is the next item. Go to floorplan, then choose a specific floorplan, and set core utilization to 0.4. I'll also set the core to 10, in addition to the core to left, the core to right, the core to top, and the core to bottom. After that, I'll plan my power. Metal 6 will be assigned to metals in the horizontal direction and Metal 5 to metals in the vertical direction. I'll make a unique design once it is finished. The circuit will thus be linked to utilizing a bespoke layer, which will connect VDD and VSS. Physical verification should happen right away. Here, I'll look at the DRC, LVS, ARC, and ERC. I will correct any infractions if I get any. Two different kinds of infractions are present here. These are violations of geometry and connection. The final SoC design will be revealed once everything has been resolved.

![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/2850f33f-984b-4f26-bfef-006f25557549)
Fig. 1.The basic flow chart of design a SOC of old mos 6502 CPU.



RESULT ANALYSIS-

TABLE. SOC results of Old mos 6502 CPU
![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/258287f7-c548-46bd-a62d-72598acaa6b1)



![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/37b6bf28-7fd6-48d5-a424-c7ef992932c9)
Fig. 2. Synthesis Result




![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/aff4263e-a967-428f-af1d-5ffbedd25ccf)
Fig. 3. Synthesized Circuit



![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/25fcf79c-274b-4c83-8be5-1d989262af02)
Fig. 4.Time Design_preCTS


![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/65a606ff-9a57-4983-9134-d16f9c2e82c1)
Fig.5.Opt Design_preCTS



![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/6c7343be-d4fa-4bec-8061-cba73e501090)
 Fig.6.Route Design




![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/ef166985-394b-4002-bff1-bd58da4e1595)
Fig.7.optDesign postRoute hold 


![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/63f2b1c0-2cb5-4584-877b-7f285d135695)
Fig.8.PnR before Routing



![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/f097e81f-4ea7-4760-8621-844fb5d43654)
Fig.9.PnR after Routing



![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/5c1a71b1-20b5-4c5f-90d1-dd0e72298016)
Fig.10.DRC verification



![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/e597bd2b-120d-4921-a004-ce6081261873)
Fig.11.Verify power via shacked via




![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/57e47442-c6ab-4c04-8e8a-08fbcbe8fa11)
Fig.12. Verify Geometry



![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/3862137d-eb17-472e-bf34-1a2c3b502c85)
 Fig.13.Verify Connectivity
 


 ![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/28eb016d-299a-4f6b-b48f-182cc8a8d829)
Fig.14.Verify AC limit




![image](https://github.com/johir95/SOC-design-of-an-Old-MOS-6502-CPU/assets/90377555/29dafd02-3870-4b44-99d4-65c16ec2be4a)
Fig.15.Final SOC of old  mos 6502 CPU 



CONCLUSION-
During physical design, we face a problem in the customer layer section. We can't connect the VDD and VSS to the circuit. We didn't face this type of issue previously. Then, when we login to another PC and do the same thing again, Then the problem is solved. Maybe it's a server issue. We face another problem in our encounter. After placement, we can't see the pin in the encounter window. Then, when we check the wpad code.I can see that the pin name PADDI is PADDI. I thought it was the pin name. Another surprising result I am facing is that when I was giving the repeat STA and verification command to take the screenshot, I got a DRC violation of 1000. Because the same things were overlapping. Otherwise, we didn't have any problems.


