# Part 01. General Information



## Chapter 01. List of abbreviations

| Reduction | Decoding                            |
| --------- | ----------------------------------- |
| LL        | Load Line                           |
| DSC       | dynamic stability curve |
| CL        | central line                        |
| SSC       | static stability curve  |
| AP        | aft perpendicular                   |
| PS        | port side                           |
| FP        | forward perpendicular               |
| SB        | starboard side                      |
| SF        | stowage factor                      |
| fr.       | frame                               |
| fr.th     | frame theoretical                   |
| ETA       | estimated time of arrival           |
| ETD       | estimated time of departure         |
| POL       | port of loading                     |
| POD       | port of discharge                   |

======================pagebreak======================



## Chapter 02. Program Information



### Software name
| Parameter           | Value                                                                          |
| ------------------- | ------------------------------------------------------------------------------ |
| Name                | BoardTrix                                                                      |
| Version             | 0.9.0                                                                          |
| Version date        | 28.12.2024                                                                     |
| Developer           | S&A Lab LLC                                                                    |
| Developer's address | 192007, St. Petersburg, Ligovsky Prospekt, 150 litera A, office 612, room 27n. |
| Developer's website | sa-lab.dev                                                                     |

For all questions related to the work, please contact
> Technical Product Manager "Shipbuilding and operational Software"
>
> Ivan Merenkov 
> 
> Tel. +7 (911) 812-94-67
>
> Email: merenkov.ia@sa-lab.dev

### Purpose of the program
The software as a cargo computer is designed to create and store a ship's cargo plan, calculate landing characteristics, stability, shear forces and bending moments in calm water, as well as compare them with acceptable values.

### Program functions
- assignment by the operator and storage of the ship's cargo plan for different types of cargo (containers, general cargo, bulk cargo, stores, liquids in tanks, taking into account density);
- assignment by the operator and storage of voyage and their accounting in the preparation of the cargo plan and calculations. Accounting for the icing of the vessel and deck cargo, the density of seawater, the navigation area;
- calculation of the mass of the ship and the position of its center of gravity;
- calculation of the characteristics of the ship draft and comparison with acceptable values (including the rules of load line marks, requirements for deepening the screws);
- calculation of stability characteristics and comparison with acceptable values in accordance with the rules of the Russian Maritime Register of Shipping and the Russian Classification Society (hereinafter the Classification Society);
- calculation of the dependence of shearing forces and bending moments along the length of the ship and comparing them with acceptable ones;
- calculation of stability characteristics and comparison with acceptable values in accordance with the rules of the Russian Maritime Register of Shipping and the Russian Classification Society (hereinafter the Classification Society);
- calculation of the dependence of shearing forces and bending moments along the length of the vessel and comparing them with acceptable ones;
- assessment of emergency stability according to the curve of the minimum permissible metacentric height;
- generation of accounting documentation.

======================pagebreak======================



## Chapter 03. Ship Information



## Ship's parameters

The software has been adapted to work for the next vessel, according to the table.

| Parameter               | Value                               |
| ----------------------- | ----------------------------------- |
| Ship name               | Sofia                               |
| Shipbuilder hull number | 506                                 |
| Navigation area         | Unrestricted                        |
| Type of ship            | General dry cargo ship              |
| IMO number              | 9245263                             |
| Call sign               | UACA5                               |
| Registration number     | 010869                              |
| MMSI                    | 273251830                           |
| Port of registry        | Novorossiysk                        |
| Flag                    | Russian Federation                  |
| Year of build           | 2002                                |
| Place of build          | Westerbroek, the Netherlands        |
| Shipowner               | LLC "Кubаn Маrinе Cоmраnу"          |
| Builder                 | Bodewes Scheepswerp Volharding B.V. |
| Classification society  | RS                                  |

## References
The following documentation was used to create the program.
| №        | Наименование                                                                                  | Примечание |
| -------- | --------------------------------------------------------------------------------------------- | ---------- |
| w/o      | Additional Stability Calculations Performed due to Modification and Increase of Draft. (2020) |            |
| w/o      | Stability Booklet                                                                             |            |
| w/o      | Information on Stability of The Ship loaded with grain                                        |            |
| ISCD5481 | Ship Data booklet                                                                             |            |
| 0023     | Tank arrangement                                                                              |            |
| 0020     | General arrangement                                                                           |            |
| 003      | Capacity plan                                                                                 |            |
| Y0019-00 | Construction plan foreship                                                                    |            |
| Y0011    | Construction plan midship                                                                     |            |
| Y0016-00 | Cross section aftship                                                                         |            |
| Y0018-00 | Cross section foreship                                                                        |            |

======================pagebreak======================



======================pagebreak======================



======================pagebreak======================

# Part 02. The order of work



## Hardware
Hardware requirements required for the operation of the software:
- CPU core i7 (8 x 3 GHz) or equivalent, architecture amd64(x86_64);
- RAM 16 GB;
- Drive: SATA SSD/NVMe 500 GB;
- OS: linux (Debian 12, GNOME DE preferred);
- Monitor with aspect ratio (16:10 or 16:9) with FullHD resolution recommended;
- The mouse and keyboard.

## System setup
`boardtrix` software developed for use on Linux OS (Debian 12, GNOME desktop environment preferred).

Hardware requirements for the software to function:
- CPU core i7 (8 x 3 GHz) or similar, amd64(x86_64) architecture;
- RAM 16 GB;
- Drive: SATA SSD/NVMe 500 GB;
- Monitor with aspect ratio (16:10 or 16:9), FullHD resolution preferred;
- Mouse and keyboard.

Installation of the software requires superuser access and working internet connection.

## Installation of the program

Copy provided archive `boardtrix.tar` to desired directory. For example, to user's home directory (`/home/<User name>`).

### 1.
Open `Terminal` app and go to directory with copied `boardtrix.tar` archive:
```bash
cd <path to `boardtrix.tar` directory>
```

### 2.
Create `boardtrix` folder in the same directory:
```bash
mkdir boardtrix
```

### 3.
Unzip `boardtrix.tar` into the created directory:
```bash
tar -xf boardtrix.tar -C ./boardtrix
```
and go to it:
```bash
cd ./boardtrix
```

### 4.
If current user doesn't have superuser permissions, you can use `./install_sudo.sh` script in the same folder, run the command and follow appearing instructions to do this:
```bash
./install_sudo.sh
```
Reboot your PC after complete execution of the script.  

### 4.5.
If step `4` was completed, open terminal again after PC reboot and go to archive direсtory (repeat step `1`) and go straight to step `5`.

### 5.
Execute `update_source_list.sh` script to add repository with `boardtrix` packages to system repository list:
```bash
sudo ./update_source_list.sh
```

### 6.
Install program by running the command below and following the instructions that appear:
```
sudo apt install boardtrix
```

Installed program can be launched either by executing a command in the terminal (from any directory):
```bash
boardtrix
```
or using the tools of the desktop environment installed in the system (for example `GNOME` or `XFCE`), by searching in the application menu by the name of the program: `boardtrix`.

## Uninstalling of the program:

To remove the application, run the command in the terminal:
```bash
sudo apt autoremove boardtrix
```


## Periodic checks
During the annual, interim and renewal inspection on board the ship in the presence of an inspector of the classification society or in other necessary case, the on-board software is checked using test calculations corresponding to the documentation on the stability of the vessel. The results of the test calculations approved by the classification society are supplied together with the documentation for the software. The download cases specified in the software, corresponding to the test calculations, are stored in the program archive together with the rest of the cases and are protected from writing and deletion.

