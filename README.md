## Eystein Danial - Intel CKT Training
## Table of contents
* Day 1 - Fundamentals of VLSI Design and overview of Sand-to-Silicon
* Day 2 - Details of IC Manufacturing Process
* Day 3 - CMOS Fabrication Process in Deep Submicron and Ultra Deep Submicron Technology
* Day 4 - Metal Oxide Semiconductor Structure
* Day 5 - Metal Oxide Semiconductor Field Effect Transistor
* Day 6 - MOSFET Intrinsic Capacitances
* Day 7 - MOSFET Parameter Extraction Scaling, Short Channel Effects and PVT Variation

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

 **Fabrication Process References:** https://www.watelectronics.com/understanding-cmos-fabrication-technology/#:~:text=20%20Steps%20of%20CMOS%20Fabrication%20Process%201%20Step2%3A,8%20Step9%3A%20Removal%20of%20SiO2%20...%20More%20items

**Sand to Silicon illutration:**
 ![image](https://user-images.githubusercontent.com/121995963/212457991-8c89d091-61c2-48da-b22e-d30bf806948a.png)
</details>

<Details>
<summary>Lab</summary>
</details>


## Day 3
### Topic - CMOS Fabrication Process in Deep Submicron and Ultra Deep Submicron Technology
<details>
 <summary>Theory</summary>
 
**Disadvantange of the Submicron CMOS Process**
 Isolation of transistors:
  * The use of reverse bias pn junction to isolate transistors become impractical as the transistor sizes decrease. 
 
 * Local Oxidation of Silicon (LOCOS) Isolation Process
  1) A very this layer silicon dioxie is grown on the wafer, called as pad oxide. Then a layer of silicon nitride is deposited which is used as an oxdie barrier
  2) Then by thermal oxidation process thick oxide is grown in the exposed area.
  3) Lastly, the removal of the silicon nitride layer.
     * The limiation of this technique is the bird's beak effect and the surface area which is lost to this encroachment.
     * The advatages of LOCOS fabrication process is simple and higg oxide quality because LOCOS strcuture is thermally grown.
 
 ![image](https://user-images.githubusercontent.com/121995963/212460949-9426b08c-9e0e-437a-8153-0c45132ac4f2.png)

 **Sallow Trench Isolation Technology**
   * Shallow trench isolation (STI) allows closer spacing of transistors by eliminating the depletion region at the surface and Bird’s beak effect due to LOCOS process
   * Sallow Trench Isolation (STI) isolation process is the preferred isolation process for deep-submicron process because it completely avoids Bird’s beak shape            characteristics.
        a. Cover the wafer with pad oxide and silicon nitride.
        b. First etch nitride and pad oxide. Next, an anisotropic etch is made in the silicon to a depth of 0.4 to 0.5 microns.
        c. Grow a thin thermal oxide layer on the trench walls
        d. A CVD dielectric film is used to fill the trench
        e. A chemical mechanical polishing (CMP) step is used to polish back the dielectric layer until the nitride is reached. The nitride acts like a CMP stop layer.
        f. Densify the dielectric material at 900°C and strip the nitride and pad oxide.
  * STI is more suitable for the increased density in a small area because it allows forming smaller isolation regions.
  * The disadvantage is larger number of process steps.
 
 ![image](https://user-images.githubusercontent.com/121995963/212461111-a8b37f4f-684b-4e16-921e-9a5c2ee5fdca.png)

**Deep Submicron (DSM) CMOS Technology other uses**
 * A deep n-wellthat can be utilized to reduce substrate noise coupling.
 * A MOS Varactor that can be used to make volatage controlled osillators 
 
 **Different Types of Resistor in Deep Submicron (DSM) CMOS Technology**  
 # ![image](https://user-images.githubusercontent.com/121995963/212461642-a0b62304-ee18-4ec5-96f8-cb0e5399d115.png)
 # ![image](https://user-images.githubusercontent.com/121995963/212461650-f6113eee-943c-44e7-8053-00bc556182b1.png)

**Typical Deep Submicron (DSM) CMOS Fabrication Process**  
    Major Fabrication Steps for a DSM CMOS Process  
      1) p and n wells  
      2) Shallow trench isolation  
      3) Threshold shift and anti-punch through implants  
      4) Thin oxide and gate polysilicon  
      5) Lightly doped drains and sources  
      6) Sidewall spacer  
      7) Heavily doped drains and sources  
      8) Siliciding (Salicide and Polycide)  
      9) Bottom metal, tungsten plugs, and oxide  
      10) Higher level metals, tungsten plugs/vias, and oxide  
      11) Top level metal, vias and protective oxide   
 
 **Deep Submicron (DSM) CMOS Fabrication Process** 
 * Step 1: n and p well Creation: 
 ![image](https://user-images.githubusercontent.com/121995963/212461850-e9e8d122-97a9-4a38-80fe-716e91f81fcb.png)
 
 * Step 2: Sallow Trench Isolation 
  * The shallow trench isolation (STI) electrically isolates one region/transistor from another.
 ![image](https://user-images.githubusercontent.com/121995963/212461904-dd9f195d-3454-4b51-85c2-137f4aa0eb8b.png)
 
 * Step 3: Threshold Shift and Anti-Punch Through Implants
  * The natural thresholds of the NMOS is about 0V and of the PMOS is about –1.2V. An p-implant is used to make the NMOS harder to invert and the PMOS easier resulting     in threshold voltages balanced around zero volts.
  * Also an implant can be applied to create a higher-doped region beneath the channels to prevent punch-through from the drain depletion region extending to source       depletion region.
 ![image](https://user-images.githubusercontent.com/121995963/212461938-5d656194-2702-42b7-9e12-81a7de9fa03e.png)
 
 * Step 4: Thin Oxide and Polysilicon Gates
   * A  thin oxide is deposited followed by polysilicon. These layers are removed where they are not wanted.
   ![image](https://user-images.githubusercontent.com/121995963/212462012-2858a2f1-fc40-44c1-bf3b-65f8cb649877.png)

 * Step 5: Lightly Doped Drains and Sources
   * A lightly-doped implant is used to create a lightly-doped source and drain next to the channel of the MOSFETs.
   ![image](https://user-images.githubusercontent.com/121995963/212462052-c8681646-a244-46f9-8e7b-ce84d83d8a7c.png)

 * Step 6: Sidewall Spacers
   * A layer of dielectric is deposited on the surface and removed in such a way as to leave “sidewall spacers” next to the thin-oxide-polysilicon-polycide sandwich.        These sidewall spacers will prevent the part of the source and drain next to the channel from becoming heavily doped.
     ![image](https://user-images.githubusercontent.com/121995963/212462091-32e6014f-e949-43bc-9082-c3e3a6102250.png)

 * Step 7: Implantation of the Heavily Doped Sources and Drains
   * Note that not only does this step provide the completed sources and drains but allows for ohmic contact into the wells and substrate.
    ![image](https://user-images.githubusercontent.com/121995963/212462104-8d151311-9d2f-4e88-a58c-e260b6663db8.png)
 
 * Step 8: Siliciding (Salicide and Polycide)
   * This step reduces the resistance of the bulk diffusions and polysilicon and forms an ohmic contact with material on which it is deposited. .
     Salicide = Self-aligned silicide
    ![image](https://user-images.githubusercontent.com/121995963/212462162-e7f519e3-c5a1-40a9-adff-424497c2183e.png) 

 * Step 9: Intermediate Oxide Layer
   * An oxide layer is used to cover the transistors and to planarize the surface.
     ![image](https://user-images.githubusercontent.com/121995963/212462191-cdc87155-fe1e-44a5-8fed-42018b2fc5c4.png)

 * Step 10: First-Level Metal
   * Tungsten plugs are built through the lower intermediate oxide layer to provide contact between the devices, wells and substrate to the first-level metal.
     ![image](https://user-images.githubusercontent.com/121995963/212462208-9a6452f8-02cf-463e-b435-a97011a28209.png)

 * Step 11 – Second-Level Metal
    * The previous step is repeated for the second-level metal.
    ![image](https://user-images.githubusercontent.com/121995963/212462238-96ec05dc-fb3b-4355-b36a-ced1d4b83c26.png)

* Completed Fabrication
   * After multiple levels of metal are applied, the fabrication is completed with a thicker toplevel metal and a protective layer to hermetically seal the circuit        from the environment. Note that metal is used for the upper level metal vias. The chip is electrically connected by removing the protective layer over large            bonding pads.
 ![image](https://user-images.githubusercontent.com/121995963/212462281-01ca4ad2-60ae-458a-b98b-73d49f9d93cd.png)

**Summary of Deep Submicron (DSM) CMOS Fabrication Process**    
   * DSM technology typically has a minimum channel length between 0.35μm and 0.1μm  
   * DSM technology addresses the problem of excessive depletion region widths in junction isolation techniques by using shallow trench isolation  
   * DSM technology may have from 4 to 8 levels of metal  
   * Lightly doped drains and sources are a key aspect of DSM technology  
    
**Ultra Deep Submicron (UDSM) CMOS Technology**
 * Minimum length is less than 0.1 microns
 * Minimum feature size less than 100 nanometers
 * 22 nm drawn length
 * 5 nm lateral diffusion (12 nm gate length)
 * 1 nm transistor gate oxide
 * 8 layers of copper interconnect
 * Specialized processing is used to increase drive capability and maintain low off currents
        
**Advantage of UDSM CMOS Technology**
 * Digital Viewpoint:
   * Improved Ion/Ioff
   * Reduced gate capacitance
   * Higher drive current capability
   * Reduced interconnect density
   * Reduction of active power
        
 * Analog Viewpoint:
   * More levels of metal
   * Higher cutoff frequency
   * Higher capacitance density
   * Reduced junction capacitance per transconductance
   * More speed
        
**Disadvantage of UDSM CMOS Technology**
 * Analog Viewpoint:
   * Reduction in power supply resulting in reduced headroom
   * Gate leakage currents
   * Reduced small signal intrinsic gain
   * Increased nonlinearity
   * Increased noise and poorer matching
</details>

<Details>
<summary>Lab</summary>
</details>

## Day 4
### Topic - Metal Oxide Semiconductor Structure
<details>
 <summary>Theory</summary>
 
 **Metal-Oxide-Semiconductor (MOS) Device Structure**
 * The capacitance of the MOS capacitor depends upon the voltage applied on the gate terminal.
 * Usually the body is grounded when the gate voltage is applied.
 * It is defined as the voltage at which there is no charge on the capacitor plates and hence there is no static electric field across the oxide
 ![image](https://user-images.githubusercontent.com/121995963/215647142-83a2f834-66ea-40bf-bb44-ed6641b5841a.png)
 
 ![image](https://user-images.githubusercontent.com/121995963/215649323-3046360f-d0ce-4058-a355-4648f3e92987.png)
 * At V(gate) > V(threshold), the capacitance is inverse proportional to frequency.

 **Fabrication**  
  * Oxidation: Process to create SiO2 on top of Silicon
  * Metallization: Process to deposit poly-silicon on top of SiO2.

 **Ideal MOS Junction or Capacitor**
 * Ideal Characteristics 
 * No charge in the device if V=0.
 # ![image](https://user-images.githubusercontent.com/121995963/215654088-cc7b171c-5e7f-4b15-bc47-9e2444f096a4.png)
 
 **Three Operation states of the MOSFET**
 
 **Accumulation Mode**
  
 Accumulation Mode( Vgs < 0 v)
 ![image](https://user-images.githubusercontent.com/121995963/215657929-ba00d0d7-6b6f-40a0-82c1-1ceb4729b69c.png)
 * Represents the Accumulation mode in which the Vgs (Gate to Source )applied is less than zero (Negative).
 * The negative charge tends to accumulate at the gate, because of these negative charges, the holes of the p-type substrate will get attracted underneath it. 
 
 **Depletion Mode (0 < V < Vt)**
                              
 ![image](https://user-images.githubusercontent.com/121995963/215658200-f2a07716-1054-4feb-835a-9fe9b2469bee.png)
 * The surface starts to deplete and the type of charge at the surface is -ve and gradually increases with the increase of voltage.
 * The voltage at the surface carrier concentration = to bulk carrier concentration, which called weak inversion.
 * The charge at the surface directly proportional to voltage.
                              
 **Strong Inversion Mode (Vgs > Vt)**
   
 ![image](https://user-images.githubusercontent.com/121995963/215660363-7612d2d7-5f24-467a-8b7e-f9f0aa9ac374.png)
 * At threshold voltage, a channel form at the surface of the semiconductor due to inversion charge.
 * Before threshold voltage, the charge comes from negatively charged ionized acceptor.
 * After threshold voltage, more charge comes from the electrons rather than depleting the holes
                               
                         
 **Non Ideal MOS Structure**
 
 * Effect if fixed charge Qf:
  * To create a zero charge non silicon negative volatage is required to give at gate terminal.
  * By applying a negative volute at gate the surface charge at silicon will be zero
  * Zero charge in the semiconductor conrresponds to flat-band condition of a MOS junctions.
 
 ![image](https://user-images.githubusercontent.com/121995963/215669766-fdbfe746-3ae9-40f7-857a-917609d8caec.png)

 * Effect of metal-semiconductor work function different, ɸms: 
 * Electrons area always move from higher energy level to lower energy level.
 * Electrons are transferred through wire.
 * To remove the electrons from the semicondutor surface, we have to provide a negative voltage to the gate.
![image](https://user-images.githubusercontent.com/121995963/215670166-ed7ea0f0-ae6c-4389-a8a6-aab4f0db39f5.png)

</details>

<Details>
<summary>Lab</summary>
</details>
 

## Day 5
### Topic - Metal Oxide Semiconductor Field Effect Transistor
<details>
 <summary>Theory</summary>

 **MOSFET Structure**
 
 * MOSFET view in Top: 
 # ![image](https://user-images.githubusercontent.com/121995963/215696938-c6bb4fa3-f6fd-49eb-a64d-a5762071550c.png)

 * MOSFET view in Front: 
 #  ![image](https://user-images.githubusercontent.com/121995963/215699369-7c048125-e578-4dbc-8ea1-a579cd4f3653.png)

 * N-MOSFET and P-MOSFET symbols:
 # ![image](https://user-images.githubusercontent.com/121995963/215697263-7da4b000-2897-4a65-a624-44df95802401.png)

 **MOSFET Operation (N-Channel Enchancment)**
 
 * When this MOSFET is activated as ON this condition results in the maximum amount of the current flow through the device. This type of MOSFET is defined as N-channel MOSFET.

 ![image](https://user-images.githubusercontent.com/121995963/215698097-382963f3-84a3-4f91-b9ff-01852ce5bc43.png)
  
**MOSFET Operation**
 
 Case 1: Cutoff
 * Gate voltage lower than threshold voltage, Vgs < Vt.
 * No channel form between source and drain.
                                                       
 Case 2: Linear Operation
 * Gate voltage slightly above threshold voltage, Vgs - Vt >= Vds. 
 * N-channel start to form between drain and source.
 * Current flow from drain to source, Id.
 * Id increase linearly with Vgs increase.
                                                       
 Case 3: Saturation Mode
 * Gate voltage much more higher than threshold voltage, Vgs - Vt < Vds
 * At saturation point, the curent from drain to source is saturated even the Vds keep increasing

 **MOSFET Channel Profile:**
                                                                       
 ![image](https://user-images.githubusercontent.com/121995963/215699988-270cdd83-b85b-472a-88b0-fd0a304fd503.png)
                                                                       
  **MOSFET Operation (P-Channel Enchancment)**
                                                                       
  * A P-channel MOSFET uses hole flow as the charge carrier, which has less mobility than the electron flow used in N-channel MOSFETs.
  * The main difference is that P-channel MOSFETs require a negative voltage from the gate to the source (VGS) to turn on (as opposed to an N-channel MOSFET, which requires a positive VGS voltage)
  * This makes P-channel MOSFETs the ideal choice for high-side switches.
                                                                       
 ![image](https://user-images.githubusercontent.com/121995963/215700784-dc32353e-4778-40a2-8edb-048e0f740fed.png)

 **Different between N and P Channel:** 
 
  ![image](https://user-images.githubusercontent.com/121995963/215697564-113128a3-c4fc-4958-b0de-95ee08c81841.png)
                                                                       
**Comparison between BJT, FET and MOSFET**
         
 ![image](https://user-images.githubusercontent.com/121995963/215700932-5d335742-41c8-429f-bf44-a69b0fb7fab6.png)

 </details>
 
<details>
<summary>Lab</summary>
</details>
 
## Day 6
### Topic - MOSFET Intrinsic Capacitances
<details>
 <summary>Theory</summary>
 
 **Intrisic Capacitances: Cutoff Region** 
 
 * Gate oxide capacitances between the gate and channel overlap
 * Also its frngging capacitances between the gate and the source/drain regions
 * Cgso = Cgdo = Cox * W * Ld
 * No channel relate capacitances
 
![image](https://user-images.githubusercontent.com/121995963/216217463-b5efaf2f-432e-46ac-a622-49661e7cf483.png) 
 
  **Intrisic Capacitances: Linear Region** 
* Cgso: gate-source overlap capacitance.
* Cgdo: gate-drain overlap capacitance.
* Cdb: drain-bulk reverse bias junction capacitance.
* Csb: source-bulk reverse bias junction capacitance.
* Cgsch: gate-channel oxide capacitance at source side.
* Cgdch: gate-channel oxide capacitance at source side.
* Cch-b: channel-bulk capacitance
* There are additional capacitance compared to cutoff due to channel form between source and drain
 
![image](https://user-images.githubusercontent.com/121995963/216217491-967f7e44-43c5-4867-9232-fdeaff4d446a.png)
 
**Intrisic Capacitances: Saturatio Region** 
* Cgso: gate-source overlap capacitance.
* Cgdo: gate-drain overlap capacitance.
* Cdb: drain-bulk reverse bias junction capacitance.
* Csb: source-bulk reverse bias junction capacitance.
* Cgsch: gate-channel oxide capacitance at source side.
* Cch-b: channel-bulk capacitance
* Cdb change because depletion region is bigger
* There is no Cgdch due to pinch off 
 
![image](https://user-images.githubusercontent.com/121995963/216217551-c14771f8-e1ad-4d41-846e-dcb86ca91058.png)

![image](https://user-images.githubusercontent.com/121995963/216217170-dd3ae203-749d-4be1-a5f8-8a138c87c5d7.png)

</details>

<details>
<summary>Lab</summary>
</details>
 
 ## Day 7
### Topic - MOSFET Parameter Extraction Scaling, Short Channel Effects and PVT Variation
<details>
 <summary> MOSFET Parameter Extraction Scaling</summary>
 
 
 **MOSFET Level1 Model Paramater:**
 1. Vt0: Zero Body biases threshold voltage
 2. y(Gamma): Body bias parameter
 3. Lambda: Channel Length Modulation
 4 KN: Transconductance parameter
 5 PHI: Surface potential
 
 ![image](https://user-images.githubusercontent.com/121995963/216221930-c59e93e4-895f-4912-bf68-ce1ea959a206.png)

**MOSFET Scaling**
 
 * Scaling of a MOS transistor means reducing the critical parameter of the device
 * To improve some performance features such as Speed, Application, Power Dissipation, while keeping the basic operational characteristics unchanged.
 
 **Advantages of scaling in MOSFET:**
 
 1) Packaging Density: The packing density of the device improves as a result of scaling hence we can fit more transistors in the same space as before.
 2) Size Chip: As we can pack more number of transistors in the same space hence we can decrease the overall area of the chip
 3) Multifunction of Chip: As transistor size is reduced we can make multifunctional chips by reducing the area of chips.
 
 **Disadvantages of Scaling**
 1) Effect on SiO2 thickness – on scaling oxide thickness eventually a sage will reach when oxide will lose its dielectric property.
 2) Subthreshold current – The carrier in the channel can be increased by increasing VDS voltage & also potential barrier can be reduced even VGS < VT. Thus, resulting current through the channel for higher values of VDS is called sub-threshold current.
 3) Noise problem – Scaling process inevitably results in noise problem, which degrades the reliability of high density chip.
**Types of Scaling in MOSFETs:**
 
 1) Constant Field Scaling
  * Attempts to preserve the magnitude of internal electric fields in the MOSFET, while the dimensions are scaled down by a factor of S.
  * Charge densities must be increased by a factor of S in order to maintain the field conditions.
 ![image](https://user-images.githubusercontent.com/121995963/216255295-80ab180b-b697-4c77-a25e-98684c875dbe.png)
 
![image](https://user-images.githubusercontent.com/121995963/216255310-c89d80f6-2576-4b9f-aff6-9a4f3895c595.png)
 
 2) Constant Voltage  Scaling
  * All dimension of the MOSFET ar reduced by a factor of S.
  * The power supply voltage and the terminal volrage remain unchanged
  * The doping densities must be increased by factor of S(2) to preserve the charge field relations
 ![image](https://user-images.githubusercontent.com/121995963/216256297-4140572e-71fb-4f19-a165-9b7f85044c24.png)
 
![image](https://user-images.githubusercontent.com/121995963/216256314-d4b4b9c9-c902-4211-973b-afedc1d28618.png)
</details>

 <details>
   <summary>Short Channel Effects</summary>
  
 **Short Channel Effect**
  
  * A MOSFET device is considered to be short when the channel length is the same order of magnitude as the depletion layer widths (Xdb, Xds) of the source and drain juntion.
  * Aslo can be defined as Short channel device if the effective channel lenght equal to the source and drain juntion depth xj.
  * As the channel lenght L is reduced to increase both the operation speed and the number of components per chip arise.
    
  ![image](https://user-images.githubusercontent.com/121995963/216262667-abb36f6b-51d1-4396-b193-e7581a3255b2.png)

  * The short channel effects are attributed to two physical phenomena:
   1) the limitation imposed on electron drift characteristics in the channel.
   2) the modification of the threshold voltage due to the shortening channel lenght.
  

  **7 different short channel effects established :**
   1) Drain Induced Barrier Lowering
      * Increases in drain voltage reduces the barrier face by electrons or holes in the source allowing them to go from ssource to drain where gate voltage remain uncharged.
      * Gate looses the contorl of flow of current throug MOS and become as good as redundant. 
      * The channel current that flows under this conditions (VGS<VT0) is called the sub-threshold current.
                                                                       
 ![image](https://user-images.githubusercontent.com/121995963/216262884-cdff4d64-e4bb-40c3-9a01-51f2be950178.png)

   2) Mobility degradation or surface scattering
       * Frm small geometry MOSFETs the electrons monility in the channel depends on a two dimensional electric filed (Ex, Ey). 
       * The surface scattering occurs when electrons are accelarated towards the surface by vertical compenent of the electric filed Ex.
       * Causes a reduction in the mobility
       * The average surface mobility is about hald as much as that of the bulk mobility
                                                                       
  ![image](https://user-images.githubusercontent.com/121995963/216264558-2e65bc40-a5ca-4d01-b7dc-cf54a4e53dc4.png)
                                                                     
  3) Velocity Saturation
     * The electron velocity is related to the electric filed through the mobility: V=uE
     * For higher field the velocity does not increase with electric field, we have defradation of mobility because of scattering by vertical field. 
     * This leads to earlier saturation of current. 
     * The velocity saturation reduces the transconductance of short-channel devices in the saturation condition.
       ![image](https://user-images.githubusercontent.com/121995963/216266131-3fae76b6-f538-4b0e-a540-02f373f8681f.png)

  4) Impact Ionization
     * The presence of high longitudinal fields can accelerate electrons that may be able of ionizing Si atoms by impacting against them
     * Most of the e- are attracted by the drains, so it has a higher concentration of holes near the sources.
     * If the holes concentration on the sources is able to creates a voltage drop on the source-substante n-p juntion of about 0.6V then 
         i) e- injected from source to substrate
         ii) e- travel towards the drain, increasing their energy and create new e-h pairs
         iii) e- may escape the drai fields and affect other devices.
![image](https://user-images.githubusercontent.com/121995963/216269201-ccc680a3-8b4f-49e3-aac0-1a5158a8974e.png)

  5) Hot Electrons
     * Caused by electrons flowing in the channel for large VDS
     * e- arriving at the Si-Si02 interface with enough kinetic evergy >3.1ev to surmount the surface potential barrier are injected into the oxide.
     * This may degrade permanently the C-V characteristics of a MOSFETs.
  
 6) Sub threshold conduction
   * When the gate voltage is high, the transistor is strongly ON. When the gate falls below Vt, the exponential decline in current appears as a straight line on the logarithmic scale.
   * This regime of Vgs < Vt is called weak inversion
   * The subthrehold leakage current increases significantly with Vds because of drain-induced barrier lowering.
   * There is lower limit on Ids set by drain junction leakage that is excerbated by the negative gate voltage. 
  ![image](https://user-images.githubusercontent.com/121995963/216272357-9daf9752-8369-4b21-a2e0-988f57851239.png)

 7) Vt toll off
 </details>

<details>
<summary>PVT Variations: Processes Variation</summary>
 
  **Variation in the process parameters:**
  * impurity concentration densities
  * oxide thicknesses
  * diffusion depths
  
  * These are caused b non-uniform conditions during the deposition and/or the diffusion of the impurities.
  * This introduces the variation of the sheet resistances and threhold voltage of transistor.

 **Variation in the dimensions:**
  * width and length variation of MOS Transistors, resistors and capacitors.
  * mismatches is emitter area in Bipolar devices.
 
 * Thse are caused by limited resolution of photolithographic process.
 * This changes the device performances in the circuit.
 
 **Process Corners**
 
 There are 5 process corners:
 1. TT ( Typical Typical): NMOS and PMOS Typical
 2. SS (Slow Slow) : NMOS Slow and PMOS Slow
 3. FF (Fast Fast) : NMOS Fast and PMOS Fast
 4. SF (Slow Fast) : NMOS Slow and PMOS Fast
 5. FS (Fast Slow) : NMOS Fast and PMOS Slow
 
 ![image](https://user-images.githubusercontent.com/121995963/216277312-99a25c57-8073-47be-ac35-88210ca99767.png)
 
</details> 
  
<details>
<summary>Lab</summary>
</details>
 
