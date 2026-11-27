# Enthalpia against published values

Enthalpia 3.1, 26 November 2026. 246 checks.

Each line below is something Enthalpia calculated, set beside a value that does not come from Enthalpia. Nothing is left out: the checks where the program is weakest are in the table with the rest.

**Where the reference values come from**

- *Reference equation of state*: the equation the standards laboratories publish for each pure fluid (IAPWS-95 for water, Setzmann and Wagner for methane, Span and Wagner for carbon dioxide and nitrogen, and so on), which reproduces the measurements to within their own uncertainty. Evaluated with the open CoolProp library.
- *GERG-2008*: the international standard equation for natural gas (ISO 20765-2), also through CoolProp.
- *Reference correlation*: the published viscosity and thermal-conductivity correlation of the fluid.
- *IAPWS-95 steam tables*: the international formulation for water and steam.
- *Handbook azeotrope tables*: values as tabulated in the chemistry and chemical engineering handbooks; sources differ among themselves by about 0.1 C and 1 mole per cent.
- *NIST-JANAF thermochemical tables*: the standard tables of ideal-gas heat capacity and enthalpy up to 6000 K.
- *Textbook problem*: a worked example with a published answer.
- *Hand calculation*: a formula from any textbook, which you can repeat with a calculator.

## 1. Pure fluids at their boiling point (Peng-Robinson)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| methane | Boiling point at 1 atm | 111.7 K | 111.6 K | -0.09 K |
| methane | Heat of vaporisation at 1 atm | 510.8 kJ/kg | 511.7 kJ/kg | +0.2 % |
| methane | Liquid density at the boiling point | 422.4 kg/m3 | 427.0 kg/m3 | +1.1 % |
| propane | Boiling point at 1 atm | 231.0 K | 231.0 K | -0.07 K |
| propane | Heat of vaporisation at 1 atm | 425.6 kJ/kg | 424.1 kJ/kg | -0.4 % |
| propane | Liquid density at the boiling point | 580.9 kg/m3 | 581.0 kg/m3 | +0.0 % |
| n-butane | Boiling point at 1 atm | 272.7 K | 272.7 K | +0.06 K |
| n-butane | Heat of vaporisation at 1 atm | 385.7 kJ/kg | 386.3 kJ/kg | +0.1 % |
| n-butane | Liquid density at the boiling point | 601.3 kg/m3 | 601.2 kg/m3 | -0.0 % |
| benzene | Boiling point at 1 atm | 353.2 K | 352.9 K | -0.28 K |
| benzene | Heat of vaporisation at 1 atm | 393.7 kJ/kg | 388.9 kJ/kg | -1.2 % |
| benzene | Liquid density at the boiling point | 813.4 kg/m3 | 814.2 kg/m3 | +0.1 % |
| ammonia | Boiling point at 1 atm | 239.8 K | 240.1 K | +0.26 K |
| ammonia | Heat of vaporisation at 1 atm | 1369.7 kJ/kg | 1393.4 kJ/kg | +1.7 % |
| ammonia | Liquid density at the boiling point | 681.6 kg/m3 | 681.3 kg/m3 | -0.0 % |
| ethanol | Boiling point at 1 atm | 351.6 K | 350.7 K | -0.84 K |
| ethanol | Heat of vaporisation at 1 atm | 849.6 kJ/kg | 853.4 kJ/kg | +0.4 % |
| ethanol | Liquid density at the boiling point | 736.4 kg/m3 | 737.2 kg/m3 | +0.1 % |
| water | Boiling point at 1 atm | 373.1 K | 373.1 K | -0.03 K |
| water | Heat of vaporisation at 1 atm | 2256.5 kJ/kg | 2266.0 kJ/kg | +0.4 % |
| water | Liquid density at the boiling point | 958.4 kg/m3 | 958.4 kg/m3 | +0.0 % |
| propane | Vapour pressure at -23 C | 218.0 kPa | 217.7 kPa | -0.1 % |
| propane | Vapour pressure at 27 C | 997.7 kPa | 997.4 kPa | -0.0 % |
| propane | Vapour pressure at 67 C | 2431.1 kPa | 2443.9 kPa | +0.5 % |
| carbon dioxide | Vapour pressure at 0 C | 3485.1 kPa | 3477.3 kPa | -0.2 % |

Average difference 0.4 %, largest 1.7 % (quantities given in per cent).

Reference: Reference equation of state.

## 2. Water and steam (Steam IAPWS-95 package)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| saturated steam | Saturation temperature at 10 bar | 179.9 C | 179.9 C | -0.00 C |
| boiler | Heat to turn water at 25 C into saturated steam at 10 bar | 2671.4 kJ/kg | 2671.4 kJ/kg | -0.0 % |
| water at 1 atm | Heat of vaporisation | 2256.5 kJ/kg | 2256.5 kJ/kg | -0.0 % |
| superheated steam, 40 bar and 400 C | Density | 13.62 kg/m3 | 13.62 kg/m3 | +0.0 % |
| steam turbine, 40 bar and 400 C to 1 bar, 85 % efficient | Work per kg of steam | 644.7 kJ/kg | 644.7 kJ/kg | -0.0 % |
| steam turbine, 40 bar and 400 C to 1 bar, 85 % efficient | Vapour fraction at the outlet | 0.953 | 0.953 | +0.000 |

Average difference 0.0 %, largest 0.0 % (quantities given in per cent).

Reference: IAPWS-95 steam tables.

## 3. Gas density at pressure (Peng-Robinson and tc-PR)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| methane, 27 C and 100 bar (Peng-Robinson) | Density | 75.18 kg/m3 | 77.13 kg/m3 | +2.6 % |
| nitrogen, 27 C and 200 bar (Peng-Robinson) | Density | 212.5 kg/m3 | 218.6 kg/m3 | +2.8 % |
| carbon dioxide, 77 C and 100 bar (Peng-Robinson) | Density | 228.8 kg/m3 | 232.2 kg/m3 | +1.5 % |
| hydrogen, 27 C and 350 bar (Peng-Robinson) | Density | 23.19 kg/m3 | 24.32 kg/m3 | +4.9 % |
| ethylene, 47 C and 80 bar (Peng-Robinson) | Density | 157.3 kg/m3 | 159.1 kg/m3 | +1.1 % |
| methane, 27 C and 100 bar (tc-PR) | Density | 75.18 kg/m3 | 74.89 kg/m3 | -0.4 % |
| nitrogen, 27 C and 200 bar (tc-PR) | Density | 212.5 kg/m3 | 208.5 kg/m3 | -1.9 % |
| carbon dioxide, 77 C and 100 bar (tc-PR) | Density | 228.8 kg/m3 | 230.2 kg/m3 | +0.6 % |
| hydrogen, 27 C and 350 bar (tc-PR) | Density | 23.19 kg/m3 | 24.32 kg/m3 | +4.9 % |
| ethylene, 47 C and 80 bar (tc-PR) | Density | 157.3 kg/m3 | 156.5 kg/m3 | -0.5 % |
| natural gas (90 % methane), 15 C and 70 bar (Peng-Robinson) | Density | 61.72 kg/m3 | 63.44 kg/m3 | +2.8 % |
| natural gas (90 % methane), 15 C and 70 bar (tc-PR) | Density | 61.72 kg/m3 | 62.07 kg/m3 | +0.6 % |
| natural gas (90 % methane), 47 C and 150 bar (Peng-Robinson) | Density | 120.1 kg/m3 | 122.7 kg/m3 | +2.2 % |
| natural gas (90 % methane), 47 C and 150 bar (tc-PR) | Density | 120.1 kg/m3 | 117.6 kg/m3 | -2.0 % |

Average difference 2.1 %, largest 4.9 % (quantities given in per cent).

Reference: GERG-2008 equation for natural gas; Reference equation of state.

## 4. Unit operations

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| compressor: methane, 30 C and 20 bar to 60 bar, 75 % efficient | Work per kg of gas | 254.4 kJ/kg | 251.8 kJ/kg | -1.0 % |
| compressor: methane, 30 C and 20 bar to 60 bar, 75 % efficient | Outlet temperature | 140.9 C | 140.9 C | +0.03 C |
| valve: methane, 27 C, from 100 to 20 bar (Peng-Robinson) | Outlet temperature | -7.521 C | -10.32 C | -2.80 C |
| valve: methane, 27 C, from 100 to 20 bar (tc-PR) | Outlet temperature | -7.521 C | -10.20 C | -2.68 C |
| valve: nitrogen, 27 C, from 200 to 1 bar (Peng-Robinson) | Outlet temperature | -3.963 C | -7.750 C | -3.79 C |
| valve: nitrogen, 27 C, from 200 to 1 bar (tc-PR) | Outlet temperature | -3.963 C | -5.699 C | -1.74 C |
| valve: carbon dioxide, 47 C, from 80 to 20 bar (Peng-Robinson) | Outlet temperature | -19.50 C | -19.26 C | +0.24 C |
| valve: carbon dioxide, 47 C, from 80 to 20 bar (tc-PR) | Outlet temperature | -19.50 C | -19.45 C | +0.05 C |
| valve: saturated liquid propane at 30 C let down to 2 bar | Outlet temperature | -25.45 C | -25.42 C | +0.03 C |
| valve: saturated liquid propane at 30 C let down to 2 bar | Vapour fraction at the outlet (by mole) | 0.345 | 0.346 | +0.001 |
| pump: 1 kg/s of water at 20 C, from 1 to 11 bar, 75 % efficient | Power | 1.336 kW | 1.336 kW | -0.0 % |
| pipe: water at 20 C, 50 mm bore, 100 m, 2 m/s | Pressure drop | 87.21 kPa | 87.84 kPa | +0.7 % |

Average difference 0.6 %, largest 1.0 % (quantities given in per cent).

Reference: Hand calculation: Darcy-Weisbach with the Colebrook friction factor; Hand calculation: flow x pressure rise / efficiency; Reference equation of state.

## 5. Mixtures: azeotropes at 1 atm (activity models)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| ethanol + water (NRTL) | Azeotrope temperature | 78.20 C | 78.18 C | -0.02 C |
| ethanol + water (NRTL) | Mole fraction of ethanol in the azeotrope | 0.894 | 0.876 | -0.018 |
| ethanol + water (UNIFAC) | Azeotrope temperature | 78.20 C | 78.15 C | -0.05 C |
| ethanol + water (UNIFAC) | Mole fraction of ethanol in the azeotrope | 0.894 | 0.892 | -0.002 |
| 2-propanol + water (UNIFAC) | Azeotrope temperature | 80.30 C | 80.15 C | -0.15 C |
| 2-propanol + water (UNIFAC) | Mole fraction of 2-propanol in the azeotrope | 0.681 | 0.690 | +0.009 |
| acetone + chloroform (NRTL) | Azeotrope temperature | 64.50 C | 64.53 C | +0.03 C |
| acetone + chloroform (NRTL) | Mole fraction of acetone in the azeotrope | 0.345 | 0.337 | -0.008 |
| ethanol + benzene (NRTL) | Azeotrope temperature | 67.90 C | 68.39 C | +0.49 C |
| ethanol + benzene (NRTL) | Mole fraction of ethanol in the azeotrope | 0.448 | 0.448 | -0.000 |

Reference: Handbook azeotrope tables.

