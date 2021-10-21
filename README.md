# SNOWIE_Z-S-relationship
This directory provides all necessary information and steps to reproduce snow accumulation maps based on DOW reflectivity data collected during SNOWIE


**General information:**
SNOWIE field cataloge: http://catalog.eol.ucar.edu/snowie
SNOWIE data access: https://data.eol.ucar.edu/master_lists/generated/snowie/

**1. Derive QC for gauge data**
This table indicates what data passed the QC. QC criteria are described in Friedrich et al. (2020). Gauge data can be downloaded from the SNOWIE data access website.

<img width="1182" alt="Screen Shot 2021-10-21 at 10 55 31 AM" src="https://user-images.githubusercontent.com/92404463/138323124-c96574a2-4c46-4261-97f2-87b14d47fb1c.png">

**2. Retrieve radar reflectivity at the gauge site**
Use the DOW6 deployed at the Snowbank site to derive the maximum reflectivity at the gauge sites at Clear Creek and Silver Creek. The method to derive a 2-d maximum reflectivity field is described in Friedrich et al. (2020). We derived the reflectivity at the gauge site by taking the mean value across a 3 x 3 array which represents an area of 500 m x 500 m. Derived reflectivity values for each IOP are stored here. 

**3. Use gauge and radar reflectivity to derive a Z-S relationship**
In this step, we combine the gauge data at the gauge sites to derive the _a_ and _b_ values in a Z = _a_ S^_b_ relationship with Z being radar reflectivity and S being accumulated snowfall. Plot log(z in mm6/m3) versus log(S in mm/h) closest in time. Python code is stored here. Results of _a_ and_ b_ are published in ???

**4. Apply Z-S relationship to generate snow accumulation maps** 
In the last step, we applied the Z-S relationship to the 2-d max reflectivity to derive snow accumulation for the entire period and for each radar time step. Data are stored here.

**References**
Friedrich, K., J. R. French, S. A. Tessendorf, M. Hatt, C. Weeks, R M. Rauber, B. Geerts, L. Xue, R. M. Rasmussen, D. R. Blestrud, M. L. Kunkel, N. Dawson, and S. Parkinson, 2021: Microphysical characteristics and evolution of seeded orographic clouds. J. Appl. Meteor. Climatol., 60, 909-934

Friedrich, K., K. Ikeda, S. A. Tessendorf, J. R. French, R. M. Rauber, B. Geerts, L. Xue, R. M. Rasmussen, D. R. Blestrud, M. L. Kunkel, N. Dawson, and S. Parkinson, 2020: Quantifying snowfall from orographic cloud seeding. Proceedings of the National Academy of Sciences of the United States of America. Feb 2020, 201917204; DOI: 10.1073/pnas.1917204117
