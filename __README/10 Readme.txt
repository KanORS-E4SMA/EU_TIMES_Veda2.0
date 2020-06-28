Open JRC-EU-TIMES
Download page: https://data.jrc.ec.europa.eu/collection/id-00287 
Contact: JRC-DATA-ENERGY-UNION@ec.europa.eu

This file gives an overview of JRC-EU-TIMES and explains what you can find in this ZIP file.

JRC-EU-TIMES_2019_11
--------------------
This folder contains a synchronised model version of the full JRC-EU-TIMES.
JRC-EU-TIMES is a model that represents all sectors of the energy system 
of the EU28 and of neighboring countries: buildings, transport, industry, 
power and agriculture. The JRC-EU-TIMES model produces projections (or scenarios) 
of the EU energy system showing its evolution up to 2060 under different sets of assumptions. 
The model's algorithm simultaneously solves for the optimum investment portfolio of 
energy technologies and their operation. The following JRC data collections are also 
inputs for JRC-EU-TIMES: ETRI, JRC-IDEES, ENSPRESO and EMHIRES.
Some modules of JRC-EU-TIMES will be made open as a separate dataset on a 
specific topic because the data can also be useful for non-TIMES users.
JRC will not make further modifications to JRC-EU-TIMES.

"JRC-EU-TIMES Publications"
---------------------------
This folder contains publications related to inputs and results of JRC-EU-TIMES.

Following files explain the rights and licensing and the software needs 
-----------------------------------------------------------------------
-"11 Rights and licensing.txt"
-"12 Software needs.ntxt"
-"12 Software needs JRC-EU-TIMES.jpg"
To use the ETSAP TIMES code, third party software is required such as GAMS.

"14 List of new modules"
------------------------
This file explains the new elements introduced by JRC.

Following files explain some settings and assumptions of JRC-EU-TIMES
---------------------------------------------------------------------
20 Scenarios and OBJ
21 CO2 emissions in JRC-EU-TIMES
22 Trade JRC-EU-TIMES
23 Variable RES in JRC-EU-TIMES
23 Variable RES script in R
24 Technologies and commodities overview JRC-EU-TIMES v9

Instructions on how to run JRC-EU-TIMES
---------------------------------------
-Using the JRC-EU-TIMES CPLEX option file is important. JRC-EU-TIMES runs fast without crossover and also, 
running with crossover may give a solution that is "optimal, but with infeasibilities after unscaling"
"13 CPLEX JRC-EU-TIMES.opt" and "13 CplexOpt JRC-EU-TIMES for older VEDA FE.jpg" give the settings for Cplex as used by JRC.
-The model runs between 1 and 3 hours on a standard PC using a 4 Core CPU with a 3.5 GHz clock speed and 32 GB of RAM memory.
-The number of time periods is determining for the run time.
-The model has 37 regions but is only operational for 31 regions (EU28 + Zwitserland, Iceland and Norway).
Some data for the Balkans was removed also because no study was performed with all regions.
The model is already imported, but FYI: a full model import from scratch takes only 3 hours.
For a start from scratch, all Subres files and scenario files can be included all at once for import.
-All energy services demands are included in the file Demand as a normal scenario file.
-The default periods (9 periods) are advisable as a minimum for making sure all bounds are included properly.
-The majority of warnings in the import log have to do with:
1.Processes turned off for the Balkan countries
2.Use of fast import DINS for a set of processes/countries even though a technology does not exist
in a certain country (like offshore in Austria or CSP in the Netherlands). The speed of import is more important.
-While synchronising the database in VEDA FE, sometimes a warning message is given on the size of the database. 
However, there is no danger because the size of this model has always been lower than 1.5 GB (activedb.MDB)

Rpt_ext.jrc
-----------
JRC-EU-TIMES runs fast without crossover and with very similar results as with crossover.
One disadvantage is that without crossover, many variables that should be zero show up with a small value instead of zero.
To remove these small values from the results, we have this code.
This code is not needed to run the model.

"TIMES extension for additional reporting"
------------------------------------------
This folder contains files that are an extension of the TIMES code that can be useful for additional reporting variables.

LAST WORD
---------
We would like to thank all the people involved in the long history of this model: our JRC management and ex-colleagues, 
ETSAP, our contractors and previous model developers. Thanks for having entrusted us with this responsibility.
And to everyone that has patiently supported us in the more difficult TIMES: un grand merci!