## 6. Viscosity and thermal conductivity (Peng-Robinson)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| nitrogen gas, 27 C and 1 bar | Viscosity | 17.89 uPa.s | 17.90 uPa.s | +0.1 % |
| nitrogen gas, 27 C and 1 bar | Thermal conductivity | 25.97 mW/m.K | 26.02 mW/m.K | +0.2 % |
| nitrogen gas, 27 C and 200 bar | Viscosity | 23.18 uPa.s | 23.47 uPa.s | +1.2 % |
| nitrogen gas, 27 C and 200 bar | Thermal conductivity | 37.48 mW/m.K | 38.44 mW/m.K | +2.5 % |
| methane gas, 27 C and 100 bar | Viscosity | 13.81 uPa.s | 13.62 uPa.s | -1.4 % |
| methane gas, 27 C and 100 bar | Thermal conductivity | 44.57 mW/m.K | 45.87 mW/m.K | +2.9 % |
| carbon dioxide gas, 127 C and 100 bar | Viscosity | 22.47 uPa.s | 22.82 uPa.s | +1.6 % |
| carbon dioxide gas, 127 C and 100 bar | Thermal conductivity | 31.87 mW/m.K | 32.53 mW/m.K | +2.1 % |
| hydrogen gas, 127 C and 200 bar | Viscosity | 11.09 uPa.s | 11.24 uPa.s | +1.3 % |
| hydrogen gas, 127 C and 200 bar | Thermal conductivity | 243.5 mW/m.K | 241.6 mW/m.K | -0.8 % |
| propane gas, 127 C and 30 bar | Viscosity | 11.98 uPa.s | 11.98 uPa.s | +0.0 % |
| propane gas, 127 C and 30 bar | Thermal conductivity | 34.96 mW/m.K | 34.30 mW/m.K | -1.9 % |
| water liquid, 20 C and 1 atm | Viscosity | 1.002 mPa.s | 1.002 mPa.s | -0.0 % |
| water liquid, 20 C and 1 atm | Thermal conductivity | 0.598 W/m.K | 0.598 W/m.K | +0.0 % |
| n-hexane liquid, 25 C and 1 atm | Viscosity | 0.298 mPa.s | 0.298 mPa.s | -0.0 % |
| n-hexane liquid, 25 C and 1 atm | Thermal conductivity | 0.120 W/m.K | 0.120 W/m.K | +0.0 % |
| ethanol liquid, 25 C and 1 atm | Viscosity | 1.082 mPa.s | 1.082 mPa.s | +0.0 % |
| ethanol liquid, 25 C and 1 atm | Thermal conductivity | 0.163 W/m.K | 0.163 W/m.K | -0.0 % |

Average difference 0.9 %, largest 2.9 % (quantities given in per cent).

Reference: Reference correlation.

## 7. Gases at high temperature (Peng-Robinson)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| methane at 727 C and 1 atm | Heat capacity | 71.80 J/mol.K | 71.80 J/mol.K | +0.0 % |
| methane at 1227 C and 1 atm | Heat capacity | 86.56 J/mol.K | 86.68 J/mol.K | +0.1 % |
| fired heater: 1 kmol/h of methane, 25 C to 827 C | Duty | 12.65 kW | 12.67 kW | +0.1 % |
| ethylene at 727 C and 1 atm | Heat capacity | 93.90 J/mol.K | 93.87 J/mol.K | -0.0 % |
| ethylene at 1227 C and 1 atm | Heat capacity | 110.0 J/mol.K | 110.2 J/mol.K | +0.2 % |
| fired heater: 1 kmol/h of ethylene, 25 C to 827 C | Duty | 16.74 kW | 16.75 kW | +0.1 % |
| acetylene at 727 C and 1 atm | Heat capacity | 68.28 J/mol.K | 67.89 J/mol.K | -0.6 % |
| acetylene at 1227 C and 1 atm | Heat capacity | 76.53 J/mol.K | 75.96 J/mol.K | -0.7 % |
| fired heater: 1 kmol/h of acetylene, 25 C to 827 C | Duty | 13.37 kW | 13.32 kW | -0.4 % |
| carbon monoxide at 727 C and 1 atm | Heat capacity | 33.18 J/mol.K | 33.18 J/mol.K | -0.0 % |
| carbon monoxide at 1227 C and 1 atm | Heat capacity | 35.22 J/mol.K | 35.23 J/mol.K | +0.0 % |
| fired heater: 1 kmol/h of carbon monoxide, 25 C to 827 C | Duty | 6.954 kW | 6.957 kW | +0.0 % |
| carbon dioxide at 727 C and 1 atm | Heat capacity | 54.31 J/mol.K | 54.32 J/mol.K | +0.0 % |
| carbon dioxide at 1227 C and 1 atm | Heat capacity | 58.38 J/mol.K | 58.38 J/mol.K | +0.0 % |
| fired heater: 1 kmol/h of carbon dioxide, 25 C to 827 C | Duty | 10.80 kW | 10.81 kW | +0.1 % |
| water at 727 C and 1 atm | Heat capacity | 41.27 J/mol.K | 41.30 J/mol.K | +0.1 % |
| water at 1227 C and 1 atm | Heat capacity | 47.09 J/mol.K | 47.10 J/mol.K | +0.0 % |
| ammonia at 727 C and 1 atm | Heat capacity | 56.49 J/mol.K | 56.52 J/mol.K | +0.0 % |
| ammonia at 1227 C and 1 atm | Heat capacity | 66.56 J/mol.K | 66.59 J/mol.K | +0.0 % |
| fired heater: 1 kmol/h of ammonia, 25 C to 827 C | Duty | 10.67 kW | 10.67 kW | -0.0 % |
| hydrogen sulfide at 727 C and 1 atm | Heat capacity | 45.79 J/mol.K | 45.77 J/mol.K | -0.0 % |
| hydrogen sulfide at 1227 C and 1 atm | Heat capacity | 51.48 J/mol.K | 51.49 J/mol.K | +0.0 % |
| fired heater: 1 kmol/h of hydrogen sulfide, 25 C to 827 C | Duty | 9.063 kW | 9.078 kW | +0.2 % |
| sulfur dioxide at 727 C and 1 atm | Heat capacity | 54.48 J/mol.K | 54.50 J/mol.K | +0.0 % |
| sulfur dioxide at 1227 C and 1 atm | Heat capacity | 57.04 J/mol.K | 57.05 J/mol.K | +0.0 % |
| fired heater: 1 kmol/h of sulfur dioxide, 25 C to 827 C | Duty | 11.09 kW | 11.11 kW | +0.2 % |

Average difference 0.1 %, largest 0.7 % (quantities given in per cent).

Reference: NIST-JANAF thermochemical tables.

## 8. Heating a liquid

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| water, 20 to 90 C (NRTL) | Heat taken up | 293.0 kJ/kg | 293.1 kJ/kg | +0.0 % |
| methanol, 10 to 60 C (NRTL) | Heat taken up | 130.3 kJ/kg | 130.3 kJ/kg | +0.0 % |
| ethanol, 10 to 70 C (NRTL) | Heat taken up | 154.0 kJ/kg | 154.0 kJ/kg | +0.0 % |
| acetone, 0 to 50 C (NRTL) | Heat taken up | 107.3 kJ/kg | 107.3 kJ/kg | +0.0 % |
| benzene, 10 to 75 C (NRTL) | Heat taken up | 116.2 kJ/kg | 116.1 kJ/kg | -0.0 % |
| toluene, 10 to 105 C (NRTL) | Heat taken up | 172.2 kJ/kg | 172.2 kJ/kg | +0.0 % |
| n-hexane, 0 to 65 C (NRTL) | Heat taken up | 150.0 kJ/kg | 150.0 kJ/kg | +0.0 % |
| n-decane, 10 to 167 C (NRTL) | Heat taken up | 384.5 kJ/kg | 384.5 kJ/kg | +0.0 % |
| propane, -93 to -45 C (NRTL) | Heat taken up | 102.9 kJ/kg | 102.9 kJ/kg | +0.0 % |
| ammonia, -73 to -35 C (NRTL) | Heat taken up | 166.7 kJ/kg | 166.7 kJ/kg | +0.0 % |
| water, 20 to 90 C (tc-PR) | Heat taken up | 293.0 kJ/kg | 292.3 kJ/kg | -0.3 % |
| methanol, 10 to 60 C (tc-PR) | Heat taken up | 130.3 kJ/kg | 133.4 kJ/kg | +2.4 % |
| ethanol, 10 to 70 C (tc-PR) | Heat taken up | 154.0 kJ/kg | 162.3 kJ/kg | +5.4 % |
| acetone, 0 to 50 C (tc-PR) | Heat taken up | 107.3 kJ/kg | 102.8 kJ/kg | -4.1 % |
| benzene, 10 to 75 C (tc-PR) | Heat taken up | 116.2 kJ/kg | 115.6 kJ/kg | -0.5 % |
| toluene, 10 to 105 C (tc-PR) | Heat taken up | 172.2 kJ/kg | 169.8 kJ/kg | -1.4 % |
| n-hexane, 0 to 65 C (tc-PR) | Heat taken up | 150.0 kJ/kg | 148.3 kJ/kg | -1.1 % |
| n-decane, 10 to 167 C (tc-PR) | Heat taken up | 384.5 kJ/kg | 383.2 kJ/kg | -0.3 % |
| propane, -93 to -45 C (tc-PR) | Heat taken up | 102.9 kJ/kg | 102.3 kJ/kg | -0.6 % |
| ammonia, -73 to -35 C (tc-PR) | Heat taken up | 166.7 kJ/kg | 171.9 kJ/kg | +3.1 % |
| water, 20 to 90 C (Peng-Robinson) | Heat taken up | 293.0 kJ/kg | 292.3 kJ/kg | -0.3 % |
| methanol, 10 to 60 C (Peng-Robinson) (a polar liquid, for which the program advises against this package) | Heat taken up | 130.3 kJ/kg | 177.0 kJ/kg | +35.9 % |
| ethanol, 10 to 70 C (Peng-Robinson) (a polar liquid, for which the program advises against this package) | Heat taken up | 154.0 kJ/kg | 187.9 kJ/kg | +22.0 % |
| acetone, 0 to 50 C (Peng-Robinson) (a polar liquid, for which the program advises against this package) | Heat taken up | 107.3 kJ/kg | 103.6 kJ/kg | -3.4 % |
| benzene, 10 to 75 C (Peng-Robinson) | Heat taken up | 116.2 kJ/kg | 103.4 kJ/kg | -11.0 % |
| toluene, 10 to 105 C (Peng-Robinson) | Heat taken up | 172.2 kJ/kg | 162.0 kJ/kg | -5.9 % |
| n-hexane, 0 to 65 C (Peng-Robinson) | Heat taken up | 150.0 kJ/kg | 144.4 kJ/kg | -3.7 % |
| n-decane, 10 to 167 C (Peng-Robinson) | Heat taken up | 384.5 kJ/kg | 370.7 kJ/kg | -3.6 % |
| propane, -93 to -45 C (Peng-Robinson) | Heat taken up | 102.9 kJ/kg | 96.73 kJ/kg | -6.0 % |
| ammonia, -73 to -35 C (Peng-Robinson) (a polar liquid, for which the program advises against this package) | Heat taken up | 166.7 kJ/kg | 165.6 kJ/kg | -0.7 % |

Average difference 3.7 %, largest 35.9 % (quantities given in per cent).

Reference: Reference equation of state.