======================pagebreak======================



======================pagebreak======================

# Part 03. Main Screen



## General information
![General view of the "Main screen" page](/assets/image/program_sheets/ru/sheet03_mainScreen/general.png "General view of the 'Main screen' page")

After launching, a page opens with the main screen of the program. There is a vertical [navigation bar](/docs/user-guide/en/part03_mainScreen/chapter02_navigationPanel.md) on the left side of the screen

The main screen is designed to display generalized information on the current cargo plan, and consists of:
- [images of the ship in two projections](/docs/user-guide/en/part03_mainScreen/chapter03_draftPicture.md);
- [a field with a circular stability indicator](/docs/user-guide/en/part03_mainScreen/chapter04_stability.md);
- [a field with a diagram of the total longitudinal strength](/docs/user-guide/en/part03_mainScreen/chapter05_strength.md);
- [a field with a table of displacement components](/docs/user-guide/en/part03_mainScreen/chapter06_weight.md).

## Navigation Bar
The "Run calculations" button is located at the top of the navigation bar. When you click on the button, the calculation is started. After the calculation is completed, all data on the ship on all pages of the program will be updated.

There are buttons below to switch between the program pages:
- [Main](/docs/user-guide/en/part03_mainScreen/part03_mainScreen.md)
- [Information](/docs/user-guide/en/part04_Info/part04_shipInfo.md);
- [Loading](/docs/user-guide/en/part05_loading/part05_loading.md);
- [Draft](/docs/user-guide/en/part06_draft/part06_draft.md);
- [Strength](/docs/user-guide/en/part07_strength/part07_strength.md);
- [Stability](/docs/user-guide/en/part08_stability/part08_stability.md);
- [Help](/docs/user-guide/en/part09_help/part09_help.md).
- [Settings](/docs/user-guide/en/part10_settings/part10_settings.md)

The following values are placed at the bottom of the navigation bar, which are displayed on all pages of the program (with the exception of help):
| №   | Name             | Dimension |
| --- | ---------------- | --------- |
| 7   | Heel             | [degree]  |
| 51  | Trim             | [m]       |
| 94  | Draft at midship | [m]       |
| 2   | Displacement     | [t]       |

## The image of the ship
At the top of the page there is an image of the vessel in two projections, which show the position of the vessel relative to the current waterline. The following values are also shown in the image:
| №   | Наименование     | Размерность |
| --- | ---------------- | ----------- |
| 4   | Draft at FP      | [m]         |
| 5   | Draft at AP      | [m]         |
| 6   | Trim             | [degree]    |
| 94  | Draft at midship | [m]         |
| 7   | Heel             | [degree]    |

More detailed information on drafts of the vessel can be found on the page  ["Draft"](/docs/user-guide/en/part06_draft/part06_draft.md).

## A field with a circular stability indicator
A circular stability indicator is shown in the middle part on the right. The indicator shows the value of the corrected metacentric height.
<!-- TODO: уточнить после реализации -->
If stability is not provided for the current loading case (at least one of the stability criteria is not met), the scale is highlighted in red.

More detailed information on the stability of the vessel can be found on the page ["Stability"](/docs/user-guide/en/part08_stability/part08_stability.md).

## A field with a diagram of the total longitudinal strength
A diagram of the total longitudinal strength is shown in the middle part. For each formation evenly distributed along the length of the vessel, the shearing force or bending moment is displayed as a percentage (based on which parameter has a higher percentage), which is the calculated value of the permissible value. If the calculated value exceeds the permissible value by more than 100% (marked on the diagram with a horizontal orange line) The corresponding column is colored with an orange shaded area.
![Exceeding the permissible strength](/assets/image/program_sheets/en/sheet03_mainScreen/strength_overLim.PNG "Exceeding the permissible strength")

More detailed information on the overall longitudinal strength of the vessel can be found on the page ["Strength"](/docs/user-guide/en/part07_strength/part07_strength.md).

## A field with a table of displacement components
At the bottom of the screen there is a table with the mass, the coordinates of the center of mass for the main components of displacement, as well as the total displacement:
- Displacement
- Deadweight
  - Cargo
  - Bulkheads
  - Ballast
  - Stores
- Icing
- Empty

More detailed information on loading the vessel can be found on the page ["Loading"](/docs/user-guide/en/part05_loading/part05_loading.md).

======================pagebreak======================



======================pagebreak======================

# Part 04. Ship and voyage information



## Chapter 01. General information

The logo of the shipping company or vessel is placed on the left side of the page, which is placed at the request of the Customer.

There is a field on the right side of the page for displaying the following tabs:
- [information about the ship](/docs/user-guide/en/part04_Info/chapter02_shipInfo/chapter02_shipInfo.md); 
- [voyage information](/docs/user-guide/en/part04_Info/chapter03_wayinfo/chapter03_wayinfo.md);
- [saving the cargo plan](/docs/user-guide/en/part04_Info/chapter04_save/chapter04_save.md).

======================pagebreak======================



## Chapter 02. Basic ship data

![General view of the "Ship Data" tab](/assets/image/program_sheets/ru/sheet04_info/shipInfo_general.png "General view of the 'Ship Data' tab")
The list of information on the vessel is given in the table. The information is used to compile reports.
| Parameter               | Note                  |
| ----------------------- | --------------------- |
| Ship name               |                       |
| Call sign               |                       |
| IMO number              |                       |
| MMSI                    |                       |
| Type of ship            |                       |
| Navigation area         |                       |
| Classification society  |                       |
| Registration number     |                       |
| Port of registry        |                       |
| Flag                    |                       |
| Shipowner               |                       |
| Shipowner code          |                       |
| Builder                 |                       |
| Place of build          |                       |
| Year of build           |                       |
| Shipbuilder hull number |                       |
| Master                  | Filled in by the user |
| Chief mate              | Filled in by the user |

======================pagebreak======================



## Chapter 03. Voyage data



### Description of the tab
![General view of the tab "Voyage data"](/assets/image/program_sheets/en/sheet04_info/wayinfo_general.png "General view of the tab  'Voyage data'")

Вкладка состоит из следующих полей:
- [General parameters](/docs/user-guide/en/part04_Info/chapter03_wayinfo/section02_general.md);
- [Itinerary](/docs/user-guide/en/part04_Info/chapter03_wayinfo/section03_way.md).

### General parameters
The list of general voyage information is given in the table. The list of information on the cargo plan is given in the table. All voyage data is filled in by the user.
| Name                       | Required | Format                  | By default |
| -------------------------- | -------- | ----------------------- | ---------- |
| Voyage Code                | None     | Any                     | -          |
| Seawater density $[t/m^3]$ | Yes      | Number                  | 1.025      |
| Icing                      | Yes      | No / Full / Partial     | No         |
| Water area                 | Yes      | "Port" / "Sea"          | "Sea"      |
| Load Line                  | Yes      | Selection from the list | Summer     |
| Voyage description         | None     | Any                     |            |

#### Flight code
The unique code of the flight or cargo plan. It is used in the preparation of reports and for the convenience of voyage identification.

#### Water area
The choice of the water area (port or sea) determines the strength limits used in the calculations of shear forces and bending moments.

