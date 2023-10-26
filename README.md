# LLNL-ASTM
The LLNL Automized Surface Titration Model (L-ASTM) is a community data-driven surface complexation modeling workflow for simulating potentiometric titration of mineral surfaces. The model accepts raw experimental potentiometric titration data formatted in a findable, accessible, interoperable, and reusable (FAIR) structure. The workflow was coded in Python and coupled to PHREEQC for surface complexation modeling and PEST for data fitting and parameter estimation.

# To execute the L-ASTM_v1 Jupyter notebook:
1) Download ‘LLNL-ASCM_v1.zip’ file

2) Unzip the file to ‘Desktop’ directory (or any desired directory). 

3) Ensure all the following folders and programs are in the unziped folder
	phreeqc-3.7.3-15968-x64 (folder) / Ferrihydrite_Potentiometric_Titration.csv (example database file) /
	LLNL-ASTM_v1.ipynb / PEST.EXE / phreeqc.exe

4) Ensure LLNL-ASTM_v1.ipynb and potentiometirc titartion database file are in the same folder.
	The exmaple database file is "Ferrihydrite_Potentiometric_Titration.csv".
	The database file should have a CSV format and the structure of the database should be identical to the example file.

5) Open "LLNL-ASTM_v1.ipynb" notebook.

6) Modify the variables of the notebook.<br/>
	&emsp;i)   &emsp;&emsp;Find “Type of Mineral” cell. And modify the name of mineral. Any name can be used.<br/>
       &nbsp;&ensp;&emsp;&emsp;&emsp;(Default) Mineral_type = 'Ferri'<br/>
	     &nbsp;&emsp;&emsp;&emsp;&ensp;(Example) Mineral_type = 'MY_MINERAL'<br/>
	&emsp;ii)  &nbsp;&ensp;&emsp;Find “Type of SCM” cell. And choose the desired SCM among the three types (i.e., DDL, CCM, NEM).<br/>
	&emsp;iii) &ensp;&emsp;Find "Import potentiometric titration data file" cell. And modify the name of database.<br/>
	     &nbsp;&ensp;&emsp;&emsp;&emsp;(Default) database = "Ferrihydrite_Potentiometric_Titration.csv"<br/>
	     &nbsp;&ensp;&emsp;&emsp;&emsp;(Example) database = "MY_DTATABASE.csv"

8) Run all cells.

9) When the simulation is done results are stored in two folders: 'individual_dataset_run' and 'Dataset_Fitting'<br/>
	&emsp;i)                    &emsp;&emsp;'individual_dataset_run' folder contains simulations results for each individual dataset.<br/>
            &nbsp;&ensp;&emsp;&emsp;&emsp;In that folder, you can find a summary of simulation results from '0.Simulation_Summary.csv' file.<br/>
            &nbsp;&ensp;&emsp;&emsp;&emsp;When you open the '0.Simulation_Summary.csv' file, you can see weighted average of pKa1 and pKa2 (+ correspondig SD).<br/>
            &nbsp;&ensp;&emsp;&emsp;&emsp;Also, you can see wheighted average of capacitance and the corresponding SD if you used CCM.<br/>
            &nbsp;&ensp;&emsp;&emsp;&emsp;<br/>
	&emsp;ii)                   &emsp;&emsp;'Dataset_Fitting' folder contains a simulation result which the model fitted the entire datasets by using weigthed <br/>
            &nbsp;&ensp;&emsp;&emsp;&emsp;pKa1 and pKa2 (+ capacitance in CCM). You can see that the used pKa1 and pKa2 (+ capacitance) values are identical to<br/>
            &nbsp;&ensp;&emsp;&emsp;&emsp;the values in '0.Simulation_Summary.csv' file. The figure in that folder, 'Charge_orgdata_Fitting.png', shows the data<br/>
            &nbsp;&ensp;&emsp;&emsp;&emsp;fitting results.

# Troubleshooting, feedback, and questions may be directed to:
&emsp;&emsp;&emsp;i)   Sol-Chan Han (Email: han14@llnl.gov / hsc09@kaist.ac.kr)<br/>
&emsp;&emsp;&emsp;ii)  Mavrik Zavarin (Email: zavarin1@llnl.gov)<br/>
