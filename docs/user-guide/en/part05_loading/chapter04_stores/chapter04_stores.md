## Stores
![General view of the tab "Stores"](/assets/image/program_sheets/en/sheet05_loading/tab04_stores/stores.png "General view of the tab 'Stores'")

The window is designed to set data on solid stocks and consists of:
- images of three projections of the vessel and the location of stocks;
- tables with information on stocks.

### Image of the ship and stocks
The tab is similar to the tab ["Ballast tanks"](/docs/user-guide/en/part05_loading/chapter02_ballast/chapter02_ballast.md). Stores on the projections of the vessel are indicated in the form of a square with a horizontal segment located along the hull. The square shows the position of the center of gravity of the reserve, the segment shows its length along the axis of the vessel.

### A table with information on stocks
| Column     | Description                       | Note                                  |
| ---------- | --------------------------------- | ------------------------------------- |
| w/n        | Stock color                       | All stocks are marked in gray         |
| Name       | Name of the stock                 |                                       |
| Weight [t] | Weight                            |                                       |
| $x_g$ [m]  | Abscissa of the center of gravity | In the ship-related coordinate system |
| $y_g$ [m]  | Ordinate of the center of gravity | In the ship-related coordinate system |
| $z_g$ [m]  | Center of gravity application     | In the ship-related coordinate system |
| X1 [m]     | Aft cargo boundary                | In the ship-related coordinate system |
| X2 [m]     | The forward boundary of the cargo | In the ship-related coordinate system |

To add a stock, click on the "Add" button at the top of the table. In the pop-up window, you must enter the necessary information given in the table.
When entering values, the following input restrictions apply, which are displayed in orange when entering:
- $x_g$ must be between X1 and X2;
- X1 must be less than X2;
- the mass must be positive.

To delete a stock, select the appropriate row and click "Delete" at the top of the table.

To adjust the stock, select the appropriate row and click "Adjust" at the top of the table. The adjustment is also available from the table.
![General view of the tab "Add stores"](/assets/image/program_sheets/ru/sheet05_loading/tab04_stores/addStores.png "General view of the tab 'Add stores'")