#### Density of seawater
The density of seawater used in calculations.

#### Load Line
Load line type determines the draft limits used in the calculations of the ship's draft. The list of cargo marks to choose from corresponds to the cargo marks applied to the vessel. In general, the list is as follows:
- Summer
- Winter
- Winter in the North Atlantic
- Tropical
- Summer in fresh water
- Tropical in fresh water
- Summer timber
- Winter timber
- Winter timber in the North Atlantic 
- Tropical timber
- Summer timber in fresh water
- Tropical timber in fresh water
- LL subdivision

#### Icing
The choice of icing is taken into account in the calculations of draft, strength and stability.

#### Voyage description
If necessary, a verbal description of the voyage or cargo plan or any comment can be added. 

### Itinerary
An unlimited number of ports of call can be set for each voyage. The information is used to compile reports and help with container bay plans.

The port is added by clicking the "Add itinerary point" button. To delete a port, select the appropriate line and click "Delete itinerary point". If, when deleting a itinerary point, there is a container in the bay plan for which this port is set as POL or POD, a corresponding message is displayed. Deletion is performed after confirmation by the user.

> [!WARNING] 
> Deleting a port in this case will reset all POL and POD records for containers on this port.

The list of information on ports of call that can be specified is given in the table. 
| Parameter                         | Note                        |
| --------------------------------- | --------------------------- |
|                                   | Port color                  |
| Port Name                         | Port name                   |
| Port code                         | Unique port code            |
| ETA                               | Estimated time of arrival   |
| ETD                               | Estimated time of departure |
| Status                            |                             |
| Max. draft [m]                    | Draft limit                 |

#### Port color
A color can be assigned for each port, which will be displayed when working with containers. The color is selected from the menu after clicking on the color of the corresponding port.
![Port color selection](/assets/image/program_sheets/en/sheet04_info/wayinfo_color.png "Port color selection")

#### Port name and code
A name and a code can be assigned for each port. These parameters are displayed when working with containers and are used when compiling a report.

#### ETA, ETD, status
For each port, the date and time of arrival and departure can be set, which are displayed when working with containers and used when compiling the report.

After clicking on the value that needs to be changed, you need to select a date in the calendar pop-up window. It is also possible to set the date using the keyboard, for which you need to click "Switch to manual input" in the lower left corner of the pop-up calendar. After selecting the date in the pop-up dial, you need to select the hours and minutes. It is also possible to set the time from the keyboard, for which you need to click "Switch to manual input" in the lower left corner of the pop-up dial.

The rows in the table are sorted automatically after adjusting the arrival or departure time, in ascending order of arrival time.

![Calendar](/assets/image/program_sheets/en/sheet04_info/wayinfo_calendar.png "Calendar")
![Date selection](/assets/image/program_sheets/en/sheet04_info/wayinfo_date.png "Date selection")
![Dial](/assets/image/program_sheets/en/sheet04_info/wayinfo_watch.png "Dial")
![Timing](/assets/image/program_sheets/en/sheet04_info/wayinfo_time.png "Timing")
The status column displays the result of checking the correctness of filling in the departure and arrival times. When you hover over the status, the error message is displayed. The following errors are detected in the software:
- the time spent in one port intersects with the time spent in another port;
- the departure time for the port is less than the arrival time.

#### The draft in the port
For each port, the maximum draft of the vessel at which entry into the port is possible can be assigned.

======================pagebreak======================



## Chapter 04. Saving the project

![Tab "Saving the project"](/assets/image/program_sheets/en/sheet04_info/save_general.png "Tab 'Saving the project'")

It is possible to save data on the current cargo plan in the software.

When you click "Save", the data is saved to a new record. The name of the record is assigned the date and time of saving.

When you click "Save as" data, you can assign a name to the record. The data is saved to a new record. If there is already a project with this name, then a pop-up window appears in which you need to confirm or cancel the recording.
![Entering the name](/assets/image/program_sheets/en/sheet04_info/save_projectname.png "Entering the name")

To open the cargo plan that was compiled and saved earlier, click "Open" in the right corner of the tab.
> [!WARNING] 
> When you open a saved cargo plan, the data for the current cargo plan will be deleted.

You can erase the project record by clicking "Delete".

======================pagebreak======================



======================pagebreak======================



======================pagebreak======================

# Part 05. Loading



## Chapter 01. General provisions

The "Loading" page is intended for specifying data on the cargo plan of the vessel. In the upper part there is a navigation panel of the page, with which you can switch between the tabs for setting different types of cargo:
- Ballast tanks;
- Stores tanks;
- Other stores;
- General cargo;
- Bulk cargo;
- Containers.

> [!NOTE]
> The list of cargoes may change depending on the equipment of the vessel.

======================pagebreak======================



## Chapter 02. Ballast tanks

![General view of the tab "Ballast"](/assets/image/program_sheets/en/sheet05_loading/tab02_ballast/ballast.png "General view of the tab 'Ballast'")

The tab is intended for specifying data on ballast tanks and consists of:
- images of three projections of the vessel and ballast tanks;
- tables with information on ballast tanks.
### Image of the vessel and ballast tanks
Изображение судна состоит из трех проекций: сбоку, сверху, с кормы в нос. На изображении предусмотрена  возможность отобразить следующие элементы:
- Axes - displays a dimensional scale in meters relative to the ship's coordinate system;
- Grid - the grid corresponding to the dimensional scale is displayed;
- Fr. - practical frames are displayed;
- Fr.th - theoretical frames are displayed.

!["Image Elements"](/assets/image/program_sheets/en/sheet05_loading/tab02_ballast/ballast_grid.jpg "Image Elements")

When you click on one of the ballast tanks on one of the projections, it is highlighted on the other projections and in the table.

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

======================pagebreak======================



## Chapter 03. Stores tanks

![General view of the tab "Stores tanks"](/assets/image/program_sheets/en/sheet05_loading/tab03_storeTanks/storeTanks.png "General view of the tab 'Stores tanks'")

The tab is used to set data on stock tanks.

The tab is similar to the tab ["Ballast tanks"](/docs/user-guide/en/part05_loading/chapter02_ballast/chapter02_ballast.md).

The following colors are accepted for stock tanks:
- Fuel - brown;
- Oil tanks - brown;
- Fresh water - blue;
- For polluted waters - black;
- Other tanks are grey.

======================pagebreak======================



## Chapter 04. Stores

![General view of the tab "Stores"](/assets/image/program_sheets/en/sheet05_loading/tab04_stores/stores.png "General view of the tab 'Stores'")

The window is designed to set data on solid stocks and consists of:
- images of three projections of the vessel and the location of stocks;
- tables with information on stocks.

### Image of the ship and stocks
The tab is similar to the tab ["Ballast tanks"](/docs/user-guide/en/part05_loading/chapter02_ballast/chapter02_ballast.md). Stores on the projections of the vessel are indicated in the form of a square with a horizontal segment located along the hull. The square shows the position of the center of gravity of the reserve, the segment shows its length along the axis of the vessel.

### A table with information on stocks
| Column     | Description                       | Note                                  |
| ---------- | --------------------------------- | ------------------------------------- |
| w/o        | Stock color                       | All stocks are marked in gray         |
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

======================pagebreak======================



## Chapter 05. General cargo

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

======================pagebreak======================



## Chapter 06. bulk cargo

