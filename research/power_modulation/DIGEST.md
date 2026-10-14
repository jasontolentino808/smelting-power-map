# A Cell Simulator for optimizing the operation practices and the process

Source: `modeling_power_modulation/A Cell Simulator for optimizing the operation practices and the process.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

Travaux 44, Proceedings of 33rd International ICSOBA Conference, Dubai, United Arab Emirates, 29 November - 1 December 2015


        A Cell Simulator for optimizing the operation practices and the process
                                             control

                                      Jacques Antille1, René von Kaenel2, Louis Bugnion3
                                                      1.  Senior consultant, KAN-NAK Ltd.
                                                             2.  CEO, KAN-NAK Ltd.
                                                       3.   Project manager, KAN-NAK Ltd.
                                    Corresponding author: rene.vonkaenel@kannak.ch

           Abstract

          The Hall-Heroult process can be described by a wide range of complex chemical and physical
           phenomena. Using MatLab-Simulink software, a mathematical model has been developed to solve the
           dynamic status of an aluminium reduction cell. Simulink provides a very powerful graphical user interface
              for building sub-models as block diagrams. The cell simulator determines various process interactions.
          The key operating parameters such as alumina concentration, bath temperature, ledge thickness, cell
             voltage and many others are computed as a function of time. Raw materials and process variations effects
             are predicted. The model can be used for improving operating strategies, can be implemented in the
            process control or can help at understanding the effect of various actions on the cell. Applications such as
             the variation of ledge thickness, specific energy, bath level, AlF3 emissions are presented.

          Keywords: Cell simulator; process control; process optimization; energy saving.

              1.      Introduction

            Despite the fact that the Hall-Heroult process is based on a simple theory, there is a wide range of
           complex physical-chemical phenomena that must be taken into consideration when modeling the overall
             process. Many of these are dynamic, either periodic or transient and the dynamics of the process has
            important implications on process efficiency. Several dynamic cell simulators have been published with
              different objectives from increasing the understanding of the process to development and analysis of
            process control [1 – 6]. These simulators are using in-house programming. Contrary to this, the simulator
            described in this paper is based on MatLab-Simulink software, which is an open modelling system.

          The objective of this work is to develop a mathematical model of a Hall-Heroult reduction cell as well as
            develop a better understanding of the reduction process itself. The effects of variations in operational
            parameters on the dynamical behavior of an aluminum reduction cell are predicted. Various couplings
              exist between  the complex physiochemical phenomena. Compromises have  to be made between
             simplicity and accuracy of the model. The most relevant aspects of the Hall-Heroult process are
             preserved. The cell simulator is structured in three main modules:

               •   Material balance model,
               •   Cell voltage model,
               •  Thermal balance model.

          The three modules are then combined into one overall cell model which can be used for improving control
              strategies, cell operation as well as developing a predictive tool for the process itself. The model is not
             limited in the period of prediction. Operations such as anode change, tapping, alumina and aluminum
             fluoride feeding can be defined easily by the user. A period of 26 days can be simulated in less than 15
            minutes. The simulation of one hour operation needs about 1 second computer time. The model can
             therefore be used online to help in process control strategies.




                                                                               Travaux 44 Page No. 635

### PDF page 12

Travaux 44, Proceedings of 33rd International ICSOBA Conference, Dubai, United Arab Emirates, 29 November - 1 December 2015





             Figure 2. 24-hour plot of the beam displacements, feeding rate in % of nominal feed, cell voltage,
                           bath and metal temperature and ledge at metal and bath level..





                  Figure 3. 24-hour plot of the bath resistance, current efficiency and energy consumption.

           There are many more plots analyzing the energy balance, the bath chemistry and any desired parameter as
             function of time. Predictions were validated with measurements.

              8.     Conclusions

       A sophisticated cell simulator has been developed using MATLAB-SIMULINK software. The software is
              fully open and can be easily modified to implement each plant alumina and aluminum fluoride feeding
              strategies or other specificities. It highlights how heat losses, current efficiency and other key operating
            parameters fluctuate during the day. It can be used to optimize the process.





                                                                               Travaux 44 Page No. 646



---

# AL54 - Model Predictive Control of Maintaining the Superheat of an Aluminium Smelting Cell during Power Modulation

Source: `modeling_power_modulation/AL54 - Model Predictive Control of Maintaining the Superheat of an Aluminium Smelting Cell during Power Modulation.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

 TRAVAUX 52, Proceedings of the 41st International ICSOBA Conference, Dubai, 5 - 9 November 2023


 AL54 - Model Predictive Control of Maintaining the Superheat of an
       Aluminium Smelting Cell during Power Modulation

    Luning Ma1, Choon-Jie Wong2, Jie Bao3, Maria Skyllas-Kazacos4, Barry Welch5,
                  Nadia Ahli6, Amal Aljasmi7 and Mohamed Mahmoud8
                                            1. PhD student
                                   2. Postdoctoral Research fellow
                                             3. Professor
                                             4. Professor
                                             5. Professor
   School of Chemical Engineering, The University of New South Wales, Sydney, Australia
                            6. Manager, Technology Transfer Contracts
                             7. Area Engineer, Reduction Engineering
                                  8. Manager, Centre of Excellence
                 Emirates Global Aluminium (EGA), United Arab Emirates
                       Corresponding author: j.bao@unsw.edu.au

Abstract

Superheat is a crucial indicator of the thermal balance in the aluminium smelting process.
Maintaining the superheat within a narrow range ensures the productivity and energy efficiency.
Large fluctuations in superheat can result in undesirable effects such as increased back reactions,
sludge formation and reduced current efficiency. Furthermore, during power modulation, the
variable power input will affect cell thermal balance and increase the difficulty of cell operations.
To reduce the variation of the superheat during power modulation, this paper develops a Model
Predictive Control (MPC) approach to maintaining the superheat by manipulating the alumina
feed and anode-cathode distance based on real-time temperature measurements or estimation.
Through mathematical modelling and simulations, the mass and heat balance inside the cell is
regulated during power modulation. This method provides an insight into superheat management
for idle operation and power modulation.

Keywords: Aluminium electrolysis, Process control, Model predictive control.

1.    Introduction

Controlling the aluminium smelting process is challenging due to its nonlinear characteristics,
and coupled mass and thermal balance. Research in the literature mainly focuses on either the
control of alumina concentration or the bath temperature and excess AlF3 concentration [1-4].
Drengstig [2] mentioned the basic framework to control the bath temperature and excess AlF3,
and Kolås et. al. [3] adopted a PI control to control the bath temperature and excess AlF3 by
adjusting AlF3 feed and ACD, whereas Shi [4] improved the alumina feeding control and used a
state observer to estimate the alumina concentration. However, to control the process effectively,
both mass balance and thermal balance should be managed simultaneously due to their coupling
nature.

The superheat of an aluminium smelting cell is an important variable which can reflect the cell
operation status. It is given by the difference between the bath temperature and the liquidus
temperature. Controlling the superheat within a certain range is helpful for maintaining stable
process conditions. If the superheat increases by 10 oC, the current efficiency will decrease by
1.2–1.5 % [5, 6]. Superheat is commonly regarded as the thermal driving force in the cell. As it
provides the energy to dissolve alumina feed in the bath, a low superheat makes it difficult for
alumina to dissolve [7]. On the other hand, increasing the superheat can lead to ledge melting,


                                     1787

### PDF page 11

 TRAVAUX 52, Proceedings of the 41st International ICSOBA Conference, Dubai, 5 - 9 November 2023



5.    Conclusions

Superheat plays a  critical  role  in the aluminium smelting process as  it impacts energy
consumption and cell lifespan. Maintaining stable superheat is vital for efficient operation. In this
paper, the MPC method is employed to maintain a stable superheat by manipulating the alumina
feed and ACD, driving the process variables of alumina concentration and bath temperature
towards their reference values. By optimizing these variables while considering constraints with
MPC, the paper demonstrates stable superheat performance during power modulation. This
research lays a foundation for enhancing process performance during power modulation. In future
research studies, it would be beneficial to improve the accuracy of the model and explore more
advanced control strategies to overcome limitations and further advance the application of MPC.

6.    References

1.    Peter M. Entner. Control of bath temperature, Essential Readings in Light Metals: Volume
     2 Aluminum Reduction Technology, 2016, 808-811, from Light Metals 1995, 227-232.
2.   Tormod Drengstig, On process model representation and AIF3 dynamics of aluminium
       electrolysis cells, Dr Ing Thesis, Department of Engineering Cybernetics, Norwegian
      University of Science and Technology (NTNU), Trondheim, Norway, August 1997.