## 9. Reactions, combustion and heat integration

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| ammonia synthesis, N2 + 3 H2 = 2 NH3, at 700 K | ln K | -9.343 | -9.468 | -0.124 |
| water-gas shift, CO + H2O = CO2 + H2, at 1000 K | Equilibrium constant K | 1.442 | 1.435 | -0.5 % |
| methane burnt in the exact amount of air, from 25 C | Adiabatic flame temperature (no dissociation) | 2327.2 K | 2327.5 K | +0.32 K |
| methane burnt in air, products cooled to 127 C | Heat released per mole of methane | 769.0 kJ/mol | 769.3 kJ/mol | +0.0 % |
| four-stream heat integration problem, minimum approach 10 C | Minimum hot utility | 20.00 kW | 20.00 kW | +0.0 % |
| four-stream heat integration problem, minimum approach 10 C | Minimum cold utility | 60.00 kW | 60.00 kW | +0.0 % |
| four-stream heat integration problem, minimum approach 10 C | Pinch temperature, hot side | 90.00 C | 90.00 C | +0.00 C |

Average difference 0.1 %, largest 0.5 % (quantities given in per cent).

Reference: NIST-JANAF thermochemical tables; NIST-JANAF thermochemical tables (energy balance on the products); NIST-JANAF thermochemical tables (heats of formation and heat capacities); Textbook problem (Linnhoff and Hindmarsh 1983; Kemp, Pinch Analysis and Process Integration).

## 10. Mixtures of light hydrocarbons and gases: bubble and dew pressure (Peng-Robinson)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| 50 % methane + 50 % ethane at -73 C | Bubble pressure | 26.39 bar | 26.03 bar | -1.4 % |
| 50 % methane + 50 % ethane at -73 C | Dew pressure | 4.409 bar | 4.386 bar | -0.5 % |
| 50 % methane + 50 % ethane at -23 C | Bubble pressure | 63.03 bar | 61.28 bar | -2.8 % |
| 50 % methane + 50 % ethane at -23 C | Dew pressure | 29.66 bar | 29.19 bar | -1.6 % |
| 30 % methane + 70 % propane at 4 C | Bubble pressure | 50.19 bar | 49.69 bar | -1.0 % |
| 30 % methane + 70 % propane at 4 C | Dew pressure | 8.169 bar | 8.052 bar | -1.4 % |
| 50 % ethane + 50 % propane at 27 C | Bubble pressure | 23.75 bar | 24.12 bar | +1.5 % |
| 50 % ethane + 50 % propane at 27 C | Dew pressure | 17.09 bar | 17.17 bar | +0.5 % |
| 50 % propane + 50 % n-butane at 47 C | Bubble pressure | 9.827 bar | 9.909 bar | +0.8 % |
| 50 % propane + 50 % n-butane at 47 C | Dew pressure | 7.251 bar | 7.282 bar | +0.4 % |
| 30 % methane + 70 % carbon dioxide at -23 C | Bubble pressure | 71.73 bar | 71.15 bar | -0.8 % |
| 30 % methane + 70 % carbon dioxide at -23 C | Dew pressure | 27.71 bar | 27.31 bar | -1.5 % |
| 30 % nitrogen + 70 % methane at -123 C | Bubble pressure | 29.77 bar | 29.75 bar | -0.1 % |
| 30 % nitrogen + 70 % methane at -123 C | Dew pressure | 15.40 bar | 15.43 bar | +0.2 % |
| 40 % carbon dioxide + 60 % propane at 7 C | Bubble pressure | 24.95 bar | 24.98 bar | +0.1 % |
| 40 % carbon dioxide + 60 % propane at 7 C | Dew pressure | 9.766 bar | 9.829 bar | +0.6 % |
| 30 % methane + 70 % n-butane at 37 C | Bubble pressure | 66.31 bar | 63.58 bar | -4.1 % |
| 30 % methane + 70 % n-butane at 37 C | Dew pressure | 5.141 bar | 5.100 bar | -0.8 % |
| 50 % ethane + 50 % n-heptane at 77 C | Bubble pressure | 38.07 bar | 35.71 bar | -6.2 % |
| 50 % ethane + 50 % n-heptane at 77 C | Dew pressure | 1.039 bar | 1.045 bar | +0.6 % |

Average difference 1.3 %, largest 6.2 % (quantities given in per cent).

Reference: GERG-2008 equation for natural gas.

## 11. Polar liquids boiling under pressure (NRTL-PR)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| water at 5 bar | Boiling temperature | 151.8 C | 151.8 C | -0.02 C |
| water at 5 bar | Heat of vaporisation | 2108.0 kJ/kg | 2117.7 kJ/kg | +0.5 % |
| water at 15 bar | Boiling temperature | 198.3 C | 198.3 C | +0.01 C |
| water at 15 bar | Heat of vaporisation | 1946.4 kJ/kg | 1975.6 kJ/kg | +1.5 % |
| ethanol at 5 bar | Boiling temperature | 125.3 C | 125.3 C | +0.03 C |
| ethanol at 5 bar | Heat of vaporisation | 755.5 kJ/kg | 760.4 kJ/kg | +0.6 % |
| ethanol at 15 bar | Boiling temperature | 167.5 C | 167.4 C | -0.06 C |
| ethanol at 15 bar | Heat of vaporisation | 632.9 kJ/kg | 646.6 kJ/kg | +2.2 % |
| methanol at 5 bar | Boiling temperature | 111.4 C | 111.4 C | +0.06 C |
| methanol at 5 bar | Heat of vaporisation | 991.5 kJ/kg | 1009.7 kJ/kg | +1.8 % |
| methanol at 15 bar | Boiling temperature | 153.1 C | 153.3 C | +0.19 C |
| methanol at 15 bar | Heat of vaporisation | 847.3 kJ/kg | 894.7 kJ/kg | +5.6 % |
| acetone at 5 bar | Boiling temperature | 111.9 C | 111.9 C | +0.00 C |
| acetone at 5 bar | Heat of vaporisation | 432.6 kJ/kg | 436.9 kJ/kg | +1.0 % |
| acetone at 15 bar | Boiling temperature | 164.3 C | 164.5 C | +0.14 C |
| acetone at 15 bar | Heat of vaporisation | 345.4 kJ/kg | 357.4 kJ/kg | +3.5 % |
| benzene at 5 bar | Boiling temperature | 142.7 C | 142.6 C | -0.03 C |
| benzene at 5 bar | Heat of vaporisation | 343.0 kJ/kg | 342.4 kJ/kg | -0.2 % |
| benzene at 15 bar | Boiling temperature | 202.6 C | 202.7 C | +0.01 C |
| benzene at 15 bar | Heat of vaporisation | 280.0 kJ/kg | 281.3 kJ/kg | +0.5 % |

Average difference 1.7 %, largest 5.6 % (quantities given in per cent).

Reference: Reference equation of state.

## 12. Mixtures: measured boiling of binary liquids at 1 atm (NRTL and UNIFAC)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| methanol + water, 10 mol % methanol in the liquid (NRTL) | Mole fraction of methanol in the vapour | 0.418 | 0.425 | +0.007 |
| methanol + water, 10 mol % methanol in the liquid (NRTL) | Boiling temperature | 87.70 C | 87.60 C | -0.10 C |
| methanol + water, 30 mol % methanol in the liquid (NRTL) | Mole fraction of methanol in the vapour | 0.665 | 0.673 | +0.008 |
| methanol + water, 30 mol % methanol in the liquid (NRTL) | Boiling temperature | 78.00 C | 77.82 C | -0.18 C |
| methanol + water, 50 mol % methanol in the liquid (NRTL) | Mole fraction of methanol in the vapour | 0.779 | 0.786 | +0.007 |
| methanol + water, 50 mol % methanol in the liquid (NRTL) | Boiling temperature | 73.10 C | 72.91 C | -0.19 C |
| methanol + water, 80 mol % methanol in the liquid (NRTL) | Mole fraction of methanol in the vapour | 0.915 | 0.916 | +0.001 |
| methanol + water, 80 mol % methanol in the liquid (NRTL) | Boiling temperature | 67.60 C | 67.57 C | -0.03 C |
| methanol + water, 10 mol % methanol in the liquid (UNIFAC) | Mole fraction of methanol in the vapour | 0.418 | 0.423 | +0.005 |
| methanol + water, 30 mol % methanol in the liquid (UNIFAC) | Mole fraction of methanol in the vapour | 0.665 | 0.669 | +0.004 |
| methanol + water, 50 mol % methanol in the liquid (UNIFAC) | Mole fraction of methanol in the vapour | 0.779 | 0.786 | +0.007 |
| methanol + water, 80 mol % methanol in the liquid (UNIFAC) | Mole fraction of methanol in the vapour | 0.915 | 0.919 | +0.004 |
| ethanol + water, 10 mol % ethanol in the liquid (NRTL) | Mole fraction of ethanol in the vapour | 0.438 | 0.435 | -0.003 |
| ethanol + water, 10 mol % ethanol in the liquid (NRTL) | Boiling temperature | 86.70 C | 86.76 C | +0.06 C |
| ethanol + water, 33 mol % ethanol in the liquid (NRTL) | Mole fraction of ethanol in the vapour | 0.583 | 0.597 | +0.014 |
| ethanol + water, 33 mol % ethanol in the liquid (NRTL) | Boiling temperature | 81.50 C | 81.08 C | -0.42 C |
| ethanol + water, 51 mol % ethanol in the liquid (NRTL) | Mole fraction of ethanol in the vapour | 0.656 | 0.661 | +0.005 |
| ethanol + water, 51 mol % ethanol in the liquid (NRTL) | Boiling temperature | 79.80 C | 79.62 C | -0.18 C |
| ethanol + water, 75 mol % ethanol in the liquid (NRTL) | Mole fraction of ethanol in the vapour | 0.781 | 0.780 | -0.001 |
| ethanol + water, 75 mol % ethanol in the liquid (NRTL) | Boiling temperature | 78.41 C | 78.39 C | -0.02 C |
| ethanol + water, 10 mol % ethanol in the liquid (UNIFAC) | Mole fraction of ethanol in the vapour | 0.438 | 0.446 | +0.008 |
| ethanol + water, 33 mol % ethanol in the liquid (UNIFAC) | Mole fraction of ethanol in the vapour | 0.583 | 0.581 | -0.002 |
| ethanol + water, 51 mol % ethanol in the liquid (UNIFAC) | Mole fraction of ethanol in the vapour | 0.656 | 0.657 | +0.001 |
| ethanol + water, 75 mol % ethanol in the liquid (UNIFAC) | Mole fraction of ethanol in the vapour | 0.781 | 0.787 | +0.006 |
| acetone + water, 10 mol % acetone in the liquid (NRTL) | Mole fraction of acetone in the vapour | 0.730 | 0.744 | +0.014 |
| acetone + water, 10 mol % acetone in the liquid (NRTL) | Boiling temperature | 68.53 C | 67.17 C | -1.36 C |
| acetone + water, 30 mol % acetone in the liquid (NRTL) | Mole fraction of acetone in the vapour | 0.812 | 0.805 | -0.007 |
| acetone + water, 30 mol % acetone in the liquid (NRTL) | Boiling temperature | 61.87 C | 62.16 C | +0.29 C |
| acetone + water, 50 mol % acetone in the liquid (NRTL) | Mole fraction of acetone in the vapour | 0.839 | 0.839 | -0.000 |
| acetone + water, 50 mol % acetone in the liquid (NRTL) | Boiling temperature | 59.95 C | 59.79 C | -0.16 C |
| acetone + water, 80 mol % acetone in the liquid (NRTL) | Mole fraction of acetone in the vapour | 0.895 | 0.897 | +0.002 |
| acetone + water, 80 mol % acetone in the liquid (NRTL) | Boiling temperature | 57.49 C | 57.08 C | -0.41 C |
| acetone + water, 10 mol % acetone in the liquid (UNIFAC) | Mole fraction of acetone in the vapour | 0.730 | 0.741 | +0.010 |
| acetone + water, 30 mol % acetone in the liquid (UNIFAC) | Mole fraction of acetone in the vapour | 0.812 | 0.809 | -0.003 |
| acetone + water, 50 mol % acetone in the liquid (UNIFAC) | Mole fraction of acetone in the vapour | 0.839 | 0.840 | +0.001 |
| acetone + water, 80 mol % acetone in the liquid (UNIFAC) | Mole fraction of acetone in the vapour | 0.895 | 0.899 | +0.004 |

