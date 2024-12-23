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