3.     S, Kolås, and T. Støre, Bath temperature and AlF3 control of an aluminium electrolysis cell.
      Control Engineering Practice 17 9 2009, 1035-1043.
4.    Jing Shi, Advanced alumina feeding control of aluminium smelting cell, PhD Thesis,
    UNSW, Sydney, 2021.
5.    Shuiping Zeng, Shasha Wang and Yaxing Qu, Control of temperature and aluminum
      fluoride concentration based on model prediction in aluminum electrolysis, Advances in
      materials science and engineering 2014, https://doi.org/10.1155/2014/181905.
6.    Y. X. Liu and Jie Li, Modern aluminum electrolysis, Metallurgy Industry Publication,
      Beijing, China 90, 2008.
7.    Yuchen Yao, Process monitoring, modelling and fault diagnosis in aluminium reduction
       cells, PhD Thesis, UNSW, Sydney, 2017.
8.   Tormod Drengstig, Dag Ljungquist and Bjarne A. Foss, On the AlF3 and temperature
      control of an aluminium electrolysis cell, Modelling, Identification and Control 1998, vol
      19, No 1, 31-59.
9.    Richard G. Haverkamp and Barry J. Welch, Modelling the dissolution of alumina powder
       in cryolite, Chemical Engineering and Processing: Process Intensification 37 2, 1998, 177-
      187.
10.  Marc Dupuis, Modeling power modulation, Light Metals 2002. 489-494.
11.   David Eisma and Pretesh Patel, Challenges in power modulation." Essential Readings in
      Light Metals: Volume 2 Aluminum Reduction Technology 2016, 683-688, original in Light
      Metals 2009, 327-332.
12.   Biedler Philip, Modeling of an aluminum reduction cell for the development of a state
      estimator, PhD Thesis, West Virginia University, 2003.
13.   Jing Shi, Advanced alumina feeding control of aluminium smelting cell, PhD Thesis,
    UNSW, Sydney, 2021.
14.   Barry J. Welch, Specific energy consumption and energy balance of aluminium reduction
        cell,  Presentation  at 8th  international congress "Non-ferrous Metals & Minerals",
      Krasnoyarsk, Russia, 2016.
15.   Choon-Jie Wong et al, Discretized thermal model of Hall-Héroult cells for monitoring and
       control, IFAC-Papers Online 54, 11 2021, 67-72.
16.   Yuchen Yao et al, Estimation of spatial alumina concentration in an aluminum reduction
       cell using a multilevel state observer, AIChE Journal 63 7, 2017, 2806-2818.
Fabio Soares, Limao Roberto and Castro Marcos, Bath temperature inference through soft sensors
      using neural networks, Light Metals 2010, 467-472.


                                     1797



---

# Alumina_Dissolution_and_Current_Efficiency_in_Hall_Herault

Source: `modeling_power_modulation/Alumina_Dissolution_and_Current_Efficiency_in_Hall_Herault.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

                                                                                     LightLight MetalsMetals 20092009 EditedEdited by:by: GeoffGeoff BearneBearne
                                                   TMSTMS (The(The Minerals,Minerals, MetalsMetals && MaterialsMaterials Society),Society), 20092009
     ALUMINA DISSOLUTION AND CURRENT EFFICIENCY IN HALL-HEROULT CELLS

                                       Bjørn Lillebuen1, Marvin Bugge1 and Helge Høie2
                                            1 Hydro Aluminium, P.O. Box 2560, NO-3908, Porsgrunn, Norway
                                            2 Hydro Aluminium Karmøy, NO-4265, Håvik, Norway

                              Keywords: Alumina, Current Efficiency (CE), Sodium, Dissolution


                         Abstract
                                                                      In this paper we will present some operational data, and discuss
The dissolution and distribution of alumina in cryolite melts can       correlations and links to the phenomena introduced above.
be described as a coupled heat and mass transport process, with
intermediate formation of solid cryolite. Current efficiency (CE)                      Alumina Dissolution
can be evaluated by means of the rate equations for the back
reaction between dissolved metal and carbon dioxide gas. Solid       1. Alumina Quality
cryolite may be formed close to the metal pad under certain
conditions in the cell. The bath superheat and the mass transfer     Alumina quality is often considered to be the main parameter for
coefficient   at  the  bath/metal  interface  will  be  important      alumina dissolution control. Modern sandy alumina has quality
parameters for the maximization of current efficiency. In some       variations that represent challenges for point feeding control, but
cells there is a clear correlation between current efficiency and the     more and more we have come to see that these variations may be
sodium content in the metal, indicating that mass transfer is the       less critical than the heat and mass transport conditions inside the
dominant factor. In other cells sodium levels can be quite low        cells. Successful implementation of point feeding has enabled
even at high current efficiency, which indicates that formation of      computer control of the alumina concentration in the bath, and
solid cryolite can play a significant role, making superheat the     made possible a dramatic reduction in anode effect frequency and
dominating factor.                                                      duration, in addition to the general performance improvement
                                                                  seen in new smelters. In order to improve from today’s situation, a
                       Introduction                                  detailed understanding and description of alumina dissolution is
                                                                         required.
1. Alumina Dissolution
                                                                              2. Dissolution of an Alumina Particle
When alumina is added to molten bath, it starts to dissolve. The
dissolution process is endothermic, so heat needs to be transported      For illustration, a simplistic calculation of the dissolution rate of
to the dissolution interface by a driving temperature gradient.      an alumina particle  is shown. The particle  is heated to bath
Since the bath temperature normally is just a few degrees above      temperature and dissolved, and Figure 1 gives an illustration of
the bath liquidus temperature, the alumina dissolution may lead to      temperature and concentration gradients in the bath boundary
local formation of solid cryolite.  This solid cryolite will then       layer (”film”) around the particle, and related to the bath phase
gradually melt as more heat is tranported to the interface.               diagram.

2. Aluminum Electrolysis

The electrolytic deposition of molten aluminum takes place with
sodium ions as charge carrier, and discharging of Al-containing
species at the metal/bath interface. This sets up a concentration
gradient with higher bath ratios at the interface than in the bulk of
the bath. Higher bath ratio means higher liquidus temperature, so
formation of cryolite may take place also at the cathodic interface
between metal and bath.

3. Current Efficiency and Sodium

The sodium levels in aluminum are determined by the bath ratio at
the cathodic interface according to the equilibrium reaction:
                                                                                   Figure 1. Particle Dissolution.
           Al + 3 NaF = AlF3 + 3 Na          (1)

From this same interface metal will dissolve and react with carbon     The following equations can be written for the dissolution rate,
dioxide by the so-called back reaction. The back reaction  is        ref. Asbjørnsen and Andersen (1):
assumed to be responsible for the largest part of the current
efficiency losses in modern cells. In addition to Al, metals like Na        M = k (c* - c)                           (2)
and Li will also dissolve and back react, and dissolved metals may
also react with impurities like phosphorous in the melt.                Q = h (T – T*)                          (3)


                                                 389



---

# ALUMINIUM FLUORIDE CONSUMPTION AND CONTROL IN SMELTING CELLS

Source: `modeling_power_modulation/ALUMINIUM FLUORIDE CONSUMPTION AND CONTROL IN SMELTING CELLS.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

                ALUMINIUM FLUORIDE CONSUMPTION AND
                  CONTROL IN SMELTING CELLS

     Invited lecture for presentation by Barry Welch at 6th Molten Slags, Fluxes and Salts
                                    Conference,
                             Stockholm, 12-16 June 2000
                                  Co-authored by
           M.M. Hyland, E.C. Patterson, F. Stevens-McFadden & B.J. Welch

                  High Temperature Materials and Processing Group
                         The University of Auckland
                          New Zealand


ABSTRACT
For optimum operation and performance of aluminium smelting cells, each technology has
an optimum aluminium fluoride concentration for the solvent electrolyte. The actual value
used  is influenced by the alumina dissolution and differs because of different alumina
feeding technologies.

The aluminium fluoride  is consumed within the cell and therefore, chemical analysis  is
performed as part of the process to determine the amount required for replenishment of the
consumption.   However  the  cell has a dynamic  energy  balance and  that causes
simultaneous  variations  in the  distribution  of  solid and  liquid  electrolyte components,
complicating the overall situation.  Ultimately,  it results in the chemical analysis varying.
Thus it becomes a major challenge to determine the amount of aluminium fluoride that needs
to be added to replenish the consumption, whilst maintaining the cell at close to its optimum
range.

In the first part of this paper, the consumption mechanisms are reviewed with respect to the
process variability.  In the second part the approach used to control the aluminium fluoride
concentration is reviewed, and the impact of the energy dynamics is also analysed.


