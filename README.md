# Finfet_CircuitDesign_Characterization
The evolution of computing represents a remarkable journey from mechanical ingenuity to modern computational challenges. In the beginning, around World War 2, Alan Turing and his colleagues invented an application-specific mechanical machine called Bombe to break the Enigma code, laying the foundation for what would eventually become integrated circuits. In the post-war era, groundbreaking inventions such as the ENIAC and EDVAC were developed for large-scale simulations, relying on vacuum tubes to carry out computations. The drawback of these pioneering machines was their enormous size—stretching from floor to ceiling and occupying entire rooms.

This historical progression of general-purpose computing has been driven by the relentless increase in transistor counts, which enabled ever-larger classes of problems to be tackled. Looking at modern systems, we can now fit the computational equivalent of the entire ENIAC machine on a chip slightly bigger than a coin—a testament to decades of miniaturization and integration advances.

However, as we've pushed the boundaries of silicon scaling, energy and cooling limits have emerged as the dominant bottleneck, stalling frequency improvements and single-thread performance gains. This reality has forced a fundamental architectural shift toward parallelism, multi-core processors, specialized accelerators, distributed racks, and eventually giga-exa- to zetta-scale systems. The need for these new computing paths becomes even more critical as next-generation chips tackle increasingly complex problems such as weather modeling and forecasting, health and precision medicine, virtual particle accelerators, and many other computationally intensive challenges that demand both massive computational power and energy efficiency.

This transformation from room-sized vacuum tube machines to coin-sized chips, and now toward massively parallel and specialized computing architectures, illustrates how the field continues to evolve in response to both technological capabilities and physical constraints.

<img width="1276" height="667" alt="Image" src="https://github.com/user-attachments/assets/30e44abe-31b8-44e0-8e86-2c6da3e6dfdb" />