Reference: Measured vapour-liquid equilibrium at 101.3 kPa (Perry's Chemical Engineers' Handbook, table of binary data).

## 13. Two liquid phases: mutual solubility of water and 1-butanol at 25 C (UNIFAC)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| water + 1-butanol, the water-rich liquid | Mole fraction of 1-butanol | 0.0190 | 0.0196 | +0.001 |
| water + 1-butanol, the butanol-rich liquid | Mole fraction of water | 0.510 | 0.518 | +0.008 |

Reference: Measured mutual solubility at 25 C (IUPAC-NIST Solubility Data Series, 1-butanol with water).

## 14. Reaction in a liquid on a resin catalyst: TAME at equilibrium, eleven runs at 325 to 363 K (UNIFAC)

| Case | Quantity | Reference | Enthalpia | Difference |
|---|---|---:|---:|---:|
| methanol / isoamylenes = 1 at 51.5 C | Mole fraction of the ether at equilibrium | 0.198 | 0.188 | -0.010 |
| methanol / isoamylenes = 1 at 51.5 C | Activity coefficient of methanol | 7.223 | 7.216 | -0.1 % |
| methanol / isoamylenes = 0.5 at 52.1 C | Mole fraction of the ether at equilibrium | 0.129 | 0.123 | -0.006 |
| methanol / isoamylenes = 0.5 at 52.1 C | Activity coefficient of methanol | 11.52 | 11.56 | +0.3 % |
| methanol / isoamylenes = 1 at 70.2 C | Mole fraction of the ether at equilibrium | 0.163 | 0.156 | -0.007 |
| methanol / isoamylenes = 1 at 70.2 C | Activity coefficient of methanol | 6.196 | 6.209 | +0.2 % |
| methanol / isoamylenes = 0.5 at 71.1 C | Mole fraction of the ether at equilibrium | 0.115 | 0.108 | -0.007 |
| methanol / isoamylenes = 0.5 at 71.1 C | Activity coefficient of methanol | 9.627 | 9.662 | +0.4 % |
| methanol / isoamylenes = 2 at 71.5 C | Mole fraction of the ether at equilibrium | 0.155 | 0.151 | -0.004 |
| methanol / isoamylenes = 2 at 71.5 C | Activity coefficient of methanol | 3.026 | 3.022 | -0.1 % |
| methanol / isoamylenes = 1 at 79.5 C | Mole fraction of the ether at equilibrium | 0.148 | 0.141 | -0.007 |
| methanol / isoamylenes = 1 at 79.5 C | Activity coefficient of methanol | 5.918 | 5.929 | +0.2 % |
| methanol / isoamylenes = 0.5 at 80.1 C | Mole fraction of the ether at equilibrium | 0.104 | 0.0992 | -0.005 |
| methanol / isoamylenes = 0.5 at 80.1 C | Activity coefficient of methanol | 8.910 | 8.930 | +0.2 % |
| methanol / isoamylenes = 1 at 85.5 C | Mole fraction of the ether at equilibrium | 0.138 | 0.131 | -0.007 |
| methanol / isoamylenes = 1 at 85.5 C | Activity coefficient of methanol | 5.369 | 5.373 | +0.1 % |
| methanol / isoamylenes = 2 at 89.1 C | Mole fraction of the ether at equilibrium | 0.127 | 0.125 | -0.002 |
| methanol / isoamylenes = 2 at 89.1 C | Activity coefficient of methanol | 2.839 | 2.837 | -0.1 % |
| methanol / isoamylenes = 0.5 at 89.9 C | Mole fraction of the ether at equilibrium | 0.0930 | 0.0892 | -0.004 |
| methanol / isoamylenes = 0.5 at 89.9 C | Activity coefficient of methanol | 8.149 | 8.167 | +0.2 % |

Average difference 0.2 %, largest 0.4 % (quantities given in per cent).

Reference: Measured in a batch reactor on Amberlyst 15 (Ferreira and Loureiro, Ind. Eng. Chem. Res. 43 (2004) 5156, Table 1 and equations 6 and 7).

## What this says

- **Steam and water** with the steam-table package agree with the international tables to the last digit shown: the package is those tables.
- **A cubic equation of state (Peng-Robinson)** gives boiling points and vapour pressures of hydrocarbons and light gases to about 1 %, gas densities at pressure to 1-3 % (5 % for hydrogen), and compressor work to about 1 %. The cooling of a gas through a valve is its hardest test: over a very large pressure drop (nitrogen from 200 bar to 1 bar) the outlet comes out up to 4 C too cold. That is what this equation gives in any simulator; it is the equation that limits it, not the program.
- **Liquid density** from a cubic equation is its known weak point, so Enthalpia corrects it; the table shows what remains.
- **Water with hydrocarbons and gases** in the Peng-Robinson packages: water has the interaction parameters Peng and Robinson gave for these pairs, and a stream that holds both is flashed with free water allowed, so gas, oil and water come out as three phases. The temperature at which water starts to condense from methane at 100 bar is within 3 C of the GERG-2008 equation (it was 11 C low).
- **Water** has a temperature function of its own inside Peng-Robinson, PR78 and SRK, as it has in the commercial simulators: it boils within 0.05 C of the steam tables and heating liquid water is within 1 %. Other polar liquids (alcohols, ammonia) are outside what these equations are made for: for polar mixtures use an activity model: the program says so when the package is chosen.
- **Mixtures of light hydrocarbons and gases** boil and condense within 1 to 3 % of the pressure the GERG-2008 standard gives; for pairs of very different size (ethane with heptane) the bubble pressure is up to 6 % low.
- **Reactions and combustion**: equilibrium constants, the heat of combustion and the flame temperature of methane agree with the JANAF tables (flame temperature within 1 K).
- **Polar liquids under pressure** with NRTL-PR (the activity model with a real-gas vapour) boil within 0.3 C of the reference at 15 bar, with heats of vaporisation within a few per cent. With an ideal-gas vapour (plain NRTL) the heat of vaporisation is 3 to 5 % high at 5 bar; the program warns above 5 bar.
- **Azeotropes** with the activity models land within 0.5 C and 2 mole per cent of the handbook values. One pair here (2-propanol and water) has no fitted NRTL parameters in the database; the program says so when NRTL is picked and recommends UNIFAC, which is what the table uses.
- **Viscosity and thermal conductivity** are estimates by the handbook methods, good to a few per cent for gases up to several hundred bar.
- **Hot gases** (furnaces, reformers, reactors): heat capacities and heating duties agree with the JANAF tables to within 1 % up to 1500 K.
- **Heating a liquid** is exact with the activity models, which use the measured heat capacity of each liquid. With the classic Peng-Robinson equation the heat capacity of a liquid comes out of the equation itself and is 3 to 11 % off for hydrocarbons and far off for alcohols: the largest known weakness of the classic cubic equations, in any simulator. The **tc-PR** package (the translated-consistent Peng-Robinson equation of 2016, with parameters fitted for each compound) brings this to about 1 % for hydrocarbons and water and a few per cent for alcohols, and is the equation of state to choose when duties on liquid streams matter.

If you have a case where Enthalpia disagrees with a measured or published value, please report it (Help > Report a problem in the program, or an issue on this page): that is how this table grows.

## Side by side with a commercial simulator

The same cases were run in Enthalpia and in a widely used commercial process simulator ("Program A" in the guide), with the same property package in both, and both are set beside the reference value. This separates what a property package gives in any simulator from what is particular to Enthalpia.

Of 227 quantities calculated by both programs, Enthalpia and Program A agree within 1 % (or 0.5 C) on 157. Where there is a reference value (166 quantities), Enthalpia is as close to it as Program A or closer on 115.

