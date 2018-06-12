# VBA-Excel-Patran_reports_creator

This repo could be helpfull for FE stress analysis only
=
This macro was created during the Blister Fiber Glass Sanwich panels Stress analysis and sizing. Panels were analyzed via Patran/Nastran application and simulated as laminate shell elements, bolts were simplified to bush elements.

INSTRUCTION:

NOTE1: If a cell in columns Check, FileName, Group or Coordinate is equal to previous, you may just left this cell blank and script will read the previous cell. But it's not applicable for LC (Load Case) name!

NOTE2: Each report must contains >= two Load Cases

    0. Fill cell I2 (partnumber and version)
    1. Fill List of created .rpt files in ".rpt name" column - generated script will add in patran "_DD-MMM-YY.rpt"; Rpt name must contain "moment" or "force"
    2. Set analysis type "Check" - Panel or Joints, this item is responsible for load types (Shell for panel analysis and Bush for joint analysis)
    3. Fill "LC name" - Load Cases in created file;
    4. Fill "Group" - Group of translated elemets to rpt;
    5. Fill "CTrans" - Coordinate Transformation, it can be: 
      AsIs (Nastran Elm CS) 
      Coord # 
      ResCoord #.# 
      Global 
      Default 
      Material 
      IJK (Patran Elm CS)
    6. Click button #GET .pcl
    7. Run Patran and open *.db
    8. !!! Delete all attached *.xdb !!!
    9. Reatach *.xdb (only one!)
    10. type: !!input RPTextract.pcl 11.type: RPTprint()
