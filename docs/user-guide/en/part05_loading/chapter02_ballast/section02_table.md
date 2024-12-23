### Table with information on ballast tanks
The table contains the following columns with information on ballast tanks
| Column              | Description                                         | Note                                  |
| ------------------- | --------------------------------------------------- | ------------------------------------- |
| w/o                 | Color of the tank                                   | All ballast tanks are marked in green |
| Name                | Name of the tank                                    |                                       |
| Weight [t]          | Weight of water                                     |                                       |
| $V [m^3]$           | Volume of water                                     |                                       |
| $\rho [t/m^3]$      | Density of water                                    |                                       |
| %                   | Percentage of filling                               | Calculated by volume                  |
| $x_g$               | Abscissa of the center of gravity of the water      | In the ship-related coordinate system |
| $y_g$               | Ordinate of the center of gravity of the water      | In the ship-related coordinate system |
| $z_g$               | Application of the center of gravity of the water   | In the ship-related coordinate system |
| $Mf.sx [t \cdot m]$ | Transverse moment of the free surface of the liquid |                                       |
| Mf.sx max           | Method of accounting for the correction             |                                       |

For each ballast tank, it is necessary to specify the data of the columns "M[t]", "V$[m^3]$", "$\rho [t/m^3]$", "%". The data in is changed by double-clicking on the corresponding field in the table. At the same time, the following logic of changing these parameters is implemented:
- when changing %
  - $\rho$ is not recalculated;
  - V and M are recalculated;
- when changing V
  - $\rho$ is not recalculated;
  - % and M are recalculated;
- when changing M 
  - $\rho$ is not recalculated;
  - % and V are recalculated;
- when changing $\rho$
  - not recalculated V;
  - % and M are recalculated.

Additionally, the table should contain information on the method of accounting for the transverse moment of the free surface of the liquid in tanks "Mf.sx max". If the tank parameter is active, the maximum torque value from the entire range of the liquid level in the tank is taken into account. If the parameter is inactive, the value for the actual liquid level in the tank is taken into account.

When you click on a row in the table, the tank is highlighted on three projections of the image.