PART I: Consumption

INTRODUCTION to BATH CHEMISTRY and CONSUMPTION

                                                 3 −It is well established that the cryolitic anion (Al F6   ) arising on melting cryolite (Na3AlF6) is
essential for dissolving alumina for the electrolytic production of aluminium.  In practice the
cryolite also dissociates on melting to give an equilibrium concentration of the cryolitic
species, sodium fluoride and sodium tetrafluoroaluminate according to equation 1:

Na3AlF6     2NaF + NaAlF4                                                                   - (1)

Since this melt also dissolves metal, leading to a lowering in current efficiency, it has been
shown that  it  is desirable to not only lower  its melting point, but also to increase the
concentration of the sodium tetrafluoroaluminate.  Essentially the dissolving reaction on
adding aluminium fluoride can be given by the following reaction:

Na3AlF6 + 2AlF3 ¡ 3NaAlF4                                                                     - (2)

This also lowers the melting point. The other additive commonly used is calcium fluoride.  Its
presence has  little impact on the concentration of the dissolving cryolitic anions, whilst
lowering the melting point significantly.




                                                                   1



---

# Electrothermic Industrial Load Model with a Dynamic Iterative Mechanism

Source: `modeling_power_modulation/Electrothermic Industrial Load Model with a Dynamic Iterative Mechanism.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

                                                        Energy Reports 16 (2026) 109536

                                                 Contents lists available at ScienceDirect
                              Energy Reports


                                            journal homepage: www.elsevier.com/locate/egyr

Research paper
Electrothermic Industrial Load Model with a Dynamic Iterative Mechanism
for Equivalent Thermal Parameters and Its Application in
Demand Response
He Huang a, Shu Zhang a,*   , Xianyong Xiao a, Zixuan Zheng a, Yongjun Zhou a,b, Qinghua Zhao c
a College of Electrical Engineering, Sichuan University, Sichuan, China
b Economic and Technology Research Institute, State Grid Tibet Electric Power Company, Lhasa, China
c Electric Power Research Institute, State Grid Heilongjiang Electric Power Company, Harbin, China


A R T I C L E  I N F O                  A B S T R A C T

Keywords:                                    As a typical electrothermic industrial load (EIL), the adjustable potential of aluminum smelter load has not been
Electrothermic industrial load                           fully utilized. The reason is the lack of a precise model to describe the conversion between electricity and thermal
Equivalent thermal parameters model                 energy, and the ignorance of energy consumption related to yield. To address these issues, this paper proposes a
Power adjustment characteristics                                                  price-based demand response (DR) strategy for EIL using an equivalent thermal parameters (ETP) model thatTemperature-power iteration                                                  considers electro-thermal coupling characteristics and energy consumption changes in the electrolytic process.
                                                             First, a dynamic thermal balance equation is employed to mathematically depict the energy conversion from
                                                         electricity to thermal in reduction cells. Second, the ETP model for EIL is derived from the dynamic thermal
                                               balance equation based on Taylor expansion, which accurately characterizes the time‑variant relationship be­
                                           tween power regulation and electrolysis temperature changes. Finally, an iterative temperature‑power mecha­
                                           nism is embedded into the DR optimization algorithm under TOU tariff to cope with the significant variation of
                                                 equivalent thermal resistance during regulation. The simulation results demonstrate that the proposed ETP
                                          model combined with the iterative algorithm can shift more peak load and reduce more electricity costs for
                                         aluminum smelters, especially during an electrolytic aluminum production cycle.


1. Introduction                                                          reserve  capacity  for power system (Paulus and  Borggrefe, 2011;
                                                                           Molina-Garci´a et al., 2011). A smelter plant with a twelve-pulse rectifier
   The power system is facing increasing supply pressure from high    system and variable direct current (DC) load has been modelled in
penetration of intermediate renewable energy resource especially in    PSCAD/ EMTDC based on electrical topology (Agalgaonkar et al., 2009).
extreme weather (Liu et al., 2025; Tan et al., 2025; Choubineh et al.,     Literatures (Jiang et al., 2013) and (Jiang et al., 2014) provide the
2025; Huang et al., 2025). To mitigate this supply pressure, the demand    mathematical representation of power consumption by a typical modern
side is regarded as an important resource to improve the power grid     EIL with a 6-branch-parallel rectifier system, and point out that the DC
adjustment ability. Among various types energy-intensive loads in de­     voltage can be controlled by self-saturable reactors. However, the
mand side, the electrothermic industrial load (EIL), such as aluminum     electrolysis of aluminum is a complex production process involving
smelter, is particularly ideal demand response (DR) resource due to large      electricity and thermodynamics. None of the above EIL models consider
capacity, which is up to hundreds or thousands megawatt class (Zhang     the electro-thermal coupling characteristics in electrolytic aluminum
et al., 2018, 2019; Sagar and Kumar, 2024), and advanced control sys­     production, which indirectly affects the power consumption by EIL and
tem, which is easy to integrate various control modules (Li et al., 2023,     determines the feasibility of the consequent interaction strategy be­
2024).                                                          tween EIL and power system. Literature (Liao et al., 2018) proposes a
   In the early stage, exploratory statistics are analyzed to model EIL by     simplified linear algebraic equation by the law of conservation of energy
engineer experience and data fitting, and the conclusion is that the     to describe the relationship between the power and reduction cell
allowed power demand variation of EIL is around ±1.5% to provide     temperature. The  feasibility of EIL participating in power system


 * Corresponding author.
    E-mail address: ZS20061621@163.com (S. Zhang).
https://doi.org/10.1016/j.egyr.2026.109536
Received 21 December 2025; Received in revised form 20 May 2026; Accepted 5 July 2026
Available online 17 July 2026
2352-4847/© 2026 The Authors. Published by Elsevier Ltd. This is an open access article under the CC BY-NC-ND license ( http://creativecommons.org/licenses/by-
nc-nd/4.0/).



---

# MODELLING THE MASS AND ENERGY BALANCE OF ALUMINUM REDUCTION CELLS

Source: `modeling_power_modulation/MODELLING THE MASS AND ENERGY BALANCE OF ALUMINUM REDUCTION CELLS.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 6

ABSTRACT

      The primary aluminium industry is continuously aiming to reduce the energy

consumption of the smelting process and the harmful smelter emission rates. Both

aspects can be optimised with a comprehensive understanding of the aluminium

electrolysis cell mass and energy balance. Traditionally, the existing cell heat balance

models present very limited material balance. They rely on curve fitted voltage data,

obtained decades ago when the cell technology and operation were totally different from

current cells.

      The electrolysis cell mass and energy balance model proposed in this thesis is

entirely based on the first law of thermodynamics. This approach is valid for any type of

cell, for both steady state and transient calculations. A new extended cell control

volume  is adopted, allowing for a more complete material balance. The model  is

composed of the main algorithm that uses input information obtained from subsidiary

3D sub-models. A new software tool was developed, which could be used on site by

process engineers to improve the smelting process.

       Important differences between the classical models results and the new mass and

energy balance model were observed. The impact of each mass stream on the cell

energy balance was studied and quantified.

       In transient simulations, a moving grid Finite Volume algorithm was specially

developed to track the ledge movement. The dynamic model was applied to study the

impact of mass and energy imbalances on the Hall-Héroult cell behaviour such as:

intermittent aluminium fluoride additions and several power modulation functions. In

the model,  the voltage compensation approach  to  mitigate  the  effects of power

modulation perturbations was tested, presenting excellent effectiveness. In addition, the

shell forced air cooling was also simulated, showing negligible contribution to the

improvement of the power modulation window.

      The dynamic model results were compared with measurements obtained from

large scale industrial cells. In general, the modelling results presented good correlation

with measurements. The effect of irregular aluminium fluoride mass addition on the cell

behaviour was studied, as well as the electrical energy input fluctuations. The dynamic

model was also applied to investigate the cell lining failure related to transient energy

imbalances.

                                                                                                         I

### PDF page 224

                                                          7 - Conclusions



     7 CONCLUSIONS


      The present thesis demonstrates that the modelling of the cell mass and energy

balance is an important tool for understanding and improving the aluminium reduction

cell technology and industrial operation practices. During the research,  it has been

realised that the industry work practices and control systems are based on many

misconceptions and poor understanding of the electrolysis process, including material

and energy balance, that lead to cell failures and efficiency losses.

    A computational application entirely based on the laws of thermodynamics was

developed and used to study the electrolysis cell energy balance behaviour. With the

help of the computational model, many findings on the cell behaviour were achieved.