### Gases under pressure

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| methane gas, 27 C and 100 bar (Peng-Robinson) | Density | 75.18 kg/m3 | 77.09 kg/m3 (+2.5 %) | 77.13 kg/m3 (+2.6 %) | 74.89 kg/m3 (-0.4 %) |
| methane gas, 27 C and 100 bar (Peng-Robinson) | Viscosity | 13.81 uPa.s | 14.15 uPa.s (+2.4 %) | 13.62 uPa.s (-1.4 %) | 13.50 uPa.s (-2.3 %) |
| methane gas, 27 C and 100 bar (Peng-Robinson) | Thermal conductivity | 44.57 mW/m.K | 44.66 mW/m.K (+0.2 %) | 45.87 mW/m.K (+2.9 %) | 45.48 mW/m.K (+2.1 %) |
| nitrogen gas, 27 C and 200 bar (Peng-Robinson) | Density | 212.5 kg/m3 | 218.3 kg/m3 (+2.7 %) | 218.6 kg/m3 (+2.8 %) | 208.5 kg/m3 (-1.9 %) |
| nitrogen gas, 27 C and 200 bar (Peng-Robinson) | Viscosity | 23.18 uPa.s | 24.02 uPa.s (+3.6 %) | 23.47 uPa.s (+1.2 %) | 23.02 uPa.s (-0.7 %) |
| nitrogen gas, 27 C and 200 bar (Peng-Robinson) | Thermal conductivity | 37.48 mW/m.K | 38.34 mW/m.K (+2.3 %) | 38.44 mW/m.K (+2.5 %) | 37.63 mW/m.K (+0.4 %) |
| carbon dioxide gas, 77 C and 100 bar (Peng-Robinson) | Density | 228.8 kg/m3 | 231.4 kg/m3 (+1.1 %) | 232.2 kg/m3 (+1.5 %) | 230.2 kg/m3 (+0.6 %) |
| carbon dioxide gas, 77 C and 100 bar (Peng-Robinson) | Viscosity | 22.03 uPa.s | 23.95 uPa.s (+8.7 %) | 22.99 uPa.s (+4.4 %) | 22.91 uPa.s (+4.0 %) |
| carbon dioxide gas, 77 C and 100 bar (Peng-Robinson) | Thermal conductivity | 33.90 mW/m.K | 33.63 mW/m.K (-0.8 %) | 32.27 mW/m.K (-4.8 %) | 32.16 mW/m.K (-5.1 %) |
| nitrogen gas, 27 C and 1 bar (Peng-Robinson) | Density | 1.123 kg/m3 | 1.124 kg/m3 (+0.0 %) | 1.124 kg/m3 (+0.0 %) | 1.123 kg/m3 (-0.0 %) |
| nitrogen gas, 27 C and 1 bar (Peng-Robinson) | Viscosity | 17.89 uPa.s | 18.41 uPa.s (+2.9 %) | 17.90 uPa.s (+0.1 %) | 17.90 uPa.s (+0.1 %) |
| nitrogen gas, 27 C and 1 bar (Peng-Robinson) | Thermal conductivity | 25.97 mW/m.K | 25.79 mW/m.K (-0.7 %) | 26.02 mW/m.K (+0.2 %) | 26.02 mW/m.K (+0.2 %) |
| carbon dioxide gas, 127 C and 100 bar (Peng-Robinson) | Density | 161.5 kg/m3 | 162.7 kg/m3 (+0.7 %) | 163.2 kg/m3 (+1.0 %) | 161.8 kg/m3 (+0.1 %) |
| carbon dioxide gas, 127 C and 100 bar (Peng-Robinson) | Viscosity | 22.47 uPa.s | 24.45 uPa.s (+8.8 %) | 22.82 uPa.s (+1.6 %) | 22.78 uPa.s (+1.4 %) |
| carbon dioxide gas, 127 C and 100 bar (Peng-Robinson) | Thermal conductivity | 31.87 mW/m.K | 33.53 mW/m.K (+5.2 %) | 32.53 mW/m.K (+2.1 %) | 32.45 mW/m.K (+1.8 %) |
| propane gas, 127 C and 30 bar (Peng-Robinson) | Density | 50.55 kg/m3 | 51.83 kg/m3 (+2.5 %) | 51.85 kg/m3 (+2.6 %) | 51.67 kg/m3 (+2.2 %) |
| propane gas, 127 C and 30 bar (Peng-Robinson) | Viscosity | 11.98 uPa.s | 12.66 uPa.s (+5.6 %) | 11.98 uPa.s (+0.0 %) | 11.98 uPa.s (-0.0 %) |
| propane gas, 127 C and 30 bar (Peng-Robinson) | Thermal conductivity | 34.96 mW/m.K | 32.17 mW/m.K (-8.0 %) | 34.30 mW/m.K (-1.9 %) | 34.29 mW/m.K (-1.9 %) |
| natural gas (90 % methane), 15 C and 70 bar (Peng-Robinson) | Density | 61.72 kg/m3 | 63.34 kg/m3 (+2.6 %) | 63.44 kg/m3 (+2.8 %) | 62.07 kg/m3 (+0.6 %) |
| natural gas (90 % methane), 15 C and 70 bar (Peng-Robinson) | Viscosity | - | 13.05 uPa.s | 12.45 uPa.s | 12.39 uPa.s |
| natural gas (90 % methane), 15 C and 70 bar (Peng-Robinson) | Thermal conductivity | - | 38.35 mW/m.K | 39.18 mW/m.K | 38.98 mW/m.K |
| natural gas (90 % methane), 47 C and 150 bar (Peng-Robinson) | Density | 120.1 kg/m3 | 122.6 kg/m3 (+2.2 %) | 122.7 kg/m3 (+2.2 %) | 117.6 kg/m3 (-2.0 %) |
| natural gas (90 % methane), 47 C and 150 bar (Peng-Robinson) | Viscosity | - | 17.31 uPa.s | 16.96 uPa.s | 16.58 uPa.s |
| natural gas (90 % methane), 47 C and 150 bar (Peng-Robinson) | Thermal conductivity | - | 53.11 mW/m.K | 54.63 mW/m.K | 53.50 mW/m.K |
| hydrogen gas, 27 C and 350 bar (Peng-Robinson) | Density | 23.19 kg/m3 | 24.44 kg/m3 (+5.4 %) | 24.32 kg/m3 (+4.9 %) | 24.32 kg/m3 (+4.9 %) |
| hydrogen gas, 27 C and 350 bar (Peng-Robinson) | Viscosity | 9.742 uPa.s | 10.00 uPa.s (+2.7 %) | 10.14 uPa.s (+4.0 %) | 10.14 uPa.s (+4.0 %) |
| hydrogen gas, 27 C and 350 bar (Peng-Robinson) | Thermal conductivity | 214.2 mW/m.K | 201.2 mW/m.K (-6.1 %) | 214.9 mW/m.K (+0.3 %) | 214.9 mW/m.K (+0.3 %) |
| synthesis gas (H2 60 %, N2 20 %, CO 10 %, CO2 10 %), 327 C and 100 bar (Peng-Robinson) | Density | - | 27.30 kg/m3 | 27.36 kg/m3 | 27.23 kg/m3 |
| synthesis gas (H2 60 %, N2 20 %, CO 10 %, CO2 10 %), 327 C and 100 bar (Peng-Robinson) | Viscosity | - | 23.12 uPa.s | 27.65 uPa.s | 27.65 uPa.s |
| synthesis gas (H2 60 %, N2 20 %, CO 10 %, CO2 10 %), 327 C and 100 bar (Peng-Robinson) | Thermal conductivity | - | 139.1 mW/m.K | 169.1 mW/m.K | 169.1 mW/m.K |
| steam, 400 C and 40 bar (Peng-Robinson) | Density | 13.62 kg/m3 | 13.72 kg/m3 (+0.8 %) | 13.72 kg/m3 (+0.8 %) | 13.78 kg/m3 (+1.2 %) |
| steam, 400 C and 40 bar (Peng-Robinson) | Viscosity | 24.40 uPa.s | 24.81 uPa.s (+1.7 %) | 24.70 uPa.s (+1.2 %) | 24.70 uPa.s (+1.2 %) |
| steam, 400 C and 40 bar (Peng-Robinson) | Thermal conductivity | 59.23 mW/m.K | 58.94 mW/m.K (-0.5 %) | 60.82 mW/m.K (+2.7 %) | 60.84 mW/m.K (+2.7 %) |
| propane gas, 127 C and 30 bar (SRK) | Density | 50.55 kg/m3 | 50.37 kg/m3 (-0.4 %) | 50.39 kg/m3 (-0.3 %) | - |
| propane gas, 127 C and 30 bar (SRK) | Viscosity | 11.98 uPa.s | 12.61 uPa.s (+5.2 %) | 11.94 uPa.s (-0.4 %) | - |
| propane gas, 127 C and 30 bar (SRK) | Thermal conductivity | 34.96 mW/m.K | 32.07 mW/m.K (-8.3 %) | 34.20 mW/m.K (-2.2 %) | - |
| propylene gas, 127 C and 30 bar (SRK) | Density | 46.65 kg/m3 | 46.37 kg/m3 (-0.6 %) | 46.45 kg/m3 (-0.4 %) | - |
| propylene gas, 127 C and 30 bar (SRK) | Viscosity | 13.06 uPa.s | 12.98 uPa.s (-0.7 %) | 12.46 uPa.s (-4.7 %) | - |
| propylene gas, 127 C and 30 bar (SRK) | Thermal conductivity | 34.32 mW/m.K | 30.55 mW/m.K (-11.0 %) | 32.32 mW/m.K (-5.8 %) | - |

Reference: reference equation of state and correlations. In brackets: the difference from the reference.

