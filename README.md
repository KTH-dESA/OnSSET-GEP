# GEP-OnSSET
This repository contains the source code of OnSSET as used in the Global Electrification Platform  

### Content

This repository contains the source code used to derive the electrification results for GEP V.1.

### How-to-use Instructions 

1. Clone repository in a directory at your local machine
2. Open onsset.py and runner.py in the IDE of your preference (the description below assumes [PyCharm](https://www.jetbrains.com/pycharm/download/#section=windows))
3. Make sure all dependencies are installed; a list is available at the top of each .py file
4. Make sure that "specs_mw_one_scenario.csv" and "Malawi.csv" files are in the same directory. Both files shall follow the format and naming convention as indicated in this repository. Parameter values can be changed accordingly
4. Run onsset.py and make sure there is no error
5. Run runner.py
  a. Select to calibrate the "Malawi.csv" as per instructions. The process will create a new, calibrated input file; you shall specify the name (e.g. "Malawi_Calibrated"
  b. After calibration (taking place only once) start running scenarios as per instructions. Note that "Malawi_Calibrated" shall be used as input.
  c. The steps of the analysis will appear on your IDE's console.
5. After a scenario run is complete, two output files will appear in the directory; one containing full results and another providing a summary.
6. Import the full result .csv file into a GIS environment (QGIS, ArcMap) to vizualize the results.

### Cautions

The first input file ("specs_mw_onescenario.csv") contains most of the inputs parameters of the analysis such as total population, urban population ratio, diesel price etc. Note that multiple scenarios are possible using the "specs_mw_144_scenarios.csv" file.

The second input file ("Malawi.csv") contains all the GIS information (21 columns) for the settlements to be included in the analysis. The calibration process add a number of columns regarding population projection, current electrification rate and a few other geo-spatial characteristics. Please refer to the relevant code section for a close review.

The "Malawi.csv" represents population settlements in the form of vectors.

Both onsset.py and runner.py files are supported by the "TODO" functionality. There are 4 patterns in the current version of the code; The RUN_PARAM pattern will guide you through all sensitive - country specific - parameters of the analysis. RUN_PARAM values in this version of the code are reflective for the case of Malawi; they need to be adjusted accordingly in case the code is used for another country.

### Supplementary material

- For any additional information please contact the GEP team [here.](https://gep-user-guide.readthedocs.io/en/latest/Contact.html)


