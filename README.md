# NASSCOM_VSD_SOC_DESIGN_PROGRAM (RTL TO GDSII)
IT IS A 2 WEEKS PROGRAM ORGANIZED BY VSD IN ASSOCIATION WITH NASSCOM</p>
# CONTENTS
**DAY-1 : Inception of open-source EDA OpenLANE and sky130 PDK**</p>
DK1Sk1: HOW TO TALK WITH COMPUTERS.</p>
DK1Sk1_L1: Introduction to QFN-48 Package chip pads core die and IPs.</p>
![Screenshot 2024-08-08 102236](https://github.com/user-attachments/assets/88abd364-c5af-4d64-8d81-76d34bec01ca)</p>
**ARDUINO BOARD**</p>
Arduino boards are open-source electronics platforms based on simple hardware(PCB) and software(IDE,to upload the code).The encircled area is the microprocessor or the chip.The design process of this chip, from the abstract level down to fabrication, is accomplished through the RTL to GDSII flow.</p>
**PROCESSOR OR SOC**
![Screenshot 2024-08-08 102403](https://github.com/user-attachments/assets/c020790c-d101-4462-b7e6-2b46d4075486)</p>
This block diagram represents a high-level view of how a Processor/SoC interfaces with various peripherals, memory units, and external components. The Processor/SoC is central, managing and controlling data flow between these elements. The diagram shows how different communication protocols like JTAG, UART, I2C, and QSPI are used to connect the Processor/SoC to external memories (like Flash and SDRAM)(FOUNDRY IP'S), input/output pins (GPIO), and other functional blocks essential for the operation of a system.</p>
**THE LAYOUT AND COMPONENTS OF CHIP**</p>
![Screenshot 2024-08-08 102557](https://github.com/user-attachments/assets/80b4c8c9-e1f4-42f4-91ca-b77a449a4344)
![Screenshot 2024-08-08 103344](https://github.com/user-attachments/assets/675f027f-8f8a-4447-8c34-1865e6a6df79)
![Screenshot 2024-08-08 103813](https://github.com/user-attachments/assets/418c6a48-2491-46fe-8f41-870ce9e2f6b3)
**DIE :** Die refers to the actual piece of silicon that contains the integrated circuit (IC).In the diagram, the die is represented by the central block that houses all the major components, such as the RISC-V SoC, GPIO bank, PLL, SRAM, and the ADC/DAC modules.</p>
**PADS :** The contact points around the die that enable it to interface with external components, power supplies, and signals. They are crucial for connecting the internal circuitry of the die to the outside world.</p>
**CORE :** The central processing unit (CPU) of the microcontroller that executes instructions. 
**CENTRAL COMPONENTS**</p>
1.RISC-V SoC:</p>
The blue block labeled "RISC-V SoC" represents the main processing unit, which is based on the RISC-V architecture. This is the central processing core of the chip, responsible for executing instructions and managing tasks.</p>
2.GPIO Bank:</p>
The "GPIO Bank" adjacent to the RISC-V SoC indicates a set of General Purpose Input/Output (GPIO) pins. These pins are versatile and can be configured for various digital input or output operations, interacting with external peripherals or sensors.</p>
3.SRAM (Static Random-Access Memory):</p>
The orange block labeled "SRAM" is the on-chip memory used by the SoC to store data and instructions temporarily while the system is running. This memory is essential for fast access and processing.</p>
**PERIPHRALS AND INTERFACES** </p>
4.PLL (Phase-Locked Loop):</p>
The yellow block labeled "PLL" is a circuit that generates a stable clock signal, which is crucial for synchronizing the operations of the SoC and other components.</p>
5.DAC and ADC:</p>
The blocks labeled "dac" and "adc" represent the Digital-to-Analog Converter (DAC) and Analog-to-Digital Converters (ADC), respectively.</p>
6.GPIO Pins (gpio0 - gpio15):</p>
These pins are distributed along the left and top edges of the chip and are connected to the GPIO bank. They are used for general-purpose input/output, providing a flexible interface to external devices.</p>
7.Flash Interface (Bottom):</p>
The series of pins labeled "flash_io0" to "flash_clk" are part of the interface for connecting to external flash memory. This allows the SoC to access additional storage for firmware, programs, or data.</p>
8.Power Supply Pins:</p>
Pins labeled "vdd3v3," "vdd1v8," and "vss" (ground) along the right side indicate the power supply lines. These provide the necessary operating voltages (3.3V, 1.8V) and ground reference to the chip.</p>

DK1Sk1_L2:Introduction to RISC-V</p>
![Screenshot 2024-08-08 104351](https://github.com/user-attachments/assets/2ac918f5-72ff-4065-a56c-a3c45c6f38a4)</p>
The image illustrates the intricate relationship between software and hardware in CPU design, using a RISC-V architecture as an example. It starts with a snippet of assembly code written for the RISC-V processor, showcasing fundamental CPU operations. Below, the implementation of the picorv32 CPU core is presented in a Hardware Description Language (likely Verilog or SystemVerilog). This section shows how assembly instructions are translated into logical operations and register transfers within the CPU architecture, including parameters for core features like counters or cache.</p>
On the right side, the physical layout of the picorv32 CPU core is depicted, visualized with tools like "qflow." This layout highlights various circuit elements such as logic gates  and flip-flops , along with their interconnections. It represents how transistors and wires are arranged on the silicon die to realize the CPU’s functionality.</p>
Overall, the image demonstrates the progression from high-level code through hardware description to the physical realization of the RISC-V core, illustrating the different abstraction levels involved in CPU design.</p>

Dk1Sk1_L3:From software applications to Hardware</p>
![Screenshot 2024-08-08 105151](https://github.com/user-attachments/assets/229525ce-e4e5-42d0-85e7-ec96ea731f93)</p>
This image illustrates the complete process from defining the instruction set to the final physical hardware implementation.</p>
1.Instruction Set Architecture (ISA): The abstract interface or architecture of the computer where assembly instructions are defined (e.g., add x6, x10, x6).</p>
2.Assembler: Converts these assembly instructions into machine code (binary format), which is represented in the image as a series of 0s and 1s.</p>
3.RTL (Register Transfer Level): A code snippet (likely in Verilog or VHDL) that defines the hardware to execute these instructions. This RTL describes the logic in terms of data flow and digital operations.</p>
4.Synthesized Netlist: The RTL is synthesized into a netlist, which is a detailed list of logical components and their connections, represented as a schematic diagram.</p>
5.Physical Design: The netlist is then implemented in physical hardware through a process called physical design, resulting in a chip layout where the logic gates and connections are physically realized.</p>

Dk1SK2: SOC DESIGN AND OPENLANE</p>
Dk1Sk2_L1:Introduction to all components of an open-source digital ASIC design</p>
**RTL Design**, or Register Transfer Level Design, is a critical phase in digital circuit design. It describes the digital system in terms of data flow between registers and the logical operations performed on the data.</p>
**EDA TOOLS** Exploratory Data Analysis (EDA) tools help analysts and data scientists explore datasets, uncover patterns, spot anomalies, test hypotheses, and summarize data through visualizations and statistics. </p>
A **Process Design Kit (PDK)** is a crucial element in semiconductor manufacturing, particularly in the design of integrated circuits (ICs). It serves as a comprehensive library of design rules, models, and data that describe the specific manufacturing process technology that a semiconductor foundry offers. PDKs enable designers to create physical layouts that can be reliably fabricated using a specific manufacturing process.</p>
**The Google SkyWater 130nm PDK** is an open-source Process Design Kit (PDK) provided by SkyWater Technology Foundry in collaboration with Google. This PDK is notable because it's one of the first openly available PDKs, enabling a broad community of developers, researchers, and hobbyists to design and fabricate their own integrated circuits (ICs) without the need for expensive commercial licenses or proprietary access.</p>