Specifically, the findings are divided into averaged steady  state aspects and  cell

dynamic aspects.

      7.1  Averaged Steady State Model


        7.1.1  Complete Mass and Energy Balance versus Traditional Approach

     Many of traditional cell energy balance models underestimate the heat losses due

to material balance because the contributions of many materials are ignored. As a result,

heat dissipation to the potroom may be overestimated. Such a simplified approach can

produce wrong cell operating targets and ledge thickness predictions, also resulting in

poor cell insulation projects. In this thesis, the mass and energy balance model takes

into account all material inputs and outputs of the cell. Each contribution has been

quantified and the error present in traditional models has been evaluated.

        7.1.2  Heat Losses Related to the Gas Collection

       In the context of the aluminium reduction cell, the cell heat lost by the duct

gases represents a very important share of the cell energy consumption. Using the

modelling methodology presented in this thesis, a study of the duct flow rate influence

on cell heat balance was performed. In general, it was found that if the cell duct flow

rate is reduced, the cell heat loss is also reduced, opening the possibility for important

amounts of energy saving. However, as a drawback,  the  cell emissions capture



                                                                    194



---

# Multilevel Coordinated Strategy for Electrolytic Aluminum System

Source: `modeling_power_modulation/Multilevel Coordinated Strategy for Electrolytic Aluminum System.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

IET Smart Grid





  ORIGINAL RESEARCH  OPEN ACCESS


Multilevel Coordinated Strategy for Electrolytic-
Aluminium System to Enhance Renewable Energy
Consumption

Huawei Deng1,2      | Qunhai Huo1,2      | Lixin Wu1  | Libo Han1  | Jingyuan Yin1,2      | Tongzhen Wei1,2

1Institute of Electrical Engineering, Chinese Academy of Sciences, Beijing, China  | 2University of Chinese Academy of Sciences, Beijing, China


Correspondence: Qunhai Huo (huoqunhai@mail.iee.ac.cn)  | Lixin Wu (wulixin@mail.iee.ac.cn)

Received: 15 February 2026  | Revised: 21 May 2026  | Accepted: 1 June 2026

Keywords: demand side management | energy consumption | energy demand management | load dispatching


 ABSTRACT

  Because of the spatial mismatch between renewable energy sources and load centres, China continues to experience substantial
  curtailment of wind and solar power. To mitigate this issue, several regions have adopted electrolytic aluminium loads to absorb
   local renewable energy. Nevertheless, the absence of effective scheduling strategies for the electrolytic aluminium system has
  posed increasing challenges to ensuring its safe and cost‐efficient operation. This paper proposes a multilevel coordinated
   strategy for the electrolytic aluminium system, which accounts for the flexible interaction of source, grid, load and storage. To
   quantitatively characterise the coupling relationship between the electrical power and thermal dynamics of the electrolytic
  aluminium load, an electric–thermal coupling model is established. Based on this model, a control and scheduling framework
   for the electrolytic aluminium system is developed. Furthermore, a long short‐term memory (LSTM)‐extreme gradient boosting
  (XGBoost) hybrid probabilistic interval prediction method is proposed to enhance the forecasting accuracy of wind and solar
  power generation. Building on these foundations, a multilevel coordinated optimisation model is constructed that incorporates
  multiple influencing factors. The proposed strategy aims to maximise renewable energy utilisation while achieving dual ob­
   jectives in terms of both economic performance and carbon reduction. Case studies conducted on an actual electrolytic
  aluminium system located in Inner Mongolia province confirm the effectiveness of the proposed approach.



1   |  Introduction                                   70% of this demand supplied by thermal power plants. Conse­
                                                                   quently, the sector faces considerable pressure to reduce carbon
As of April 2025, China's cumulative installed capacity of wind
                                                                  emissions. Integrating wind and solar power with the electro­
and solar power reached approximately 1482 GW, surpassing
                                                                                lytic aluminium industry provides a promising pathway to
the installed capacity of thermal power and continuing to grow
                                                                   mitigate these challenges. As a temperature‐sensitive industrialyear‐on‐year [1]. With the rapid expansion of renewable energy,
                                                                       load, electrolytic aluminium load can function as an adjustablewind‐solar power curtailment has re‐emerged as a  critical
operational challenge. In 2024, the total curtailed wind and solar    resource, with a regulation range from −25% to +10% of its
power amounted to 67,350 GWh [2]. The electrolytic aluminium    rated power and a response capability on the order of seconds.
industry, as one of the largest industrial electricity consumers,    This flexibility underscores its critical role in enhancing system
consumed 594,100 GWh of electricity in 2024 [3], with nearly     adaptability to renewable energy integration.





This is an open access article under the terms of the Creative Commons Attribution‐NonCommercial‐NoDerivs License, which permits use and distribution in any me­
dium, provided the original work is properly cited, the use is non‐commercial and no modifications or adaptations are made.

© 2026 The Author(s). IET Smart Grid published by John Wiley & Sons Ltd on behalf of The Institution of Engineering and Technology.


IET Smart Grid, 2026; 9:e70096                                                                                     1 of 19
https://doi.org/10.1049/stg2.70096



---

# Optimisation of power modulation for Hall-H´eroult cells

Source: `modeling_power_modulation/Optimisation of power modulation for Hall-H´eroult cells.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 13

C.-J. Wong et al.                                                                                                                        Journal of Energy Storage 178 (2026) 123594





Fig. 17. Comparison of (a) cell profits for nominal operation and power modulation (normal and slow response cases) in a 48-h period and (b) net profit gained for
power modulation vs nominal operation.

of change. Whilst the constraints are held, there is reduced opportunity
for economic benefit due to slower transitions in power consumption,
challenging the ability to respond to changes in the power prices. This
demonstrates the impact of physical limitations on the potential smelter
economic benefit, i.e., permitting sharper changes in power consump­
tion allows for longer operation near the constraint boundaries where
economic benefit is most significant.
    Fig. 16. Optimised line current and ACD profiles with evolution of
ledge thickness with time in response to time-of-use tariff between
±0.36 cm/h for ACD and between ±36 kA/h for line current.
   The net revenue of operating a cell is calculated using the cost
function defined in Eq. 24, which accounts for raw materials and elec­
tricity costs and the market value of aluminium produced, while
excluding capital, maintenance, labour, and storage costs. Fig. 17(a)
shows the net profit over the 48-h period of both line current rate of
change constraints (±360 kA/h and ± 36 kA/h), relative to nominal
operation. The corresponding gain in net profit is illustrated in Fig. 17
(b), demonstrating a consistent improvement in profitability under
power modulation, with higher permissible rate of change in current
yielding greater economic benefit. This reflects the ability of power      Fig. 18. NSW Australia power spot price profile starting at midnight for 18th to
modulation to flexibly adjust the aluminium production rate in response     19th of August 2021.
to electricity prices. Profitability can be further enhanced if the smelter
participates in demand response schemes that provide financial in­                                                                        or equal to 15 cm) and constraints on the line current and ACD rates ofcentives for load flexibility.                                                                 change (bounds of ±360 kA/h and ± 0.36 cm/h respectively). Using the
                                                                     feedback-update optimisation, power modulation was optimised on a
                                                                monthly frequency of 48-h spot price profiles from August 2021 to4.3. Scenario III: power spot price profile
                                                                  January 2022, producing the overall cell profits for these periods and
                                                              compared with the profits under nominal operation of 425 kA line   As an extension to Scenario II (time-of-use tariff studies), optimisa­
                                                                          current and an average ACD of 2.8 cm. A sample spot price profile fortions were performed under consideration of NSW Australia spot market
                                                                  August 2021 is given in Fig. 18, showing the typical spot price fluctu­prices, permitting the cell power load to respond freely to maximise cell
                                                                            ations observed in NSW.profits in a 48-h period. Typically, the aluminium smelting industry
                                                                The net profit per cell over the 48-h period is calculated using Eq. 24relies upon agreements with the grid such that power prices are
                                                                                for several 48-h periods chosen for the large fluctuations observed inconsistent and manufacture remains economically viable for constant
                                                                         spot pricing. As before, the capital, maintenance, labour, and storagesmelter power loads. Whilst these studies represent an extreme power
                                                                               costs are not included. Fig. 19(a) shows the net profit of cells undergoingmodulation scenario, they provide insight into efficacy of power mod­
                                                             power modulation relative to nominal operation, and Fig. 19(b) dem­ulation for economic benefit and reduction of costs associated with spot
                                                                            onstrates consistent improvements across all months with power mod­price pricing scheme. Evaluation of such pricing schemes yield valuable
                                                                               ulation, averaging an improvement of A$1232.insights, particularly when considering the uncertain future of power
