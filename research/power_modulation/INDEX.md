# Power-modulation research archive: index

Condensed extracts of 14 source documents on Hall-Héroult cell behaviour under
power modulation. See `README.md` in this folder for how the archive was
produced and its limits (extractive digests, auto-cropped figures, no digitised
curves). Open `START_HERE.html` for per-document links.

Purpose in this repo: reference material for specifying a cell that modulates
further, faster and with less ledge damage than the TRIMET Essen EnPot potline
cited in the siting map (`index.html`, entry "TRIMET Essen").

## What each document contributes

| id | Document | Use for |
|----|----------|---------|
| 09 | Düssel (TRIMET), Paradigm Shift in the Indication of a Stable Cell during Power Modulation, ICSOBA 2018 | The benchmark. 162 kA nominal, +12 to +18 kA tests, shell heat exchangers hold heat loss constant to ~180 kA, ~200 kA only briefly with ACD cuts. Cooling reaction time 1.5 to 4 h. Ledge thickness change "cannot be avoided". |
| 11 | Wong et al. (UNSW/EGA), Power Modulation based on a Discretized Mass and Thermal Dynamic Model, 2023 | Spatially discretised cell model. Ledge profile and local superheat over repeated modulation cycles. Basis for a cell-level simulator. |
| 08 | Wong et al., Optimisation of power modulation for Hall-Héroult cells, J. Energy Storage 2026 | Optimal line-current and ACD trajectories under thermal constraints, time-of-use pricing, profit comparison. Defines the economic objective. |
| 02 | Ma et al., MPC of superheat during power modulation, ICSOBA 2023 | Superheat held near 12 °C under ±5 % line current by manipulating alumina feed and ACD. Control-layer reference. |
| 10 | Power modulation modeling for renewable integration, ICAE 2019 | Simple thermodynamic model, ACD window 3.4 to 5 cm, shell-heat-exchanger heat-loss envelope of ±12 %. |
| 01 | Antille, von Kaenel, Bugnion (KAN-NAK), A Cell Simulator, ICSOBA 2015 | Validated dynamic cell simulator including anode change, tapping and current noise. |
| 06 | Thesis, Modelling the Mass and Energy Balance of Aluminum Reduction Cells (250 pp.) | Full mass and energy balance derivation. Replaces curve-fitted voltage models. |
| 14 | US 5,089,093 (Blatch et al., Comalco), Process for Controlling Aluminum Smelting Cells, 1992 | Prior-art control of cell thermal balance via voltage and chemistry. Freedom-to-operate check. |
| 05 | Electrothermic Industrial Load Model with dynamic iterative mechanism, Energy Reports 2026 | Grid-side equivalent thermal parameter model of a potline as a demand-response load. |
| 07 | Multilevel Coordinated Strategy for Electrolytic Aluminum System, IET Smart Grid | Potline plus renewables coordination. System-level, not cell-level. |
| 13 | Liu, Wei, Chen, Taylor, The Structure of the Aluminium Smelting Cell Ledge, ICSOBA 2019 | Ledge microstructure. Why ledge does not freeze and melt symmetrically. |
| 12 | Yang et al., Formation and Dissolution of Crust upon Alumina Addition, JOM 2015 | Crust and alumina dissolution kinetics at low superheat. |
| 03 | Lillebuen, Bugge, Høie, Alumina Dissolution and Current Efficiency, Light Metals 2009 | Current-efficiency penalty from sludge and poor dissolution. |
| 04 | Hyland, Patterson, Stevens-McFadden, Welch, AlF3 consumption and control, 2000 | Bath chemistry drift and AlF3 demand over work cycles. Chemistry constraints on fast modulation. |

## Gaps this archive does not close

- No document gives a cell design that beats TRIMET. The archive is modelling,
  control and chemistry literature; a design spec has to be derived from it.
- No digitised curves. Any quantitative use of a figure needs the source PDF.
- The only field data on heat-exchanger modulation is TRIMET's own (doc 09).
  Everything else is simulation.
- The siting map credits TRIMET Essen with -13 %/+20 % for 48 h. Doc 09
  reports +18 kA on 162 kA (about +11 %) with ~200 kA (about +23 %) reachable
  only briefly. The map figure comes from EnPot marketing material, not from
  this paper. Reconcile before using either number as a target.
