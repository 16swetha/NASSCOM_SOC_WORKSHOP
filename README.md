## NASSCOM_VSD_SOC_DESIGN_PROGRAM (RTL TO GDSII)
 ### IT IS A 2 WEEKS PROGRAM ORGANIZED BY VSD IN ASSOCIATION WITH NASSCOM</p>
 
## CONTENTS
### **DAY-1 : Inception of open-source EDA OpenLANE and sky130 PDK**</p>
` DK1Sk1: HOW TO TALK WITH COMPUTERS ` </p>

**DK1Sk1_L1: Introduction to QFN-48 Package chip pads core die and IPs.** </p>

![Screenshot 2024-08-08 102236](https://github.com/user-attachments/assets/88abd364-c5af-4d64-8d81-76d34bec01ca)</p>
**ARDUINO BOARD**</p>
- Arduino boards are open-source electronics platforms based on simple hardware(PCB) and software(IDE,to upload the code).The encircled area is the microprocessor or the chip.The design process of this chip, from the abstract level down to fabrication, is accomplished through the RTL to GDSII flow.</p>

**PROCESSOR OR SOC**</p>
![Screenshot 2024-08-08 102403](https://github.com/user-attachments/assets/c020790c-d101-4462-b7e6-2b46d4075486)</p>
- This block diagram represents a high-level view of how a Processor/SoC interfaces with various peripherals, memory units, and external components. The Processor/SoC is central, managing and controlling data flow between these elements. The diagram shows how different communication protocols like JTAG, UART, I2C, and QSPI are used to connect the Processor/SoC to external memories (like Flash and SDRAM)(FOUNDRY IP'S), input/output pins (GPIO), and other functional blocks essential for the operation of a system.</p>

**THE LAYOUT AND COMPONENTS OF CHIP**</p>
![Screenshot 2024-08-08 102557](https://github.com/user-attachments/assets/80b4c8c9-e1f4-42f4-91ca-b77a449a4344)</p>
![Screenshot 2024-08-08 103344](https://github.com/user-attachments/assets/675f027f-8f8a-4447-8c34-1865e6a6df79)</p>
![Screenshot 2024-08-08 103813](https://github.com/user-attachments/assets/418c6a48-2491-46fe-8f41-870ce9e2f6b3)</p>

1. **DIE :** </p>
- Die refers to the actual piece of silicon that contains the integrated circuit (IC).In the diagram, the die is represented by the central block that houses all the major components, such as the RISC-V SoC, GPIO bank, PLL, SRAM, and the ADC/DAC modules.</p>
2. **PADS :** </p>
- The contact points around the die that enable it to interface with external components, power supplies, and signals. They are crucial for connecting the internal circuitry of the die to the outside world.</p>
3. **CORE :** </p>
- The central processing unit (CPU) of the microcontroller that executes instructions.

**COMPONENTS**</p>
1. **RISC-V SoC:** </p>
- The blue block labeled "RISC-V SoC" represents the main processing unit, which is based on the RISC-V architecture. This is the central processing core of the chip, responsible for executing instructions and managing tasks.</p>
2. **GPIO Bank:** </p>
- The "GPIO Bank" adjacent to the RISC-V SoC indicates a set of General Purpose Input/Output (GPIO) pins. These pins are versatile and can be configured for various digital input or output operations, interacting with external peripherals or sensors.</p>
3. **SRAM (Static Random-Access Memory):** </p>
- The orange block labeled "SRAM" is the on-chip memory used by the SoC to store data and instructions temporarily while the system is running. This memory is essential for fast access and processing.</p>
4. **PLL (Phase-Locked Loop):** </p>
- The yellow block labeled "PLL" is a circuit that generates a stable clock signal, which is crucial for synchronizing the operations of the SoC and other components.</p>
5. **DAC and ADC:** </p>
- The blocks labeled "dac" and "adc" represent the Digital-to-Analog Converter (DAC) and Analog-to-Digital Converters (ADC), respectively.</p>
6. **GPIO Pins (gpio0 - gpio15):** </p>
- These pins are distributed along the left and top edges of the chip and are connected to the GPIO bank. They are used for general-purpose input/output, providing a flexible interface to external devices.</p>
7. **Flash Interface (Bottom):** </p>
- The series of pins labeled "flash_io0" to "flash_clk" are part of the interface for connecting to external flash memory. This allows the SoC to access additional storage for firmware, programs, or data.</p>
8.**Power Supply Pins:** </p>
- Pins labeled "vdd3v3," "vdd1v8," and "vss" (ground) along the right side indicate the power supply lines. These provide the necessary operating voltages (3.3V, 1.8V) and ground reference to the chip.</p>

**DK1Sk1_L2:Introduction to RISC-V**</p>

![Screenshot 2024-08-08 104351](https://github.com/user-attachments/assets/2ac918f5-72ff-4065-a56c-a3c45c6f38a4)</p>
- The image illustrates the intricate relationship between software and hardware in CPU design, using a RISC-V architecture as an example. It starts with a snippet of assembly code written for the RISC-V processor, showcasing fundamental CPU operations. Below, the implementation of the picorv32 CPU core is presented in a Hardware Description Language (likely Verilog or SystemVerilog). This section shows how assembly instructions are translated into logical operations and register transfers within the CPU architecture, including parameters for core features like counters or cache.</p>
- On the right side, the physical layout of the picorv32 CPU core is depicted, visualized with tools like "qflow." This layout highlights various circuit elements such as logic gates  and flip-flops , along with their interconnections. It represents how transistors and wires are arranged on the silicon die to realize the CPU’s functionality.</p>
- Overall, the image demonstrates the progression from high-level code through hardware description to the physical realization of the RISC-V core, illustrating the different abstraction levels involved in CPU design.</p>

**Dk1Sk1_L3:From software applications to Hardware**</p>

![Screenshot 2024-08-08 105151](https://github.com/user-attachments/assets/229525ce-e4e5-42d0-85e7-ec96ea731f93)</p>
- This image illustrates the complete process from defining the instruction set to the final physical hardware implementation.</p>
1. **Instruction Set Architecture (ISA):** </p>
- The abstract interface or architecture of the computer where assembly instructions are defined (e.g., add x6, x10, x6).</p>
**Assembler:** </p>
- Converts these assembly instructions into machine code (binary format), which is represented in the image as a series of 0s and 1s.</p>
2. **RTL (Register Transfer Level):** </p>
- A code snippet (likely in Verilog or VHDL) that defines the hardware to execute these instructions. This RTL describes the logic in terms of data flow and digital operations.</p>
3. **Synthesized Netlist:** </p>
- The RTL is synthesized into a netlist, which is a detailed list of logical components and their connections, represented as a schematic diagram.</p>
4. **Physical Design:** </p>
- The netlist is then implemented in physical hardware through a process called physical design, resulting in a chip layout where the logic gates and connections are physically realized.</p>

`Dk1SK2: SOC DESIGN AND OPENLANE`</p>

**Dk1Sk2_L1:Introduction to all components of an open-source digital ASIC design**</p>
- **RTL Design**, or Register Transfer Level Design, is a critical phase in digital circuit design. It describes the digital system in terms of data flow between registers and the logical operations performed on the data.</p>

- **EDA TOOLS** Exploratory Data Analysis (EDA) tools help analysts and data scientists explore datasets, uncover patterns, spot anomalies, test hypotheses, and summarize data through visualizations and statistics. </p>

- A **Process Design Kit (PDK)** is a crucial element in semiconductor manufacturing, particularly in the design of integrated circuits (ICs). It serves as a comprehensive library of design rules, models, and data that describe the specific manufacturing process technology that a semiconductor foundry offers. PDKs enable designers to create physical layouts that can be reliably fabricated using a specific manufacturing process.</p>

- **The Google SkyWater 130nm PDK** is an open-source Process Design Kit (PDK) provided by SkyWater Technology Foundry in collaboration with Google. This PDK is notable because it's one of the first openly available PDKs, enabling a broad community of developers, researchers, and hobbyists to design and fabricate their own integrated circuits (ICs) without the need for expensive commercial licenses or proprietary access.</p>

**Dk1Sk2_L2:simplified RTL TO GDSII MODEL**</p>

![Screenshot 2024-08-09 141423](https://github.com/user-attachments/assets/34a130f0-84c4-4307-a960-6f0fdc0c79aa)</p>
![Screenshot 2024-08-09 143244](https://github.com/user-attachments/assets/a7131780-660d-449c-95cb-3aada57fe04e)
 **1. RTL (Register Transfer Level):**</p>
   - **Input**: RTL is the high-level representation of the digital circuit design written in hardware description languages like Verilog or VHDL.</p>
 **2. Synthesis (Synth):**</p>
   - **Purpose**: Converts the RTL code into a gate-level netlist, which specifies the logic gates and connections required to implement the design.</p>
   - **Output**: A netlist that is used in the subsequent stages of the physical design process.</p>
**3. Floor/Power Planning (FP+PP):**</p>
   - **Floorplanning (FP)**: Arranges the different blocks of the circuit on the chip, optimizing space, performance, and power.</p>
   - **Power Planning (PP)**: Ensures efficient power distribution across the chip by designing the power grid.</p>
 **4. Placement (Place):**</p>
   - **Purpose**: Involves positioning the individual standard cells (like logic gates) within the blocks defined during floorplanning to minimize wiring length, delay, and power consumption.</p>
**5. Clock Tree Synthesis (CTS):**</p>
   - **Purpose**: Builds the clock distribution network, ensuring that the clock signal is distributed evenly across the chip with minimal skew (timing differences).</p>
**6. Routing (Route):**</p>
   - **Purpose**: Connects the placed standard cells with metal wires, creating the final layout. This step ensures that all the necessary connections are made without violating design rules.</p>
 **7. Sign Off:**</p>
   - **Purpose**: Involves a series of checks and validations to ensure that the design meets all the required specifications and is ready for manufacturing. This includes timing analysis, power analysis, and physical verification.</p>
 **Final Output - GDSII:**</p>
   - **GDSII File**: The final result is a GDSII file, which contains the physical layout of the integrated circuit, ready to be sent to a semiconductor foundry for fabrication.</p>
 **PDK (Process Design Kit):**</p>
   - The diagram also shows that the PDK (Process Design Kit) is used during these stages to provide the necessary design rules, device models, and other data required for the physical design.</p>
   
`Dk1Sk3:Get Familiar with Open Source EDA Tools`</p>
# OpenLane Flow using Docker and Synthesis Commands

## After Synthesis Calculation
- **FLOP RATIO** = `No of D flipflop / Total Number of cells`
- **Percentage** = `Flop Ratio × 100`

## Steps to Start OpenLane using Docker and Run Synthesis

1. **Navigate to the OpenLane Working Directory:**
    ```bash
    cd Desktop/work/tools/openlane_working_dir/openlane
    docker
    ```
![11](https://github.com/user-attachments/assets/279609dd-e5f4-4349-9a13-f7122d626950)
![12](https://github.com/user-attachments/assets/33057154-25f2-44f0-bfd4-3ccfd8a27e5a)



2. **Enter the OpenLane Flow Contained Docker Sub-System:**
    ```bash
    ./flow.tcl -interactive
    ```

    
3. **Load Required Packages for OpenLane Functionality:**
    ```tcl
    package require openlane 0.9
    ```
![13](https://github.com/user-attachments/assets/c1730a16-8216-4cc6-9fda-0b5771141a12)

    

5. **Prepare the Design:**
    ```bash
    prep -design picorv32a
    ```
 ![14](https://github.com/user-attachments/assets/384c1689-ca1c-4c4e-b7e9-c7e8553e9a9e)


6. **Run Synthesis:**
    ```bash
    run_synthesis
    ```
![16](https://github.com/user-attachments/assets/d59310d2-7408-4dc4-8f70-79183738da14)


## Notes
- Make sure to replace `picorv32a` with the design you are working on.
- The FLOP ratio and percentage calculation are essential metrics to assess after synthesis.

### **DAY-2 GOOD FLOORPLAN VS BAD FLOOR PLAN AND INTRODUCTION TO LIBRARY CELLS**</p>

` Dk2_Sk1-Chip floor planning considerations` </p>

- The session says about the height and the width of the core and die</p>
- The initial step in the physical design process involves determining the width and height of the layout. Let's start with a netlist that includes two flip-flops and a simple combinational logic circuit between them. A netlist represents the connectivity of an electronic design. Here, we're focusing on the dimensions of the logic gates (AND & OR) and the specific flip-flops. Our goal is to convert these symbols into physical dimensions, with an emphasis on the dimensions of the Core and Die, rather than the wiring.</p>

![Screenshot 2024-08-10 114934](https://github.com/user-attachments/assets/cbb1ee84-aa25-4953-aabd-683886133d5b)
![Screenshot 2024-08-10 114946](https://github.com/user-attachments/assets/d98c509b-7de8-429d-b93e-76c9803b60fe)</p>
From the above diagram</p>
let us consider standard cell that has the dimensions of 1unit * 1unit</p>
so area = 1sq units</p>
![Screenshot 2024-08-10 115125](https://github.com/user-attachments/assets/41b9187d-7587-4b85-b380-5e973ac0d384)
![Screenshot 2024-08-10 115312](https://github.com/user-attachments/assets/fe64320a-6319-4520-9e46-5f0f1d565b19)</p>
 utilization factor = 1
(1 means core is fully utilized  the area and no space left)

Aspect Ratio = Height / width = 2 unit / 2unit = 1

Aspect Ratio is 1 it signifies that chip is square shaped. When it is not 1 it means the chip is in rectangular shape.

![Screenshot 2024-08-10 120207](https://github.com/user-attachments/assets/dfcc9ac7-8b8a-4327-9cad-9bfb6b47bf77)</p>
The image shows the process of defining the locations of preplaced cells in a physical design layout. It begins with a combinational logic design, which is then broken down into specific components like logic gates and flip-flops. The circuit is divided into two parts (cut1 and cut2) and further grouped into two blocks, "Block 1" and "Block 2". Each block contains a specific set of cells, which are preplaced in defined locations to optimize the layout for performance, power, and area requirements.</p>
![Screenshot 2024-08-10 120249](https://github.com/user-attachments/assets/33c15cbd-34ff-4f37-b6b3-5d8001ef4381)
![Screenshot 2024-08-10 120312](https://github.com/user-attachments/assets/cf13f099-d3c3-4c57-9b9d-a6005057ec17)
![Screenshot 2024-08-10 120322](https://github.com/user-attachments/assets/ad4fe523-a904-4c00-a8b7-2b2346870efb)</p>
In both blocks, we extend the input-output pins and then black box them, making the internal design invisible to those viewing the main netlist. By separating them as distinct IPs or modules, we enable reuse of these blocks after a single implementation. This approach is similar to other IPs like Memory, Clock-gating cells, Comparators, and MUXes, which are part of the top-level netlist. These IPs receive signals, perform specific functions, and deliver outputs, but their functionality is implemented only once.</p>
![Screenshot 2024-08-10 120635](https://github.com/user-attachments/assets/89fb7b3d-ec9a-4998-b6ae-65304a77e0ab)</p>

The arrangement of IPs on a chip is called floorplanning. Pre-placed cells, which have user-defined locations, are positioned so that automated tools don’t change their placement. In circuits, de-coupling capacitors manage switching currents when gates change states, ensuring proper voltage levels. However, the presence of resistance and inductance can cause a voltage drop, leading to a reduced voltage at certain nodes during switching.</p>

![Screenshot 2024-08-10 121146](https://github.com/user-attachments/assets/cb562266-8b71-40a7-9297-dacab3c20cff)
![Screenshot 2024-08-10 122209](https://github.com/user-attachments/assets/30ec5a23-fa2e-425d-b05e-0e653eb9d958)
![Screenshot 2024-08-10 122530](https://github.com/user-attachments/assets/5f1d48e0-b86f-47ba-8381-f4cf004ebc89)
![Screenshot 2024-08-10 122845](https://github.com/user-attachments/assets/c44f264e-4186-4423-8286-b2d646171473)</p>
In the chip layout, decoupling capacitors are placed between Block A, Block B, and Block C to ensure that power is properly supplied by these capacitors. This setup handles local communication effectively. 

**Power Planning:**
Consider the local circuitry as a black box that can be repeated multiple times, with logic at the boundaries. The current demand issue is addressed by decoupling capacitors. Signals sent from a driver to a load, such as a logic 0 to logic 1 transition, need to be maintained consistently, requiring sufficient power from the supply. For a 16-bit bus, however, placing decoupling capacitors along the entire path isn’t feasible, leading to potential voltage drops due to the distance from the power supply.

When the bus signals transition, capacitors charged to Vdd (logic 1) or discharged to ground (logic 0) will switch states. If the bus is connected to an inverter, all initially charged capacitors will discharge and vice-versa. The issue arises because all capacitors share a single ground connection, causing a spike, known as **Ground Bounce**, during discharge. If this spike exceeds the noise margin, it could push the signal into an undefined state, leading to unpredictable logic levels.

Similarly, when capacitors charged to 0 volts need to be charged to V volts, they draw current through a single Vdd connection, potentially lowering the voltage at the Vdd tap point. If this voltage drop stays within the noise margin, the circuit remains stable, but if it enters an undefined region, the behavior becomes unpredictable. This problem occurs because power is supplied from only one point.

**Solution:**
To address this issue, multiple power supplies should be used, creating a mesh network. Each block would draw power from the nearest supply and similarly discharge to the closest ground. This mesh power supply design helps maintain consistent power levels across the chip, preventing issues like Ground Bounce and voltage drops.

So the LAYOUT will be like:</p>
![Screenshot 2024-08-10 123006](https://github.com/user-attachments/assets/72a59b85-4b4a-4d5f-9b2c-59b95c4033f2)

The connectivity information between the gates is coded using VHDL/Verilog language and is called as 'Netlist'.</p>
![Screenshot 2024-08-10 123503](https://github.com/user-attachments/assets/0eb8831a-802e-48e5-82d2-f647e0fcabce)</p>

### RUNNING OF FLOORPLAN
    
    run_floorplan

 
**This is the floorplan folder with its directives**

![f1](https://github.com/user-attachments/assets/bc6a5018-e677-4e84-93ac-85b2721390f0)</p>
 
- Here we can see the core utilization is 50% and aspect ratio is 1.These both are by default values.

![f2](https://github.com/user-attachments/assets/381c1b0e-606d-4d89-9713-9bcc94c5a275)</p>

- It is the ` placement `area</p>
![f3](https://github.com/user-attachments/assets/c9791490-3514-4518-a80a-4ec122450888)</p>

In OpenLANE, FP_PDN files are used to configure the power distribution network, and these switches are set by default during the floorplan stage. The FP_IO MODE setting (1, 0) indicates that pin positioning is random but equally spaced.

In terms of priority, OpenLANE first considers the system default settings in `floorplanning.tcl`, followed by the settings in `config.tcl`, and finally, the settings in the PDK variant file (`sky130A_sky130_fd_sc_hd_config.tcl`).

![f5](https://github.com/user-attachments/assets/1b7ae4e0-9f38-4f71-9cae-77eebcac6721)

![f6](https://github.com/user-attachments/assets/8de234d2-f263-43d7-9d5f-01c756bdb480)

![f7](https://github.com/user-attachments/assets/d9e90bf4-8929-49fd-a519-5270acda3f50)

**THIS IS HOW THE FLOORPLAN WORKS**

![2](https://github.com/user-attachments/assets/ac671417-2f8c-4b4c-af92-518a77e8700e)

![FLOORPLAN](https://github.com/user-attachments/assets/8d1b09cf-9582-497f-8154-bcbba0b1afab)

### Die Area Calculation
```bash
**Given:**
- Unit distance: 1 micron
- Die width in unit distance: 660,685
- Die height in unit distance: 671,405

**Conversions:**
- Die width in microns = \( \frac{660,685}{1000} = 660.685 \) microns
- Die height in microns = \( \frac{671,405}{10,000} = 671.405 \) microns

**Area Calculation:**
- Area of the die in microns = \( 660.685 \times 671.405 = 443,587.212425 \) square microns
```

### Load Floorplan `.def` File in Magic Tool

To view the generated floorplan using the Magic layout tool, follow these steps:

1. **Change Directory:**

Navigate to the directory containing the generated floorplan `.def` file:

   ```bash
   cd  /Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/10-08_12-54/results/floorplan/
   ```
2. **Load the Floorplan in Magic:**

Run the following command to load the floorplan .def file in Magic:

```bash
magic -T  /Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech \lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```
![f8](https://github.com/user-attachments/assets/331eb8f0-ad05-4e61-aa86-fe8ade8260ea)

![f9](https://github.com/user-attachments/assets/11c5270c-9a80-469b-b885-2d3d28983863)

![f10](https://github.com/user-attachments/assets/cf42a34b-1439-4ceb-85bb-85b91db9bfd5)

![f11](https://github.com/user-attachments/assets/1100b721-83a2-4940-830b-f696d62eddde)

![f12](https://github.com/user-attachments/assets/1d12ae4c-2de9-40d2-82cf-1333f5292843)

` D2_Sk2-LIBRARY BINDING AND PLACEMENT `</p>

Binding a netlist with physical cells is a critical step in the process of designing and implementing integrated circuits (ICs). This step involves mapping the logical components of your design, represented by the netlist, to the actual physical cells in a standard cell library, which are used during the layout phase of IC design. Here’s an overview of how this process typically works:</p>
1. Netlist Creation:</p>
The netlist is generated from a high-level design, typically written in a hardware description language (HDL) like Verilog or VHDL. The netlist describes the circuit's components (like gates, flip-flops, etc.) and the connections between them.</p>
2. Standard Cell Library:</p>
A standard cell library contains pre-designed and pre-characterized physical representations of various logic gates and other components. Each cell in the library corresponds to a specific logic function, such as NAND, NOR, D flip-flop, etc., and comes with details like area, power consumption, and delay characteristics.</p>

![f13](https://github.com/user-attachments/assets/0657c463-6aa5-4ac3-879c-c1817fa0344f)

A Library in the context of integrated circuit (IC) design refers to a collection of pre-designed, pre-characterized components (cells) that are used during various stages of the design process. These libraries are essential for translating a digital design from its high-level representation (e.g., Verilog or VHDL code) to a physical implementation on silicon.Library divides into 2 sublibraries. First may consists of size and shape  and other consists of the delay information.</p>

**PLACEMENT :**</p>

Once the netlist is bound to physical cells, the placement tool arranges these cells on the IC layout. This step considers the physical constraints and aims to optimize the placement for minimal delay, power, and area usage.</p>

Consider the circuit diagram</p> 
![f14](https://github.com/user-attachments/assets/05a75725-cf73-46af-856f-f0b64b735edd)</p>
Signal integrity: </p>
Signal integrity in PCB (Printed Circuit Board) placement refers to maintaining the quality and fidelity of electrical signals as they travel through a circuit. Good signal integrity ensures that the signals are not distorted, delayed, or lost due to the layout and placement of components on the board. Poor signal integrity can lead to errors, malfunction, and degraded performance of electronic devices.</p>

Optimize placement:</p>
Optimizing  placement plays a crucial for ensuring signal integrity, minimizing delays, and improving overall performance. The key goal is to reduce the length of critical signal paths and manage capacitance to minimize unwanted effects like signal degradation, noise, and power loss.</p> 
We add `repeaters`(buffers) inorder to create a new singal between the input and the output such that the data is encrypted correctly and the information is not loss.</p>
Consider the placement of the ff-1:</p>
We donot add any buffers as the data can be accessible easily.</p>
![f15](https://github.com/user-attachments/assets/702b03a7-92f7-4fd1-884c-a3c2404bc3f2)</p>

Now let us consider the ff-2:</p>
The signal path for `Din2` starts at its input, where it first passes through a buffer to strengthen the signal. It then reaches Flip-Flop 1 (FF1) and continues through additional buffers and logic components labeled "1" and "2." Finally, the signal arrives at Flip-Flop 2 (FF2) and is connected to `Dout2`. Buffers are strategically placed along the path to ensure the signal remains strong and stable, optimizing signal integrity throughout the route.</p>
![f16](https://github.com/user-attachments/assets/d3f7d8ae-d433-4f29-92be-ccf61c31ac20) </p>

consider ff-3:</p>
The signal path for `Din3` begins at its input on the left side of the PCB layout. It first reaches Flip-Flop 1 (FF1), then passes through a buffer to strengthen the signal. The signal continues through a logic block labeled "2" and is routed through another buffer before reaching its final destination at Flip-Flop 2 (FF2), which is connected to `Dout3`. Buffers are strategically placed along this path to ensure that the signal remains strong and stable throughout its journey.</p>
![f17](https://github.com/user-attachments/assets/416bd415-2a46-4bd4-9445-e3557fffe60e)</p>


consider ff-4:</p>
The path of `Din4` begins at the left side of the diagram and first passes through a yellow flip-flop labeled `FF1`. The signal then moves through a green buffer (`Buf`) before entering a green flip-flop, also labeled `FF1`. After that, it passes through a blue flip-flop labeled `FF2`. Finally, the signal exits the diagram as `Dout4` on the right side. This entire path is visually emphasized by being enclosed in a dotted oval in the bottom right section of the diagram.</p>

![f18](https://github.com/user-attachments/assets/7747c1cd-a8d7-455a-85c3-1d4bb849da35)</p>

Congestion-aware placement using RePlAce involves:</p>

Global Placement: Initial rough positioning of cells with a focus on managing congestion.</p>
Detailed Placement: Fine-tuning of cell positions to optimize local routing and meet design constraints.</p>
RePlAce integrates both global and detailed placement stages, with an emphasis on managing and reducing congestion throughout the placement process.</p>

Run `picorv32a`

![f20](https://github.com/user-attachments/assets/19595c21-b5f7-4dec-93b0-4841ae51cb4c)</p>
![f19](https://github.com/user-attachments/assets/007b31a8-c568-414c-82f1-e15f3993fbdb)</p>

`Dk2_Sk3-CELL DESIGN AND CHARACTERIZATION FLOWS`</p>

Steps for characterization and modelling</p>
S-1 logic synthesis</p>
S-2 floorplanning</p>
S-3 placement</p>
S-4 clock tree synthesis</p>
S-5 routing</p>
S-6 static timing analysis</p>
**CELL DESIGN FLOW**</p>
Standard cells are present in the library . Library consists of cells of different functionality,sizes and thresholds.Larger the size,Largest the drivestences.</p>

![Screenshot 2024-08-13 183216](https://github.com/user-attachments/assets/902728a5-8e64-4aec-abdb-b662bcbdb784)</p>

![Screenshot 2024-08-13 183533](https://github.com/user-attachments/assets/37178593-6e1a-43cb-8483-5abc8e3bb569)</p>

 The right side of the image shows the metal layers which are used in the fabrication of the circuit. These layers are responsible for connecting different parts of the circuit together. The overall flow of the process is shown by the arrows that connect the different stages of the process. The process is iterative, meaning that the designer may need to go back and make changes to the design at any stage.</p>
The design steps are:</p>
- Circuit design


![Screenshot 2024-08-13 184131](https://github.com/user-attachments/assets/fc98c351-95ed-4c1c-b1d6-6b4aed7adba1)

![Screenshot 2024-08-13 184357](https://github.com/user-attachments/assets/3a0c823c-5bcf-46b7-a295-13cf90dc1dfe)</P>

- Layout design</p>
Art of Layout: EULER'S GRAPH , STICK DIAGRAM

![Screenshot 2024-08-13 184406](https://github.com/user-attachments/assets/43c183c5-f6a6-4420-8c80-2e5eba1190ca)</p>

![Screenshot 2024-08-13 185134](https://github.com/user-attachments/assets/2bfd81b2-2041-4aca-a433-b2684991f84d)</p>

**Characterization Flow**</p>
Steps:</p>
S-1: Read in the modules</p>
S-2: Read the extract spiece Netlist</p>
S-3: Behaviour of Buffer</p>
S-4: Sub ckt of Buffers</p>
S-5: Attach the power sources</p>
S-6: Apply the stimulus</p>
S-7: Output Capacitance</p>
S-8: Provide the necessary stimulus command</p>
S-9: Guna software</p>

![Screenshot 2024-08-13 190414](https://github.com/user-attachments/assets/6c0fcd84-16da-413e-9db5-80cfa717a3df)

`Dk2_Sk4-TIMING CHARACTERIZATION PARAMETERS`</p>

![Screenshot 2024-08-13 185725](https://github.com/user-attachments/assets/fca1a1be-01d6-48ac-a1b7-78ba16ed76a7)
![Screenshot 2024-08-13 190611](https://github.com/user-attachments/assets/fab34e82-9c26-433b-9776-2761dcdc9de5)
![Screenshot 2024-08-13 191031](https://github.com/user-attachments/assets/c6cc9916-e214-49b5-8e43-4ffe36f8df79) </p>

- Slew Low Rise Threshold: Start point of the rising edge transition.</p>
- Slew High Rise Threshold: End point of the rising edge transition.</p>
- Slew Low Fall Threshold: Start point of the falling edge transition.</p>
- Slew High Fall Threshold: End point of the falling edge transition.</p>
- Input Rise Threshold: Voltage level where input is considered 'high'.</p>
- Input Fall Threshold: Voltage level where input is considered 'low'.</p>
- Output Rise Threshold: Voltage level where output is considered 'high'.</p>
- Output Fall Threshold: Voltage level where output is considered 'low'.</p>
 **PROPAGATION DELAY</p>
 
  time(out__thr)-time(in__thr)</p>
  
![Screenshot 2024-08-13 191451](https://github.com/user-attachments/assets/40445262-8984-409f-96f4-dd121ce7cd2d)</p>

**TRANSITION TIME**</p>

time(slew_high)-time(slew_low)</p>

![Screenshot 2024-08-13 191911](https://github.com/user-attachments/assets/3133170d-ed6e-4128-9b50-dbf8415e2b6f)</p>

### **DAY3 : Design library cells using magic layout and ngspice characterization**
`Dk3_Sk1-Labs for CMOS Inverter and ngspice simulation`</p>
Firstly the configruation of the switches was "env(FP_IO_MODE) 1" . we need to change to 2 inorder to get that the syntax is</p>
"env(FP_IO_MODE) 2" </p>
run the floorplan and check the pin locations through magic -T</p>

![s1](https://github.com/user-attachments/assets/62d4bc6a-7171-443e-ae36-8e62ce085d5f)

![s2](https://github.com/user-attachments/assets/c539cc81-48d8-4fe1-a6e4-c2132d998219)

![s3](https://github.com/user-attachments/assets/0090f9c4-411b-4702-87eb-6eaf12acaff1)

### SPICE DECK FOR CMOS INVERTER</p>

![Screenshot 2024-08-15 133749](https://github.com/user-attachments/assets/dd8adff3-2a77-4231-b989-b4387cd62c4a)

![Screenshot 2024-08-15 133840](https://github.com/user-attachments/assets/8a7e3324-d5be-4ad6-be53-bcf73ab0338d)

![Screenshot 2024-08-15 134025](https://github.com/user-attachments/assets/fb3c688f-2715-48f8-86a7-f2705612a80b)

![Screenshot 2024-08-15 134631](https://github.com/user-attachments/assets/0522fc31-4b8f-4221-9bf5-81c77331728d)</p>


Component Connectivity:
In this section, we define the connectivity of the substrate pin, which is crucial for adjusting the threshold voltage of the PMOS and NMOS transistors.</p>

Component Values:
The values for the PMOS and NMOS transistors are defined. Both PMOS and NMOS are chosen to have the same size.</p>

Identifying Nodes:
Nodes are defined as the points between which a component is connected. These nodes are essential for defining the netlist.</p>

Naming the Nodes:
The nodes are named as follows: Vin, Vss, Vdd, and out.</p>

Connections:
- **M1 MOSFET**: The drain is connected to the out node, the gate is connected to the in node, and both the source and substrate of the PMOS transistor are connected to the Vdd node.</p>
- **M2 MOSFET**: The drain is connected to the out node, the gate is connected to the in node, and both the source and substrate of the NMOS transistor are connected to ground (node 0).</p>
- **CLOAD**: This capacitor is connected between the out node and ground (node 0) with a value of 10fF.</p>
- **Supply Voltage (Vdd)**: The supply voltage is connected between the Vdd node and ground (node 0) with a value of 2.5V.</p>
- **Input Voltage (Vin)**: The input voltage is connected between the Vin node and ground (node 0) with a value of 2.5V.</p>

Simulation Commands:
Simulation commands are provided to sweep the Vin from 0 to 2.5V with a step size of 0.05V, allowing us to observe Vout as Vin changes.</p>

Final Modeling:
The final step involves defining the model files, which contain the complete descriptions of the NMOS and PMOS transistors.</p>

### SPICE SIMULATION LAB FOR CMOS

![Screenshot 2024-08-15 135243](https://github.com/user-attachments/assets/ae1e9ffa-16f0-4a30-b2e2-d6ed81f8b9ec)</p>

**DC CHARACTERISTICS**

![Screenshot 2024-08-15 135906](https://github.com/user-attachments/assets/697c1254-36d8-43e5-a9e2-32abe205ce72)</p>

![Screenshot 2024-08-15 140742](https://github.com/user-attachments/assets/568d4588-a35b-45bf-a3dc-efbd701a024f)

![Screenshot 2024-08-15 141017](https://github.com/user-attachments/assets/75ef8a51-2fa8-4b14-9c38-e0bfa0325920)


# LABS FOR CMOS
``` bash
# Change directory to OpenLane
cd Desktop/work/tools/openlane_working_dir/openlane

# Clone the repository with the custom inverter design
git clone https://github.com/nickson-jose/vsdstdcelldesign

# Change into the repository directory
cd vsdstdcelldesign

# Copy the Magic tech file to the repository directory for easy access
cp /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech .

# Check the contents to ensure everything is present
ls -ltr

# Command to open the custom inverter layout in Magic
magic -T sky130A.tech sky130_inv.mag &

```
![s4](https://github.com/user-attachments/assets/9d35d7d6-5029-421c-96cc-cb2b9087ded0)

![s5](https://github.com/user-attachments/assets/8e183c53-6286-48ae-861d-1b85eaf02ea8)

![s6](https://github.com/user-attachments/assets/41688f36-70c9-444a-a3a3-9c5ac3598c39)

![s7](https://github.com/user-attachments/assets/453684b2-5fd2-4d0e-b337-b8a597d1ff99)

![s8](https://github.com/user-attachments/assets/22a26f69-719f-4fb5-a7ff-29a53f973a67)

![s10](https://github.com/user-attachments/assets/81a0d67a-0b8a-4cd1-87e8-778f33ad6c8b)


# MODIFICATIONS

![S11](https://github.com/user-attachments/assets/85f31864-3f5f-4e34-b7ba-7d29fc85908c)

![s12](https://github.com/user-attachments/assets/77553a55-9089-43fc-9a0e-8d7d9927a0ec)

``` bash
# Command to directly load spice file for simulation to ngspice
ngspice sky130_inv.spice

# Now that we have entered ngspice with the simulation spice file loaded we just have to load the plot
plot y vs time a
```

![s13](https://github.com/user-attachments/assets/de0285b7-9149-45e7-9902-4b27853cb8a8)

![s14](https://github.com/user-attachments/assets/c5001dce-5bc8-415c-8b24-ffa0244d243f)

![s15](https://github.com/user-attachments/assets/c8fc98b9-367e-47a9-8b8b-8b400cc3b19d)

![s16](https://github.com/user-attachments/assets/f974db7b-2484-4be1-ba1e-f786ff0011e3)

Rise time It is time taken to the output waveform to 20% value to 80% value.</p>
rise time= (2.24609 - 2.18215)e-09 = 63.94 psec.</p>
Fall time</p>
it is the time take by output for transition from 80% to 20%.</p>
fall time 4 095-4 59</p>
 fall time= (4.09515 - 4.05269)e-09 = 42.46 psec</p>
Propagation delay</p>
it is the time difference between the 50% of input and 50% of the output.</p>
propogation delay =(2.21086 - 2.15)e-09 = 60.86 psec.</p>
Cell rise delay</p>
Time taken by output to rise to 50% and input to fall to 50%</p>
cell rise delay=(2.21078-2.14992)e-09=60.86psec</p>
Cell fall delay</p>
Time taken by output to fall to 50% and input to rise to 50%</p>
cell fall delay=(4.07586-4.04914)e-09=26.72psec</p>

`D3_Sk3-Sky130 Tech File labs`</p>
To Find problem in the DRC section of the old magic tech file for the skywater process and fix them.</p>
```bash
# Lab Setup Instructions
Ensure you have the necessary tools installed:
- `wget`
- `tar`
- `gvim`
- `magic`

## Step-by-Step Instructions

```bash
# 1. Change to Home Directory
cd

# 2. Download the Lab Files
wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz

# 3. Extract the Lab Files
tar xfz drc_tests.tgz

# 4. Navigate to the Lab Directory
cd drc_tests

# 5. List All Files and Directories
ls -al

# 6. View the .magicrc File
gvim .magicrc

# 7. Open Magic Tool with Better Graphics
magic -d XR &
```
![a2](https://github.com/user-attachments/assets/c260d657-7962-4abd-846e-364a6cdcb75a)

![a1](https://github.com/user-attachments/assets/f999fb61-3fdb-41df-af12-926552e9fee9)

![a3](https://github.com/user-attachments/assets/6f64e239-2727-4d53-ac6d-b87df38ffa42)

![a4](https://github.com/user-attachments/assets/b47b76f9-3af1-4f45-a333-66c1738ea215)

``` bash
#in tckon window
paint v2
cif see VIA2
```

![a6](https://github.com/user-attachments/assets/2eda404b-108f-46cc-a74f-137e76550cc8)

![a7](https://github.com/user-attachments/assets/3d1f8dfe-c657-4dc5-ad80-33b1db872148)


```bash
#in tckon window
load poly
```
```bash
#in order to change the tech file in terminal
vi sky130A.tech
```
```bash
#in tckon window
tech load sky130A.tech
drc check
```
![a8](https://github.com/user-attachments/assets/9c853356-5384-4b64-b5ac-3cb5ce9b3568)

![a9](https://github.com/user-attachments/assets/b68e64f0-0a95-461d-a2d3-fa3c73564886)

![a10](https://github.com/user-attachments/assets/547b1d42-83d7-4559-9048-6a9be20efd04)

![a11](https://github.com/user-attachments/assets/6e465afd-ec2a-4c9e-8e7c-12f3e7a6acf6)

![a20](https://github.com/user-attachments/assets/cb1b5ada-50a2-44c6-9278-6cb792625b16)

![a12](https://github.com/user-attachments/assets/3c1bcbd5-abcf-424d-a922-5a3434c6735e)

![a13](https://github.com/user-attachments/assets/6afea4fc-8592-4950-8b65-119db465ec6d)

![a14](https://github.com/user-attachments/assets/f89df0d7-80bb-497a-91d8-495a24c4483c)</p>

```bash
#open the mag file
```
![a15](https://github.com/user-attachments/assets/453dc230-5de0-42fe-a243-81f1617e8a7e)

![a16](https://github.com/user-attachments/assets/78af0628-32de-4fa1-8e29-cd8311e94ef9)

![a17](https://github.com/user-attachments/assets/0fc918e4-96f4-4e00-a4c8-7facda719344)

![a18](https://github.com/user-attachments/assets/f500717e-452f-415c-a20e-e6928ab8bd38)

![a19](https://github.com/user-attachments/assets/29457fcc-6235-4f45-bd56-d2048ce5aecd)


### DAY-4 PRELAYOUT TIMING ANALYSIS AND IMPORTANCE OF GOOD CLOCK TREE :</p>
`SK1 Timing modelling using delay tables:`</p>
In this sk we will get about the process to fix the small DRC errors and integrate a custom inverter cell into the OpenLane flow:</p>
This process ensures that the custom inverter cell is properly integrated into the design and that all timing and design rule checks are satisfied.</p>

1. **Fix DRC Errors and Verify Design:**  
   Ensure the input and output ports of the standard cell align with the intersection of the vertical and horizontal tracks. The width of the standard cell should be an odd multiple of the horizontal track pitch, and the height should be an even multiple of the vertical track pitch. You can verify these conditions by referencing the `track.info` file located in the PDK at `pdk/sky130/libs.tech/openlane/sky130_fd_sc_hd/track.info`.

2. **Save and Open Finalized Layout:**  
   After fixing the DRC errors, save the finalized layout with a custom name. Reopen it to ensure that all changes are intact.

3. **Generate LEF from Layout:**  
   Generate a LEF file from the finalized layout, which describes the physical properties of the custom inverter cell.

4. **Copy LEF and Associated Files:**  
   Copy the newly generated LEF file along with the required library files to the `src` directory of the `picorv32a` design.

5. **Update `config.tcl`:**  
   Edit the `config.tcl` file to include the new LEF file and update the library file paths to ensure the custom inverter cell is included in the OpenLane flow.

6. **Run Synthesis in OpenLane:**  
   Execute the synthesis process with the custom inverter cell included. During synthesis, you may need to adjust design parameters to remove or reduce any violations introduced by the custom cell.

7. **Verify Cell in PnR Flow:**  
   Once synthesis is successful, run the floorplan and placement steps to ensure the custom inverter cell is correctly integrated into the PnR flow.

8. **Post-Synthesis Timing Analysis:**  
   Perform post-synthesis timing analysis using the OpenSTA tool. Address any timing violations by making Timing ECO (Engineering Change Order) fixes.

9. **Update Netlist and Continue Flow:**  
   Replace the old netlist with the new one generated after the timing ECO fixes. Proceed with floorplanning, placement, and clock tree synthesis (CTS).

10. **Post-CTS Timing Analysis:**  
    Run post-CTS timing analysis using OpenROAD. Experiment with removing the `sky130_fd_sc_hd__clkbuf_1` cell from the `CTS_CLK_BUFFER_LIST` variable and observe the effects on the timing.
    ```bash
    #change the directory to:
    cd Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/openlane/sky130_fd_sc_hd
    #command
    ls -ltr (to list the files existing in sky130_fd_sc_hd directory)
    #open 
    less tracks.info
    ```
Below is the file of tracks.info</p>
![y1](https://github.com/user-attachments/assets/0d11d846-1e64-4523-b750-4b95e9756f51)

Here’s how you can execute the tasks you've listed:

1. **Change Directory**:
   ```bash
   cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
   ```

2. **Open Custom Inverter Layout in Magic**:
   ```bash
   magic -T sky130A.tech sky130_inv.mag &
   ```

3. **Get Syntax for the Grid Command in Magic**:
   Inside the Magic console, type:
   ```bash
   help grid
   ```

4. **Set Grid Values in Magic**:
   After you understand the grid command syntax from the help output, you can set the grid as follows:
   ```tcl
   grid 0.46um 0.34um 0.23um 0.17um
   ```
![y2](https://github.com/user-attachments/assets/e316f3ec-1980-4791-afda-9f3f2173b643)

![y3](https://github.com/user-attachments/assets/f0ae204b-cd3b-46d2-b1df-e611880c37a7)

![y4](https://github.com/user-attachments/assets/1f3a04be-fa55-492a-84fc-c00e5f884ec3)


This provides a step-by-step process for opening, inspecting, and saving your custom inverter layout using Magic with the Sky130 PDK.
```
# Navigate to the working directory
cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign

# Open the custom inverter layout in Magic
magic -T sky130A.tech sky130_vsdinv.mag &

# Check the various port names and their values in Magic
# Use this command in the Magic console to list all labels (including port names)
labels

# Alternatively, query specific points in the layout to identify labels and values
what

# Save the layout after inspection
save sky130_vsdinv.mag
```
![y5](https://github.com/user-attachments/assets/2244d1a9-8642-42b9-a94b-f8049557245d)

![y6](https://github.com/user-attachments/assets/0c2476b1-504c-4600-b0ca-7a0031102f50)

![y7](https://github.com/user-attachments/assets/7a7f154f-551b-40f2-b4bf-58b2fa496653)

![y9](https://github.com/user-attachments/assets/1d1912fb-2761-4434-9987-de058f4d1bd4)

![y10](https://github.com/user-attachments/assets/2292043a-8c3e-405b-954d-9d4c43bd287d)</p>

Open the file 

![y11](https://github.com/user-attachments/assets/a83f3653-1d3d-48b6-b07c-bfe235f15b59)

For copying the LEF file and library files, and then verifying their presence in the destination directory:

```bash
# Copy the LEF file to the target directory
cp sky130_vsdinv.lef ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/

# List the contents of the target directory to check if the LEF file was copied successfully
ls ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/

# Copy the library files to the target directory
cp libs/sky130_fd_sc_hd__* ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/

# List the contents of the target directory to check if the library files were copied successfully
ls ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/src/
```
This guides us through copying the necessary files and verifying their successful transfer to the specified directory.

![y12](https://github.com/user-attachments/assets/c212fe7c-aaea-4e8f-8002-4eeb053bf15c)

**Checking the typical lib file**</p>
![y13](https://github.com/user-attachments/assets/6c6cb5b9-690c-4ceb-b8b8-85be3a3040bf)

![y14](https://github.com/user-attachments/assets/9af23813-ea5f-49de-9f46-9033c8e3f3ad)


To modify the `config.tcl` file and include the new library file and LEF file in the OpenLane flow, you should add the following commands:

1. **Add the new library file**:
   ```tcl
   set ::env(LIB_SYNTH) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"
   set ::env(LIB_FASTEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__fast.lib"
   set ::env(LIB_SLOWEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__slow.lib"
   set ::env(LIB_TYPICAL) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"
   ```

2. **Add the new LEF file**:
   ```tcl
   set ::env(EXTRA_LEFS) [glob $::env(OPENLANE_ROOT)/designs/$::env(DESIGN_NAME)/src/*.lef]
   ```

![y16](https://github.com/user-attachments/assets/37e0466a-e0af-4472-8fff-90c080817e8f)</p>

**Setting up and running the OpenLANE flow with the new LEF file and library configuration:**</p>

```bash
# Step 1: Change directory to the OpenLANE flow directory
cd Desktop/work/tools/openlane_working_dir/openlane

# Step 2: Enter the OpenLANE flow Docker sub-system
docker

# Step 3: Invoke the OpenLANE flow in Interactive mode
./flow.tcl -interactive

# Step 4: Load the required OpenLANE package
package require openlane 0.9

# Step 5: Prepare the design environment for 'picorv32a'
prep -design picorv32a

# Step 6: Include the newly added LEF files into the OpenLANE flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Step 7: Run synthesis for the 'picorv32a' design
run_synthesis
```
![y17](https://github.com/user-attachments/assets/4f3af49d-bd63-4027-a378-b7da907d395f)

![y18](https://github.com/user-attachments/assets/f28d27f6-5b16-4dfd-99c8-01e4ede6ab80)

![y19](https://github.com/user-attachments/assets/c7216caa-dc58-4f7f-b890-c8b938cafc4e)

**DELAY TABLES**
Delay tables are data structures used in digital integrated circuit design to model and store the delay characteristics of components such as gates, interconnects, and cells. They provide detailed information on how long it takes for a signal to propagate through a component under various conditions, helping designers make informed decisions about circuit performance and reliability.

![DELAY](https://github.com/user-attachments/assets/7d537005-3951-4060-8623-12366f094dfa)

![POWER](https://github.com/user-attachments/assets/cd1ed06a-8cf0-4d09-a9a6-e42309d34c97)

In a power-aware clock tree synthesis (CTS), the enable pin functions differently depending on the gate type. For an AND gate, setting the enable pin to logic '1' allows the clock to propagate, while setting it to logic '0' blocks the clock. Conversely, for an OR gate, setting the enable pin to logic '0' enables clock propagation, whereas setting it to logic '1' blocks it. This ability to block the clock during certain periods can significantly reduce power consumption in the clock tree.

**Why Delay Tables Are Essential**

1. **Accurate Timing Analysis**: Delay tables are critical for precise timing analysis. They enable designers to predict circuit behavior and ensure that the circuit meets timing constraints, which is essential for reliable operation. By using delay tables, designers can detect and mitigate potential timing issues before physical implementation.

2. **Performance Optimization**: Understanding delay characteristics helps in optimizing circuit design for better performance. Designers can adjust parameters to reduce critical path delays, balance timing across the circuit, and enhance overall speed and efficiency.

3. **Design Verification**: Delay tables are used to verify that the design meets all timing constraints. This verification process helps prevent timing violations that could lead to functional errors or reduced reliability, ensuring that the final design performs as intended.

4. **Library Characterization**: During the creation of standard cell libraries, delay tables are essential for characterizing each cell's performance under different conditions. This characterization includes variations in load, input slew, voltage, and temperature, which helps in creating accurate models for use in design tools.

**Components of Delay Tables**

- **Input Slew Rate**: Measures the speed at which an input signal transitions between low and high states. Accurate modeling of input slew rate is important for predicting how quickly a signal can change and how it affects the timing of subsequent stages.

- **Output Load**: Represents the capacitance that the output of a gate or cell must drive. Load variations can significantly impact the delay characteristics, making it crucial to include in delay tables.

- **Voltage and Temperature**: Delay can vary with changes in operating voltage and temperature. Delay tables often include data for different voltage and temperature conditions to ensure accurate timing analysis under varying environmental conditions.

- **Transition Time (Slew)**: The time required for a signal to transition from one logic level to another. This is important for ensuring that signals propagate through the circuit at the correct speed.

- **Propagation Delay**: The time it takes for a signal to travel from the input to the output of a cell. This delay is fundamental in timing analysis, as it impacts the overall speed and performance of the circuit.

**Applications of Delay Tables**

1. **Static Timing Analysis (STA)**: STA tools leverage delay tables to calculate the timing of each path in a circuit. They aggregate the delays of individual components along a path to determine the total delay and check if it meets the design's timing constraints. This analysis helps in identifying and addressing timing issues early in the design process.

2. **Timing Closure**: During the place-and-route (P&R) phase, delay tables are used to achieve timing closure. Designers adjust cell placement, routing, and other parameters to minimize delays and meet timing requirements. This process ensures that the design will function correctly in its final form.

3. **Simulation**: Timing simulations use delay tables to predict circuit behavior under different conditions. Accurate delay modeling is essential for functional verification, ensuring that the circuit operates reliably across various scenarios and conditions.

4. **Library Development**: Delay tables are crucial in the development of standard cell libraries. They provide detailed information about each cell's delay characteristics, which is used by EDA tools for timing analysis and optimization. This helps in creating reliable and efficient cells for use in various designs.

**Additional Considerations**

- **Corner Cases**: Delay tables often include data for different "corner" cases, such as fast, typical, and slow process variations. These cases account for variations in manufacturing processes, temperature, and voltage, providing a comprehensive view of potential delays.

- **Dynamic Behavior**: In addition to static delay information, some delay tables may include data on dynamic behavior, such as how delays change with varying input frequencies or signal patterns. This helps in analyzing circuits under more realistic conditions.

- **Integration with EDA Tools**: Delay tables are integrated into Electronic Design Automation (EDA) tools, where they are used for various stages of design, including synthesis, place-and-route, and timing analysis. This integration ensures that the design is optimized and verified using accurate delay information.
By incorporating delay tables into the design and verification processes, designers can achieve higher performance, better power efficiency, and more reliable digital circuits.

![DELAY2](https://github.com/user-attachments/assets/49a15e3d-4fa8-47e8-958d-aa18291e398e)

![DELAY3](https://github.com/user-attachments/assets/ef80e5ba-013b-469d-a58d-3355fcce50f1)

**RUN THE OPENLANE**
```tcl
# Step 1: Change directory to the OpenLANE flow directory
cd Desktop/work/tools/openlane_working_dir/openlane

# Step 2: Enter the OpenLANE flow Docker sub-system
docker

# Step 3: Invoke the OpenLANE flow in Interactive mode
./flow.tcl -interactive

# Step 4: Load the required OpenLANE package
package require openlane 0.9

# Step 5: Prepare the design environment, overwriting existing setup
prep -design picorv32a -tag 16-08_08-39 -overwrite 

# Step 6: Include the newly added LEF files into the OpenLANE flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Step 7: Display the current value of the SYNTH_STRATEGY variable
echo $::env(SYNTH_STRATEGY)

# Step 8: Set a new value for the SYNTH_STRATEGY variable
set ::env(SYNTH_STRATEGY) 1

# Step 9: Display the current value of the SYNTH_BUFFERING variable to check if it's enabled
echo $::env(SYNTH_BUFFERING)

# Step 10: Display the current value of the SYNTH_SIZING variable
echo $::env(SYNTH_SIZING)

# Step 11: Set a new value for the SYNTH_SIZING variable
set ::env(SYNTH_SIZING) 1

# Step 12: Display the current value of the SYNTH_DRIVING_CELL variable to verify the correct cell
echo $::env(SYNTH_DRIVING_CELL)

# Step 13: Run synthesis for the design
run_synthesis

# Step 14: Run floorplanning
run_floorplan

# Step 15: Run placement
run_placement
```


![y21](https://github.com/user-attachments/assets/c5132b27-0c94-42cb-85a3-da98380f408a)

![y22](https://github.com/user-attachments/assets/f1eee549-473c-4773-a46f-7a330c8e8144)

![y23](https://github.com/user-attachments/assets/fc432873-64dd-4c75-8951-b7d6ef87e5ab)

![y25](https://github.com/user-attachments/assets/ba38401a-5ce3-4d76-957b-8d351d531f76)

![y26](https://github.com/user-attachments/assets/02d0978f-898e-4252-aba6-f1f5181b3ae2)

![y27](https://github.com/user-attachments/assets/2362b7e8-4c4b-4173-bb7d-14d0aebe7b98)

![y28](https://github.com/user-attachments/assets/0db4e243-42a9-4596-b488-b14abb3f2b8d)