![General view of the tab "bulk cargo"](/assets/image/program_sheets/en/sheet05_loading/tab06_bulkCargo/bulkCargo.png "General view of the tab 'bulk cargo'")
The window is designed to set data on bulk cargoes placed in the hold. The assignment of such cargo for the hold is made through the stowage factor (SF).

When specifying bulk cargo data, the separation of the hold by bulkheads for bulk cargo can be taken into account. To do this, in the special "Grain bulkheads" window, you need to specify the installation locations of bulkheads for bulk cargo. After saving the data in the Grain Bulkheads window, the hold will be automatically divided into compartments, while all the necessary parameters for calculations will be determined automatically.
> [!CAUTION]
> All cargo data for the hold for which the bulkhead positions for bulk cargo have been changed will be deleted after saving!

![General view of the tab "Bulkheads"](/assets/image/program_sheets/en/sheet05_loading/tab06_bulkCargo/bulkheads.png "General view of the tab 'Bulkheads'")

For each hold (or its component parts), you must specify the data of the columns "M[t]", "V$[m^3]$", "UPO $[m^3/t]$", "%", "Bulk cargo". At the same time, the following logic of changing these parameters is implemented:
- when changing %
  - the SF is not recalculated;
  - V and M are recalculated;
- when changing V
  - the SF is not recalculated;
  - % and M are recalculated;
- when changing M 
  - the SF is not recalculated;
  - % and V are recalculated;
- when changing the SF
  - not recalculated V;
  - % and M are recalculated.

In the column "Shifting cargo", a sign can be placed for the cargo in each hold (part of the hold). If such a sign is affixed to at least one part of the hold, when checking the stability criteria, the requirements for a vessel carrying grain are checked, namely:
- the criterion of the roll angle from grain displacement is checked;
- the criterion of the remaining area of the static stability curve is checked;
- the metacentric height should be more than 0.30 m.
> [!WARNING]
> The grain moment from the displacement of the grain is determined only for the cargo for which the "Shifting cargo" sign is affixed!

======================pagebreak======================



## Chapter 07. Containers



### General provisions
The window is intended for setting container data.
![General view of the tab "Containers"](/assets/image/program_sheets/en/sheet05_loading/tab07_containers/container_general.png "General view of the tab 'Containers'")
The window consists of
- bay plan;
- container tables.

### Types of containers

It is possible to place the following types of containers in the software according to the table.

| Name                  | ISO designation | Size code |
| --------------------- | --------------- | --------- |
| 20-foot low standard  | 1C              | 20        |
| 20-foot standard      | 1CC             | 22        |
| 20-foot high cube     | 1CC             | 25        |
| 30-foot low standard  | 1B              | 30        |
| 30-foot standard      | 1BB             | 32        |
| 30-foot high cube     | 1BBB            | 35        |
| 40- foot low standard | 1A              | 40        |
| 40-foot standard      | 1AA             | 42        |
| 40- foot high cube    | 1AAA            | 45        |

> [!NOTE]
> The list of containers available for installation may vary depending on the equipment of the vessel.

1. The "ISO designation" of containers in accordance with ISO 668:2020/Amd.1:2022(E).
2. The "size code" (i.e. the external dimension) of the container is determined in accordance with ISO6346:2022. The size code format is two alphanumeric characters:
- the first is a numeric or alphabetic character, denotes the length;
- the second one is a numeric or alphabetic character, denotes width and height.<br>

The length code is equal to:
- 2 for a container with a length of 6058 mm;
- 3 for a container with a length of 9125 mm;
- 4 for a container with a length of 12192 mm.<br>

The width and height code is equal to:
- 0 for a container with a width of 2438 and a height of 2438;
- 2 for a container with a width of 2438 and a height of 2591;
- 5 for a container with a width of 2438 and a height of 2896.

The external dimensions and permissible weight of one container in accordance with ISO 668:2020/Amd.1:2022 are shown in the table.
| Designation | Length [mm] | Width [mm] | Height [mm] | Permissible gross weight [kg] |
| ----------- | ----------- | ---------- | ----------- | ----------------------------- |
| 1C          | 6058        | 2438       | 2438        | 36000                         |
| 1СС         | 6058        | 2438       | 2591        | 36000                         |
| 1ССC        | 6058        | 2438       | 2896        | 36000                         |
| 1B          | 9125        | 2438       | 2438        | 36000                         |
| 1BB         | 9125        | 2438       | 2591        | 36000                         |
| 1BBB        | 9125        | 2438       | 2896        | 36000                         |
| 1A          | 12192       | 2438       | 2438        | 36000                         |
| 1AA         | 12192       | 2438       | 2591        | 36000                         |
| 1AAA        | 12192       | 2438       | 2896        | 36000                         |

### Adding containers
![General view of the tab "Adding containers"](/assets/image/program_sheets/en/sheet05_loading/tab07_containers/container_added.png "General view of the tab 'Adding containers'")
In order to add a container to the list of available containers on the ship, click on the "Add" button. In the window that opens, you must specify the data placed in the left column in accordance with the table:
| No. | Name                 | Definition                                                  | Required | Format         | Default value                        |
| --- | -------------------- | ----------------------------------------------------------- | -------- | -------------- | ------------------------------------ |
| 1   | Length               | Overall length of the container                             | yes      | Drop-down list | 20 ft                                |
| 2   | Height               | Overall height of the container                             | yes      | drop-down list | Standard                             |
| 3   | Type code            | Type code and the main characteristic of the type           | no       | two symbols    | GP                                   |
|     |                      |                                                             |          |                |                                      |
| 4   | Gross weight         | Weight of the transported container with cargo              | yes      | Number         | -                                    |
| 5   | Maximum gross weight | Maximum permissible weight of a container with cargo        | no       | Number         | according to ISO 668:2020/Amd.1:2022 |
| 6   | Tare weight          | Weight of the container without cargo                       | no       | Number         | -                                    |
|     |                      |                                                             |          |                |                                      |
| 7   | Owner's code         | Unique container owner's code                               | none     | three letters  | OWN                                  |
| 8   | Serial number        | Container serial number                                     | none     | six digits     | 000000                               |
| 9   | Control number       | The authenticity code of the owner's code and serial number | none     | one digit      | 0                                    |
|     |                      |                                                             |          |                |                                      |
| 10  | POL                  | Loading port                                                | yes      | drop-down list | First port of the route              |
| 11  | POD                  | Unloading port                                              | yes      | drop-down list | Last port of the route               |
|     |                      |                                                             |          |                |                                      |
| 12  | Number of containers | Number of containers to add                                 | yes      | number         | 1                                    |

When you enter data in the left column, the right one is filled in automatically:
| Apostille | Name                | Definition                              | Meaning                                                 |
| --------- | ------------------- | --------------------------------------- | ------------------------------------------------------- |
| 1         | ISO code            | Container external dimension code       | three symbols according to ISO 668:2020/Amd.1:2022(E)   |
| 2         | Size code           | Container external dimension code       | two symbols according to ISO6346:2022                   |
|           |                     |                                         |                                                         |
| 4         | Maximum net weight  | Maximum permissible weight of the cargo | maximum net weight = Maximum gross weight - Tare weight |
| 5         | Net weight          | Weight of the cargo in the container    | net weight = Gross weight - Tare weight                 |
|           |                     |                                         |                                                         |
| 6         | Container code      | Unique container code                   | according to ISO6346:2022                               |
|           |                     |                                         |                                                         |
| 7         | POL ETA-ETD         | Time spent at the port of loading       | according to the specified route                        |
| 8         | POL ETA-ETD         | Time spent at the port of discharge     | according to the specified route                        |

