# 7) Streams, rivers, and channels

```note
## Lab 7: Rating curves & Mixing and Dispersion in Rivers

Download the lab and data files to your computer. First you will need the lab worksheet [Mixing and Dilution Worksheet](lab7/CEE348_Spring_2022_Week9Lab.pdf)  This is will be part of Homework 8, but we want to start early.

* [Lab 7-1: Rating Curves](lab7/lab7-1.ipynb)
  * data: [Lyell_h_Q_sorted.mat](data/Lyell_h_Q_sorted.mat)
  * image: [LyellForkTuolumnegagesite](lab7/LyellFork_Tuolumne_flowcontrol.png)
  * Note, this python workbook is optional, if you are interested in how rating curves are made.
* [Lab 7-2: Mixing and Dispersion in Rivers](lab7/lab7-2.ipynb)
  * data (to examine not in python): [CEE348_dye_data_Lab7.xlsx](data/CEE348_dye_data_Lab7.xlsx)
  * data (to examine in python): [Dye_data_GA050630c.csv](data/Dye_data_GA050630c.csv)

```
## Homework 7:

### Problem 1:  (note, we solved this together in lab class, but you need to turn in your write-up for homework)
![Bottom shear stress](data/BottomShearStress.png)
Hints:  For 1a, use the full conservation of momentum expression derived in class, before we simplified using uniform flow.  Remember that the friction slope, S<sub>f</sub> = h<sub>L</sub>/L  (head loss divided by the length).  For 1b, use the expression you generated in 1a.
          
2.  Friction slope
* a) Using the values from Problem 1, above, justify why it is common practice to use the water surface slope (S<sub>surface</sub>) as an approximation for the friction slope (S<sub>f</sub>).  (Hint:  Use your equation from above with both values plugged in and see how different they are.)

* b) What is the percent difference between the actual friction slope and the water surface slope?

* c) When would you expect the difference between S<sub>surface</sub> and S<sub>f</sub> to be large? 

### Probelm 2: River bed erosion
 
To avoid erosion, the river bed is armored with large cobbles, increasing the bed resistance. In a 1km section of the river the depth decreases from 1.9 m to 1.5 m. For this calculation you are told that the discharge is 44 m<sup>3</sup>/s.  The channel bed slope and width can be considered to be the same as in the prior problem.  Determine:

* The head loss and friction slope
* The shear velocity, u<sub>*</sub>


