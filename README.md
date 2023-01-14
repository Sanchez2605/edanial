## Eystein Danial - Intel CKT Training
## Table of contents
* Day 1 - Fundamentals of VLSI Design and overview of Sand-to-Silicon
* Day 2 - Details of IC Manufacturing Process
* Day 3 - CMOS Fabrication Process in Deep Submicron and Ultra Deep Submicron Technology

## Day 1
### Topic - Fundamentals of VLSI Design and overview of Sand-to-Silicon
<Details>
 <summary>Theory</summary>
 
 **Overview of VLSI Design**
* **Packaged Chip**  
  - Packaging of silicon die with plastic case to protect the die. The Central Part of the Chip is call die.
  ![image](https://user-images.githubusercontent.com/121995963/212446810-49006395-7b92-4ecd-ab18-f5d289adf246.png)

  * Examples types of packaging:
    * System in a package (SIP)
      - A system in package, or SiP, is a way of bundling two or more ICs inside a single package. This is in contrast to a system on chip, or SoC, where the functions         on those chips are integrated onto the same die.
      ![image](https://user-images.githubusercontent.com/121995963/212447058-7238737a-c6d0-402f-b5e3-61395582998a.png)

    * Dual in-line package (DIP)
      - An electronic component package with a rectangular housing and two parallel rows of electrical connecting pins. The package may be through-hole mounted to a           printed circuit board (PCB) or inserted in a socket.
      ![image](https://user-images.githubusercontent.com/121995963/212447020-65137fc0-1fa8-4a6c-9769-4be4e34637cd.png)

    * Quad-flat no-leads (QFN)
      - Flat no-leads, also known as micro leadframe (MLF) and SON (small-outline no leads), is a surface-mount technology, one of several package technologies that           connect ICs to the surfaces of PCBs without through-holes. Flat no-lead is a near chip scale plastic encapsulated package made with a planar copper lead frame         substrate.
      
      ![image](https://user-images.githubusercontent.com/121995963/212447142-a416b274-78e9-4c14-8958-f19887cb5013.png)

    * Ball grid array (BGA)
      - A ball grid array (BGA) is a type of surface-mount packaging (a chip carrier) used for integrated circuits. BGA packages are used to permanently mount devices         such as microprocessors. A BGA can provide more interconnection pins than can be put on a dual in-line or flat package
      ![image](https://user-images.githubusercontent.com/121995963/212447167-ae4b244a-d7c3-40e0-8d0d-7f09022c6082.png)

 * **Die** 
    * Size is generally 1mmx1mm or 1mmx2mm
    * Made from a wafer which every single wafer consists of many die

 * **Inside the Die**
    * Digital  
        i) Consists of Gates, Muxes, Decoders, Counters, Resistors, FSMs etc which all are made by standard cells using semi custom VLSI design flow.
    * Analog and RF
        i) Consists of Clock: VCO and PLL.
        ii) Voltage Ref. and Reg.: Bandgap reference, LDO, DC-DC converter; Data: PRBS generator; Amplifiers and Filters.
        iii) Interfaces: ADC and DAC.
        iv) All are made using custom VLSI flow.
    * Memory and Memory Controller  
        i) Consists of Static Random Access Memory (SRAM) and SRAM controller.
        
  * **Moore's Law**
      * Moore's Law is the observation that the number of transistors in a dense integrated circuit (IC) doubles aboout every two years.
      * The feature size reduced by 1/square root of 2 times. 
      
  * **VLSI Design Methodology**
      * Field Programming gate array (FPGA) Design
        * Faster prototyping and cost-effective
        * A FPGA chip consist of input/output buffers, array of configurable logic blocks, and programmable interconnect structures.
        * By programming the RAM, accomplished to programmed the interconnects. 
        * Signal routing between the CLBs and the I/O blocks made by configurable switching matrice.
        
  * **ASIC**
      * Standard Cell based design
          * Prevalent full custorm design and requires development of a full custom mask set.
          * Commonly used logic cells are developed, characterized, and stored in a standard-cell library.
          * Constant height for all cells in a same technology.
          * Can have several version for different fan-out driving capability.
            ![image](https://user-images.githubusercontent.com/121995963/212448308-3c2cf5a7-1406-4658-a976-f8de551b5ae1.png)

      * Full Custom Design
          * The entire mask deisgn is done without using any library.
          * Development cost of such a design style is becoming higner.
          * All the analaog and RF design are full custorm design.
  
  * **Differences between FPGA & ASIC**
        ![image](https://user-images.githubusercontent.com/121995963/212448407-784aeb89-5c51-4ad1-9f6d-3e8acf04a863.png)

 * **VLSI Design Quality**  
    * **Testability**  
      - Design of testable chip  
      - Availability of good test fixture at speed.
    * **Yield and Manufacturability**  
      - Yield: No. of tested of chips/Total no. of Chips    
      - Functional Yield: Checks at lower speed  
      - Parametric Yield: Checks at required speed
    * **Reliability**  
      - Consist of ESD, EOS, Electromigration, Oxide breakdown, Power and ground bouncing, On-chip noise and cross-talk.
      
 * **Technology Upgradability**  
   * Rapid development of process technology results
      * Design of complatex chip in a shother time.
      * Techonology updated to new design rules.
      * Updating the mask to new design rules.
   
   * Design style must be flexible to technology update so that the design can be use back with minimal cost. 
   * Use advanced CAD tools to automatically generate physical layout.
 
 * **CAD Tools**  
   * CAD tools essential for timely deveopment of integirated circuits.
   * Executing using CAD tools can time consuming and computation intensive mechanistic parts of the design.
   * CAD techonology for VLSI Chip chip design can be categorzied into below areas:
      * High Level sysnthesis
      * Logic systhesis
      * Circuit optimization
      * Layout
      * Placement and routing
      * Simulation
      * Design Rules and Checking
      
  * **Package Technology**
     * Many high perfomanances VLSI chips can fail if various packagin contraints and parasitic have not included in the design phase, and lenght of bonding wire or          lead length  of the packge can create serious issue. ALl this can be solve if Chip designers should work closely with package designers.
 
 * **References Sand to Silicon:** https://community.intel.com/t5/Blogs/Intel/We-Are-Intel/From-Sand-to-Silicon-The-Making-of-a-Chip/post/1334092
</details>

<Details>
<summary>Lab</summary>
</details>


## Day 2
### Topic - Details of IC Manufacturing Process
<details>
 <summary>Theory</summary>
 
 **Analog IC Design Process** 
 **Process Flow of IC Design:**
![image](https://user-images.githubusercontent.com/121995963/212457913-43c8bdc3-404f-4d4d-8689-946f89aa8142.png)

 **Diferrences of Electrical, Physical & Test Design scope:**
 ![image](https://user-images.githubusercontent.com/121995963/212456977-0dbd2ddb-96d5-434f-87d9-19a25a7e57aa.png)

 **Analog IC Design Process and its Relation with CAD and PDK:**
![image](https://user-images.githubusercontent.com/121995963/212457325-bd086e9e-8dc2-49cc-82dc-9f57515205a9.png)


 **Comparisom of Analog and Digital Circuit:** 
 * ![image](https://user-images.githubusercontent.com/121995963/212457976-64b78a07-2a30-42f5-8997-39829fc3354b.png)

 
 **Role of Circuit Designer**
   * Physical implementation of the circuit has a major impact on perforamances, power and cost.
   * Design a practical circuit based on the device limit, technology constraint and physical implementation.
   * Need to have a good understanding of layout design, so that in less interation the design can be fridged.
   * Should always dissssed with the layout designer for better and efficient circuit design.

 **CMOS Technology**
 * **What is CMOS?**
    * Is a type of metal–oxide–semiconductor field-effect transistor (MOSFET) fabrication process that uses complementary and symmetrical pairs of p-type and n-type         MOSFETs for logic functions.[1] CMOS technology is used for constructing integrated circuit (IC) chips, including microprocessors, microcontrollers, memory chips       (including CMOS BIOS), and other digital logic circuits.
 
 * **Why CMOS Techonology?**
   * ![image](https://user-images.githubusercontent.com/121995963/212457479-51942a03-3896-4e2f-83f4-386c3c1eb463.png)
   * Comparison favours BJT, however similar comparison made from digital viewpoint would come up on the side of CMOS.
   * Since Large volume mixed-mode technology will be driven by digital demands, CMOS is an obvious choice.
 
 **Categorization of the CMOS Technology:**
   * Submicron Technology: Lmin ≥ 0.35 µm
   * Deep Submicron Technology (DSM): 0.1 µm ≤ Lmin ≤ 0.35 µm
   * Ultra-Deep Submicron Technology (UDSM): Lmin ≤ 0.1 µm
   * BiCMOS Technology: Lmin = 0.5 µm
 
 **CMOS Fabrication Process**
   1) Wafer Formation
      * Raw material used in CMOS Fabs is wafer or disk of silicon. 
   2) Photolithography
      * The silicon dioxide layer is covered with the photoresist material. It is a light-sensitive material that forms the coating over the surface of the SiO2               layer. It is useful in reducing the size of the transistors.
       * ![image](https://user-images.githubusercontent.com/121995963/212458530-3ba204f1-23bf-4d61-870b-0d5ae4862fed.png)

      * After the photoresist is applied on the silicon dioxide layer, a mask with the desired pattern is used as a medium to expose UV (Ultra-Violet) lights. The UV           light through the mask reaches the photoresist material. The exposed resist remains on the surface and the unexposed part is removed from the surface.
        * ![image](https://user-images.githubusercontent.com/121995963/212458534-2a16b609-d3f6-4a05-b70b-d3f9067e246c.png)
 
   3) Well and Channel Formation
       * N-well process: In a n-well process, the pMOS transistors are built in a n-well and the nMOS transistor is placed in the p-type substrate.
       * P-well process: In a p-well process, the nMOS transistors are built in a p-well and the pMOS transistor is placed in the n-type substrate. p-well processes            were used to optimize the pMOS transistor performance.
       * Twin-well process: Twin-well processes accompanied the emergence of n-well processes. A twinwell process allows the optimization of each transistor type.
       * Triple-well process: The triple-well process has emerged to provide good isolation between analog and digital blocks in mixed-signal chips; it is also used to          isolate high-density dynamic memory from logic.
        ![image](https://user-images.githubusercontent.com/121995963/212458676-1e45b2eb-4004-4e2b-ac76-33b240577a4d.png)

   4) Silicon Dioxide (Sio2) 
      * Oxidation of silicon is achieved by heating silicon wafers in an oxidizing atmospthere The following are some approaches:
         * Wet Oxidation: When the oxidizing atmosphere contains water vapor.
         * Dry OixidatationL when the oxidizing atmosphere is pure oxygen.
         * Atomic Layer Deposition: when a thin layer (materail A) is attached to a surface then a chemical (Material B) is introduced to produe a thin layer of the              required layer.
   5) Isolation
      * Devices in a CMOS process need to be isolated from one another so that they do not have unexpected interactions.
      * The transistor gate consists of a thin gate oxide layer.
      * The thick oxide used to be formed by a process called Local Oxidation of Silicon (LOCOS).
      * A problem with LOCOS-based processes is the transition between thick andthin oxide, which extended some distance laterally to form a so-called bird’s beak.
      * Starting around the 0.35 µm node, shallow trench isolation (STI) was introduced to avoid the problems with LOCOS.
      * STI forms insulating trenches of SiO2 surrounding the transistors (everywhere except the active area).
 
   6) Gate Oxide
      * This process is to form the oxide for the transistor. 
 
   7) Gate and Source/Drain Formations
      * Grow gate oxide wherever transistors are required (area = source + drain + gate)––elsewhere there will be thick oxide or trench isolation.
      * Deposit polysilicon on chip
      * Pattern polysilicon (both gates and interconnect)
      * Etch exposed gate oxid
      * Implant pMOS and nMOS source/drain regions

   8) Contacts and Metallization
      * Contact cuts are made to source, drain, and gate according to the contact mask. These are holes etched in the dielectric after the source/drain formation.
      * Older processes commonly use aluminum (Al) for wires, although newer ones offer copper (Cu) for lower resistance.
      * Tungsten (W) can be used as a plug to fill the contact holes (to alleviate problems of aluminum not conforming to small contacts)
 
   9) Passivation
      * The final processing step is to add a protective glass layer called passivation or over glass that prevents the ingress of contaminants.
      * Openings in the passivation layer, called overglass cuts, allow connection to I/O pads and test probe points if needed.
 
  10) Metrolgy 
      * Is the science of measuring. Everything that is built in a semiconductor process has to be measured to give feedback to the manufacturing process.

 **Illustration of N-Well Process for CMOS Fabrication**
 * Step1: Substrate
 # ![image](https://user-images.githubusercontent.com/121995963/212459286-5b987425-8a9d-4c0e-ae11-1592f4c68367.png)
 
 * Step2: Oxidation
 # ![image](https://user-images.githubusercontent.com/121995963/212459290-0bc74373-e83c-4e1c-a236-237fa215356c.png)
 
 * Step3: Photoresist
 # ![image](https://user-images.githubusercontent.com/121995963/212459299-2fa561d5-c574-4bb1-9477-a425ad252f65.png)
 
 * Step4: Masking
 # ![image](https://user-images.githubusercontent.com/121995963/212459304-3429e648-013f-465e-9540-22be5bc19e80.png)
 
 * Step5: Photoresist removal
 # ![image](https://user-images.githubusercontent.com/121995963/212459313-20126026-fc31-4708-95e5-8cee8bfcb07f.png)
 
 * Step6: Removal of SiO2 using acid etching
 # ![image](https://user-images.githubusercontent.com/121995963/212459317-74929ed1-f4e5-4567-9147-266e6bd1710c.png)
 
 * Step7: Removal of photoresist
 # ![image](https://user-images.githubusercontent.com/121995963/212459326-e0d51b95-a84f-4b10-9f25-3b6796854642.png)
 
 * Step8: Formation of the N-well
 # ![image](https://user-images.githubusercontent.com/121995963/212459333-ca6d5331-9fcf-4561-8335-d6b82ac7329f.png)
 
 * Step9: Removal of SiO2
 # ![image](https://user-images.githubusercontent.com/121995963/212459337-4de4f001-a9f6-4717-9575-52fd8417c309.png)
 
 * Step10: Deposition of polysilicon
 # ![image](https://user-images.githubusercontent.com/121995963/212459343-fe938ea3-5734-41f2-860d-0d6049b25228.png)
 
 * Step11: Removing  the  layer barring a small area for the Gates
 # ![image](https://user-images.githubusercontent.com/121995963/212459352-65ea292a-5714-4abc-bb98-297afb34f519.png)
 
 * Step12: Oxidation process
 # ![image](https://user-images.githubusercontent.com/121995963/212459360-46012abd-0b18-4f60-95e2-d27817debdb9.png)
 
 * Step13: Masking and N-diffusion
 Masking:
 # ![image](https://user-images.githubusercontent.com/121995963/212459365-7c259a3f-4bde-4f6c-a7cd-bdb0dac5b462.png)
 
 N-diffusion:
 # ![image](https://user-images.githubusercontent.com/121995963/212459373-ee42a094-fbc0-41dd-8427-2f43dc01c250.png)
 
 *Step14: Oxide stripping
 # ![image](https://user-images.githubusercontent.com/121995963/212459393-b0eba6bb-f806-4bee-abcb-b1ae2ce63c13.png)
 
 *Step15: P-diffusion
 # ![image](https://user-images.githubusercontent.com/121995963/212459400-eb377413-140c-4cd6-8931-a51682fb7587.png)
 
 *Step16: Thick field oxide
 # ![image](https://user-images.githubusercontent.com/121995963/212459407-ec49a794-e2e7-4b71-8df8-4cdd5459c87d.png)
 
 *Step17: Metallization
 # ![image](https://user-images.githubusercontent.com/121995963/212459413-04150f3c-c304-47dd-aa51-98bc22d52e01.png)
 
 * Step18: Removal of excess metal
 # ![image](https://user-images.githubusercontent.com/121995963/212459415-268b5a85-b26d-43f4-b783-b2465597add1.png)
 
 *Step19: Terminals
 # ![image](https://user-images.githubusercontent.com/121995963/212459423-3033b653-8988-47e2-8fe1-777bf66e5d70.png)
 
 *Step20: Assigning the names of the terminals of the NMOS and PMOS
 # ![image](https://user-images.githubusercontent.com/121995963/212459436-72cd2579-e7c8-407f-9179-9f69e5fd3398.png)

 **References from:** https://www.watelectronics.com/understanding-cmos-fabrication-technology/#:~:text=20%20Steps%20of%20CMOS%20Fabrication%20Process%201%20Step2%3A,8%20Step9%3A%20Removal%20of%20SiO2%20...%20More%20items

**Sand to Silicon illutration:**
 ![image](https://user-images.githubusercontent.com/121995963/212457991-8c89d091-61c2-48da-b22e-d30bf806948a.png)
</details>


 <Details>
<summary>Lab</summary>
</details>
