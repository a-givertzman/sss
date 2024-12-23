## General cargo
![General view of the tab "General cargo"](/assets/image/program_sheets/en/sheet05_loading/tab05_unitCargo/unitCargo_general.png "General view of the tab 'General cargo'")

The window is designed to set data on general cargo placed on the ship and consists of:
- images of three projections of the ship and the location of general cargo;
- tables with information on general cargo.

### Image of the ship and cargo
The projection of the ship and the work with the image is similar to the tab ["Ballast tanks"](/docs/user-guide/en/part05_loading/chapter02_ballast/chapter02_ballast.md). The general cargo on the projections of the vessel is indicated in the form of a parallelepiped with dimensions specified by the user.

### Cargo information table
For the general cargo, the following data must be entered in accordance with the table.
| Column     | Description                       | Note                                  |
| ---------- | --------------------------------- | ------------------------------------- |
| w/o        | Cargo color                       | All shipments are marked in gray      |
| Name       | Cargo name                        |                                       |
| Weight [t] | Weight                            |                                       |
| $x_g$ [m]  | Longitudinal center of gravity    | In the ship-related coordinate system |
| $y_g$ [m]  | Transverse center of gravity      | In the ship-related coordinate system |
| $z_g$ [m]  | Vertical center of gravity        | In the ship-related coordinate system |
| X1 [m]     | Aft cargo boundary                | In the ship-related coordinate system |
| X2 [m]     | The forward boundary of the cargo | In the ship-related coordinate system |
| Y1 [m]     | The right border of the cargo     | In the ship-related coordinate system |
| Y2 [m]     | Left border of the cargo          | In the ship-related coordinate system |
| Z1 [m]     | The lower border of the cargo     | In the ship-related coordinate system |
| Z2 [m]     | The upper border of the cargo     | In the ship-related coordinate system |
| Deck       | Cargo is placed on the upper deck |                                       |

To add a load, click on the "Add" button at the top of the table. In the pop-up window, you must enter the necessary information given in the table.
When entering values, the following input restrictions apply, which are displayed in orange when entering:
- $x_g$ must be between X1 and X2 (also for y and z);
- X1 must be less than X2 (also for y and z);
- the mass must be positive.

To delete a load, select the appropriate row and click "Delete" at the top of the table.

To adjust the load, select the appropriate row and click "Adjust" at the top of the table. The adjustment is also available from the table.

![General view of the tab "Added general cargo"](/assets/image/program_sheets/en/sheet05_loading/tab05_unitCargo/unitCargo_addCargo.png "General view of the tab 'Added general cargo'")

Additionally, the "Deck cargo" sign can be affixed to the cargo. If the feature is active, the geometry of the cargo is taken into account when determining windage, icing, and stability criteria.