After saving, the container(s) are added to the general list available for placement. To delete a container, select the appropriate line and click "Delete". It is impossible to remove containers that are already installed on the ship, to remove it, it must be unloaded from the ship.

To delete all containers, click "Delete all containers". It is impossible to remove all containers with at least one container installed, for removal it is necessary to unload all containers from the ship.

After adding the data for containers, it is also possible to change from the table with the general list of containers. The following colors are displayed in the table and on the bayplane of the container:

- green - 20-foot;
- purple - 30-foot;
- blue - 40-foot.

When you hover over the color of the container, a hint with its "ISO value" is displayed in the table.

### Description of the bay plan
At the top of the screen there is a bay plan, which is designed in accordance with ISO 9711-1 part 1.
The "section-row-tier" system has been adopted for the placement of containers. The format of the container placement code is BBRRTT, where BB is a section, RR is a row, TT is a tier.

#### Section 
Numbering from bow to stern. Odd numbers are accepted for numbering 20-foot containers. For 40-footers, even ones. 30-foot ones are indicated by even numbers with a "*" sign. 

In the case of mixed stacking of two 20-foot containers in a 40-foot compartment, the aft 20-foot container is shown on the plan of the 40-foot compartment, while the 20-foot container is shown on the plan of a separate compartment having the previous odd number in seniority. 

For a plan that accommodates only 20-foot containers, the even section is enclosed in brackets. For mixed plans or in which only 40-footers are placed, the odd section is enclosed in brackets. 

The plans are scrolled by clicking on the line with the plan numbers located under the section plans.

To the right of the bay plan is the total number of containers in the hold and on deck in each section.

#### Row
Numbering from the diametrical plane. The rows of containers located on the ship to the right of the CL are numbered with odd numbers, on the left with even numbers. If the number of rows is odd, the row located in the CL is numbered 00.

#### Tier
Numbering of containers from the bottom. Containers located in the hold are numbered from 02, standing directly on the main deck are numbered 80, and those standing on hatches are numbered from 82. With each tier, 2 is added to the figure. The numbering scheme of the tiers remains unchanged, even if containers are loaded with a height other than the standard one.

### Loading of containers

The container is selected by clicking on the corresponding container from the list or (if it is installed on the ship) from the bay plane. To load the container, select the container from the list and the installation location, and then click "Load container". You can also load the selected container by double-clicking on an empty space.
If you select a container from the general list, you can place it in the available installation locations. At the same time, the following restrictions on the installation of containers apply:
- installation of a shorter container on a longer container (20- or 30-foot by 40-foot) is not allowed; 
- the number of containers installed in one stack depends on the height of the containers and is limited by the permissible height of the stack;
- when installing a 40-foot container on a container of a shorter length, it is assumed that it is installed on one side on an overpass, the overpasses are highlighted in brown;
- when installing a 40-foot container on two containers of shorter length with different heights, the installation height of the 40-foot container is determined by the higher height of the lower containers. The second side assumes that the container is installed on an overpass, which is also highlighted in brown;
- when removing a container from the lower tier, on which the container(s) is already installed, it is assumed that it is replaced by an overpass of a similar height, which is also highlighted in brown.

After assigning a place to the container, its center of gravity coordinates are determined automatically. The center of gravity of each container in height, length and width is taken at its center. When determining the center of gravity by height, separation between containers is taken into account, as well as separation of the lower container from the deck of the installation. When containers are installed on deck, the windage and icing of the deck cargo of containers are taken into account in the calculation, and the criterion "Roll from circulation" is calculated.

To unload containers, select a container and click unload container. It is also possible to unload the container by right-clicking on it. Additionally, it is possible to unload all loaded containers, for this you need to click on the clear plan button.

======================pagebreak======================



======================pagebreak======================



======================pagebreak======================

# Part 06. Draft



## General provisions
![General view of the page "Drafts"](/assets/image/program_sheets/en/sheet06_draft/draft_perpendicular.png "General view of the page 'Drafts'")

The page consists of:
- an image of a vessel with precipitation, located at the top of the page;
- a table with landing criteria located at the bottom of the page.

## Image of the ship
The ship's draft is displayed on the ship's image. In the upper part there is a field for selecting the precipitation output mode:
- on the perpendiculars;
- on marks.

![Draft on marks](/assets/image/program_sheets/en/sheet06_draft/draft_perpendicular.png "Draft on marks")

When precipitation is displayed on the perpendiculars, the following precipitation is displayed
| №   | Name             | Dimension |
| --- | ---------------- | --------- |
| 4   | Draft at FP      | [m]       |
| 5   | Draft at AP      | [m]       |
| 94  | Draft at midship | [m]       |

When precipitation is displayed on marks, the following precipitation is displayed
| №   | Name                                 | Dimension |
| --- | ------------------------------------ | --------- |
| 79  | Draft aft at marks SB                | [m]       |
| 80  | Draft aft at marks PS                | [m]       |
| 81  | Draft aft at marks mean              | [m]       |
| 82  | Draft intermediate aft at marks SB   | [m]       |
| 83  | Draft intermediate aft at marks PS   | [m]       |
| 84  | Draft intermediate aft at marks mean | [m]       |
| 85  | Draft middle at marks SB             | [m]       |
| 86  | Draft middle at marks PS             | [m]       |
| 87  | Draft middle at marks mean           | [m]       |
| 88  | Draft intermediate fwd at marks SB   | [m]       |
| 89  | Draft intermediate fwd at marks PS   | [m]       |
| 90  | Draft intermediate fwd at marks mean | [m]       |
| 91  | Draft fwd at marks SB                | [m]       |
| 92  | Draft fwd at marks PS                | [m]       |
| 93  | Draft fwd at marks mean              | [m]       |

## Table with landing criteria
The criteria table provides a summary of information on the fulfillment of the landing criteria required for the vessel:
- name of the criterion with dimension;
- its calculated value;
- fulfillment condition (more/less);
- acceptable value;
- the status of the criterion fulfillment for the current download.
  
The list of calculated criteria is given in the table. The list of criteria to be applied to the vessel, depending on the specified cargo, is determined automatically. The criteria are calculated in accordance with the rules of the classification society:
- [1] [Guidelines on application of provisions of the interntional convention of the interntional convention, ND No 2-030101-046-E, RMRS, 2024](/reference/en/RMRS/Guidelines/ships_&_offshore_installations/2-030101-046_LL_66_88.pdf).