## Moore’s law vs performance
- Data across “40–50 Years of Microprocessor Trend Data” shows transistor counts kept rising in line with Moore’s Law even after 2005, but the curves for frequency and single‑thread performance flattened compared to the 1990s, indicating diminishing per‑core speedups despite more transistors.
- Researchers note that post‑2010 improvements in single‑thread performance are modest and largely from microarchitectural tweaks and turbo/power management, not big frequency jumps, underscoring the divergence between Moore’s Law (transistors) and user‑visible per‑thread speed.[
## Why performance stalled: power and cooling
- The key inflection was the breakdown of Dennard scaling around 2005–2007: voltage no longer scaled with geometry, leakage rose, and power density hit the “power wall,” making further frequency increases thermally impractical despite more transistors.
- With dynamic power $$P \propto C V^{2} f$$, limits on reducing $$V$$ meant higher $$f$$ drove excessive heat; as a result mainstream CPU clocks plateaued near a few GHz and TDPs around 100 W, forcing designs to cap frequency to stay within cooling envelopes.

## Shift to multi‑core
- To use the extra transistors without exceeding power, vendors increased the number of cores per chip, a trend visible as a power‑law rise in core counts while frequency stays flat; this pushes software toward parallel algorithms constrained by Amdahl’s Law.
- Industry outlooks emphasize large‑scale parallelism, heterogeneous cores, and accelerators as the path for performance per watt, because energy—not raw transistor count—now dominates achievable compute.

<img width="1310" height="638" alt="Image" src="https://github.com/user-attachments/assets/77cc1055-4413-4457-a24e-4db7e34113b8" />

## Mobile’s rise and power focus
- The smartphone era intensified the power imperative: mobile devices lack active cooling and run from batteries, so energy efficiency and strict thermal design power budgets dictate CPU/GPU operation and aggressive power management instead of high frequency.
## Toward zetta‑scale
- For solving larger and larger problems, we will see a shift from indiviual devices to data-centre scale computing. In a data-centre, racks will be used as a socket. A rack contains many computing elements. In this scale, we use flop(floating point operations per second) to measure its performance. Currently, we have attained 8-10 Exaflop performance. The trend suggests that the flop performance doubles every 2 years. But, with increase in flops, the system demands more power.
- Progress therefore hinges on compute density per watt through accelerators, memory hierarchy efficiency, interconnects, and system‑level cooling, rather than raw frequency increases, aligning the entire stack to overcome the power wall on the path to zetta‑scale computing.

<img width="1470" height="651" alt="Image" src="https://github.com/user-attachments/assets/99124294-35ee-4079-aed2-9a00ee075ac7" />

### CMOS Evolution an Next-Gen Candidates

<img width="1371" height="640" alt="Image" src="https://github.com/user-attachments/assets/e30ef2b5-adaf-4afd-b905-f3bcc4ab3641" />

The evolution of CMOS circuits is rapidly advancing towards the 1nm technology node and beyond, representing a fundamental shift from the traditional scaling paradigm. The Moore's Law principle has been essential to the semiconductor industry, but as device dimensions continue to shrink, simple lithographic scaling alone has become increasingly challenging. To overcome these limitations, comprehensive research is being conducted across multiple technological fronts, creating an integrated approach to semiconductor advancement.

## Patterning Innovations
Scaling now relies on advanced lithography techniques progressing from ArF immersion to EUV and High-NA EUV systems to maintain critical dimension control as traditional Dennard scaling gains have faded. These patterning advances enable tighter device features essential for new architectures. EUV lithography with 13.5 nm wavelength and the transition to High-NA EUV systems with numerical aperture increased from 0.33 to 0.55 are critical for achieving sub-1nm nodes. Without precise CD control from these advanced patterning techniques, revolutionary architectures like GAAFET and CFET would be impractical at commercially useful densities.

## Advanced Channel Materials
While silicon remains the foundational material, the industry is exploring revolutionary alternatives. SiGe channels improve hole mobility for PMOS devices, while research actively investigates Germanium and 2D semiconductors such as MoS₂ and WSe₂ to sustain electrostatics and maintain mobility below 3 nm gate lengths. These 2D materials promise ultra-thin channels that can suppress short-channel effects and enable novel stacking architectures like 2D-CFETs, though manufacturability challenges including contacts, transfer processes, and variability control remain significant barriers to widespread adoption.

## Gate Stack Evolution
The transition to high-k/metal-gate (HKMG) technology replaced traditional SiO₂/polysilicon structures to reduce gate leakage and maintain capacitance at smaller equivalent oxide thickness (EOT), forming the foundation for FinFETs and nanosheets at advanced nodes. Emerging gate stack innovations include negative-capacitance FETs using ferroelectric materials to overcome the 60 mV/decade subthreshold slope limit, and steep-slope devices like tunnel FETs (TFETs) for ultra-low-power logic applications.

## Device Architecture Revolution
## Structural Evolution
The semiconductor industry has progressed from planar MOSFETs to FinFETs and is now transitioning to gate-all-around nanosheet/nanowire FETs (GAAFET/NSFET) near the 3nm era to improve electrostatic control and drive current within reduced footprints. Next-generation candidates include forksheet designs with dielectric walls separating n/p stacks to reduce cell height, complementary FETs (CFETs) featuring vertical stacking of nFET over pFET for ultimate standard-cell area scaling, and experimental vertical FETs with 3D stacked architectures like Multi-Bridge Channel FETs (MBC-FETs) and 3D Stacked FETs (3DS-FETs).

## Interconnect and Power Delivery Innovation
Copper interconnect scaling faces fundamental resistance and reliability limitations, driving exploration of alternative materials like cobalt and ruthenium, along with advanced barrier/liner innovations to reduce RC delay at tight pitches. Backside power delivery networks (BSPDN) represent a paradigm shift, moving power rails to the wafer backside with buried power rails (BPR) and nano-through-silicon-vias (TSVs), freeing front-side routing while reducing IR drop and improving signal integrity.

## 3D Integration and Beyond
The roadmap increasingly shifts from pure lithographic scaling to a comprehensively co-optimized technology stack incorporating GAA/CFET devices, improved interconnects, backside power delivery, and 2.5D/3D STCO with chiplets. Success depends on integrating patterning capabilities, device physics innovations, advanced power delivery solutions, and sophisticated packaging technologies—treating CMOS evolution as a holistic system challenge rather than isolated transistor improvements. This transformation represents CMOS 2.0, where functional units are broken down into advanced 3D designs that surpass today's chiplet-based approaches, pointing toward a future where vertical integration and atomic-scale channels enable continued performance scaling beyond traditional dimensional limits.

## Fin-FETS 
FinFET (Fin Field-Effect Transistor) represents a paradigm shift from traditional planar semiconductor design, featuring a sophisticated three-dimensional structure where thin, fin-like silicon channels protrude vertically from the substrate. Unlike conventional planar transistors, the gate electrode wraps around the channel on three sides, creating superior electrostatic control that fundamentally transforms transistor performance characteristics.

<img width="1373" height="681" alt="Image" src="https://github.com/user-attachments/assets/88cec553-acea-4ff5-af3e-46832f866410" />

## Technology Node Implementation
FinFET technology became commercially dominant at the 22nm technology node and below, with widespread adoption at 14nm, 10nm, and 7nm process nodes. This transition became necessary as planar MOSFET structures encountered insurmountable scaling challenges, particularly short-channel effects that compromised device reliability and performance.

Key Features:
- Multi-fin configuration: Modern implementations often incorporate multiple fins arranged side by side under a single gate structure
- Single transistor operation: Multiple fins effectively function as one transistor to increase drive strength

Advanced nodes: Essential for sub-14nm technology nodes

- Superior Electrostatic Control
- The three-dimensional gate-around-channel architecture provides exceptional control over current flow, dramatically reducing subthreshold leakage currents that plagued planar designs.

Advantages:
- Elimination of sub-channel leakage: Multi-gate configuration effectively eliminates unwanted current paths
- Enhanced gate control: Enables use of thicker gate oxides compared to planar devices
- Reduced gate leakage: Significantly curtails gate leakage current while maintaining high performance

Improved reliability: Better control over short-channel effects

FinFETs demonstrate near-ideal subthreshold swing characteristics, typically achieving values around 87 millivolts per decade, approaching the theoretical limit for MOSFET devices.

Performance Benefits:
- Superior gate coupling: Results from the three-dimensional wraparound structure
- Reduced short-channel effects: Inherent to the fin architecture
- Enhanced gate capacitance: Contributes to faster switching speeds

Improved short-channel performance: Compared to planar alternatives

Performance Characteristics
The innovative fin architecture delivers multiple performance advantages:

Power and Speed:
- Significantly reduced power consumption through lower leakage currents
- Faster switching speeds enabled by improved carrier mobility
- Enhanced scalability for continued dimensional scaling

Electrical Properties:
- Minimal channel doping requirement: Reduces impurity scattering effects
- Improved carrier mobility: Within the channel region
- Superior voltage gain: Better amplification characteristics

Temperature stability: Maintains stable operation across varying conditions

## 7nm FinFET Nmos Performance Analysis
In this segment, we will conduct a comprehensive electrical characterization of NMOS FinFET of the 7nm technology node. Our analysis will focus on extracting key performance metrics through two fundamental I-V characteristic curves that define transistor behavior.
Characterization Objectives :- We will systematically analyze the following critical characteristics:

Transfer Characteristics (ID vs VGS)
Drain current (ID) versus gate-source voltage (VGS) 

Output Characteristics (ID vs VDS)
Drain current (ID) versus drain-source voltage (VDS) at various gate voltages

## ID vs Vin
<img width="1919" height="1133" alt="Image" src="https://github.com/user-attachments/assets/bfcdbe6a-16f0-49b9-9c1f-e444d6dc090c" />

## ID vs VD
<img width="1919" height="1132" alt="Image" src="https://github.com/user-attachments/assets/3981cad8-870d-4fea-a7a3-94fdf5d15127" />

## CMOS Inverter_vtc Characteristics

In this segment, we will conduct an in-depth analysis of CMOS inverter performance through systematic characterization of its voltage transfer characteristics and associated electrical parameters. This comprehensive evaluation will provide crucial insights into the fundamental behavior and performance metrics of CMOS logic circuits.

Voltage transfer characteristics (VTC):-Input voltage (VIN) versus Output voltage (VOUT) relationship
drain current
power analysis 
propogation delay
gain 
noise margin 
transconductance 
frequency 
output resistance

The spice deck used for simulation without the dummy voltage used is 
```
** sch_path: /home/vsduser/Desktop/asap_7nm_Xschem/inverter_vtc.sch
**.subckt inverter_vtc
Xpfet1 nfet_out nfet_in vdd vdd asap_7nm_pfet l=7e-009 nfin=14
Xnfet1 nfet_out nfet_in GND GND asap_7nm_nfet l=7e-009 nfin=14
V1 nfet_in GND pulse(0 0.7 20p 10p 10p 20p 500p 1)
V2 vdd GND 0.7
Vuniq in 0 DC 0.764
**** begin user architecture code


.dc v1 0 0.7 1m
*.tran 1e-12 100e-12

.control
    * First run DC
    dc v1 0 0.7 1m
    run

    * DC measurements
    meas dc v_th when nfet_out = nfet_in
    plot nfet_out nfet_in
    
    let gain_av = abs(deriv(nfet_out))
    meas dc max_gain max gain_av
    let gain_target = max_gain * 0.999
    meas dc vil find nfet_in when gain_av = gain_target cross=1
    meas dc voh find nfet_out when gain_av = gain_target cross=1
    meas dc vih find nfet_in when gain_av = gain_target cross=2
    meas dc vol find nfet_out when gain_av = gain_target cross=2
    let nmh = voh - vih
    let nml = vil - vol
    print v_th max_gain vil voh vih vol nmh nml
    
    *Transconductance
    
    let id = v2#branch
    let gm = real(deriv(id, nfet_in))
    meas dc gm_max MAX gm
    plot gm
    let r_out= deriv(nfet_out,id)
    plot r_out
    plot id
    
    * Transient measurements
    tran 1e-12 100e-12
    meas tran tpr when nfet_in = 0.35 rise = 1
    meas tran tpf when nfet_out = 0.35 fall = 1
    let tp = (tpr + tpf) / 2
    let trans_current = v2#branch
    meas tran id_pwr integ trans_current from=2e-11 to=6e-11
    let pwr = id_pwr * 0.7
    let power = abs(pwr / 40e-12)
    print tpr tpf tp id_pwr pwr power
  
    tran 0.1 100p                         
    meas tran tr when nfet_in=0.07 RISE=1  
    meas tran tf when nfet_out=0.63 FALL=1 
    let t_delay = tr + tf                  
    print t_delay                         
    let f = 1/t_delay                     
    print f                              

    

.endc




**** end user architecture code
**.ends
.GLOBAL GND
**** begin user architecture code

.subckt asap_7nm_pfet S G D B l=7e-009 nfin=14
	npmos_finfet S G D B BSIMCMG_osdi_P l=7e-009 nfin=14
.ends asap_7nm_pfet

.model BSIMCMG_osdi_P BSIMCMG_va (
+ TYPE = 0

************************************************************
*                         general                          *
************************************************************
+version = 107             bulkmod = 1               igcmod  = 1               igbmod  = 0
+gidlmod = 1               iimod   = 0               geomod  = 1               rdsmod  = 0
+rgatemod= 0               rgeomod = 0               shmod   = 0               nqsmod  = 0
+coremod = 0               cgeomod = 0               capmod  = 0               tnom    = 25
+eot     = 1e-009          eotbox  = 1.4e-007        eotacc  = 3e-010          tfin    = 6.5e-009
+toxp    = 2.1e-009        nbody   = 1e+022          phig    = 4.9278          epsrox  = 3.9
+epsrsub = 11.9            easub   = 4.05            ni0sub  = 1.1e+016        bg0sub  = 1.17
+nc0sub  = 2.86e+025       nsd     = 2e+026          ngate   = 0               nseg    = 5
+l       = 2.1e-008        xl      = 1e-009          lint    = -2.5e-009       dlc     = 0
+dlbin   = 0               hfin    = 3.2e-008        deltaw  = 0               deltawcv= 0
+sdterm  = 0               epsrsp  = 3.9             nfin    = 1
+toxg    = 1.8e-009
************************************************************
*                            dc                            *
************************************************************
+cit     = 0               cdsc    = 0.003469        cdscd   = 0.001486        dvt0    = 0.05
+dvt1    = 0.36            phin    = 0.05            eta0    = 0.094           dsub    = 0.24
+k1rsce  = 0               lpe0    = 0               dvtshift= 0               qmfactor= 0
+etaqm   = 0.54            qm0     = 2.183e-012      pqm     = 0.66            u0      = 0.0237
+etamob  = 4               up      = 0               ua      = 1.133           eu      = 0.05
+ud      = 0.0105          ucs     = 0.2672          rdswmin = 0               rdsw    = 200
+wr      = 1               rswmin  = 0               rdwmin  = 0               rshs    = 0
+rshd    = 0               vsat    = 60000           deltavsat= 0.17            ksativ  = 1.592
+mexp    = 2.491           ptwg    = 25              pclm    = 0.01            pclmg   = 1
+pdibl1  = 800             pdibl2  = 0.005704        drout   = 4.97            pvag    = 200
+fpitch  = 2.7e-008        rth0    = 0.15            cth0    = 1.243e-006      wth0    = 2.6e-007
+lcdscd  = 0               lcdscdr = 0               lrdsw   = 1.3             lvsat   = 1441
************************************************************
*                         leakage                          *
************************************************************
+aigc    = 0.007           bigc    = 0.0015          cigc    = 1               dlcigs  = 5e-009
+dlcigd  = 5e-009          aigs    = 0.006           aigd    = 0.006           bigs    = 0.001944
+bigd    = 0.001944        cigs    = 1               cigd    = 1               poxedge = 1.152
+agidl   = 2e-012          agisl   = 2e-012          bgidl   = 1.5e+008        bgisl   = 1.5e+008
+egidl   = 1.142           egisl   = 1.142
************************************************************
*                            rf                            *
************************************************************
************************************************************
*                         junction                         *
************************************************************
************************************************************
*                       capacitance                        *
************************************************************
+cfs     = 0               cfd     = 0               cgso    = 1.6e-010        cgdo    = 1.6e-010
+cgsl    = 0               cgdl    = 0               ckappas = 0.6             ckappad = 0.6
+cgbo    = 0               cgbl    = 0
************************************************************
*                       temperature                        *
************************************************************
+tbgasub = 0.000473        tbgbsub = 636             kt1     = 0               kt1l    = 0
+ute     = -1.2            utl     = 0               ua1     = 0.001032        ud1     = 0
+ucste   = -0.004775       at      = 0.001           ptwgt   = 0.004           tmexp   = 0
+prt     = 0               tgidl   = -0.007          igt     = 2.5
************************************************************
*                          noise                           *
************************************************************
**)
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
.endc



.subckt asap_7nm_nfet S G D B l=7e-009 nfin=14
	nnmos_finfet S G D B BSIMCMG_osdi_N l=7e-009 nfin=14
.ends asap_7nm_nfet

.model BSIMCMG_osdi_N BSIMCMG_va (
+ TYPE = 1
************************************************************
*                         general                          *
************************************************************
+version = 107             bulkmod = 1               igcmod  = 1               igbmod  = 0
+gidlmod = 1               iimod   = 0               geomod  = 1               rdsmod  = 0
+rgatemod= 0               rgeomod = 0               shmod   = 0               nqsmod  = 0
+coremod = 0               cgeomod = 0               capmod  = 0               tnom    = 25
+eot     = 1e-009          eotbox  = 1.4e-007        eotacc  = 1e-010          tfin    = 6.5e-009
+toxp    = 2.1e-009        nbody   = 1e+022          phig    = 4.2466          epsrox  = 3.9
+epsrsub = 11.9            easub   = 4.05            ni0sub  = 1.1e+016        bg0sub  = 1.17
+nc0sub  = 2.86e+025       nsd     = 2e+026          ngate   = 0               nseg    = 5
+l       = 2.1e-008        xl      = 1e-009          lint    = -2e-009         dlc     = 0
+dlbin   = 0               hfin    = 3.2e-008        deltaw  = 0               deltawcv= 0
+sdterm  = 0               epsrsp  = 3.9             nfin    = 1
+toxg    = 1.80e-009
************************************************************
*                            dc                            *
************************************************************
+cit     = 0               cdsc    = 0.01            cdscd   = 0.01            dvt0    = 0.05
+dvt1    = 0.47            phin    = 0.05            eta0    = 0.07            dsub    = 0.35
+k1rsce  = 0               lpe0    = 0               dvtshift= 0               qmfactor= 2.5
+etaqm   = 0.54            qm0     = 0.001           pqm     = 0.66            u0      = 0.0303
+etamob  = 2               up      = 0               ua      = 0.55            eu      = 1.2
+ud      = 0               ucs     = 1               rdswmin = 0               rdsw    = 200
+wr      = 1               rswmin  = 0               rdwmin  = 0               rshs    = 0
+rshd    = 0               vsat    = 70000           deltavsat= 0.2             ksativ  = 2
+mexp    = 4               ptwg    = 30              pclm    = 0.05            pclmg   = 0
+pdibl1  = 0               pdibl2  = 0.002           drout   = 1               pvag    = 0
+fpitch  = 2.7e-008        rth0    = 0.225           cth0    = 1.243e-006      wth0    = 2.6e-007
+lcdscd  = 5e-005          lcdscdr = 5e-005          lrdsw   = 0.2             lvsat   = 0
************************************************************
*                         leakage                          *
************************************************************
+aigc    = 0.014           bigc    = 0.005           cigc    = 0.25            dlcigs  = 1e-009
+dlcigd  = 1e-009          aigs    = 0.0115          aigd    = 0.0115          bigs    = 0.00332
+bigd    = 0.00332         cigs    = 0.35            cigd    = 0.35            poxedge = 1.1
+agidl   = 1e-012          agisl   = 1e-012          bgidl   = 10000000        bgisl   = 10000000
+egidl   = 0.35            egisl   = 0.35
************************************************************
*                            rf                            *
************************************************************
************************************************************
*                         junction                         *
************************************************************
************************************************************
*                       capacitance                        *
************************************************************
+cfs     = 0               cfd     = 0               cgso    = 1.6e-010        cgdo    = 1.6e-010
+cgsl    = 0               cgdl    = 0               ckappas = 0.6             ckappad = 0.6
+cgbo    = 0               cgbl    = 0
************************************************************
*                       temperature                        *
************************************************************
+tbgasub = 0.000473        tbgbsub = 636             kt1     = 0               kt1l    = 0
+ute     = -0.7            utl     = 0               ua1     = 0.001032        ud1     = 0
+ucste   = -0.004775       at      = 0.001           ptwgt   = 0.004           tmexp   = 0
+prt     = 0               tgidl   = -0.007          igt     = 2.5
************************************************************
*                          noise                           *
************************************************************
**)
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
.endc


**** end user architecture code
.end

```
baseline values 
##FOR pmos W/L=14 and nmos W/L=14
## Voltage transfer characteristics (VTC):-Input voltage (VIN) versus Output voltage (VOUT) relationship

<img width="1919" height="1143" alt="Image" src="https://github.com/user-attachments/assets/3d037628-1423-42a8-a50c-19e246d855e4" />

## Drain current

<img width="1918" height="1148" alt="Image" src="https://github.com/user-attachments/assets/5a730262-9717-4130-8d24-815c9f531f24" />

## Output resistance ro

<img width="1919" height="1138" alt="Image" src="https://github.com/user-attachments/assets/1e6b7615-0d8b-4ac0-b18c-c7eac3fd05d8" />

## Transconductance gm  

<img width="1919" height="1139" alt="Image" src="https://github.com/user-attachments/assets/1ad9bf8d-f1b6-4697-892f-2574a7ff8164" />

## Values for switching threshold , drain current , Power , tpd , Av and frequency derived from graphs 

<img width="1618" height="949" alt="Image" src="https://github.com/user-attachments/assets/6b3e14a3-357b-491f-b232-db8b2f233176" />

<img width="1625" height="418" alt="Image" src="https://github.com/user-attachments/assets/e9c71a93-221e-4fd4-8810-de08441eb18c" />

## Characterisation table for different W/L ratios with unique source

Now that we have analyzed the nfet, we can move on to the analysis of inverter circuit using the finfet. WE will be using offset in the pulse voltage to obtain unique results.

The offset voltage value is derived from adding the ASCII values of my name (astitva = 97 + 115 + 116 + 105+116+118+97 = 764)
To add the offset voltage, we will use the following command,
```
V1 nfet_in GND pulse(0.764 1.464 20p 10p 10p 20p 500p 1)
```

The spice deck used is 
```
** sch_path: /home/vsduser/Desktop/asap_7nm_Xschem/inverter_vtc.sch
**.subckt inverter_vtc
Xpfet1 nfet_out nfet_in vdd vdd asap_7nm_pfet l=7e-009 nfin=14
Xnfet1 nfet_out nfet_in GND GND asap_7nm_nfet l=7e-009 nfin=14
V1 nfet_in GND pulse(0.764 1.464 20p 10p 10p 20p 500p 1)
V2 vdd GND 0.7
**** begin user architecture code


.dc v1 0 0.7 1m
*.tran 1e-12 100e-12

.control
    * First run DC
    dc v1 0.764 1.464 1m
    run

    * DC measurements
    meas dc v_th when nfet_out = nfet_in
    plot nfet_out nfet_in
    
    let gain_av = abs(deriv(nfet_out))
    meas dc max_gain max gain_av
    let gain_target = max_gain * 0.999
    meas dc vil find nfet_in when gain_av = gain_target cross=1
    meas dc voh find nfet_out when gain_av = gain_target cross=1
    meas dc vih find nfet_in when gain_av = gain_target cross=2
    meas dc vol find nfet_out when gain_av = gain_target cross=2
    let nmh = voh - vih
    let nml = vil - vol
    print v_th max_gain vil voh vih vol nmh nml
    
    *Transconductance
    
    let id = v2#branch
    let gm = real(deriv(id, nfet_in))
    meas dc gm_max MAX gm
    plot gm
    let r_out= deriv(nfet_out,id)
    plot r_out
    plot id
    
    * Transient measurements
    tran 1e-12 100e-12
    meas tran tpr when v(nfet_in)=1.114 RISE=1
    meas tran tpf when v(nfet_out)=0.00435 FALL=1
    let  tp = (tpr + tpf) /2
    let trans_current = v2#branch
    meas tran id_pwr integ trans_current from=2e-11 to=6e-11
    let pwr = id_pwr * 0.7
    let power = abs(pwr / 40e-12)
    print tpr tpf tp id_pwr pwr power
  
    tran 0.1 100p
                             
    meas tran tr when nfet_in=0.834 RISE=1
    meas tran tf when nfet_out=0.00783 FALL=1       
    let t_delay = tr + tf                  
    print t_delay                         
    let f = 1/t_delay                     
    print f                              

    

.endc




**** end user architecture code
**.ends
.GLOBAL GND
**** begin user architecture code

.subckt asap_7nm_pfet S G D B l=7e-009 nfin=14
	npmos_finfet S G D B BSIMCMG_osdi_P l=7e-009 nfin=14
.ends asap_7nm_pfet

.model BSIMCMG_osdi_P BSIMCMG_va (
+ TYPE = 0

************************************************************
*                         general                          *
************************************************************
+version = 107             bulkmod = 1               igcmod  = 1               igbmod  = 0
+gidlmod = 1               iimod   = 0               geomod  = 1               rdsmod  = 0
+rgatemod= 0               rgeomod = 0               shmod   = 0               nqsmod  = 0
+coremod = 0               cgeomod = 0               capmod  = 0               tnom    = 25
+eot     = 1e-009          eotbox  = 1.4e-007        eotacc  = 3e-010          tfin    = 6.5e-009
+toxp    = 2.1e-009        nbody   = 1e+022          phig    = 4.9278          epsrox  = 3.9
+epsrsub = 11.9            easub   = 4.05            ni0sub  = 1.1e+016        bg0sub  = 1.17
+nc0sub  = 2.86e+025       nsd     = 2e+026          ngate   = 0               nseg    = 5
+l       = 2.1e-008        xl      = 1e-009          lint    = -2.5e-009       dlc     = 0
+dlbin   = 0               hfin    = 3.2e-008        deltaw  = 0               deltawcv= 0
+sdterm  = 0               epsrsp  = 3.9             nfin    = 1
+toxg    = 1.8e-009
************************************************************
*                            dc                            *
************************************************************
+cit     = 0               cdsc    = 0.003469        cdscd   = 0.001486        dvt0    = 0.05
+dvt1    = 0.36            phin    = 0.05            eta0    = 0.094           dsub    = 0.24
+k1rsce  = 0               lpe0    = 0               dvtshift= 0               qmfactor= 0
+etaqm   = 0.54            qm0     = 2.183e-012      pqm     = 0.66            u0      = 0.0237
+etamob  = 4               up      = 0               ua      = 1.133           eu      = 0.05
+ud      = 0.0105          ucs     = 0.2672          rdswmin = 0               rdsw    = 200
+wr      = 1               rswmin  = 0               rdwmin  = 0               rshs    = 0
+rshd    = 0               vsat    = 60000           deltavsat= 0.17            ksativ  = 1.592
+mexp    = 2.491           ptwg    = 25              pclm    = 0.01            pclmg   = 1
+pdibl1  = 800             pdibl2  = 0.005704        drout   = 4.97            pvag    = 200
+fpitch  = 2.7e-008        rth0    = 0.15            cth0    = 1.243e-006      wth0    = 2.6e-007
+lcdscd  = 0               lcdscdr = 0               lrdsw   = 1.3             lvsat   = 1441
************************************************************
*                         leakage                          *
************************************************************
+aigc    = 0.007           bigc    = 0.0015          cigc    = 1               dlcigs  = 5e-009
+dlcigd  = 5e-009          aigs    = 0.006           aigd    = 0.006           bigs    = 0.001944
+bigd    = 0.001944        cigs    = 1               cigd    = 1               poxedge = 1.152
+agidl   = 2e-012          agisl   = 2e-012          bgidl   = 1.5e+008        bgisl   = 1.5e+008
+egidl   = 1.142           egisl   = 1.142
************************************************************
*                            rf                            *
************************************************************
************************************************************
*                         junction                         *
************************************************************
************************************************************
*                       capacitance                        *
************************************************************
+cfs     = 0               cfd     = 0               cgso    = 1.6e-010        cgdo    = 1.6e-010
+cgsl    = 0               cgdl    = 0               ckappas = 0.6             ckappad = 0.6
+cgbo    = 0               cgbl    = 0
************************************************************
*                       temperature                        *
************************************************************
+tbgasub = 0.000473        tbgbsub = 636             kt1     = 0               kt1l    = 0
+ute     = -1.2            utl     = 0               ua1     = 0.001032        ud1     = 0
+ucste   = -0.004775       at      = 0.001           ptwgt   = 0.004           tmexp   = 0
+prt     = 0               tgidl   = -0.007          igt     = 2.5
************************************************************
*                          noise                           *
************************************************************
**)
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
.endc



.subckt asap_7nm_nfet S G D B l=7e-009 nfin=14
	nnmos_finfet S G D B BSIMCMG_osdi_N l=7e-009 nfin=14
.ends asap_7nm_nfet

.model BSIMCMG_osdi_N BSIMCMG_va (
+ TYPE = 1
************************************************************
*                         general                          *
************************************************************
+version = 107             bulkmod = 1               igcmod  = 1               igbmod  = 0
+gidlmod = 1               iimod   = 0               geomod  = 1               rdsmod  = 0
+rgatemod= 0               rgeomod = 0               shmod   = 0               nqsmod  = 0
+coremod = 0               cgeomod = 0               capmod  = 0               tnom    = 25
+eot     = 1e-009          eotbox  = 1.4e-007        eotacc  = 1e-010          tfin    = 6.5e-009
+toxp    = 2.1e-009        nbody   = 1e+022          phig    = 4.2466          epsrox  = 3.9
+epsrsub = 11.9            easub   = 4.05            ni0sub  = 1.1e+016        bg0sub  = 1.17
+nc0sub  = 2.86e+025       nsd     = 2e+026          ngate   = 0               nseg    = 5
+l       = 2.1e-008        xl      = 1e-009          lint    = -2e-009         dlc     = 0
+dlbin   = 0               hfin    = 3.2e-008        deltaw  = 0               deltawcv= 0
+sdterm  = 0               epsrsp  = 3.9             nfin    = 1
+toxg    = 1.80e-009
************************************************************
*                            dc                            *
************************************************************
+cit     = 0               cdsc    = 0.01            cdscd   = 0.01            dvt0    = 0.05
+dvt1    = 0.47            phin    = 0.05            eta0    = 0.07            dsub    = 0.35
+k1rsce  = 0               lpe0    = 0               dvtshift= 0               qmfactor= 2.5
+etaqm   = 0.54            qm0     = 0.001           pqm     = 0.66            u0      = 0.0303
+etamob  = 2               up      = 0               ua      = 0.55            eu      = 1.2
+ud      = 0               ucs     = 1               rdswmin = 0               rdsw    = 200
+wr      = 1               rswmin  = 0               rdwmin  = 0               rshs    = 0
+rshd    = 0               vsat    = 70000           deltavsat= 0.2             ksativ  = 2
+mexp    = 4               ptwg    = 30              pclm    = 0.05            pclmg   = 0
+pdibl1  = 0               pdibl2  = 0.002           drout   = 1               pvag    = 0
+fpitch  = 2.7e-008        rth0    = 0.225           cth0    = 1.243e-006      wth0    = 2.6e-007
+lcdscd  = 5e-005          lcdscdr = 5e-005          lrdsw   = 0.2             lvsat   = 0
************************************************************
*                         leakage                          *
************************************************************
+aigc    = 0.014           bigc    = 0.005           cigc    = 0.25            dlcigs  = 1e-009
+dlcigd  = 1e-009          aigs    = 0.0115          aigd    = 0.0115          bigs    = 0.00332
+bigd    = 0.00332         cigs    = 0.35            cigd    = 0.35            poxedge = 1.1
+agidl   = 1e-012          agisl   = 1e-012          bgidl   = 10000000        bgisl   = 10000000
+egidl   = 0.35            egisl   = 0.35
************************************************************
*                            rf                            *
************************************************************
************************************************************
*                         junction                         *
************************************************************
************************************************************
*                       capacitance                        *
************************************************************
+cfs     = 0               cfd     = 0               cgso    = 1.6e-010        cgdo    = 1.6e-010
+cgsl    = 0               cgdl    = 0               ckappas = 0.6             ckappad = 0.6
+cgbo    = 0               cgbl    = 0
************************************************************
*                       temperature                        *
************************************************************
+tbgasub = 0.000473        tbgbsub = 636             kt1     = 0               kt1l    = 0
+ute     = -0.7            utl     = 0               ua1     = 0.001032        ud1     = 0
+ucste   = -0.004775       at      = 0.001           ptwgt   = 0.004           tmexp   = 0
+prt     = 0               tgidl   = -0.007          igt     = 2.5
************************************************************
*                          noise                           *
************************************************************
**)
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
.endc


**** end user architecture code
.end
```
## For changing the W/L ratio

The length remains constant at 7nm and we just change the no of fins at the top as 

```
Xpfet1 nfet_out nfet_in vdd vdd asap_7nm_pfet l=7e-009 nfin=14
Xpfet1 nfet_out nfet_in vdd vdd asap_7nm_pfet l=7e-009 nfin=x
Xnfet1 nfet_out nfet_in vdd vdd asap_7nm_pfet l=7e-009 nfin=x
```
and we change the no of fins in the model for pmos and nmos as 

```
.subckt asap_7nm_pfet S G D B l=7e-009 nfin=14
	npmos_finfet S G D B BSIMCMG_osdi_P l=7e-009 nfin=14

.subckt asap_7nm_pfet S G D B l=7e-009 nfin=x
	npmos_finfet S G D B BSIMCMG_osdi_P l=7e-009 nfin=x
```
 
The change of ratio affects the tpf and tpr and tr and tf slightly 

## FOR pmos W/L=14 and nmos W/L=14
## Voltage transfer characteristics (VTC):-Input voltage (VIN) versus Output voltage (VOUT) relationship

<img width="1919" height="1139" alt="Image" src="https://github.com/user-attachments/assets/f0ac8c76-78bf-4074-96a2-739fd59b9aad" />

## Drain current

<img width="1919" height="1141" alt="14_14id" src="https://github.com/user-attachments/assets/9d477544-41fe-4cb7-b611-b180119845a0" />

## Output resistance ro

<img width="1919" height="1142" alt="Image" src="https://github.com/user-attachments/assets/0aeed82e-d424-4c7a-9a84-f25cf12d576b" />

## Transconductance gm  

<img width="1919" height="1138" alt="Image" src="https://github.com/user-attachments/assets/0f0dc5a0-b357-4cfa-bf1c-fca139380a93" />

## Values for switching threshold , drain current , Power , tpd , Av and frequency derived from graphs 

<img width="1919" height="1114" alt="14_14values1" src="https://github.com/user-attachments/assets/9132bb1a-f5f7-4da9-9615-5b735893b780" />

<img width="1911" height="1139" alt="14_14values2" src="https://github.com/user-attachments/assets/f9da7a4e-52e6-4ecc-822e-293ecc73a5fb" />

<img width="1919" height="1141" alt="14_14values3" src="https://github.com/user-attachments/assets/94f15a5d-d860-470e-a921-5403d77b1e71" />


## FOR pmos W/L=15 and nmos W/L=14
## Voltage transfer characteristics (VTC):-Input voltage (VIN) versus Output voltage (VOUT) relationship

<img width="1919" height="1140" alt="15_14vtc" src="https://github.com/user-attachments/assets/e5a10fd2-ba77-4e5a-a621-12dfed1c855d" />


## Drain current

<img width="1919" height="1140" alt="15_14id" src="https://github.com/user-attachments/assets/4354c3b3-4734-4e21-804d-85422af21f8b" />


## Output resistance ro

<img width="1917" height="1138" alt="15_14rout" src="https://github.com/user-attachments/assets/ed4cf141-c5ea-4aed-8d0b-f2b0ee716db8" />


## Transconductance gm  

<img width="1919" height="1144" alt="15_14gm" src="https://github.com/user-attachments/assets/e8a76661-e4d8-472b-b4be-b36c53d9ccc5" />

## Values for switching threshold , drain current , Power , tpd , Av and frequency derived from graphs 

<img width="1919" height="1139" alt="15_14values1" src="https://github.com/user-attachments/assets/d1afab8e-c09a-4e05-9624-f610151138f3" />

<img width="1919" height="1144" alt="15_14values2" src="https://github.com/user-attachments/assets/58d4f703-f479-48a2-9495-6beb2ed492aa" />

<img width="1919" height="1142" alt="15_14values3" src="https://github.com/user-attachments/assets/5169d37c-2da6-493c-805b-f167b77d6cba" />

## FOR pmos W/L=16 and nmos W/L=14
## Voltage transfer characteristics (VTC):-Input voltage (VIN) versus Output voltage (VOUT) relationship

<img width="1919" height="1144" alt="16_14vtc" src="https://github.com/user-attachments/assets/e1692dda-b8fa-48e8-9a27-dd4350602241" />



## Drain current

<img width="1919" height="1144" alt="16_14id" src="https://github.com/user-attachments/assets/17817ae2-ca33-43e0-a1c5-e7d8909e3d16" />


## Output resistance ro

<img width="1919" height="1143" alt="16_14rout" src="https://github.com/user-attachments/assets/36021e4e-ab8b-4158-a87c-ff25f907ef3c" />


## Transconductance gm  

<img width="1919" height="1139" alt="16_14gm" src="https://github.com/user-attachments/assets/c7dff37f-e84b-4276-a998-1dd4b678617c" />

## Values for switching threshold , drain current , Power , tpd , Av and frequency derived from graphs 

<img width="1919" height="1141" alt="16_14values1" src="https://github.com/user-attachments/assets/3652c337-2fe0-403a-80e0-f8d844af6774" />

<img width="1919" height="1134" alt="16_14values2" src="https://github.com/user-attachments/assets/58843231-c7fd-4ffb-a1e7-8213a6a0f94d" />

<img width="1919" height="1137" alt="16_14values3" src="https://github.com/user-attachments/assets/469306ba-05d2-478a-875c-ef789e48040a" />

The values derived from the graphs 

## Characterization table for inverter
<img width="1046" height="138" alt="image" src="https://github.com/user-attachments/assets/d3554973-5caf-4620-9d62-d1e97e9769af" />



## Bandgap Reference Design and Simulation using Xschem

The below photo is taken as the reference circuit for designing the Bandgap reference.

<img width="840" height="531" alt="Image" src="https://github.com/user-attachments/assets/14150a0b-fd74-442a-97b5-b697b246ed16" />

### Steps to implement the circuit in Xschem


1. Open Xschem
```
Xschem
```
2. Press ``` ctrl + I ``` to ivoke the component list.
3. Search pfet and nfet and select them indivually and drag them onto the board to create the circuit.
4. To get multiple nfet of same properties, you can duplicate the nfet/pfet.
5. Create the circuit
6. Make connections as given in the schematic.
7. Search for VDD, GND, source, resistance in the component list and connect them in their respective place.
8. Add a simulation deck command window
9. Add the commands to plot various desired graphs.

## Design using Xschem 

We have added our own  resistance in the startup branch by selecting a resistor of ASCII values of my name (astitva = 97 + 115 + 116 + 105+116+118+97 = 764)

<img width="1568" height="804" alt="Image" src="https://github.com/user-attachments/assets/02abf75f-1465-447d-bc97-f1522b609f5e" />

Code for dc analysis used to plot Vref and Vctat
```
name=s1 only_toplevel=false value="
.dc temp -45 150 5
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
run
plot v(Vref) v(Vctat)
plot v(Vref)-v(Vctat)
plot v(Vctat)
plot v(Vref)
let temp_coeff = deriv(v(Vref))/1.24
plot temp_coeff
plot net9/30k Vref/33.33k Vctat/33.33k
plot abs(v2#branch)
.endc
"
```
Code for transient analysis used to plot Vref and Vctat



spice deck

```
** sch_path: /home/vsduser/Desktop/asap_7nm_Xschem/bandgap_ref2.sch
**.subckt bandgap_ref2
V1 VDD GND PWL(0 0 1u 0 1.1u 1 2m 1)
Xnfet1 net7 net8 net6 net11 asap_7nm_nfet l=7e-009 nfin=14
Xpfet1 net6 net5 VDD net12 asap_7nm_pfet l=7e-009 nfin=14
Xpfet2 net5 net5 VDD net13 asap_7nm_pfet l=7e-009 nfin=14
Xpfet3 Vref net14 VDD net15 asap_7nm_pfet l=7e-009 nfin=14
Xpfet4 net4 net5 VDD net16 asap_7nm_pfet l=7e-009 nfin=14
Xpfet5 net1 net5 net4 net17 asap_7nm_pfet l=7e-009 nfin=14
Xpfet6 net8 net5 net5 net18 asap_7nm_pfet l=7e-009 nfin=14
Xnfet2 net10 net8 net5 net19 asap_7nm_nfet l=7e-009 nfin=14
Xnfet3 net1 net1 net2 net20 asap_7nm_nfet l=7e-009 nfin=14
Xnfet4 net2 net2 net3 net21 asap_7nm_nfet l=7e-009 nfin=14
Xnfet5 net7 net7 GND net22 asap_7nm_nfet l=7e-009 nfin=14
Xnfet6 net9 net9 GND GND asap_7nm_nfet l=7e-009 nfin=14
Xnfet7 net9 net9 GND GND asap_7nm_nfet l=7e-009 nfin=14
Xnfet8 net9 net9 GND GND asap_7nm_nfet l=7e-009 nfin=14
Xnfet9 net9 net9 GND GND asap_7nm_nfet l=7e-009 nfin=14
R1 net10 net9 33k ac=1k m=1
R2 Vref Vctat 50k ac=1k m=1
Xnfet10 Vctat Vctat GND net23 asap_7nm_nfet l=7e-009 nfin=14
R3 net3 GND 764 m=1
**** begin user architecture code



.tran 10u 2m uic
.temp 27
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
run
 meas tran vref_final FIND v(vref) AT=1.99m
  meas tran t_99 WHEN v(vref)=0.99*vref_final FALL=1
  print t_99
plot v(VCTAT)
plot v(Vref)

.endc

.endc


**** end user architecture code
**.ends
.GLOBAL VDD
.GLOBAL GND
**** begin user architecture code

.subckt asap_7nm_pfet S G D B l=7e-009 nfin=14
        npmos_finfet S G D B BSIMCMG_osdi_P l=7e-009 nfin=14
.ends asap_7nm_pfet


.model BSIMCMG_osdi_P BSIMCMG_va (
+ TYPE = 0

************************************************************
*                         general                          *
************************************************************
+version = 107             bulkmod = 1               igcmod  = 1               igbmod  = 0
+gidlmod = 1               iimod   = 0               geomod  = 1               rdsmod  = 0
+rgatemod= 0               rgeomod = 0               shmod   = 0               nqsmod  = 0
+coremod = 0               cgeomod = 0               capmod  = 0               tnom    = 25
+eot     = 1e-009          eotbox  = 1.4e-007        eotacc  = 3e-010          tfin    = 6.5e-009
+toxp    = 2.1e-009        nbody   = 1e+022          phig    = 4.9278          epsrox  = 3.9
+epsrsub = 11.9            easub   = 4.05            ni0sub  = 1.1e+016        bg0sub  = 1.17
+nc0sub  = 2.86e+025       nsd     = 2e+026          ngate   = 0               nseg    = 5
+l       = 2.1e-008        xl      = 1e-009          lint    = -2.5e-009       dlc     = 0
+dlbin   = 0               hfin    = 3.2e-008        deltaw  = 0               deltawcv= 0
+sdterm  = 0               epsrsp  = 3.9             nfin    = 1
+toxg    = 1.8e-009
************************************************************
*                            dc                            *
************************************************************
+cit     = 0               cdsc    = 0.003469        cdscd   = 0.001486        dvt0    = 0.05
+dvt1    = 0.36            phin    = 0.05            eta0    = 0.094           dsub    = 0.24
+k1rsce  = 0               lpe0    = 0               dvtshift= 0               qmfactor= 0
+etaqm   = 0.54            qm0     = 2.183e-012      pqm     = 0.66            u0      = 0.0237
+etamob  = 4               up      = 0               ua      = 1.133           eu      = 0.05
+ud      = 0.0105          ucs     = 0.2672          rdswmin = 0               rdsw    = 200
+wr      = 1               rswmin  = 0               rdwmin  = 0               rshs    = 0
+rshd    = 0               vsat    = 60000           deltavsat= 0.17            ksativ  = 1.592
+mexp    = 2.491           ptwg    = 25              pclm    = 0.01            pclmg   = 1
+pdibl1  = 800             pdibl2  = 0.005704        drout   = 4.97            pvag    = 200
+fpitch  = 2.7e-008        rth0    = 0.15            cth0    = 1.243e-006      wth0    = 2.6e-007
+lcdscd  = 0               lcdscdr = 0               lrdsw   = 1.3             lvsat   = 1441
************************************************************
*                         leakage                          *
************************************************************
+aigc    = 0.007           bigc    = 0.0015          cigc    = 1               dlcigs  = 5e-009
+dlcigd  = 5e-009          aigs    = 0.006           aigd    = 0.006           bigs    = 0.001944
+bigd    = 0.001944        cigs    = 1               cigd    = 1               poxedge = 1.152
+agidl   = 2e-012          agisl   = 2e-012          bgidl   = 1.5e+008        bgisl   = 1.5e+008
+egidl   = 1.142           egisl   = 1.142
************************************************************
*                            rf                            *
************************************************************
************************************************************
*                         junction                         *
************************************************************
************************************************************
*                       capacitance                        *
************************************************************
+cfs     = 0               cfd     = 0               cgso    = 1.6e-010        cgdo    = 1.6e-010
+cgsl    = 0               cgdl    = 0               ckappas = 0.6             ckappad = 0.6
+cgbo    = 0               cgbl    = 0
************************************************************
*                       temperature                        *
************************************************************
+tbgasub = 0.000473        tbgbsub = 636             kt1     = 0               kt1l    = 0
+ute     = -1.2            utl     = 0               ua1     = 0.001032        ud1     = 0
+ucste   = -0.004775       at      = 0.001           ptwgt   = 0.004           tmexp   = 0
+prt     = 0               tgidl   = -0.007          igt     = 2.5
************************************************************
*                          noise                           *
************************************************************
**)
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
.endc



.subckt asap_7nm_nfet S G D B l=7e-009 nfin=14
        nnmos_finfet S G D B BSIMCMG_osdi_N l=7e-009 nfin=14
.ends asap_7nm_nfet

.model BSIMCMG_osdi_N BSIMCMG_va (
+ TYPE = 1
************************************************************
*                         general                          *
************************************************************
+version = 107             bulkmod = 1               igcmod  = 1               igbmod  = 0
+gidlmod = 1               iimod   = 0               geomod  = 1               rdsmod  = 0
+rgatemod= 0               rgeomod = 0               shmod   = 0               nqsmod  = 0
+coremod = 0               cgeomod = 0               capmod  = 0               tnom    = 25
+eot     = 1e-009          eotbox  = 1.4e-007        eotacc  = 1e-010          tfin    = 6.5e-009
+toxp    = 2.1e-009        nbody   = 1e+022          phig    = 4.2466          epsrox  = 3.9
+epsrsub = 11.9            easub   = 4.05            ni0sub  = 1.1e+016        bg0sub  = 1.17
+nc0sub  = 2.86e+025       nsd     = 2e+026          ngate   = 0               nseg    = 5
+l       = 2.1e-008        xl      = 1e-009          lint    = -2e-009         dlc     = 0
+dlbin   = 0               hfin    = 3.2e-008        deltaw  = 0               deltawcv= 0
+sdterm  = 0               epsrsp  = 3.9             nfin    = 1
+toxg    = 1.80e-009
************************************************************
*                            dc                            *
************************************************************
+cit     = 0               cdsc    = 0.01            cdscd   = 0.01            dvt0    = 0.05
+dvt1    = 0.47            phin    = 0.05            eta0    = 0.07            dsub    = 0.35
+k1rsce  = 0               lpe0    = 0               dvtshift= 0               qmfactor= 2.5
+etaqm   = 0.54            qm0     = 0.001           pqm     = 0.66            u0      = 0.0303
+etamob  = 2               up      = 0               ua      = 0.55            eu      = 1.2
+ud      = 0               ucs     = 1               rdswmin = 0               rdsw    = 200
+wr      = 1               rswmin  = 0               rdwmin  = 0               rshs    = 0
+rshd    = 0               vsat    = 70000           deltavsat= 0.2             ksativ  = 2
+mexp    = 4               ptwg    = 30              pclm    = 0.05            pclmg   = 0
+pdibl1  = 0               pdibl2  = 0.002           drout   = 1               pvag    = 0
+fpitch  = 2.7e-008        rth0    = 0.225           cth0    = 1.243e-006      wth0    = 2.6e-007
+lcdscd  = 5e-005          lcdscdr = 5e-005          lrdsw   = 0.2             lvsat   = 0
************************************************************
*                         leakage                          *
************************************************************
+aigc    = 0.014           bigc    = 0.005           cigc    = 0.25            dlcigs  = 1e-009
+dlcigd  = 1e-009          aigs    = 0.0115          aigd    = 0.0115          bigs    = 0.00332
+bigd    = 0.00332         cigs    = 0.35            cigd    = 0.35            poxedge = 1.1
+agidl   = 1e-012          agisl   = 1e-012          bgidl   = 10000000        bgisl   = 10000000
+egidl   = 0.35            egisl   = 0.35
************************************************************
*                            rf                            *
************************************************************
************************************************************
*                         junction                         *
************************************************************
************************************************************
*                       capacitance                        *
************************************************************
+cfs     = 0               cfd     = 0               cgso    = 1.6e-010        cgdo    = 1.6e-010
+cgsl    = 0               cgdl    = 0               ckappas = 0.6             ckappad = 0.6
+cgbo    = 0               cgbl    = 0
************************************************************
*                       temperature                        *
************************************************************
+tbgasub = 0.000473        tbgbsub = 636             kt1     = 0               kt1l    = 0
+ute     = -0.7            utl     = 0               ua1     = 0.001032        ud1     = 0
+ucste   = -0.004775       at      = 0.001           ptwgt   = 0.004           tmexp   = 0
+prt     = 0               tgidl   = -0.007          igt     = 2.5
************************************************************
*                          noise                           *
************************************************************
**)
.control
pre_osdi /home/vsduser/Desktop/asap_7nm_Xschem/bsimcmg.osdi
.endc

**** end user architecture code
.end
```
## DC and transient  Graphs for 0.8V VDD 

<img width="940" height="559" alt="image" src="https://github.com/user-attachments/assets/ce4bd9b9-b318-4cee-92e9-678bf33043af" />


<img width="940" height="561" alt="image" src="https://github.com/user-attachments/assets/73e60720-06b3-4b2b-b728-70c3c07d0cc7" />


<img width="940" height="564" alt="image" src="https://github.com/user-attachments/assets/8a82279a-e0cb-459d-a6e1-356db4a2991f" />


<img width="940" height="564" alt="image" src="https://github.com/user-attachments/assets/45a25747-0dfb-4c9c-b182-c7804210d7b2" />


<img width="940" height="561" alt="image" src="https://github.com/user-attachments/assets/7a53c514-4925-45b6-aa14-1d348939cf5f" />


<img width="940" height="562" alt="image" src="https://github.com/user-attachments/assets/cac74586-5f9f-4dc2-9efc-6ddfa4ca4d3e" />


<img width="1919" height="1103" alt="vrefat8trans" src="https://github.com/user-attachments/assets/c12ec6c0-d917-40c4-9bc2-d2f8ac57a237" />

## DC and transient Graphs for 0.9V VDD 

<img width="940" height="597" alt="image" src="https://github.com/user-attachments/assets/d7aa4fcf-a972-4d6b-9066-9b5c1a25b4b3" />


<img width="940" height="577" alt="image" src="https://github.com/user-attachments/assets/fcd5462d-b4a1-4007-92e8-89971f314846" />


<img width="940" height="561" alt="image" src="https://github.com/user-attachments/assets/43b7b28f-16bb-4978-9c86-7053e9e87b50" />


<img width="940" height="596" alt="image" src="https://github.com/user-attachments/assets/9cea2e83-ce47-4315-a40d-eda977517473" />


<img width="940" height="593" alt="image" src="https://github.com/user-attachments/assets/627e5e24-4a7b-4a87-88a2-948076909583" />


<img width="940" height="590" alt="image" src="https://github.com/user-attachments/assets/27887f52-5f1e-4b9c-8b46-18f7380a3abd" />


<img width="1894" height="1143" alt="09at27startuptime" src="https://github.com/user-attachments/assets/879fbad6-62c9-4a64-bc56-13a2b9673e7b" />

## DC and transient Graphs for 1V VDD 

<img width="940" height="561" alt="image" src="https://github.com/user-attachments/assets/2fa9e43d-637d-4496-9200-fba4e8b1fc4c" />

<img width="940" height="561" alt="image" src="https://github.com/user-attachments/assets/73d48214-6613-4b57-aaf4-be8e6671caf5" />

<img width="940" height="565" alt="image" src="https://github.com/user-attachments/assets/c6632095-0144-4642-b933-f15ade21da50" />

<img width="940" height="560" alt="image" src="https://github.com/user-attachments/assets/42df18a9-98c9-404f-a9e3-e9da043838e1" />

<img width="940" height="565" alt="image" src="https://github.com/user-attachments/assets/75bc97ef-fa8b-4d39-a95a-6b01abe67dcc" />

<img width="940" height="559" alt="image" src="https://github.com/user-attachments/assets/fe61fdd5-d12a-48f1-b732-a4d575690270" />

Transient analysis for 27°C

<img width="1918" height="1147" alt="1vtrans27" src="https://github.com/user-attachments/assets/af42a47b-f8ed-4b88-a791-ef02bf391dcb" />

Transient analysis for -40°C

<img width="1919" height="1144" alt="1vtrans40" src="https://github.com/user-attachments/assets/ee37e1cd-4111-4faa-9270-b28d8d2d2917" />

Transient analysis for 125°C

<img width="1919" height="1141" alt="1vtrans125" src="https://github.com/user-attachments/assets/37b8c27d-cbac-4745-af0e-86053eea8623" />



We have analyzed the startup time, refernce voltage and Line Regression and created a characterization table

## Characterization table

<img width="880" height="185" alt="image" src="https://github.com/user-attachments/assets/60c3e4fe-cf13-4375-ad20-ab60c53e12e8" />

## Conclusion

In this workshop, we learned how to analyze the performance parameters of 7nm Fin_FET. We used ASAP 7nm Fin_FET pdk for the simulations. We also learnt how to design a Bandgap Reference Circuit using the 7nm pfet and nfet in Xschem. We learnt how to generate a spice file for a circuit and how to analyze the spice file using ngspice. We also analyzed the startup time, reference voltage of the BAndgap REference Circuit.

# Acknowledgements and References

Kunal Ghosh, VSD Corp Pvt. Ltd. (Co-Founder) [LinkedIn](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)

Soundarya Madhuri Royyuru, [GitHub](https://github.com/RSMadhuri66)

GitHub, [avsdbgr_7nm](https://github.com/RSMadhuri66/avsdbgr_7nm?tab=readme-ov-file)

GitHub, [Bandgap-Reference-Circuit-with-SCMB-with-ASAP-7nm-PDK-](https://github.com/RSMadhuri66/Bandgap-Reference-Circuit-with-SCMB-with-ASAP-7nm-PDK-)
