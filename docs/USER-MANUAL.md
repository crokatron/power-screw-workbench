# Power Screw Workbench — visual user manual

[Project overview](../README.md) · [Offline interactive demo](../demo.html)

Start with the numbered picture guide. Each number identifies the exact highlighted control. Work through one step at a time; the longer reference is below it.

### Actual tool · controls at a glance

Actual application screenshot. Numbered boxes point to the controls described below. 

![Power Screw Workbench — numbered controls](images/guide-1.jpg)

1. **Start with the geometry.** Enter load in newtons and dimensions in millimetres. Pitch and lead are different.
2. **Read the result.** Compare total raising torque, back-drive behaviour and efficiency.
3. **Save a run.** Save named alternatives before exporting your comparison.

### Try the working offline example

Screenshot of this project’s interactive demo. Side-by-side services are explicitly simulated.

![Power Screw Workbench — numbered controls](images/guide-2.jpg)

1. **Enter force, not mass.** The demo uses newtons and a fixed mean diameter.
2. **Change the thread starts.** Lead changes with pitch × starts.
3. **Read calculated behaviour.** Compare raising torque, lowering torque and the simple back-drive test.

## Detailed task reference

### Define a meaningful case

1. Give the run a name, then enter axial force in N and dimensions in mm. Do not enter mass where a force is requested.
2. Select Pitch or Helix angle as the independent input. Check thread starts: lead is starts multiplied by pitch, so one turn can advance more than one pitch.
3. Use a measured/supplier mean diameter when available instead of silently treating the preliminary estimate as a standard thread specification.

### Interpret torque and back-driving

1. Open Materials and choose the relevant material/process/lubrication conditions. Replace estimated friction with measured or supplier values when available.
2. Enable Collar only when the intended assembly has that friction contribution and enter its mean diameter and coefficient.
3. Read the thread-alone and total screw-plus-collar results separately. Expand the equations and sign convention before interpreting a negative lowering torque.
4. Change one input at a time and save named runs. A back-drivable result depends on the entered assumptions; it is not a brake or safety-system approval.

### Inspect and compare designs

1. Orbit the 3D screw or choose Side/End and use rotation to see equivalent nut advance. The shown length/root diameter also affect the illustration.
2. Expand Compare 2, 3 & 4 starts and the unwrapped-thread diagrams to understand why a geometry change changes lead and torque.
3. Save run, export JSON for restorable data, and use Excel-compatible outputs for a report. Restore JSON when continuing on another browser.

## Keep your work

Runs and current settings are stored on this device’s browser. Export JSON before clearing site data or changing computers. Spreadsheet exports are for review; JSON is the explicit restore format.

## If something looks wrong

- Torque looks wrong: check N versus kg, mm values, starts versus pitch, and collar state.
- Helix field is disabled: it is calculated when pitch is the selected independent input.
- Runs missing: confirm the same browser/origin or restore your JSON backup.

## What this manual does not promise

This is a preliminary geometry/friction model. It does not replace checking buckling, fatigue, thread strength, lubrication variation and the actual assembly. No new engineering validation was performed during documentation work.

Screenshots show the actual application where captured. The offline demo is a deliberately smaller simulation and identifies its dummy services. It never controls devices, sends notifications, uploads files or launches printing.