| №   | Name                                     | Dimension |
| --- | ---------------------------------------- | --------- |
| 101 | Summer LL draft SB                       | [m]       |
| 102 | Summer LL draft PS                       | [m]       |
| 103 | Winter LL draft SB                       | [m]       |
| 104 | Winter LL draft PS                       | [m]       |
| 105 | Winter North Atlantic LL draft SB        | [m]       |
| 106 | Winter North Atlantic LL draft PS        | [m]       |
| 107 | Tropical LL draft SB                     | [m]       |
| 108 | Tropical LL draft PS                     | [m]       |
| 109 | Fresh water LL draft in summer SB        | [m]       |
| 110 | Fresh water LL draft in summer PS        | [m]       |
| 111 | Tropical fresh water LL draft SB         | [m]       |
| 112 | Tropical fresh water LL draft PS         | [m]       |
| 113 | Summer timber LL draft SB                | [m]       |
| 114 | Summer timber LL draft PS                | [m]       |
| 115 | Winter timber LL draft SB                | [m]       |
| 116 | Winter timber LL draft LW PS             | [m]       |
| 117 | Winter North Atlantic timber LL draft SB | [m]       |
| 118 | Winter North Atlantic timber LL draft PS | [m]       |
| 119 | Tropical timber LL draft SB              | [m]       |
| 120 | Tropical timber LL draft PS              | [m]       |
| 121 | Fresh water timber LL draft in summer SB | [m]       |
| 122 | Fresh water timber LL draft in summer PS | [m]       |
| 123 | Tropical fresh water timber LL draft SB  | [m]       |
| 124 | Tropical fresh water timber LL draft PS  | [m]       |
| 125 | LL draft SI1 (reserve)                   | [m]       |
| 140 | LL draft SI16 (reserve)                  | [m]       |
| 141 | Maximum forward trim                     | [m]       |
| 142 | Maximum aft trim                         | [m]       |
| 143 | Depth at forward perpendicular SB        | [m]       |
| 144 | Depth at forward perpendicular PS        | [m]       |
| 145 | Screw immersion CL                       | [%]       |
| 146 | Screw immersion SB                       | [%]       |
| 147 | Screw immersion PS                       | [%]       |
| 148 | Screw immersion (reserve)                | [%]       |
| 149 | Screw immersion (reserve)                | [%]       |
| 150 | Reserve buoyancy in bow                  | $[m^2]$   |

======================pagebreak======================



======================pagebreak======================

# Part 07. Page "Strength" 

![General view of the page "Strength"](/assets/image/program_sheets/en/sheet07_strength/strength.png "General view of the page 'Strength'")

The Strength page is designed to display the results of calculating shear forces and bending moments and compare them with acceptable values and consists of graphs and tables of bending moments (in the upper part) and shear forces (in the lower part) accordingly.

The data are given for spacings evenly distributed along the length of the vessel. The tables for each location show:
| Name of the parameter | Description |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| " Value" | Calculated values of bending moments and shearing forces. The values are also displayed on the charts as histograms |
| "Lower limit", "Top limit" | Upper and lower permissible limits. The values are also displayed on the charts with orange limits |
| "Acceptable" | The percentage of the calculated value of the acceptable value
 
The rows in the table can be sorted in ascending or descending order by the values of each column, the sorting mode for the column changes when you click on its header.

======================pagebreak======================



======================pagebreak======================

# Part 08. Page "Stability"

![General view of the page "Stability"](/assets/image/program_sheets/en/sheet08_stability/stability.png "General view of the page 'Stability'")

The Stability page is designed to display the results of calculating the criteria and parameters of stability and consists of:
- stability shoulder graphics;
- tables of stability criteria;
- tables of stability parameters.## Stability curves graph
The graph of stability curves shows:
- line static stability curve (SSC);
- line dynamic stability curve (DSC);
- line initial stability $h$.

The stability curves is plotted towards the initial roll of $\theta_0$. The direction of the graph is indicated in the title. The graph also shows the values:
- the initial roll of the vessel $\theta_0$;
- the roll of the vessel is equal to $\theta_0+1rad$;
- corrected initial metacentric height of $h$.
When you hover over the graph field, the value for each curve is displayed for each roll angle in increments of 1 degree.

## Table of stability criteria
The table provides a summary of information on the fulfillment of the stability criteria required for the vessel: 
- name of the criterion with dimension;
- its calculated value;
- fulfillment condition (more/less);
- acceptable value; 
- the status of the criterion fulfillment for the current download.
  
The list of calculated criteria is given in the table. The list of criteria applied to the vessel, depending on the specified cargo, is determined automatically. The criteria are calculated in accordance with the RMRS rules.:
- [1] [Rules for the classification and construction of sea-going ships, part IV "Stability", ND № 2-020101-174-4, RMRS, 2024](/reference/en/RMRS/Rules/classification_&_construction_of_ships_&_offshore_installations/Ships_(primary_group)/Sea-Going_Ships/2-020101-174-4_stability.pdf);
- [2] [Rukes for the carriage of grain, ND №2-020101-013-E, RMRS, 2006](/reference/en/RMRS/Rules/different_types_of_ships/2-020101-013-E.pdf);
- [3] [Rules for the classification and construction of sea-going ships, part V «Subdivision»,ND № 2-020101-174-5, RMRS, 2024](/reference/en/RMRS/Rules/classification_&_construction_of_ships_&_offshore_installations/Ships_(primary_group)/Sea-Going_Ships/2-020101-174-5_subdivision.pdf).

| №   | Name                                             | Demention | Rule                             |
| --- | ------------------------------------------------ | --------- | -------------------------------- |
| 1   | Weather criterion                                | -         | [1] chapter 2.1                  |
| 2   | Wind static heel                                 | [degree]  |                                  |
|     | - all ships                                      |           | [1] point 2.1.3                  |
|     | - timber carrier                                 |           | [1] point 3.3.5                  |
|     | - when transporting containers                   |           | [1] point 3.10.6 – 3.10.8        |
| 3   | Area of LC up to 30°                             | [m∙rad]   | [1] chapter 2.21                 |
| 4   | Area of LC up to $θ_{l_{max}}$                   | [m∙rad]   | [1] chapter 2.2.3                |
| 5   | Area of LC up to 40°                             | [m∙rad]   |                                  |
|     | - all ships                                      |           | [1] chapter 2.2.1                |
|     | - timber carrier                                 |           | [1] chapter 3.3.5                |
| 6   | Area of LC between 30° & 40°                     | [m∙rad]   | [1] point 2.2.1                  |
| 7   | Maximum LC                                       | [m]       | [1] point 2.2.1.1                |
| 8   | Maximum LC with timber                           | [m]       | [1] chapter 3.3.5                |
| 9   | Maximum LC with icing                            | [m]       | [1] chapter 2.4.9                |
| 10  | Heel with maximum LC                             | [degree]  |                                  |
|     | - all ships                                      |           | [1] chapter 2.2.1                |
|     | - if $B/D>2$                                     |           | [1] chapter 2.2.2                |
| 11  | Heel with first maximum LC                       | [degree]  |                                  |
|     | - all ships                                      |           | [1] chapter 2.2.1                |
|     | - if $B/D>2$                                     |           | [1] chapter 2.2.2                |
| 12  | Min. metacentric height                          | [m]       |                                  |
|     | - all ships                                      |           | [1] point 2.3                    |
|     | - for ro-ro dry cargo ships                      |           | [1] point 3.2.4                  |
|     | - timber carrier                                 |           | [1] point 3.3.5                  |
|     | - when transporting grain                        |           | [2]                              |
| 13  | Acceleration criterion                           | -         | [1] point 3.2.5, point 3.12.4    |
| 14  | Heel on turning                                  | [degree]  | [1] point 3.10.6, 3.10.8, 3.10.9 |
| 15  | Heel from grain displacement                     | [degree]  | [2]                              |
| 16  | Area of LC from grain displacement               | [m∙rad]   | [2]                              |
| 17  | Min. metacentric height due to subdivision index | [m]       | [3]                              |