### Boiling at a given pressure

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| methane boiling at 1 atm (Peng-Robinson) | Boiling temperature | -161.5 C | -161.6 C (-0.11) | -161.6 C (-0.09) | -161.5 C (-0.03) |
| methane boiling at 1 atm (Peng-Robinson) | Heat of vaporisation | 510.8 kJ/kg | 512.2 kJ/kg (+0.3 %) | 511.7 kJ/kg (+0.2 %) | 510.0 kJ/kg (-0.2 %) |
| methane boiling at 1 atm (Peng-Robinson) | Liquid density | 422.4 kg/m3 | 423.5 kg/m3 (+0.3 %) | 427.0 kg/m3 (+1.1 %) | 426.9 kg/m3 (+1.1 %) |
| propane boiling at 1 atm (Peng-Robinson) | Boiling temperature | -42.11 C | -42.19 C (-0.08) | -42.19 C (-0.07) | -42.05 C (+0.06) |
| propane boiling at 1 atm (Peng-Robinson) | Heat of vaporisation | 425.6 kJ/kg | 424.2 kJ/kg (-0.3 %) | 424.1 kJ/kg (-0.4 %) | 428.9 kJ/kg (+0.8 %) |
| propane boiling at 1 atm (Peng-Robinson) | Liquid density | 580.9 kg/m3 | 581.5 kg/m3 (+0.1 %) | 581.0 kg/m3 (+0.0 %) | 580.8 kg/m3 (-0.0 %) |
| n-butane boiling at 1 atm (Peng-Robinson) | Boiling temperature | -0.490 C | -0.386 C (+0.10) | -0.429 C (+0.06) | -0.481 C (+0.01) |
| n-butane boiling at 1 atm (Peng-Robinson) | Heat of vaporisation | 385.7 kJ/kg | 386.3 kJ/kg (+0.2 %) | 386.3 kJ/kg (+0.1 %) | 387.8 kJ/kg (+0.5 %) |
| n-butane boiling at 1 atm (Peng-Robinson) | Liquid density | 601.3 kg/m3 | 601.6 kg/m3 (+0.1 %) | 601.2 kg/m3 (-0.0 %) | 601.3 kg/m3 (-0.0 %) |
| n-hexane boiling at 1 atm (Peng-Robinson) | Boiling temperature | 68.72 C | 69.01 C (+0.30) | 68.77 C (+0.06) | 68.76 C (+0.04) |
| n-hexane boiling at 1 atm (Peng-Robinson) | Heat of vaporisation | 335.1 kJ/kg | 336.5 kJ/kg (+0.4 %) | 336.3 kJ/kg (+0.4 %) | 336.6 kJ/kg (+0.4 %) |
| n-hexane boiling at 1 atm (Peng-Robinson) | Liquid density | 613.4 kg/m3 | 614.4 kg/m3 (+0.2 %) | 613.3 kg/m3 (-0.0 %) | 613.3 kg/m3 (-0.0 %) |
| water boiling at 1 atm (Peng-Robinson) | Boiling temperature | 99.97 C | 100.00 C (+0.02) | 99.95 C (-0.03) | 99.95 C (-0.03) |
| water boiling at 1 atm (Peng-Robinson) | Heat of vaporisation | 2256.5 kJ/kg | 2256.5 kJ/kg (+0.0 %) | 2266.0 kJ/kg (+0.4 %) | 2266.0 kJ/kg (+0.4 %) |
| water boiling at 1 atm (Peng-Robinson) | Liquid density | 958.4 kg/m3 | 947.9 kg/m3 (-1.1 %) | 958.4 kg/m3 (+0.0 %) | 958.4 kg/m3 (+0.0 %) |
| ammonia boiling at 1 atm (Peng-Robinson) | Boiling temperature | -33.32 C | -32.99 C (+0.32) | -33.06 C (+0.26) | -33.90 C (-0.59) |
| ammonia boiling at 1 atm (Peng-Robinson) | Heat of vaporisation | 1369.7 kJ/kg | 1391.6 kJ/kg (+1.6 %) | 1393.4 kJ/kg (+1.7 %) | 1371.7 kJ/kg (+0.1 %) |
| ammonia boiling at 1 atm (Peng-Robinson) | Liquid density | 681.6 kg/m3 | 673.1 kg/m3 (-1.3 %) | 681.3 kg/m3 (-0.0 %) | 682.4 kg/m3 (+0.1 %) |
| water boiling at 1 atm (NRTL) | Boiling temperature | 99.97 C | 100.00 C (+0.02) | 99.97 C (-0.00) | - |
| water boiling at 1 atm (NRTL) | Heat of vaporisation | 2256.5 kJ/kg | 2256.5 kJ/kg (+0.0 %) | 2256.5 kJ/kg (-0.0 %) | - |
| water boiling at 1 atm (NRTL) | Liquid density | 958.4 kg/m3 | 947.9 kg/m3 (-1.1 %) | 958.4 kg/m3 (+0.0 %) | - |
| water boiling at 5 bar (NRTL) | Boiling temperature | 151.8 C | 151.9 C (+0.02) | 151.8 C (-0.00) | - |
| water boiling at 5 bar (NRTL) | Heat of vaporisation | 2108.0 kJ/kg | 2106.7 kJ/kg (-0.1 %) | 2134.3 kJ/kg (+1.2 %) | - |
| water boiling at 5 bar (NRTL) | Liquid density | 915.3 kg/m3 | 902.0 kg/m3 (-1.5 %) | 915.3 kg/m3 (+0.0 %) | - |
| ethanol boiling at 1 atm (NRTL) | Boiling temperature | 78.42 C | 78.17 C (-0.25) | 78.42 C (+0.00) | - |
| ethanol boiling at 1 atm (NRTL) | Heat of vaporisation | 849.6 kJ/kg | 835.4 kJ/kg (-1.7 %) | 849.6 kJ/kg (-0.0 %) | - |
| ethanol boiling at 1 atm (NRTL) | Liquid density | 736.4 kg/m3 | 735.6 kg/m3 (-0.1 %) | 736.4 kg/m3 (+0.0 %) | - |
| ethanol boiling at 5 bar (NRTL) | Boiling temperature | 125.3 C | 125.0 C (-0.29) | 125.3 C (+0.00) | - |
| ethanol boiling at 5 bar (NRTL) | Heat of vaporisation | 755.5 kJ/kg | 740.2 kJ/kg (-2.0 %) | 778.2 kJ/kg (+3.0 %) | - |
| ethanol boiling at 5 bar (NRTL) | Liquid density | 684.2 kg/m3 | 681.8 kg/m3 (-0.3 %) | 684.2 kg/m3 (-0.0 %) | - |
| methanol boiling at 1 atm (NRTL) | Boiling temperature | 64.48 C | 64.48 C (+0.00) | 64.48 C (-0.00) | - |
| methanol boiling at 1 atm (NRTL) | Heat of vaporisation | 1101.1 kJ/kg | 1101.4 kJ/kg (+0.0 %) | 1101.1 kJ/kg (+0.0 %) | - |
| methanol boiling at 1 atm (NRTL) | Liquid density | 748.4 kg/m3 | 743.2 kg/m3 (-0.7 %) | 748.4 kg/m3 (+0.0 %) | - |
| methanol boiling at 5 bar (NRTL) | Boiling temperature | 111.4 C | 111.4 C (+0.01) | 111.4 C (-0.00) | - |
| methanol boiling at 5 bar (NRTL) | Heat of vaporisation | 991.5 kJ/kg | 990.5 kJ/kg (-0.1 %) | 1029.1 kJ/kg (+3.8 %) | - |
| methanol boiling at 5 bar (NRTL) | Liquid density | 697.8 kg/m3 | 686.4 kg/m3 (-1.6 %) | 697.8 kg/m3 (-0.0 %) | - |
| water boiling at 10 bar (Peng-Robinson) | Boiling temperature | 179.9 C | 180.0 C (+0.16) | 180.0 C (+0.16) | 180.0 C (+0.16) |
| water boiling at 10 bar (Peng-Robinson) | Heat of vaporisation | 2014.6 kJ/kg | 2039.0 kJ/kg (+1.2 %) | 2050.3 kJ/kg (+1.8 %) | 2050.3 kJ/kg (+1.8 %) |
| water boiling at 10 bar (Peng-Robinson) | Liquid density | 887.1 kg/m3 | 874.6 kg/m3 (-1.4 %) | 887.0 kg/m3 (-0.0 %) | 887.0 kg/m3 (-0.0 %) |
| water boiling at 100 bar (Peng-Robinson) | Boiling temperature | 311.0 C | 310.0 C (-0.95) | 310.7 C (-0.29) | 310.7 C (-0.29) |
| water boiling at 100 bar (Peng-Robinson) | Heat of vaporisation | 1317.4 kJ/kg | 1354.6 kJ/kg (+2.8 %) | 1361.6 kJ/kg (+3.4 %) | 1361.6 kJ/kg (+3.4 %) |
| water boiling at 100 bar (Peng-Robinson) | Liquid density | 688.4 kg/m3 | 701.1 kg/m3 (+1.8 %) | 689.1 kg/m3 (+0.1 %) | 689.1 kg/m3 (+0.1 %) |
| propane boiling at 1 atm (SRK) | Boiling temperature | -42.11 C | -41.84 C (+0.27) | -41.88 C (+0.24) | - |
| propane boiling at 1 atm (SRK) | Heat of vaporisation | 425.6 kJ/kg | 432.0 kJ/kg (+1.5 %) | 431.7 kJ/kg (+1.4 %) | - |
| propane boiling at 1 atm (SRK) | Liquid density | 580.9 kg/m3 | 581.1 kg/m3 (+0.0 %) | 580.6 kg/m3 (-0.0 %) | - |
| propane boiling at 15 bar (SRK) | Boiling temperature | 43.99 C | 43.37 C (-0.62) | 43.39 C (-0.60) | - |
| propane boiling at 15 bar (SRK) | Heat of vaporisation | 298.5 kJ/kg | 301.8 kJ/kg (+1.1 %) | 301.4 kJ/kg (+1.0 %) | - |
| propane boiling at 15 bar (SRK) | Liquid density | 460.3 kg/m3 | 461.7 kg/m3 (+0.3 %) | 461.4 kg/m3 (+0.2 %) | - |
| propylene boiling at 1 atm (SRK) | Boiling temperature | -47.62 C | -47.11 C (+0.51) | -47.42 C (+0.20) | - |
| propylene boiling at 1 atm (SRK) | Heat of vaporisation | 438.9 kJ/kg | 446.3 kJ/kg (+1.7 %) | 444.2 kJ/kg (+1.2 %) | - |
| propylene boiling at 1 atm (SRK) | Liquid density | 610.1 kg/m3 | 608.4 kg/m3 (-0.3 %) | 609.8 kg/m3 (-0.0 %) | - |
| propylene boiling at 15 bar (SRK) | Boiling temperature | 35.89 C | 35.46 C (-0.42) | 35.34 C (-0.54) | - |
| propylene boiling at 15 bar (SRK) | Heat of vaporisation | 312.6 kJ/kg | 319.1 kJ/kg (+2.1 %) | 316.6 kJ/kg (+1.3 %) | - |
| propylene boiling at 15 bar (SRK) | Liquid density | 486.6 kg/m3 | 488.3 kg/m3 (+0.4 %) | 487.6 kg/m3 (+0.2 %) | - |
| n-pentane boiling at 1 atm (Peng-Robinson) | Boiling temperature | 36.06 C | 36.23 C (+0.18) | 36.12 C (+0.06) | 36.14 C (+0.08) |
| n-pentane boiling at 1 atm (Peng-Robinson) | Heat of vaporisation | 357.7 kJ/kg | 358.9 kJ/kg (+0.3 %) | 358.0 kJ/kg (+0.1 %) | 359.1 kJ/kg (+0.4 %) |
| n-pentane boiling at 1 atm (Peng-Robinson) | Liquid density | 610.0 kg/m3 | 609.1 kg/m3 (-0.1 %) | 609.9 kg/m3 (-0.0 %) | 609.9 kg/m3 (-0.0 %) |

Reference: reference equation of state. In brackets: the difference from the reference.

### Vapour pressure

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| propane at -23 C (Peng-Robinson) | Vapour pressure | 218.0 kPa | 217.7 kPa (-0.1 %) | 217.7 kPa (-0.1 %) | 218.0 kPa (+0.0 %) |
| propane at 27 C (Peng-Robinson) | Vapour pressure | 997.7 kPa | 998.2 kPa (+0.1 %) | 997.4 kPa (-0.0 %) | 1004.5 kPa (+0.7 %) |
| propane at 67 C (Peng-Robinson) | Vapour pressure | 2431.1 kPa | 2446.4 kPa (+0.6 %) | 2443.9 kPa (+0.5 %) | 2454.6 kPa (+1.0 %) |
| carbon dioxide at 0 C (Peng-Robinson) | Vapour pressure | 3485.1 kPa | 3447.8 kPa (-1.1 %) | 3477.3 kPa (-0.2 %) | 3483.5 kPa (-0.0 %) |

Reference: reference equation of state. In brackets: the difference from the reference.

### Valves

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| valve: methane, 27 C, from 100 to 20 bar (Peng-Robinson) | Outlet temperature | -7.521 C | -9.899 C (-2.38) | -10.32 C (-2.80) | -10.20 C (-2.68) |
| valve: nitrogen, 27 C, from 200 to 1 bar (Peng-Robinson) | Outlet temperature | -3.963 C | -7.725 C (-3.76) | -7.750 C (-3.79) | -5.699 C (-1.74) |
| valve: carbon dioxide, 47 C, from 80 to 20 bar (Peng-Robinson) | Outlet temperature | -19.50 C | -18.78 C (+0.72) | -19.26 C (+0.24) | -19.45 C (+0.05) |
| valve: saturated liquid propane at 30 C let down to 2 bar (Peng-Robinson) | Outlet temperature | -25.45 C | -25.43 C (+0.02) | -25.42 C (+0.03) | -25.44 C (+0.01) |
| valve: saturated liquid propane at 30 C let down to 2 bar (Peng-Robinson) | Vapour fraction at the outlet | 0.345 | 0.350 (+0.006) | 0.346 (+0.001) | 0.353 (+0.008) |
| valve: saturated liquid ammonia at 30 C let down to 2 bar (Peng-Robinson) | Outlet temperature | -18.84 C | -18.53 C (+0.31) | -18.62 C (+0.23) | -19.33 C (-0.49) |

Reference: reference equation of state. In brackets: the difference from the reference.

### Compressor

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| compressor: methane, 30 C and 20 bar to 60 bar, 75 % efficient (Peng-Robinson) | Work per kg of gas | 254.4 kJ/kg | 251.7 kJ/kg (-1.1 %) | 251.8 kJ/kg (-1.0 %) | 254.4 kJ/kg (+0.0 %) |
| compressor: methane, 30 C and 20 bar to 60 bar, 75 % efficient (Peng-Robinson) | Outlet temperature | 140.9 C | 140.4 C (-0.44) | 140.9 C (+0.03) | 141.5 C (+0.61) |
| turbine: steam, 400 C and 40 bar to 5 bar, 85 % efficient (Peng-Robinson) | Work per kg of gas | -414.2 kJ/kg | -411.4 kJ/kg (-0.7 %) | -410.7 kJ/kg (-0.9 %) | -409.8 kJ/kg (-1.1 %) |
| turbine: steam, 400 C and 40 bar to 5 bar, 85 % efficient (Peng-Robinson) | Outlet temperature | 174.5 C | 169.2 C (-5.32) | 168.1 C (-6.41) | 168.0 C (-6.49) |

Reference: reference equation of state. In brackets: the difference from the reference.

