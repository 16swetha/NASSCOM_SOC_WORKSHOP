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

 
- **This is the floorplan folder with its directives**

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
   cd  /Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/29-07_10-25/results/floorplan/
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



  
   


