## Table of stability parameters
The table of stability parameters provides a summary of stability parameters and auxiliary values required for calculating stability criteria. The list of displayed parameters is given in the table. The list of parameters changes automatically depending on the type of cargo and the required criteria. The rows in the table can be sorted in ascending or descending order by the values of each column, the sorting mode for the column changes when you click on its header.

| №   | Name                                                     | Dimension |
| --- | -------------------------------------------------------- | --------- |
| 1   | Vertical centre of gravity fixed                         | [m]       |
| 8   | Tonnes per 1 cmи                                         | [t]       |
| 9   | Moment to heel 1 degree                                  | [t•m]     |
| 10  | Moment to trim 1 cm                                      | [t•m/cm]  |
| 11  | Vertical centre of buoyancy                              | [m]       |
| 12  | Vertical centre of gravity                               | [m]       |
| 13  | Transverse metacentric radius                            | [m]       |
| 14  | Vertical centre of transverse metacentre                 | [m]       |
| 15  | Transverse metacentric height                            | [m]       |
| 16  | Correction to transverse metacentric height of stores    | [m]       |
| 17  | Correction to transverse metacentric height of ballast   | [m]       |
| 18  | Transverse metacentric height fixed                      | [m]       |
| 19  | Longitudinal metacentric radius                          | [m]       |
| 20  | Vertical centre of longitudinal metacentre               | [m]       |
| 21  | Longitudinal metacentric height                          | [m]       |
| 22  | Correction to longitudinal metacentric height of stores  | [m]       |
| 23  | Correction to longitudinal metacentric height of ballast | [m]       |
| 24  | Longitudinal metacentric height fixed                    | [m]       |
| 32  | Longitudinal center of gravity                           | [m]       |
| 33  | Wind pressure                                            | [Pa]      |
| 34  | Windage area                                             | $[m^2]$   |
| 35  | Windage area lever                                       | [m]       |
| 36  | Static windage heeling lever                             | [m]       |
| 37  | Dynamic windage heeling lever                            | [m]       |
| 38  | Static windage heeling angle                             | [degree]  |
| 39  | Dynamic windage heeling angle                            | [degree]  |
| 40  | Heeling angle of second point of intersection            | [degree]  |
| 41  | Roll amplitude                                           | [degree]  |
| 42  | Roll period                                              | [s]       |
| 43  | Area  a                                                  | $[m^2]$   |
| 44  | Area  b                                                  | $[m^2]$   |
| 45  | Open deck edge immersion angle                           | [degree]  |
| 46  | Angle of down-flooding                                   | [degree]  |
| 47  | Sunset angle                                             | [degree]  |
| 48  | Heeling moment due to the transverse shift of grain      | [t•m]     |
| 49  | Heeling angle with maximum difference                    | [degree]  |
| 50  | Vessel speed                                             | [knot]    |
| 53  | Transverse center of buoyancy                            | [m]       |
| 54  | Longitudinal center of flotation, from AP                | [m]       |
| 55  | Longitudinal center of buoyancy, from AP                 | [m]       |
| 56  | Longitudinal center of gravity, from AP                  | [m]       |
| 95  | Correction to transverse metacentric height              | [m]       |

## Damage stability
The assessment of damage stability is performed by comparing the corrected metacentric height $h$ for the current loading case with the minimum allowable metacentric height of division into compartments $h_{sub}$ for the current displacement (or draft). The damage stability for the current loading case is considered satisfactory if the condition $h\geq h_{sub}$ is met. The result of calculating the corrected metacentric height, the minimum allowable metacentric height of the division into compartments, as well as the status of the criterion is given in the stability criteria table.

======================pagebreak======================



======================pagebreak======================

# Part 09. Page "Manual"


![General view of the page "Manual"](/assets/image/program_sheets/en/sheet09_help/help_general.png "General view of the page 'Manual'")

The "Manual" page is intended to display the current user manual. the page consists of:
- navigation tree for the manual on the left side;
- the article navigation tree on the right side;
- the fields for displaying the manual article in the central part.

When you select any element (part, chapter, section) in the navigation tree of the manual (in the left part), an article with the content of the selected element is displayed in the central field. This article is navigated through the tree on the right side of the page.

======================pagebreak======================



======================pagebreak======================

# Part 10. Settings


![General view of the page "Settings"](/assets/image/program_sheets/en/sheet10_settings/settings_general_ru.png "General view of the page 'Settings'")

The page is designed to specify the language used in the program. To select a language, select the desired language from the drop-down list and restart the software.

![Language selection](/assets/image/program_sheets/en/sheet10_settings/settings_choose.png "Language selection")

Also you can exit from the application by pressing "Close the app" button;

======================pagebreak======================



======================pagebreak======================

# Part 11. Appendix (reference)



