# G-Code-to-Autoleveller-codede-conversion
# Aim
To convert the G-Code into Auto leveler Code using Autoleveller software.
# Software Required
Autoleveller
# Procedure
1.Open the Autoleveller software </br>
2. Select the software option as Mach3 </br>
3. Load the G Code - Click “Browse for G Code” button and open your Engraving G-Code.</br>
4. After loading G-Code below a window will open. In that Select Unit “millimeters”</br>
5. Create level code and the save the code</br>
6. Remove the unwanted portion from your Auto Levelled G-Code. </br>
7. Add few lines in the code and save the file</br>
8. Follow this same procedure for remaining all G-codes ( Drill and cut).</br>
9.Autolevelling should be done for only engraving file.</br>

# Theory

PCB AutoLEVLER is a software tool used in conjunction with CNC (Computer Numerical Control) machines for PCB (Printed Circuit Board) manufacturing. Its primary function is to compensate for variations in the flatness of the substrate or the surface of the copper-clad board. This compensation ensures that the depth of milling or engraving remains consistent across the entire board, even if the board itself is not perfectly flat.

## Purpose:
PCB AutoLEVLER is designed to address the following challenges in PCB manufacturing:
### Substrate Variations: 
Substrates or copper-clad boards may have variations in flatness, which can affect the accuracy of milling or engraving depths.
### Consistency: 
Ensuring consistent depth of milling or engraving across the entire PCB surface is crucial for precise PCB fabrication.
## Functionality:
### Automatic Depth Adjustment: 
PCB AutoLEVLER automatically adjusts the Z-axis depth of the milling or engraving tool based on the surface variations of the PCB substrate. It dynamically compensates for any unevenness in the board to maintain a consistent depth of cut.
### Surface Mapping: 
The software typically includes a surface mapping feature that scans the surface of the PCB and generates a digital map indicating areas of variation in flatness. This map is then used to adjust the tool's depth as it moves across the board.
### Integration with CNC Machines:
PCB AutoLEVLER is integrated with CNC machines through compatible control software. It communicates with the CNC controller to adjust tool depth in real-time during the milling or engraving process.
## Benefits:
### Improved Accuracy: 
By compensating for surface variations, PCB AutoLEVLER helps maintain precise milling or engraving depths, resulting in higher accuracy and quality of PCBs.
### Time Savings:
The software automates the depth adjustment process, saving time compared to manual adjustments or rework caused by uneven milling depths.
Reduced Waste: Consistent depth of milling or engraving minimizes the risk of errors and waste material, resulting in cost savings for PCB manufacturers.
### Compatibility:
PCB AutoLEVLER is typically compatible with a range of CNC machines commonly used in PCB manufacturing, including routers, engravers, and milling machines. It may also integrate with various CAD/CAM software packages to streamline the design-to-manufacturing workflow.
## Implementation:
Implementing PCB AutoLEVLER involves installing the software on a computer connected to the CNC machine and configuring it to work with the specific machine and PCB design requirements. Training may be provided to operators on how to use the software effectively.
Overall, PCB AutoLEVLER plays a vital role in ensuring the accuracy, consistency, and efficiency of PCB manufacturing processes, particularly in environments where precise milling or engraving is essential for high-quality PCBs.
# Auto leveller Code
### Engraving Code
```
M6TX
G54
G0 X0 Y0
G0 Z5
M01



G31 Z-10 F100
G92 Z0
G0 Z2
G31 Z-1 F50
G92 Z0
G0 Z2
G0 X0 Y0
G31 Z-1 F100
#500=#2002
G0 Z2
G0 X10.6365 Y0
G31 Z-1 F100
#501=#2002
G0 Z2
G0 X21.273 Y0
G31 Z-1 F100
#502=#2002
G0 Z2
G0 X21.273 Y11.747
G31 Z-1 F100
#505=#2002
G0 Z2
G0 X10.6365 Y11.747
G31 Z-1 F100
#504=#2002
G0 Z2
G0 X0 Y11.747
G31 Z-1 F100
#503=#2002
G0 Z2
G0 X0 Y0 Z20




M03 S12000




M01




G00 X2.122 Y3.434
G00 Z0
G01 F60 Z-1
G01 F300 X2.172
G02 I-0.05 J0 X2.172 Y3.434
G00 Z2
G00 X2.122 Y0.894
G00 Z0
G01 F60 Z-1
G01 F300 X2.172
G02 I-0.05 J0 X2.172 Y0.894
G00 Z2
G00 X9.742 Y11.054
G00 Z0
G01 F60 Z-1
G01 F300 X9.792
G02 I-0.05 J0 X9.792 Y11.054
G00 Z2
G00 X12.282
G00 Z0
G01 F60 Z-1
G01 F300 X12.332
G02 I-0.05 J0 X12.332 Y11.054
G00 Z2
G00 X19.902 Y3.434
G00 Z0
G01 F60 Z-1
G01 F300 X19.952
G02 I-0.05 J0 X19.952 Y3.434
G00 Z2
G00 X19.902 Y0.894
G00 Z0
G01 F60 Z-1
G01 F300 X19.952
G02 I-0.05 J0 X19.952 Y0.894
G00 Z2



G00 X00 Y00


M05
M02
%




```


