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










## Section 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK (14/03/2024 - 15/03/2024)

### Theory

<details>
  <summary>
Expand or Collapse
  </summary>

#### Package

* In any embedded board we have seen, the part of the board we consider as the chip is only the ***PACKAGE*** of the chip which is nothing but a protective layer or packet bound over the actual chip and the actual manufatured chip is usually present at the center of a package wherein, the connections from package is fed to the chip by ***WIRE BOUND*** method which is none other than basic wired connection.