## Calculation parameters
| №   | Name                                                        | Dimension |
| --- | ----------------------------------------------------------- | --------- |
| 1   | Vertical centre of gravity fixed                            | [m]       |
| 2   | Displacement                                                | [t]       |
| 3   | Draft at center of flotation                                | [m]       |
| 4   | Draft at FP                                                 | [m]       |
| 5   | Draft at AP                                                 | [m]       |
| 6   | Trim                                                        | [degree]  |
| 7   | Heel                                                        | [degree]  |
| 8   | Tonnes per 1 cmи                                            | [t]       |
| 9   | Moment to heel 1 degree                                     | [t•m]     |
| 10  | Moment to trim 1 cm                                         | [t•m/cm]  |
| 11  | Vertical centre of buoyancy                                 | [m]       |
| 12  | Vertical centre of gravity                                  | [m]       |
| 13  | Transverse metacentric radius                               | [m]       |
| 14  | Vertical centre of transverse metacentre                     | [m]       |
| 15  | Transverse metacentric height                               | [m]       |
| 16  | Correction to transverse metacentric height of stores       | [m]       |
| 17  | Correction to transverse metacentric height of ballast      | [m]       |
| 18  | Transverse metacentric height fixed                         | [m]       |
| 19  | Longitudinal metacentric radius                             | [m]       |
| 20  | Vertical centre of longitudinal metacentre                   | [m]       |
| 21  | Longitudinal metacentric height                             | [m]       |
| 22  | Correction to longitudinal metacentric height of stores     | [m]       |
| 23  | Correction to longitudinal metacentric height of ballast    | [m]       |
| 24  | Longitudinal metacentric height fixed                       | [m]       |
| 25  | Weight of ballast                                           | [t]       |
| 26  | Weight of stores                                            | [t]       |
| 27  | Weight of cargo                                             | [t]       |
| 28  | Volume of deadweight                                        | [t]       |
| 29  | Weight of lightship                                         | [t]       |
| 30  | Weight of icing                                             | [t]       |
| 31  | Weight of wetting timber deck cargo                         | [t]       |
| 32  | Longitudinal center of gravity                              | [m]       |
| 33  | Wind pressure                                               | [Pa]      |
| 34  | Windage area                                                | $[m^2]$   |
| 35  | Windage area lever                                          | [m]       |
| 36  | Static windage heeling lever                                | [m]       |
| 37  | Dynamic windage heeling lever                               | [m]       |
| 38  | Static windage heeling angle                                | [degree]  |
| 39  | Dynamic windage heeling angle                               | [degree]  |
| 40  | Heeling angle of second point of intersection               | [degree]  |
| 41  | Roll amplitude                                              | [degree]  |
| 42  | Roll period                                                 | [s]       |
| 43  | Area  a                                                     | $[m^2]$   |
| 44  | Area  b                                                     | $[m^2]$   |
| 45  | Open deck edge immersion angle                              | [degree]  |
| 46  | Angle of down-flooding                                      | [degree]  |
| 47  | Sunset angle                                                | [degree]  |
| 48  | Heeling moment due to the transverse shift of grain         | [t•m]     |
| 49  | Heeling angle with maximum difference                       | [degree]  |
| 50  | Vessel speed                                                | [knot]    |
| 51  | Trim                                                        | [m]       |
| 52  | Transverse center of gravity                                | [m]       |
| 53  | Transverse center of buoyancy                               | [m]       |
| 54  | Longitudinal center of flotation, from AP                   | [m]       |
| 55  | Longitudinal center of buoyancy, from AP                    | [m]       |
| 56  | Longitudinal center of gravity, from AP                     | [m]       |
| 57  | Weight of bulkheads                                         | [t]       |
| 58  | Longitudinal center of gravity of lightship                 | [m]       |
| 59  | Longitudinal center of gravity of ballast                   | [m]       |
| 60  | Longitudinal center of gravity of stores                    | [m]       |
| 61  | Longitudinal center of gravity of cargo                     | [m]       |
| 62  | Longitudinal center of gravity of icing                     | [m]       |
| 63  | Longitudinal center of gravity of wetting timber deck cargo | [m]       |
| 64  | Transverse center of gravity of ballast                     | [m]       |
| 65  | Transverse center of gravity of stores                      | [m]       |
| 66  | Transverse center of gravity of cargo                       | [m]       |
| 67  | Transverse center of gravity of bulkheads                   | [m]       |
| 68  | Transverse center of gravity of icing                       | [m]       |
| 69  | Transverse center of gravity of wetting timber deck cargo   | [m]       |
| 70  | Vertical center of gravity of ballast                       | [m]       |
| 71  | Vertical center of gravity of stores                        | [m]       |
| 72  | Vertical center of gravity of cargo                         | [m]       |
| 73  | Vertical center of gravity of bulkheads                     | [m]       |
| 74  | Vertical center of gravity of icing                         | [m]       |
| 75  | Vertical center of gravity of wetting timber deck cargo     | [m]       |
| 76  | Longitudinal center of gravity of bulkheads                 | [m]       |
| 77  | Transverse center of gravity of lightship                   | [m]       |
| 78  | Vertical center of gravity of lightship                     | [m]       |
| 79  | Draft aft at marks SB                                       | [m]       |
| 80  | Draft aft at marks PS                                       | [m]       |
| 81  | Draft aft at marks mean                                     | [m]       |
| 82  | Draft intermediate aft at marks SB                          | [m]       |
| 83  | Draft intermediate aft at marks PS                          | [m]       |
| 84  | Draft intermediate aft at marks mean                        | [m]       |
| 85  | Draft middle at marks SB                                    | [m]       |
| 86  | Draft middle at marks PS                                    | [m]       |
| 87  | Draft middle at marks mean                                  | [m]       |
| 88  | Draft intermediate fwd at marks SB                          | [m]       |
| 89  | Draft intermediate fwd at marks PS                          | [m]       |
| 90  | Draft intermediate fwd at marks mean                        | [m]       |
| 91  | Draft fwd at marks SB                                       | [m]       |
| 92  | Draft fwd at marks PS                                       | [m]       |
| 93  | Draft fwd at marks mean                                     | [m]       |
| 94  | Draft at midship                                            | [m]       |
| 95  | Correction to transverse metacentric height                 | [m]       |
| 96  | Vertical center of gravity of deadweight                    | [m]       |
| 97  | Transverse center of gravity of deadweight                  | [m]       |
| 98  | Longitudinal center of gravity of deadweight                | [m]       |

## Calculation criterion

| №   | Name                                             | Dimension |
| --- | ------------------------------------------------ | --------- |
| 1   | Weather criterion                                | -         |
| 2   | Wind static heel                                 | [degree]  |
| 3   | Area of LC up to 30°                             | [m∙rad]   |
| 4   | Area of LC up to $θ_{l_{max}}$                   | [m∙rad]   |
| 5   | Area of LC up to 40°                             | [m∙rad]   |
| 6   | Area of LC between 30° & 40°                     | [m∙rad]   |
| 7   | Maximum LC                                       | [m]       |
| 8   | Maximum LC with timber                           | [m]       |
| 9   | Maximum LC with icing                            | [m]       |
| 10  | Heel with maximum LC                             | [degree]  |
| 11  | Heel with first maximum LC                       | [degree]  |
| 12  | Min. metacentric height                          | [m]       |
| 13  | Acceleration criterion                           | -         |
| 14  | Heel on turning                                  | [degree]  |
| 15  | Heel from grain displacement                     | [degree]  |
| 16  | Area of LC from grain displacement               | [m∙rad]   |
| 17  | Min. metacentric height due to subdivision index | [m]       |
| 101 | Summer LL draft SB                               | [m]       |
| 102 | Summer LL draft PS                               | [m]       |
| 103 | Winter LL draft SB                               | [m]       |
| 104 | Winter LL draft PS                               | [m]       |
| 105 | Winter North Atlantic LL draft SB                | [m]       |
| 106 | Winter North Atlantic LL draft PS                | [m]       |
| 107 | Tropical LL draft SB                             | [m]       |
| 108 | Tropical LL draft PS                             | [m]       |
| 109 | Fresh water LL draft in summer SB                | [m]       |
| 110 | Fresh water LL draft in summer PS                | [m]       |
| 111 | Tropical fresh water LL draft SB                 | [m]       |
| 112 | Tropical fresh water LL draft PS                 | [m]       |
| 113 | Summer timber LL draft SB                        | [m]       |
| 114 | Summer timber LL draft PS                        | [m]       |
| 115 | Winter timber LL draft SB                        | [m]       |
| 116 | Winter timber LL draft LW PS                     | [m]       |
| 117 | Winter North Atlantic timber LL draft SB         | [m]       |
| 118 | Winter North Atlantic timber LL draft PS         | [m]       |
| 119 | Tropical timber LL draft SB                      | [m]       |
| 120 | Tropical timber LL draft PS                      | [m]       |
| 121 | Fresh water timber LL draft in summer SB         | [m]       |
| 122 | Fresh water timber LL draft in summer PS         | [m]       |
| 123 | Tropical fresh water timber LL draft SB          | [m]       |
| 124 | Tropical fresh water timber LL draft PS          | [m]       |
| 125 | LL draft SI1 (reserve)                           | [m]       |
| 140 | LL draft SI16 (reserve)                          | [m]       |
| 141 | Maximum forward trim                             | [m]       |
| 142 | Maximum aft trim                                 | [m]       |
| 143 | Depth at forward perpendicular SB                | [m]       |
| 144 | Depth at forward perpendicular PS                | [m]       |
| 145 | Screw immersion CL                               | [%]       |
| 146 | Screw immersion SB                               | [%]       |
| 147 | Screw immersion PS                               | [%]       |
| 148 | Screw immersion (reserve)                        | [%]       |
| 149 | Screw immersion (reserve)                        | [%]       |
| 150 | Reserve buoyancy in bow                          | $[m^2]$   |

======================pagebreak======================



======================pagebreak======================