### Drill Code
```
M6TX
G54
G0 X0 Y0
G0 Z5
M01



G31 Z-10 F100
G92 Z0
G0 Z2
G31 Z-1 F50
G92 Z0
G0 Z2
G0 X0 Y0
G31 Z-1 F100
#500=#2002
G0 Z2
G0 X10.6365 Y0
G31 Z-1 F100
#501=#2002
G0 Z2
G0 X21.273 Y0
G31 Z-1 F100
#502=#2002
G0 Z2
G0 X21.273 Y11.747
G31 Z-1 F100
#505=#2002
G0 Z2
G0 X10.6365 Y11.747
G31 Z-1 F100
#504=#2002
G0 Z2
G0 X0 Y11.747
G31 Z-1 F100
#503=#2002
G0 Z2
G0 X0 Y0 Z20




M03 S12000




M01




G00 X2.122 Y3.434
G00 Z0
G01 F60 Z-1
G01 F300 X2.172
G02 I-0.05 J0 X2.172 Y3.434
G00 Z2
G00 X2.122 Y0.894
G00 Z0
G01 F60 Z-1
G01 F300 X2.172
G02 I-0.05 J0 X2.172 Y0.894
G00 Z2
G00 X9.742 Y11.054
G00 Z0
G01 F60 Z-1
G01 F300 X9.792
G02 I-0.05 J0 X9.792 Y11.054
G00 Z2
G00 X12.282
G00 Z0
G01 F60 Z-1
G01 F300 X12.332
G02 I-0.05 J0 X12.332 Y11.054
G00 Z2
G00 X19.902 Y3.434
G00 Z0
G01 F60 Z-1
G01 F300 X19.952
G02 I-0.05 J0 X19.952 Y3.434
G00 Z2
G00 X19.902 Y0.894
G00 Z0
G01 F60 Z-1
G01 F300 X19.952
G02 I-0.05 J0 X19.952 Y0.894
G00 Z2



G00 X00 Y00


M05
M02
%




```
### Cuttting Code
```
M6TX
G54
G0 X0 Y0
G0 Z5
M01



G31 Z-10 F100
G92 Z0
G0 Z2
G31 Z-1 F50
G92 Z0
G0 Z2
G0 X0 Y0
G31 Z-1 F100
#500=#2002
G0 Z2
G0 X10.6365 Y0
G31 Z-1 F100
#501=#2002
G0 Z2
G0 X21.273 Y0
G31 Z-1 F100
#502=#2002
G0 Z2
G0 X21.273 Y11.747
G31 Z-1 F100
#505=#2002
G0 Z2
G0 X10.6365 Y11.747
G31 Z-1 F100
#504=#2002
G0 Z2
G0 X0 Y11.747
G31 Z-1 F100
#503=#2002
G0 Z2
G0 X0 Y0 Z20




M03 S12000




M01




G00 X2.122 Y3.434
G00 Z0
G01 F60 Z-1
G01 F300 X2.172
G02 I-0.05 J0 X2.172 Y3.434
G00 Z2
G00 X2.122 Y0.894
G00 Z0
G01 F60 Z-1
G01 F300 X2.172
G02 I-0.05 J0 X2.172 Y0.894
G00 Z2
G00 X9.742 Y11.054
G00 Z0
G01 F60 Z-1
G01 F300 X9.792
G02 I-0.05 J0 X9.792 Y11.054
G00 Z2
G00 X12.282
G00 Z0
G01 F60 Z-1
G01 F300 X12.332
G02 I-0.05 J0 X12.332 Y11.054
G00 Z2
G00 X19.902 Y3.434
G00 Z0
G01 F60 Z-1
G01 F300 X19.952
G02 I-0.05 J0 X19.952 Y3.434
G00 Z2
G00 X19.902 Y0.894
G00 Z0
G01 F60 Z-1
G01 F300 X19.952
G02 I-0.05 J0 X19.952 Y0.894
G00 Z2



G00 X00 Y00


M05
M02
%


```
# Result
Thus the G-Code is converted into Auto leveler Code using Autoleveller software.


