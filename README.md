# compinf
This repository includes code and data related to "Competition and Price Informativeness: An Experiment" by Daniel Kwiatkowski. The folder "zTree code" contains zTree treatment files, "raw data" containes the data as excel files created by zTree, and "python code" contains all code for the paper, including data cleaning, analysis, and creation of figures. The folder "output" contains the output of the python code, including cleaned data and latex figures, and the folder "paper" contains the latex code for the paper itself and the pdf of the paper.

zTree code
------
zTree treatment files (.ztt files) to run the lab experiments discussed in "Competition and Price Informativeness: An Experiment" by Daniel Kwiatkowski. These files are compatible with zTree 5.1.1.

The files are: 
- client_initialization.ztt
- 1seller_current.ztt
- 2seller_current.ztt
- 1seller_pricegrid_current.ztt
- 2seller_pricegrid_current.ztt
- payoff_display.ztt

client_initialization.ztt should be run first to define variables for the clients table which keeps track of total payoffs across all treatments run in the experiment. Then one or more of the baseline treatments (1seller_current.ztt, 2seller_current.ztt) and the robustness treatments (1seller_pricegrid_current.ztt, 2seller_pricegrid_current.ztt). payoff_display.ztt is run last to display the payoffs from each treatment and their sum.

Credit for zTree software: Fischbacher, Urs. "z-Tree: Zurich toolbox for ready-made economic experiments." Experimental economics 10, no. 2 (2007): 171-178.

raw data
------
zTree creates excel files with extension .xls; I saved these as .xlsx files before putting them in the raw data folder. I also renamed them "session1" through "session14" (by default, zTree names them with the data and time that the zTree session started). This folder also includes the excel file "pilot.xlsx" which has the data from the pilot, and "combined_data.xlsx" which includes each session as a separate sheet (combined_data.xlsx is created in the python code).

python code
------
This folder contains 10 jupyter notebook files. "compinf_code.ipynb" simply runs the other nine files in order. "Theory Section.ipynb" does the analysis for the theory section of the paper and creates latex figure files in output. "Data Background.ipynb" does the data cleaning and saves cleaned data in output. "Results Section.ipynb" creates latex figures of the data and runs the permutation tests. "MSE Calculation.ipynb" does the mean-squared-error calculations and creates the MSE latex table. "QRE.ipynb" solves for the logit quantal response equilibrium correspondence, using the path-following algorithm developed by Turocy: Turocy, Theodore L. (2005), A dynamic homotopy interpretation of the logistic quantal
response equilibrium correspondence." Games and Economic Behavior, 51, 243-263. It also runs the finite mixture model to find the likelihood-maximizing precision. "Trembling Hand.ipynb" makes latex figures for the trembling hand perfect equilibrium correspondence as the level of noise varies, and finds the likelihood-maximizing level of noise. "Price Grid.ipynd" examines the treatment with the price grid and makes the figure for the price grid appendix. "zTree images.ipynb" creates the latex figures that show the decision screens in the experiment. "Results with Both Orders.ipynb" re-runs the result section figures and tests including treatments run second.

output
------
This folder is organized the same way as the python code. The output of each python code file is saved in an equivalently named subfolder. So the folder "Theory Section" contains the latex figures created by "Theory Section.ipynb" and the folder "Data Background" contains all the clean data.

paper
------
The latex file to create the pdf of the paper is called "compinf.tex", and the pdf it creates is "compinf.pdf".