pricing for aluminium smelters as the present agreements come to an
                                                                           5. Conclusions and future workend.
   Optimisation was performed considering a 48-h window subject to
                                                                               In this paper, the operability and economic benefits of Hall-H´eroultthe previous constraints detailed for ledge thickness (minimum ledge
                                                                                       cells under power modulation was studied as an optimisation problemthickness greater than or equal to 2 cm, average ledge thickness less than

                                                                        13



---

# ParadigmShiftInIndicationOfStableCellDuringPowerModulation

Source: `modeling_power_modulation/ParadigmShiftInIndicationOfStableCellDuringPowerModulation.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

Travaux 47, Proceedings of the 36th International ICSOBA Conference, Belem, Brazil, 29 October - 1 November, 2018



          Paradigm Shift in the Indication of a Stable Cell during Power
                                 Modulation

                                  Roman Düssel
                                            Reduction Manager
                         TRIMET Aluminium SE, Essen, Germany
                                        Roman.Duessel@trimet.de

          Abstract

      A megatrend of the next decades is the energy transition from conventional power to renewable.
          Adapting the aluminium smelting process to a flexible power supply needs the rethinking of a
         number of aspects  in the smelting process. Manipulating thermal and magnetic impacts
           associated with amperage changes are just a few of these aspects.

         The core element of our Virtual Battery is our newly developed control system. Conventional
           pot control systems are designed for conventional operations and static process targets. This
         becomes obsolete or even contradictory when operating with power modulation. Hence we need
           a different approach.

         The approach that is outlined here is divided into three areas. The first step is to reduce the
          energy input as far as possible and to compensate in a subsequent step the heat loss by heat
           exchangers. Each cell is subject to thermal and process engineering limits, which were intended
            for the cell at TRIMET Essen. If the minimum cell resistance and the min/max limits of the heat
            losses are well known, the regulation of the heat balance can be done by changing the
            resistance. According to Ohm’s law the resistance can be adjusted to its minimum inversely
           proportionally to the current. After reaching the resistance minimum, the heat loss through the
           heat exchanger is increased in proportion to further current increases. Finally control systems of
          an existing process control must be adjusted so that it does not counteract the energy flexibility,
           but promote it. The limits and values, such as temperatures and their deviations, of operating a
             cell have to be modified and the meaning of a stable cell rethought.

         Keywords: Aluminium  reduction  cell  process  control,  virtual  battery,  energy demand
          management, renewable energy, real-time heat balance control, energy counter.

            1.  History of Power Modulation

         The idea of current modulation using aluminum electrolysis cells is not new; as early as in the
           1990s, experiments were carried out in electrolysis cells in Brazil [1, 2]. Load management was
            also already an issue in 1974 in the electrolysis in Essen. Alusuisse engineers [3, 4] made
           various calculations for power reduction. Their ideas, however, mainly involved turning off pots
            rather than modulating them with the help of amperage. The innovation of load management
         nowadays is that over a certain period of time production volume and thus performance are kept
            constant. The modulation takes place for only a short time and above all with a faster change.
          This development was accelerated by the addition of renewable energies to the grid and
            therefore changed the time of the generation of electricity tremendously. Figure 1 shows the
           production and consumption profile predicted for the year 2050, showing the deficit in red and
           the surplus in green.





                                               851

### PDF page 6

Travaux 47, Proceedings of the 36th International ICSOBA Conference, Belem, Brazil, 29 October - 1 November, 2018





                              Figure 4. Relation of cover and side ledge loss.

         At the start of the modulation during amperage increase to 180 kA, the liquid electrolyte
           quantity increased by 900 kg on average, while the excess AlF3 decreased from 12.6 to 11.3 %.
         The mass fraction of AlF3 in the lower cover material is approximately 15 – 19 % [14]. The side
           ledge is pure cryolite or some cases it may have very low excess AlF3 [13]. Assuming that the
            side ledge has a surplus of 3 % excess AlF3, the distribution of molten side ledge to molten
           cover is calculated to be nine to one (see Figure 4). The amount of heat needed to melt the side
           ledge and raise the temperature in the cell is given in Table 3Table 3. Thermal reactions of a
         170 kA electrolytic pot. The table was supplemented with the ratio of the heat distribution,
          which results from the measured values (Figure 2), and a heat addition of 212 kWh.  It is
            interesting that in all cells after a short time a temperature plateau is reached, which shows that a
        new equilibrium has set in. Previous studies [15], [16] have shown that equilibrium without heat
          exchangers occurs much later. It can be concluded that the reason for the rapid change is the
          massive cooling reaction by the heat exchangers. With an amperage increase of 18 kA a new
           operating condition can be achieved after less than 4 h. The significantly lower decrease of the
            electrolyte and liquidus temperature is due to a slower cooling process. The entire experiment
           has shown that with the start of the modulation, the cells should be operated with a much higher
           cooling to get a quicker equilibrium, while after about 3 hours normal cooling can be continued.

                 3.1. Conclusion

           In summary, the results show that regulation of the heat balance with the heat exchanger is
            possible, but a complete change of the side ledge thickness cannot be avoided. Due to the
           temperature changes on both sides, inside by the power change and outside by the heat
           exchangers, the isothermal lines move parallel to each other or away from each other (the
           temperature change  per cm  wall  thickness  increases  or  decreases). However,  the  heat
          exchangers reduce the risk of furnace failure shortly after the power changes and help achieving
           a steady state in a timely manner.

            4.  Energy Counter

         The previous chapter showed that a new equilibrium occurs within a modulation period. For
          example, a cell at 960 °C cell may be considered hot after a low-energy phase and cold after a
           high-energy phase [17]. For this reason, it is extremely important for process control to know




                                               856

### PDF page 12

Travaux 47, Proceedings of the 36th International ICSOBA Conference, Belem, Brazil, 29 October - 1 November, 2018




            5.2.    Cooling by Heat Balance Difference (PI)

          For the control of the cooling, a P and an I component were developed together with the
          Department  of Automation  [26]. To  realize ΔQ =  0,  the energy counter determines a
          manipulated variable (frequency in Hz) calculated for the fans of the heat exchangers.

      ̇ ̇  ̇

    ̇ ̇ ̇

      ̇


                                                                                                   (14)

          where:
                  Frequency, Hz
    Flow rate, m3 s-1

         The I component is calculated using the heat energy difference, Figure 8. If the difference
          exceeds a fixed positive or negative limit, the frequency is changed by +/- 3Hz.





          Figure 8. Simplified representation of the PI controller using Shell Heat Exchanger (SHE)
                                     and energy counter.

            5.2.1.  Conclusion

         The  I component was  installed in order to continuously minimize any system deviation
           occurring. Unfortunately, the previously expressed concerns that the heat balance control and
           the control concept of the cell (9Box) stimulate each other were confirmed in the test phase. The
         9Box system is already parallel working to the alumina control in a multi-size system. By
            integrating this further control system, its reference variables become interference variables of
           the existing systems and make the overall system unstable. Furthermore,  it is much more
            effective to counteract the cause of the heat change directly where  it develops. The heat is
           generated mainly in the area of the anode-cathode distance (ACD), thus, a reduction of the ACD
           during amperage increase and an increase of the ACD during amperage reductions make sense.
            Finally, with the large number of cells, 120 units with 5280 heat exchangers in one control loop,
                 it is difficult to control with a mean value. Should individual groups heat up and others cool
         down, then the average over all cells may be within the target range, or if that is not the case, the
            controller will move some cells out of the range while others will be brought into the range. For
           the reasons mentioned, a linear control with a simple P element is presented below. By adapting
           the ACD, the desired result can be achieved in combination with the heat exchangers and the
          energy counter. On top of that, the proven 9Box control system is used to control individual
           groups. A combination of both is being developed at the moment in a totally new process
            control system.





                                               862

### PDF page 17

Travaux 47, Proceedings of the 36th International ICSOBA Conference, Belem, Brazil, 29 October - 1 November, 2018





                            Figure 15. Results from the virtual control system.

         The transient calculations showed, that with reduction of the ACD and additional cooling with
           the heat exchangers  it was possible to keep the side ledge (Figure 15). While in a second
            calculation without cooling and reduction of the voltage, the side ledge was lost quickly (Figure
            16). The calculated value of about 3 h cooling reaction time (equation 4a) was confirmed by the
         model and furthermore verified with thermocouples in tests at the cells. However, a range of 1.5
         – 4 h was registered by thermocouples here, which could be related to the wall thickness that
         was hard to measure accurately.





            Figure 16. Results from the virtual control system without SHE and ACD adjustment

            6.  Conclusions

      A Megatrend of the next decades is the energy transition from conventional power to renewable.
          This huge task for our society is comparable to the first moon expedition. It can be a despair
           challenge for our industry or a winning opportunity. If we want to capture the opportunity, we
          need a revolution of the aluminium production process. We gave this revolution a name. “The
            Virtual Battery”. This concept is a landmark project in the German Energy Transition.

          Adapting the aluminium smelting process to a flexible power supply needs the rethinking of a
         number of aspects  in the smelting process. Manipulating thermal and magnetic impacts




                                               867



---

# POWER MODULATION MODELING OF ALUMINUM REDUCTION CELLS FOR RENEWABLE ENERGY INTEGRATION

Source: `modeling_power_modulation/POWER MODULATION MODELING OF ALUMINUM REDUCTION CELLS FOR RENEWABLE ENERGY INTEGRATION.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

                                                                                International Conference on Applied Energy 2019
                                                                          Aug 12-15, 2019, Västerås, Sweden
                                                                                                   Paper ID: 0827



  POWER MODULATION MODELING OF ALUMINUM REDUCTION CELLS FOR RENEWABLE
                        ENERGY INTEGRATION

                       Gustavo Ospina-Aldana1, Mohamed I. Hassan Ali2, Sgouris Sgouridis1, Ali Bouabid1

                                     1 Khalifa University of Science and Technology

                           2 Khalifa University of Science and Technology (Corresponding Author)


  ABSTRACT
                                                                   1. INTRODUCTION
    This  paper  presents  the  development  of  a
                                                     Aluminum  is an important metal for the energythermodynamic model  to  determine  the extended
                                                                     transition. It’s the most abundant metal on the earth’soperating window of an aluminum cell to enable power
                                                                 crust and its lightweight, corrosion resistance, and highmodulation. The integration of renewable energy to
                                                         thermal and electrical conductivity makes aluminumaluminum production needs to overcome the challenge
                                                        range of application very wide. Aluminum is widely usedof narrow operating windows of aluminum cells. The
                                                                     in construction, aerospace, marine, rail and primarily theproposed model takes an industrial aluminum cell as a
                                                        automotive industry. Aluminum use will likely increase,case study to demonstrate how to build the operating
                                                            as tighter emissions regulations push its wider adoptionwindow,  constrained  by  the  cell  design  technical
                                                                 into  lighter  vehicles.  However,  the  production  oflimitations. The extended operating window can also be
                                                   aluminum is highly energy intensive.used  to  estimate  the  heat  exchanger  heat  rate
requirements to enable an aluminum cell to operate          The total primary aluminum energy consumption in
under a wide power modulation.                         2017 was 863.3 TWh, 3.38% of global electricity demand
                                                                            [1]. The aluminum energy intensity production varies by   Keywords: Aluminum production, energy transition,
                                                          the state of technology used and can be a significantpower modulation, renewable energy.
                                                  component of the country’s demand. In the UAE, the
  NOMENCLATURE                               aluminum industry requires 20% of the total installed
                                                                        electricity generation capacity of the country.
     Abbreviations
                                                     Aluminum cells are operated within a narrow power    ACD              Anode-to-cathode distance
                                                             input  operating window  to  achieve a  target bath
    CD                Current density
                                                            operating temperature between 955 °C and 970 °C, this
    CE                Current efficiency
                                                       temperature  range  provides  the  best  operating
    SEC                  Specific energy consumption
                                                              conditions for an aluminum cell [2]. To keep aluminum
    UAE              United Arab Emirates
                                                                          cells within this narrow operating range, operations
                                                              prefer constant power.



    Selection and peer-review under responsibility of the scientific committee of the 11th Int. Conf. on Applied Energy
(ICAE2019).

    Copyright © 2019 ICAE

### PDF page 5

needs to be provided to an  ideal  electrolysis  cell,       49.89 MWh while the energy stored in the cell at 970 °C
according to the ideal aluminum electrolysis reaction           is approximately 54.18 MWh.
(Eq. 2) with (𝜂= 1). Using the Gibbs Free energy change
                                                           There is an energy difference of 4.29 MWh between
of the ideal electrolysis reaction (Eq. 2), and combining
                                                          the  target  temperatures.  This  value  is needed  to
the  Faraday's Law, the standard  potential can be
                                                           estimate the maximum duration of a given power input
calculated with the following equation:
                                                        modulation cycle without adding heat exchangers. Using
                                                      a conservative approach from previous industrial tests
                   ∆G
                  Eo =                           (8)           presented in [10], only 30% of the calculated energy                     nF
                                                               difference will be considered
   Where F is the Faraday's constant, n is the number of
free electrons and ∆G  is the Gibbs free energy change           Using the thermal energy storage calculation, it was
of Eq. 2 reaction with η=1.                                  estimated that the power input to the  cell can be
                                                            increased by 8% from the nominal value (up to 477.2 kA,
    In order for the electrolysis reaction to occur at an
                                                              4.2 V, at ACD 3.4cm) for approximately 8.5 hours,
appropriate  speed, an  additional  voltage must be
                                                           followed by a 8% power reduction (down to 432.1 kA, 3.9
supplied. The anodic reaction overvoltage (Vra), anodic
                                                                V, at ACD 3.4cm) for approximately 4.3 hours.
concentration   overvoltage    (Vsa)   and   cathodic
concentration overvoltage (Vcc) equations can be found            4.2 Thermodynamic model
in [18].                                                       The  specific energy consumption and aluminum
    3.2.1  Aluminum production and SEC                    production of the cell at the rated point of 454.8 kA and
                                                           4.08 V[4] were calculated with the model within 2% error
   The equation to calculate aluminum production by
                                                     from the published industrial data. The thermodynamic
electrolysis is derived from the Al3+ to Al (s) half-reaction.
                                                   model was used  to  build the steady  state power
The Faraday’s constant (F=96485.33 s A/mol) allows to
                                                        modulation window of EGA’s aluminum cell. The usage
calculate the number of moles of electrons that will pass
                                                              of a  shell heat exchanger can allow the aluminum
through the cell for a given charge. The electric charge is
                                                          production to be modulated between -16.9% and +5.2%
simply the product of current and time (1 C=1 A*s). Using
                                                     from the nominal production rate (3481 kg Al/day). This
the aluminum molar weight, the  specific aluminum
                                                          production  range  can be  achieved  with  a power
production per day ṁ Alcan be obtained. The fractional                                                        modulation between  -14.5% and  +8.6%  from  the
current efficiency term η  is introduced to account for
                                                       nominal power (1855.2 kW).
the aluminum back-reaction.
                                                                    This modulation scheme can be performed at a
     ṁ Al = 8.0537 ∙I ∙η kg/kA-day                 (9)                                                              nearly constant SEC of 13.2 kWh/kg Al, within region I,
   The aluminum specific energy consumption (SEC) is      bounded by an ACD between 3.4 cm and 5 cm (Figure 1).
calculated as the ratio of the energy input  (I ∙Vcell)      A further production modulation can be achieved getting
over the specific aluminum production rate ṁ Al.               into region II reaching the lower limit of current density,
                                                       however, reducing the current below this limit will start
    4. RESULTS
                                                             to reduce the current efficiency of the process.
    4.1 Thermal energy storage calculation
                                                                   5. CONCLUSION
   The thermal energy storage calculation sheet was
                                                       The power and production of an aluminum cell can
validated using the data presented in [10]. The error was
                                                   be controlled over a wide range by controlling the heat
less than 1%. Analyzing the EGA DX+ Ultra cell, which
                                                                losses from the side walls. Controlling the heat losses of
operates at a nominal point of 454.8 kA and 4.08 V, it was
                                                    an aluminum cell enables the adaptation of aluminum
found that the energy stored at 955 °C is approximately


                                                   5                              Copyright © 2019 ICAE



---

# Studies on Power Modulation of Aluminum Smelting Cells based

Source: `modeling_power_modulation/Studies on Power Modulation of Aluminum Smelting Cells based.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

Studies on Power Modulation of Aluminum Smelting Cells based
     on a Discretized Mass and Thermal Dynamic Model

         Choon-Jie Wong1, Jie Bao1, Maria Skyllas-Kazacos1, Barry Welch1,
           Mohamed Mahmoud2, Alexander Arkhipov2, Nadia Ahli2

        1 School of Chemical Engineering, University of New South Wales, Sydney NSW 2052, Australia
       2 Emirates Global Aluminium, Jebel Ali Operations, P.O. Box 3627, Dubai, United Arab Emirates

Published online 04 Jan 2023 in Metallurgical and Materials Transactions B. DOI: 10.1007/s11663-022-02709-w


Abstract                             Keywords    Aluminum   smelting,   Hall-H´eroult
                                                          process,  Power  modulation,  Discretized  dynamic
                                                  mathematical  model,  Coupled  mass  and  energy
With   increasing  penetration   of  intermittent  balance, Demand-side power management
renewables,  flexible operation  of the aluminum
smelting process under variable power supply will
become critical for smelter operational feasibility 1  Introduction
and for providing grid demand-side service. As a
demand-side power management approach, power  Aluminum   plays   an   important    role   as
modulation  dynamically  varies  the  aluminum  decarbonization  policies  and  the  shift  to  a
production  rate  (thus  power  consumption)  in  more sustainable world drive a greater adoption
response to power availability/price. While there  of renewable  energies and  electric  vehicles  [1].
were power modulation  trials  in  the  industry,  The  reliability  of  low-cost  energy  supply   is
many  resulted  in poor  plant performance due  crucial for the aluminum smelting industry, which
to  the  operational  difficulties  caused  by  the  consumes 8% of global industrial electricity  [2],
spatial  variations  of  process  conditions  and  with electricity costs representing more than 30%
multi-timescale smelting cell dynamics. This paper  of the total production costs  [3].  However, the
presents studies on the feasibility and cell behavior  increased penetration of intermittent renewables
under power modulation based on a first-principles  also leads to a more variable supply and pricing
spatially-discretized dynamic material and energy  of  electricity  [4].   This challenges the smelting
balance model.  Various combinations of process  industry   to  compromise  between   increasing
inputs (line current and interelectrode distance)  production costs and disrupting the delicate mass
were  used  to  study  the  protective  side  ledge  and thermal balances of their smelting cells, which
profile,  as  it should always be maintained  for  impacts cell stability, productivity, and lifespan [5].
a well performing, long-lasting  cell.  Simulation   Aluminum  smelting   cells  are   traditionally
studies of repeated modulation cycles show that  operated  at  fairly  constant  power.    As  a
ledge does not solidify and dissolve in the same  demand-side   power   management   approach,
timeframe  unless  energy  is  rebalanced,  while  power  modulation  of aluminum  smelting  cells
having slow dynamics thus only stabilizing after  can  dynamically  vary  the  production   rate
a few modulation cycles under a high frequency  (thus power consumption) in response to power
modulation.  This work contributes to the power  availability/price. With this increased operational
modulation modeling and analysis of aluminum   flexibility, smelters can be powered by renewable
smelters,  allowing  for  operational and  control  energy  and  act  as  virtual  “grid-level  storage
optimization.                                     battery” by overproducing during periods of low


                                             1



---

# The Formation and Dissolution of Crust Upon Alumina Addition into Cryoltie Electrolyte

Source: `modeling_power_modulation/The Formation and Dissolution of Crust Upon Alumina Addition into Cryoltie Electrolyte.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

JOM, Vol. 67, No. 9, 2015
DOI: 10.1007/s11837-015-1525-2
  2015 The Minerals, Metals & Materials Society



The Formation and Dissolution of Crust Upon Alumina Addition
into Cryolite Electrolyte


           YOUJIAN YANG,1,2 BINGLIANG GAO,1,3 ZHAOWEN WANG,1
          ZHONGNING SHI,1 and XIANWEI HU1


                 1.—School of Materials and Metallurgy, Northeastern University, Mail Box 117, Shenyang, China.
                  2.—e-mail: yangyou100@163.com. 3.—e-mail: blgao@mail.neu.edu.cn

            The properties of the alumina agglomerate/crust formed upon smelting grade
             alumina feeding and the corresponding dissolution rates in cryolite electrolyte
             were studied using a suspended weighing device. A series of experiments was
              designed to investigate the dissolution rate of the crust at various tempera-
               tures and the effects of initial alumina concentration in the electrolyte on the
              formation process and properties of the crust. Initial results showed that
             under experimental non-stirring conditions, a large proportion as high as 54–
           64% of the fed alumina participated in the formation of the crust upon feeding
               at 1233–1238 K (960–965 C). The dissolution rate of the crust decreased
               greatly with the increase of initial alumina concentration and the decrease of
               operating temperature. The mass of the crust increased signiﬁcantly at high
                  initial alumina concentrations and decreased temperature, while the alumina
               content of the crust showed a slight decreasing trend. Other parameters of the
               crust such as volume density and gas-ﬁlling fraction were also measured. The
              inﬂuence of physical stirring on alumina dissolution rate was also discussed.




                                                  path in the cell and then causes the unstable ﬂow of
          INTRODUCTION
                                                     the metal pad as well as other consequences. With a
  Smelting grade alumina (SG alumina) is used as     poor dissolution capacity, the formation of the crust/
the raw material in the aluminum electrolysis pro-     sludge induces problem in maintaining the alumina
cess, where it acts as a solute in the molten cryolite     concentration in the bath.
electrolyte. In industrial practice, it has been difﬁ-      Most of the earlier research on the dissolution of
cult to control the process of alumina dissolution.    alumina crust was established with the purpose to
The alumina is fed periodically to the cell and the     obtain a fast dissolution rate, in which physical
batch size depends on the feeding strategy. Once the     stirring was introduced and the crust was artiﬁ-
cold alumina  is added into the molten bath,  it      cially broken into small pieces. The crust behavior,
spreads out quickly on the liquid surface and a piece     including the formation, composition and dissolu-
of agglomerate could be observed. The normal size of     tion rate, has not been well investigated.
each feeding (about 1–2 kg) is still too large to ob-       Rolseth et al.1 tested the dissolution rate of SG
tain immediate dispersion of all the alumina powder    alumina  powder  under  similar  gas-stirring  as
in the relative small surface area and volume of the     industrial  conditions. A  two-stage  dissolution
bath between neighboring anodes in the feeding     behavior was observed when a batch of alumina
zone, though the central point feeding system used    powder was added. The ﬁrst stage was the fast dis-
in modern cells facilitates the dispersion and the     persion of alumina powder upon feeding where 30–
dissolution rate  of alumina beneﬁting from the    50% of the batch dissolved in seconds, and the second
physical stirring caused by the release of anode gas.     stage was the relative slow dissolution of the crust.
  The alumina crust has a slow dissolution rate in    Walker et al.2 retrieved the alumina agglomerate
contrast to the fast-dispersed alumina powder upon    from an industrial cell with a stainless steel mesh
feeding. Undissolved alumina tends to accumulate     basket at different time durations after the alumina
on the bottom of the cells to form sludge. The bottom     feeding. It was found that the density of the crust
sludge is undesirable because it disturbs the current    would  approach  2.4 g cm 3  and  the  porosity


2170                                                                                             (Published online July 8, 2015)



---

# The Structure of the Aluminium Smelting Cell Ledge

Source: `modeling_power_modulation/The Structure of the Aluminium Smelting Cell Ledge.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

         TRAVAUX 48, Proceedings of the 37th International ICSOBA Conference and
      XXV Conference «Aluminium of Siberia», Krasnoyarsk, Russia, 16 – 20 September, 2019


  AL17 - The Structure of the Aluminium Smelting Cell Ledge

           Jingjing Liu1, Shanghai Wei2, John J.J. Chen3 and Mark P. Taylor4
                                       1. Postdoctoral Fellow
                                             2. Professor
                                             3. Professor
                       4. Department of Chemical & Materials Engineering,
                                         5. Research Fellow
                                              6. Director
               NZ Product Accelerator, Faculty of Engineering
                   All at: University of Auckland, Auckland, New Zealand
                    Corresponding author: jingjing.liu@auckland.ac.nz

Abstract

In aluminium smelting cells, ledges form on the cell walls. Modern cell design and control cause
a suitable ledge profile to form and maintained in order to protect the cell walls from the corrosive
liquids, and ensure efficient current distribution and cell heat balance. During cell operation,
significant ledge freezing and melting does occur following heat balance changes due to batch
operations. In the laboratory scale, a ledge formation mechanism has been studied. It shows a
linkage between the rate and directional nature of ledge growth, and its structure, as affected
through a superheat change. An open ledge structure can dominate the ledge material growth or
melt it out quickly when the superheat either decreases or increases, respectively. This paper
begins the investigation of industrial ledge samples, in terms of structure and composition
primarily, to identify if this  ledge formation mechanism exists in the industrial cell.

Keywords: Aluminium smelting, industrial ledge, structure.

1.     Background

Cell wall integrity is critical for maintaining the cell heat balance and a safe operation of an
aluminium reduction cell. In terms of integrity, we include the lining materials, such as SiC and
refractory bricks etc., and the side ledge that is frozen on the walls. The ledge should be
maintained in a profile which allows sufficient heat transfer through side wall (not too thick), and
also protect the lining materials from the corrosive liquids (not too thin). Although the side ledge
is submerged in molten liquids and is therefore not visible during the daily operation, the ledge
profile can be measured as required to ensure the sufficient protection of the walls and good
thermal balance of the cell. Not only the ledge and its profile that is formed on the walls is critical,
the part of the ledge that extends on the cathode surface (ledge toe) has a significant impact on the
current distribution if the ledge toe extends beneath the anode shadow, making the current flow
path from the anode to cathode to be non-vertical since the frozen ledge is an insulating material.

Studies on ledges date from 1980s and the industrial ledge dynamic behaviours have been studied
(ledge thickness and ledge profile) and discussed by many researchers in terms of heat transfer
and ledge composition [1-3]. In principle, the ledge material has been traditionally considered as
pure cryolite precipitating from the molten bath as the primary phase and is frozen to the walls as
the temperature there drops below the bath liquidus temperature. A thin dynamic boundary layer
should be formed at the ledge/bath interface in theory, where the temperature is close to bath
liquidus point.

Of course in the industrial ledge, bath components such as AlF3, CaF2 and alumina are present in
the boundary layer, and have also been found [2, 3] in the ledge itself. And recent research has




                                     877

### PDF page 9

         TRAVAUX 48, Proceedings of the 37th International ICSOBA Conference and
      XXV Conference «Aluminium of Siberia», Krasnoyarsk, Russia, 16 – 20 September, 2019



Despite the difference in morphology observed here, it is certain that the presence of chiolite and
alumina in the ‘mixed’ zones in specimen 8_1 bears a striking similarity to the open crystalline
layer composition in the laboratory samples. The effect of the high modifier composition of the
mixed zones on the local liquidus point within these sections of ledge will also be similar.





                  Figure 6. Typical structure of ledge specimen 8_1.

4.     Conclusions

Several industrial ledge specimens obtained from a scheduled cut-out cell have been analysed and
compared with laboratory formed ledge in terms of composition and micro-structure. The
following findings are evident at this early stage in the investigation:
•     As expected, industrial ledge shows more complexity, such as the inclusions of carbon
        dusts through the ledge.
•       Industrial ledge grains grow into a bigger size and with a slightly thicker ‘cold face’
       columnar layer. The thermal gradient across industrial ledge  is much greater than
        lab-scale ledge, which could drive both of these effects.
•       In one sample studied here, the interaction with the carbon dust has changed the open
       porous structure in the industrial ledge. Alumina phase forms as corundum platelets in the
       porous mixture zone together with chiolite.
•     No obvious liquid channels have been observed between the larger cryolite crystals as
       were observed in the laboratory ledge open crystalline layer. However, it must be noted
         that the laboratory ledge was only maintained at temperature for about 1.5 hrs, and is
        therefore far away from its final chemical balance. The industrial ledge, by comparison
       has been aging at cell temperature for many operating days. This is probably long enough
        for the ledge to reach chemical balance to a greater extent. Liquid channels would then be
       taken up by the cryolite and chiolite crystal growth into the mixed zones, creating a
        different apparent morphology for the open structure layer.



                                     885



---

# US5089093_PROCESS_FOR_CONTROLLING_ALUMINUM_SMELTING_CELLS

Source: `modeling_power_modulation/US5089093_PROCESS_FOR_CONTROLLING_ALUMINUM_SMELTING_CELLS.pdf`

## Extractive digest

Verbatim source-page extracts selected by abstract/summary/conclusion headings. These are not a verified analytical summary. Refer to full text for methods, qualifications, and references.

### PDF page 1

               ||||||||||||III                                                                   US005089.093A
United States Patent   (19)                 11   Patent Number:     5,089,093
Blatch et al.                                                      (45)  Date of Patent:    Feb. 18, 1992

(54)  PROCESS FOR CONTROLLING                 57            ABSTRACT
   ALUMINUM SMELTING CELLS          A process for controlling an aluminum smelting cell
 75)  Inventors:  Geoffrey I. Blatch, Westgarth; Mark    comprising monitoring the cell voltage and current,
                  P. Taylor, Greensborough; Mark       alumina dumps, additions, operations and anode to cath
                   Fyfe, Slengarry, all of Australia        ode distance movements, continuously calculating the                                                                   cell resistance and the bath resistivity from said moni
 73)  Assignee:  Comalco Aluminum Ltd.,                tored cell voltage and current, monitoring the existence
               Georgetown, Australia                of low frequency and high frequency noise in the volt
                                                     age of the cell, continuously calculating the time rate of(21)  Appl. No.: 481,845                                                  change of resistance of the cell, suspending calculation
 22).  Filed:      Feb. 20, 1990                            for a predetermined time when an alumina dump, addi
(30)       Foreign Application Priority Data                 tion, operation or ACD movement occurs, establishing                                                                   filtered   resistance  slope   thresholds,  determining
  Feb. 24, 1989 AU)   Australia  ............................... PJ2938    whether the low frequency noise is above a predeter
 51)   Int. Cl............................ C25C3/06; C25C 3/20    mined threshold, and if so, increasing the filtered slope
 52   U.S. Cl. ...................................... 204/67; 204/225;     thresholds for low alumina concentration detection,                                    204/228; 204/245     calculating an alumina inventory from the alumina
 58)   Field of Search ...................... 204/67, 243 R-247,    dumps, determining whether the cell is overfed, and if                             204/153. 1, 400, 225, 228     not feeding alumina to prevent an anode affect, calculat
                                                        ing the heat supplied and heat required for aluminum
(56)               References Cited                       production, calculating the heat available for dissipa
           U.S. PATENT DOCUMENTS                  tion, calculating the target heat for the cell, calculating
                                                         the difference between the available heat and the target     3,573,79  3/1971  Dirth et al.  ........................... 204/67    heat with respect to time, calculating a running heat     3,625,842 12/1971  Bristol et al.  ......................... 204/67
     3,660,256  5/1972  Lippitt et al.  ......................... 204/67    inventory from the integral of this difference, establish     3,712,857   1/1973  Piller  ..................................... 204/67    ing a target resistance for the cell and modifying that
     3,812,024  5/1974 Goodnow et al.  .................... 204/67     target resistance to achieve a zero heat integral, check
     4,425,201   1/1984  Wilson et al.  ......................... 204/67    ing that the target resistance is an allowable value, and
     4,814,050 3/ 1989 McGraw et al.  ..................... 204/67    moving the anodes of the cell to establish the new target
                                                                 resistance, estimating the time rate of change of bath     FOREIGN PATENT DOCUMENTS                                                                     resistivity and checking whether  resistivity and the
      0044794  7/1981  European Pat. Off.   .                   derivative are greater than predetermined limits, and if
      2238775  2/1975  France   .                                 so, adjusting the target heat of the cell to maintain the
 WO86/05008  8/1986 PCT Int'l Appl.   .                   long term heat balance of the cell.
Primary Examiner-Donald R. Valentine
Attorney, Agent, or Firm-Kenyon & Kenyon                        32 Claims, 12 Drawing Sheets
            HEAT AND MASS BALANCE CONTROL STRATEGY

                      TIME SCALE:   Short Terrn  -  ..........................awswovovovoodooeuvrute 48009008woooow- Medium/Long Tern

                     NITAL                             NPUT OTARGE:
                NPUS                             CESUPERHEAT TARGETRAiGETHERMODATA.EMF
                   DYNAMIC                 7uma DuPS                               CACULATE BATHRESSMY
                     INPUTS     /vie /       ADDITIOMS,OPERATIONS,
                                                                               ACE MCWEMES
                            CALC RESISTANCE
                                 (V-EMF/

                                      00.1 Hz (LO)     NOSE f-----
                           04-Hz (HI)        CALC.                                                                            CA.C.HEAT SUPPLIED &
                                                                  HEATRECURED FOR A.
                                                                              PROD.
                     CA.C.FTERED
                      RESSTANCE SLOPE  -                                                              -                                         YES
                                (Every second)                                          CA.C.HEAT AVAILABLE                                             Awrage
                        Day Times                                FOR OSSAPATION                                                            Superhead
                                 Racak.R                           OAwakW (10 min)                                                             out orange
                        S Yfiller Const's
    -4.KOSE ABOEFREG FEED                                  Neware
             NHEsote?        .                                CAC  WOFFERENCE
                    x /                                         Of (OAVAIL-0TARGE)                                     WHME

