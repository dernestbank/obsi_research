
# LCA Process Map - 
Steps for LCA in OpenLCA
Open LCA docuumentation https://greendelta.github.io/openLCA2-manual/introduction/index.html

![[Pasted image 20250215055345.png]]


- Nodes and Process Flow:


- Start: Define project in OpenLCA
- 1. Goal and Scope Definition:

- Input project metadata
- Set functional unit and boundaries

- 2. Life Cycle Inventory (LCI):

- Import/create datasets
- Map flows to processes

- 3. Life Cycle Impact Assessment (LCIA):

- Assign impact categories
- Run the calculation

- 4. Interpretation and Improvement:

- Interpret results
- Perform sensitivity checks

- 5. Reporting and Documentation:

- Export results as reports
- Conduct external review if necessary

- End: Completed LCA with improvement actions noted



process_map_lifecycle_assessment.

Start
Define project in OpenLCA
Goal and Scope Definition
Input project metadata
Set functional unit and boundaries
Life Cycle Inventory (LCI)
Import/create datasets
Map flows to processes
Life Cycle Impact Assessment (LCIA)
Assign impact categories
Run the calculation
Interpretation and Improvement
Interpret results
Perform sensitivity checks
Reporting and Documentation
Export results as reports
Conduct external review if necessary
End

![[process_map_lifecycle_assessment.svg]]










Open LCA python API

Inter-process communiction - IPC

Documentation
link https://greendelta.github.io/openLCA-ApiDoc/


        +--------+                  +--------------------+
        | Client | <--------------> | openLCA IPC Server |
        +--------+                  +--------------------+
                    IPC - Protocol
                    * data management
                    * calculations
                    * result details
                    * ...

Starting an IPC server
Tools>Developer tools> IPC Server


Available protocols
- JSON_RPC (JSON and HTTP based),
- gRPC 
- REST API
https://github.com/GreenDelta/olca-ipc.py