### Heating a liquid

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| liquid n-hexane, 0 to 65 C (Peng-Robinson) | Heat taken up | 150.0 kJ/kg | 144.0 kJ/kg (-4.0 %) | 144.4 kJ/kg (-3.7 %) | 148.3 kJ/kg (-1.1 %) |
| liquid n-heptane, 10 to 95 C (Peng-Robinson) | Heat taken up | 200.2 kJ/kg | 193.3 kJ/kg (-3.4 %) | 193.1 kJ/kg (-3.5 %) | 198.9 kJ/kg (-0.6 %) |
| liquid n-octane, 10 to 120 C (Peng-Robinson) | Heat taken up | 262.6 kJ/kg | 255.3 kJ/kg (-2.8 %) | 253.3 kJ/kg (-3.5 %) | 261.2 kJ/kg (-0.5 %) |
| liquid n-decane, 10 to 167 C (Peng-Robinson) | Heat taken up | 384.5 kJ/kg | 372.3 kJ/kg (-3.2 %) | 370.7 kJ/kg (-3.6 %) | 383.2 kJ/kg (-0.3 %) |
| liquid propane, -93 to -45 C (Peng-Robinson) | Heat taken up | 102.9 kJ/kg | 96.78 kJ/kg (-6.0 %) | 96.73 kJ/kg (-6.0 %) | 102.3 kJ/kg (-0.6 %) |
| liquid n-butane, -53 to -3 C (Peng-Robinson) | Heat taken up | 109.9 kJ/kg | 102.8 kJ/kg (-6.5 %) | 105.4 kJ/kg (-4.1 %) | 108.6 kJ/kg (-1.1 %) |
| liquid water, 20 to 90 C (Peng-Robinson) | Heat taken up | 293.0 kJ/kg | 294.8 kJ/kg (+0.6 %) | 292.3 kJ/kg (-0.3 %) | 292.3 kJ/kg (-0.3 %) |
| liquid ammonia, -73 to -35 C (Peng-Robinson) | Heat taken up | 166.7 kJ/kg | 166.0 kJ/kg (-0.4 %) | 165.6 kJ/kg (-0.7 %) | 171.9 kJ/kg (+3.1 %) |
| liquid water, 20 to 90 C (NRTL) | Heat taken up | 293.0 kJ/kg | 294.8 kJ/kg (+0.6 %) | 293.1 kJ/kg (+0.0 %) | - |
| liquid ethanol, 10 to 70 C (NRTL) | Heat taken up | 154.0 kJ/kg | 202.0 kJ/kg (+31.1 %) | 154.0 kJ/kg (+0.0 %) | - |
| liquid methanol, 10 to 60 C (NRTL) | Heat taken up | 130.3 kJ/kg | 182.0 kJ/kg (+39.7 %) | 130.3 kJ/kg (+0.0 %) | - |
| liquid benzene, 10 to 75 C (NRTL) | Heat taken up | 116.2 kJ/kg | 109.5 kJ/kg (-5.8 %) | 116.1 kJ/kg (-0.0 %) | - |
| liquid benzene, 10 to 75 C (UNIQUAC) | Heat taken up | 116.2 kJ/kg | 109.5 kJ/kg (-5.8 %) | 116.1 kJ/kg (-0.0 %) | - |
| liquid propane, -93 to -53 C (SRK) | Heat taken up | 85.18 kJ/kg | 83.41 kJ/kg (-2.1 %) | 83.47 kJ/kg (-2.0 %) | - |
| liquid propylene, -93 to -53 C (SRK) | Heat taken up | 84.68 kJ/kg | 77.82 kJ/kg (-8.1 %) | 81.64 kJ/kg (-3.6 %) | - |

Reference: reference equation of state. In brackets: the difference from the reference.

### Gases at furnace temperature

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| methane gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 45.55 kJ/mol | 45.77 kJ/mol (+0.5 %) | 45.62 kJ/mol (+0.1 %) | 45.62 kJ/mol (+0.2 %) |
| methane gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 71.80 J/mol.K | 72.05 J/mol.K (+0.4 %) | 71.80 J/mol.K (+0.0 %) | 71.80 J/mol.K (+0.0 %) |
| ethane gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 77.05 kJ/mol | 77.22 kJ/mol (+0.2 %) | 77.08 kJ/mol (+0.0 %) | 77.08 kJ/mol (+0.0 %) |
| ethane gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 122.6 J/mol.K | 122.2 J/mol.K (-0.3 %) | 122.6 J/mol.K (+0.0 %) | 122.6 J/mol.K (+0.0 %) |
| propane gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 110.3 kJ/mol | 110.5 kJ/mol (+0.1 %) | 110.3 kJ/mol (-0.0 %) | 110.3 kJ/mol (-0.0 %) |
| propane gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 174.5 J/mol.K | 175.7 J/mol.K (+0.7 %) | 174.5 J/mol.K (+0.0 %) | 174.5 J/mol.K (+0.0 %) |
| carbon dioxide gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 38.89 kJ/mol | 38.56 kJ/mol (-0.9 %) | 38.93 kJ/mol (+0.1 %) | 38.94 kJ/mol (+0.1 %) |
| carbon dioxide gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 54.31 J/mol.K | 53.87 J/mol.K (-0.8 %) | 54.32 J/mol.K (+0.0 %) | 54.33 J/mol.K (+0.0 %) |
| nitrogen gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 24.76 kJ/mol | 24.77 kJ/mol (+0.0 %) | 24.77 kJ/mol (+0.0 %) | 24.77 kJ/mol (+0.0 %) |
| nitrogen gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 32.69 J/mol.K | 32.71 J/mol.K (+0.1 %) | 32.70 J/mol.K (+0.0 %) | 32.70 J/mol.K (+0.0 %) |
| water gas at 1 atm (Peng-Robinson) | Heat to bring it from 125 C to 827 C | 26.80 kJ/mol | 26.94 kJ/mol (+0.5 %) | 26.86 kJ/mol (+0.2 %) | 26.86 kJ/mol (+0.2 %) |
| water gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 41.27 J/mol.K | 41.30 J/mol.K (+0.1 %) | 41.30 J/mol.K (+0.1 %) | 41.30 J/mol.K (+0.1 %) |
| carbon monoxide gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 25.03 kJ/mol | 25.05 kJ/mol (+0.1 %) | 25.04 kJ/mol (+0.0 %) | 25.05 kJ/mol (+0.0 %) |
| carbon monoxide gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 33.18 J/mol.K | 33.21 J/mol.K (+0.1 %) | 33.18 J/mol.K (-0.0 %) | 33.18 J/mol.K (-0.0 %) |
| hydrogen gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 23.72 kJ/mol | 23.70 kJ/mol (-0.1 %) | 23.73 kJ/mol (+0.0 %) | 23.73 kJ/mol (+0.0 %) |
| hydrogen gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 30.20 J/mol.K | 30.19 J/mol.K (-0.0 %) | 30.22 J/mol.K (+0.1 %) | 30.22 J/mol.K (+0.1 %) |
| oxygen gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 26.21 kJ/mol | 26.22 kJ/mol (+0.0 %) | 26.23 kJ/mol (+0.0 %) | 26.23 kJ/mol (+0.0 %) |
| oxygen gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 34.86 J/mol.K | 34.88 J/mol.K (+0.1 %) | 34.88 J/mol.K (+0.0 %) | 34.88 J/mol.K (+0.0 %) |
| ammonia gas at 1 atm (Peng-Robinson) | Heat to bring it from 25 C to 827 C | 38.41 kJ/mol | 38.07 kJ/mol (-0.9 %) | 38.39 kJ/mol (-0.0 %) | 38.40 kJ/mol (-0.0 %) |
| ammonia gas at 1 atm (Peng-Robinson) | Heat capacity at 727 C | 56.49 J/mol.K | 55.97 J/mol.K (-0.9 %) | 56.52 J/mol.K (+0.0 %) | 56.52 J/mol.K (+0.1 %) |

Reference: NIST-JANAF or NIST Shomate tables. In brackets: the difference from the reference.

### Mixtures: where they boil and condense

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| 50 % methane + 50 % ethane at -73 C (Peng-Robinson) | Bubble pressure | 26.39 bar | 26.62 bar (+0.9 %) | 26.03 bar (-1.4 %) | 26.12 bar (-1.0 %) |
| 50 % methane + 50 % ethane at -73 C (Peng-Robinson) | Dew pressure | 4.409 bar | 4.404 bar (-0.1 %) | 4.386 bar (-0.5 %) | 4.370 bar (-0.9 %) |
| 50 % methane + 50 % ethane at -23 C (Peng-Robinson) | Bubble pressure | 63.03 bar | 62.15 bar (-1.4 %) | 61.28 bar (-2.8 %) | 62.22 bar (-1.3 %) |
| 50 % methane + 50 % ethane at -23 C (Peng-Robinson) | Dew pressure | 29.66 bar | 29.37 bar (-1.0 %) | 29.19 bar (-1.6 %) | 29.32 bar (-1.1 %) |
| 30 % methane + 70 % propane at 4 C (Peng-Robinson) | Bubble pressure | 50.19 bar | 50.43 bar (+0.5 %) | 49.69 bar (-1.0 %) | 51.32 bar (+2.3 %) |
| 30 % methane + 70 % propane at 4 C (Peng-Robinson) | Dew pressure | 8.169 bar | 8.059 bar (-1.3 %) | 8.052 bar (-1.4 %) | 8.110 bar (-0.7 %) |
| 50 % ethane + 50 % propane at 27 C (Peng-Robinson) | Bubble pressure | 23.75 bar | 24.31 bar (+2.3 %) | 24.12 bar (+1.5 %) | 24.16 bar (+1.7 %) |
| 50 % ethane + 50 % propane at 27 C (Peng-Robinson) | Dew pressure | 17.09 bar | 17.27 bar (+1.0 %) | 17.17 bar (+0.5 %) | 17.26 bar (+1.0 %) |
| 50 % propane + 50 % n-butane at 47 C (Peng-Robinson) | Bubble pressure | 9.827 bar | 9.900 bar (+0.7 %) | 9.909 bar (+0.8 %) | 9.965 bar (+1.4 %) |
| 50 % propane + 50 % n-butane at 47 C (Peng-Robinson) | Dew pressure | 7.251 bar | 7.270 bar (+0.3 %) | 7.282 bar (+0.4 %) | 7.320 bar (+0.9 %) |
| 30 % methane + 70 % carbon dioxide at -23 C (Peng-Robinson) | Bubble pressure | 71.73 bar | 71.64 bar (-0.1 %) | 71.15 bar (-0.8 %) | 72.53 bar (+1.1 %) |
| 30 % methane + 70 % carbon dioxide at -23 C (Peng-Robinson) | Dew pressure | 27.71 bar | 26.83 bar (-3.2 %) | 27.31 bar (-1.5 %) | 27.54 bar (-0.6 %) |
| 30 % nitrogen + 70 % methane at -123 C (Peng-Robinson) | Bubble pressure | 29.77 bar | 30.42 bar (+2.2 %) | 29.75 bar (-0.1 %) | 29.91 bar (+0.5 %) |
| 30 % nitrogen + 70 % methane at -123 C (Peng-Robinson) | Dew pressure | 15.40 bar | 15.54 bar (+0.9 %) | 15.43 bar (+0.2 %) | 15.31 bar (-0.6 %) |
| 40 % carbon dioxide + 60 % propane at 7 C (Peng-Robinson) | Bubble pressure | 24.95 bar | 25.12 bar (+0.7 %) | 24.98 bar (+0.1 %) | 25.02 bar (+0.3 %) |
| 40 % carbon dioxide + 60 % propane at 7 C (Peng-Robinson) | Dew pressure | 9.766 bar | 9.844 bar (+0.8 %) | 9.829 bar (+0.6 %) | 9.893 bar (+1.3 %) |
| 30 % methane + 70 % n-butane at 37 C (Peng-Robinson) | Bubble pressure | 66.31 bar | 63.23 bar (-4.7 %) | 63.58 bar (-4.1 %) | 66.81 bar (+0.7 %) |
| 30 % methane + 70 % n-butane at 37 C (Peng-Robinson) | Dew pressure | 5.141 bar | 5.092 bar (-1.0 %) | 5.100 bar (-0.8 %) | 5.126 bar (-0.3 %) |
| 50 % ethane + 50 % n-heptane at 77 C (Peng-Robinson) | Bubble pressure | 38.07 bar | 35.70 bar (-6.2 %) | 35.71 bar (-6.2 %) | 35.75 bar (-6.1 %) |
| 50 % ethane + 50 % n-heptane at 77 C (Peng-Robinson) | Dew pressure | 1.039 bar | 1.044 bar (+0.5 %) | 1.045 bar (+0.6 %) | 1.040 bar (+0.2 %) |

