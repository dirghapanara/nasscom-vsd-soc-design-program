# nasscom-vsd-soc-design-program
> 2 Weeks digital VLSI SoC design and planning workshop with complete RTL2GDSII flow organised by VSD in collaboration with NASSCOM

### Introduction: Inception of open-source EDA, OpenLANE and Sky130 PDK
<details open>
  <summary> Images and screen captures </summary>

  In the modern day circuit boards, the CHIP is placed on the board and provided connection with different peripherals

  ![image](https://github.com/user-attachments/assets/bced977a-44b5-4512-82eb-b5582ed1ec71)

  Internals of the CHIP
  
  ![image](https://github.com/user-attachments/assets/d35a4a61-da6f-4c7d-8218-d2f79572d950)
  ![image](https://github.com/user-attachments/assets/edd0b18c-6468-48be-98ee-ec54c3cb4192)
  ![image](https://github.com/user-attachments/assets/08e4f618-e428-4f1c-9902-39c9f2cc2061)
  ![image](https://github.com/user-attachments/assets/1714a717-825e-4ef1-a73d-011fd541b89b)

  A program is compiled and converted to machine level language program which is understood by the hardware. Finally, it generates the GDSII output

  ![image](https://github.com/user-attachments/assets/cddcd36e-193f-45f0-97fd-d8e1b5beda71)




  
  <img width="1608" alt="Screenshot 2025-01-26 at 10 25 48 AM" src="https://github.com/user-attachments/assets/5a6a67f9-3c53-433b-bb6f-e778e938993d" />
  <img width="1608" alt="Screenshot 2025-01-26 at 10 31 15 AM" src="https://github.com/user-attachments/assets/46388ab9-b364-48c5-9d28-6945babe7d35" />
  <img width="1608" alt="Screenshot 2025-01-26 at 10 50 32 AM" src="https://github.com/user-attachments/assets/f09adc48-23e8-4b1d-8a89-bd64e8cdbe41" />
  <img width="1608" alt="Screenshot 2025-01-26 at 11 09 27 AM" src="https://github.com/user-attachments/assets/a1dbd4b7-7a94-44ff-b473-9c1f2882a7e4" />

</details>

### Basic commands
```
  # Change directory to openlane flow directory
  cd Desktop/work/tools/openlane_working_dir/openlane

  # Run docker
  docker

  # Invoke the OpenLANE flow in the Interactive mode
  ./flow.tcl -interactive

  # Set required openlane package
  package require openlane 0.9

  # Create some necessary files and directories for running a the design, ie. 'picorv32a'
  prep -design picorv32a

  # Run synthesis
  run_synthesis
```

### Screen Captures relating to basic commands

  ![image](https://github.com/user-attachments/assets/25b77b91-b903-4a1a-bee4-283fe0d8bed9)
  ![image](https://github.com/user-attachments/assets/ae9f33d0-6e95-49b3-894a-f3f1714468d2)
  ![image](https://github.com/user-attachments/assets/d8395878-b3c1-4d72-ae47-cc97bbc1e1e6)
  ![image](https://github.com/user-attachments/assets/af8e0f01-4d87-40c0-bd63-ec1a62ff6709)
  ![image](https://github.com/user-attachments/assets/3b573dcd-2c67-4a49-aa75-1b0b210342fb)
  ![image](https://github.com/user-attachments/assets/9df7995e-0ea9-4262-939c-5851ded03c14)

#### Calculate Flop Ratio
  ![image](https://github.com/user-attachments/assets/9bd18fbf-0fdd-463a-aad4-69e9ddfba75b)

  - Number of cells             :14876
  - sky130_fd_sc_hd__dfxtp_2    :1613

  ```math
  Flop\ Ratio = \frac{Number\ of\ D\ Flip\ Flops}{Total\ Number\ of\ Cells}
  ```
  ```math
  Percentage\ of\ DFF's = Flop\ Ratio * 100
  ```
  - Flop Ratio = 0.1084
  - % of DEF's = 10.84

#### Synthesis Result
  ![image](https://github.com/user-attachments/assets/90e1b9ea-dbae-4053-b480-b9fc6257d1eb)
  ![image](https://github.com/user-attachments/assets/262c05aa-ef41-40fb-88f4-324395526432)

## Floor Plan

<details open>
  <summary> Images and screen captures </summary>

  ![Screenshot (10)](https://github.com/user-attachments/assets/f470b311-bd38-4eaa-a24f-257ed02877e4)
  ![Screenshot (9)](https://github.com/user-attachments/assets/1b8f97ba-6683-41c5-a979-099bb525137e)
  ![Screenshot (8)](https://github.com/user-attachments/assets/f8014060-8bc4-4f6e-90d9-590e97c51665)
  ![Screenshot (7)](https://github.com/user-attachments/assets/9a374a94-073f-4e1a-b400-029e2ea589fb)
  ![Screenshot (6)](https://github.com/user-attachments/assets/dff3562d-eae9-4e4c-a107-edd87f2a6ee5)
  ![Screenshot (5)](https://github.com/user-attachments/assets/08f2eb80-d1e7-463c-8eb3-dea065f9f4fa)
  ![Screenshot (4)](https://github.com/user-attachments/assets/1d64d95f-be89-40d1-8ed9-9c42d783dc83)
  ![Screenshot (3)](https://github.com/user-attachments/assets/da5703b6-807d-4c8a-b7e8-27c759f456cb)
  ![Screenshot (13)](https://github.com/user-attachments/assets/c12b94de-0b06-4d6b-818e-cf0ce2dabe68)

</details>


### Commands
```
  # Change directory to openlane flow directory
  cd Desktop/work/tools/openlane_working_dir/openlane

  # Run docker
  docker

  # Invoke the OpenLANE flow in the Interactive mode
  ./flow.tcl -interactive

  # Set required openlane package
  package require openlane 0.9

  # Create some necessary files and directories for running a the design, ie. 'picorv32a'
  prep -design picorv32a

  # Run synthesis
  run_synthesis

  # Run floor plan
  run_floorplan
```

### Screen Captures
  ![ijg](https://github.com/user-attachments/assets/d10d0dfd-bbcd-4da8-acbc-e54bba44991f)
  ![Capture_run_floorplan](https://github.com/user-attachments/assets/64603b91-e0e7-4468-a946-fd9759c6acf8)
  ![Capture](https://github.com/user-attachments/assets/6c33b7a8-bb61-4017-9b41-84d94fac55e3)


### Review floor plan in magic

  ![Capture_run_floorplan_next](https://github.com/user-attachments/assets/8661087d-c675-4ba3-9b93-7d682a9670c0)
  ![Capture_run_floorplan_next_1](https://github.com/user-attachments/assets/cf00b4af-81c4-4fcd-b4ce-9b102f5a45a9)
  ![kxejty](https://github.com/user-attachments/assets/8c6963c6-ae27-4883-a9af-ad82c7e4f98f)



## Library Binding and Placement

  ![Screenshot (15)](https://github.com/user-attachments/assets/22be118b-9b81-4f9b-843f-d7b343f287e0)
  ![Screenshot (16)](https://github.com/user-attachments/assets/efffd6fc-b595-46ce-84ac-f4f15ddb3e67)
  ![Screenshot (17)](https://github.com/user-attachments/assets/00a93a97-9371-4aff-b07d-273dea5ff164)
  ![Screenshot (14)](https://github.com/user-attachments/assets/e84d15ab-9a9b-4557-a505-b2ecdbb53587)
  ![Screenshot (18)](https://github.com/user-attachments/assets/a61e923c-ee6a-4a78-a0ff-e66c354da273)
  ![Screenshot (19)](https://github.com/user-attachments/assets/a282788b-8ae3-4a82-9dbc-fed769b8b9bf)
  

### Run 'picorv32a' design congestion aware placement using OpenLANE flow and generate necessary outputs.

### Commands
```
  # Congestion aware placement by default
  run_placement

  # Change directory to path containing generated placement def
  cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/17-03_12-06/results/placement/

  # Command to load the placement def in magic tool
  magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read     picorv32a.placement.def &
```

### Screen captures
  ![d2sk2l5_0](https://github.com/user-attachments/assets/4c127b5f-24c3-46df-971d-d9a758aa35be)
  ![d2sk2l5](https://github.com/user-attachments/assets/52c7c3fd-0ee5-45d1-8516-5f7d4964c0c3)
  ![d2sk2l5_1](https://github.com/user-attachments/assets/3b66507a-2331-4722-a37b-827cdb11c5f0)











