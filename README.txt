###############################################################################################

                README.txt File in Running LLNL Automized Surface Titration Model

###############################################################################################

Please refer to the relevant paper:
Sol-Chan Han, Elliot Chang, Susanne Zechel, Frank Bok, Mavrik Zavarin,
Application of community data to surface complexation modeling framework development: Iron oxide protolysis,
Journal of Colloid and Interface Science, Volume 648, 2023, Pages 1015-1024, ISSN 0021-9797,
https://doi.org/10.1016/j.jcis.2023.06.054 (https://www.sciencedirect.com/science/article/pii/S0021979723010810)

To execute the L-ASTM_v1 Jupyter notebook:

1) Download ‘LLNL-ASCM_v1.zip’ file

2) Unzip the file to ‘Desktop’ directory (or any desired directory). 

3) Ensure all the following folders and programs are in the unziped folder
	phreeqc-3.7.3-15968-x64 (folder) / Ferrihydrite_Potentiometric_Titration.csv (example database file) /
	LLNL-ASTM_v1.ipynb / PEST.EXE / phreeqc.exe

4) Ensure LLNL-ASTM_v1.ipynb and potentiometirc titartion database file are in the same folder.
	The exmaple database file is "Ferrihydrite_Potentiometric_Titration.csv".
	The database file should have a CSV format and the structure of the database should be identical to the example file.

5) Open "LLNL-ASTM_v1.ipynb" notebook.

6) Modify the variables of the notebook.
	i)   Find “Type of Mineral” cell. And modify the name of mineral. Any name can be used.
	     (Default) Mineral_type = 'Ferri'
	     (Example) Mineral_type = 'MY_MINERAL'
	ii)  Find “Type of SCM” cell. And choose the desired SCM among the three types (i.e., DDL, CCM, NEM).
	iii) Find "Import potentiometric titration data file" cell. And modify the name of database.
	     (Default) database = "Ferrihydrite_Potentiometric_Titration.csv"
	     (Example) database = "MY_DTATABASE.csv"

7) Run all cells.

8) When the simulation is done results are stored in two folders: 'individual_dataset_run' and 'Dataset_Fitting'
	i)   'individual_dataset_run' folder contains simulations results for each individual dataset.
	     In that folder, you can find a summary of simulation results from '0.Simulation_Summary.csv' file.
	     When you open the '0.Simulation_Summary.csv' file, you can see weighted average of pKa1 and pKa2 (+ correspondig SD).
	     Also, you can see wheighted average of capacitance and the corresponding SD if you used CCM.
	     In that folder, you can find subfolder, '1.Figures', as well. Each figure in that folder shows the fitting result on
	     each dataset. You should remember that pKa1 and pKa2 values used for obtaining the fitted curve in each figure may
	     differ by figures (datasets). The corresponding pKa1, pKa2, and capacitance can be found in
	     '0.Simulation_Summary.csv' file.
	ii)  'Dataset_Fitting' folder contains a simulation result which the model fitted the entire datasets by using weigthed
	     pKa1 and pKa2 (+ capacitance in CCM). You can see that the used pKa1 and pKa2 (+ capacitance) values are identical to
	     the values in '0.Simulation_Summary.csv' file. The figure in that folder, 'Charge_orgdata_Fitting.png', shows the data
	     fitting results.

Troubleshooting, feedback, and questions may be directed to:
	i)   Sol-Chan Han (Email: han14@llnl.gov / hsc09@kaist.ac.kr)
	ii)  Mavrik Zavarin (Email: zavarin1@llnl.gov)