Reference: GERG-2008. In brackets: the difference from the reference.

### Azeotropes

| Case | Quantity | Reference | Program A | Enthalpia |
|---|---|---:|---:|---:|
| ethanol + water at 1 atm: lowest boiling mixture (NRTL) | Lowest boiling temperature | 78.20 C | 78.09 C (-0.11) | 78.18 C (-0.02) |
| ethanol + water at 1 atm: lowest boiling mixture (NRTL) | Mole fraction of ethanol there | 0.894 | 0.932 (+0.038) | 0.876 (-0.018) |
| ethanol + benzene at 1 atm: lowest boiling mixture (NRTL) | Lowest boiling temperature | 67.90 C | 67.29 C (-0.61) | 68.39 C (+0.49) |
| ethanol + benzene at 1 atm: lowest boiling mixture (NRTL) | Mole fraction of ethanol there | 0.448 | 0.449 (+0.001) | 0.448 (-0.000) |

Reference: handbook azeotrope tables. In brackets: the difference from the reference.

### Mixtures along their boiling curve

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| ethanol + water at 1 atm (NRTL) | Boiling temperature with 10 % ethanol | - | 86.35 C | 86.55 C | - |
| ethanol + water at 1 atm (NRTL) | Boiling temperature with 30 % ethanol | - | 81.50 C | 81.38 C | - |
| ethanol + water at 1 atm (NRTL) | Boiling temperature with 50 % ethanol | - | 79.79 C | 79.67 C | - |
| ethanol + water at 1 atm (NRTL) | Boiling temperature with 70 % ethanol | - | 78.61 C | 78.56 C | - |
| ethanol + water at 1 atm (NRTL) | Boiling temperature with 90 % ethanol | - | 78.09 C | 78.19 C | - |
| methanol + water at 1 atm (NRTL) | Boiling temperature with 10 % methanol | - | 87.72 C | 87.60 C | - |
| methanol + water at 1 atm (NRTL) | Boiling temperature with 30 % methanol | - | 77.51 C | 77.82 C | - |
| methanol + water at 1 atm (NRTL) | Boiling temperature with 50 % methanol | - | 72.54 C | 72.91 C | - |
| methanol + water at 1 atm (NRTL) | Boiling temperature with 70 % methanol | - | 68.97 C | 69.22 C | - |
| methanol + water at 1 atm (NRTL) | Boiling temperature with 90 % methanol | - | 65.91 C | 65.99 C | - |
| ethanol + benzene at 1 atm (NRTL) | Boiling temperature with 10 % ethanol | - | 70.24 C | 71.36 C | - |
| ethanol + benzene at 1 atm (NRTL) | Boiling temperature with 30 % ethanol | - | 67.50 C | 68.61 C | - |
| ethanol + benzene at 1 atm (NRTL) | Boiling temperature with 50 % ethanol | - | 67.33 C | 68.42 C | - |
| ethanol + benzene at 1 atm (NRTL) | Boiling temperature with 70 % ethanol | - | 68.22 C | 69.35 C | - |
| ethanol + benzene at 1 atm (NRTL) | Boiling temperature with 90 % ethanol | - | 72.54 C | 73.49 C | - |
| propane + propylene at 15 bar (SRK) | Boiling temperature with 10 % propylene | - | 42.28 C | 42.54 C | - |
| propane + propylene at 15 bar (SRK) | Boiling temperature with 50 % propylene | - | 38.64 C | 39.23 C | - |
| propane + propylene at 15 bar (SRK) | Boiling temperature with 90 % propylene | - | 35.99 C | 36.10 C | - |
| propane, butane and pentane with water at 5 bar: where it starts to boil (Peng-Robinson) | Boiling temperature with 5 % water | - | 33.30 C | 31.60 C | 31.38 C |
| propane, butane and pentane with water at 5 bar: where it starts to boil (Peng-Robinson) | Boiling temperature with 30 % water | - | 33.31 C | 31.60 C | 31.38 C |
| propane, butane and pentane, dry, at 5 bar (Peng-Robinson) | Boiling temperature with 33.3333 % propane | 32.45 C | 33.73 C (+1.27) | 31.99 C (-0.46) | 31.76 C (-0.69) |
| propane, butane and pentane, dry, at 5 bar (a second sample case) (Peng-Robinson) | Boiling temperature with 33.3333 % propane | 32.45 C | 33.46 C (+1.01) | 31.99 C (-0.46) | 31.76 C (-0.69) |

Reference: GERG-2008 where a value is given; otherwise the two programs are set beside each other. In brackets: the difference from the reference.

### Mixtures along their condensing curve

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| ethanol + water at 1 atm (NRTL) | Condensing temperature with 10 % ethanol | - | 97.34 C | 97.33 C | - |
| ethanol + water at 1 atm (NRTL) | Condensing temperature with 30 % ethanol | - | 91.33 C | 91.37 C | - |
| ethanol + water at 1 atm (NRTL) | Condensing temperature with 50 % ethanol | - | 84.30 C | 84.38 C | - |
| ethanol + water at 1 atm (NRTL) | Condensing temperature with 70 % ethanol | - | 79.13 C | 79.05 C | - |
| ethanol + water at 1 atm (NRTL) | Condensing temperature with 90 % ethanol | - | 78.10 C | 78.19 C | - |
| methanol + water at 1 atm (NRTL) | Condensing temperature with 10 % methanol | - | 97.48 C | 97.44 C | - |
| methanol + water at 1 atm (NRTL) | Condensing temperature with 30 % methanol | - | 91.79 C | 91.73 C | - |
| methanol + water at 1 atm (NRTL) | Condensing temperature with 50 % methanol | - | 84.94 C | 84.87 C | - |
| methanol + water at 1 atm (NRTL) | Condensing temperature with 70 % methanol | - | 76.60 C | 76.65 C | - |
| methanol + water at 1 atm (NRTL) | Condensing temperature with 90 % methanol | - | 67.96 C | 68.21 C | - |
| ethanol + benzene at 1 atm (NRTL) | Condensing temperature with 10 % ethanol | - | 75.97 C | 77.25 C | - |
| ethanol + benzene at 1 atm (NRTL) | Condensing temperature with 30 % ethanol | - | 70.19 C | 71.37 C | - |
| ethanol + benzene at 1 atm (NRTL) | Condensing temperature with 50 % ethanol | - | 67.83 C | 68.78 C | - |
| ethanol + benzene at 1 atm (NRTL) | Condensing temperature with 70 % ethanol | - | 71.97 C | 72.54 C | - |
| ethanol + benzene at 1 atm (NRTL) | Condensing temperature with 90 % ethanol | - | 76.21 C | 76.55 C | - |
| methane with water at 10 bar: where water starts to condense (Peng-Robinson) | Condensing temperature with 99.9 % methane | - | 6.702 C | 6.144 C | 6.146 C |
| methane with water at 10 bar: where water starts to condense (Peng-Robinson) | Condensing temperature with 99 % methane | - | 45.32 C | 44.99 C | 44.99 C |
| methane with water at 50 bar: where water starts to condense (Peng-Robinson) | Condensing temperature with 99.9 % methane | - | 29.72 C | 29.28 C | 29.30 C |
| methane with water at 50 bar: where water starts to condense (Peng-Robinson) | Condensing temperature with 99 % methane | - | 77.96 C | 77.83 C | 77.86 C |
| methane with water at 100 bar: where water starts to condense (Peng-Robinson) | Condensing temperature with 99.9 % methane | - | 39.18 C | 38.79 C | 38.85 C |
| methane with water at 100 bar: where water starts to condense (Peng-Robinson) | Condensing temperature with 99 % methane | - | 92.89 C | 92.83 C | 92.92 C |
| propane + propylene at 15 bar (SRK) | Condensing temperature with 10 % propylene | - | 42.43 C | 42.63 C | - |
| propane + propylene at 15 bar (SRK) | Condensing temperature with 50 % propylene | - | 38.91 C | 39.50 C | - |
| propane + propylene at 15 bar (SRK) | Condensing temperature with 90 % propylene | - | 36.04 C | 36.20 C | - |
| propane, butane and pentane with water at 5 bar: where the first liquid appears (Peng-Robinson) | Condensing temperature with 5 % water | - | 65.66 C | 65.43 C | 65.43 C |
| propane, butane and pentane with water at 5 bar: where the first liquid appears (Peng-Robinson) | Condensing temperature with 30 % water | - | 111.3 C | 111.4 C | 111.4 C |
| propane, butane and pentane, dry, at 5 bar (Peng-Robinson) | Condensing temperature with 33.3333 % propane | 62.43 C | 63.02 C (+0.59) | 61.53 C (-0.90) | 61.46 C (-0.98) |
| propane, butane and pentane, dry, at 5 bar (a second sample case) (Peng-Robinson) | Condensing temperature with 33.3333 % propane | 62.43 C | 63.01 C (+0.58) | 61.53 C (-0.90) | 61.46 C (-0.98) |

Reference: GERG-2008 where a value is given; otherwise the two programs are set beside each other. In brackets: the difference from the reference.

### Gas and condensate with water

| Case | Quantity | Reference | Program A | Enthalpia | Enthalpia tc-PR |
|---|---|---:|---:|---:|---:|
| propane, butane and pentane with 10 % water (Peng-Robinson) | Vapour fraction at 107 C and 10 bar | - | 1.000 | 1.000 | 1.000 |
| propane, butane and pentane with 10 % water (Peng-Robinson) | Vapour fraction at 27 C and 10 bar | - | 0.0000 | 0.0000 | 0.0000 |
| propane, butane and pentane with 10 % water (Peng-Robinson) | Temperature after the valve to 2 bar | - | 5.991 C | 4.536 C | 4.520 C |
| propane, butane and pentane with 10 % water (Peng-Robinson) | Heat given off between the first two states | - | 565.3 kJ/kg | 558.9 kJ/kg | 559.6 kJ/kg |
| propane, butane and pentane with 10 % water, part vapour (Peng-Robinson) | Vapour fraction at 72 C and 10 bar | - | 0.299 | 0.368 | 0.373 |
| propane, butane and pentane with 10 % water, part vapour (Peng-Robinson) | Vapour fraction at 62 C and 10 bar | - | 0.0000 | 0.0125 | 0.0193 |
| propane, butane and pentane with 10 % water, part vapour (Peng-Robinson) | Temperature after the valve to 3 bar | - | 24.59 C | 23.37 C | 23.52 C |
| propane, butane and pentane with 10 % water, part vapour (Peng-Robinson) | Heat given off between the first two states | - | 120.9 kJ/kg | 137.6 kJ/kg | 136.9 kJ/kg |

Reference: none: the two programs are set beside each other. In brackets: the difference from the reference.
