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
| Take into account in the criteria |                             |

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

#### Осадка в порту
#### The draft in the port
For each port, the maximum draft of the vessel at which entry into the port is possible can be assigned. When the "Take into account in criteria" is activated, such a draft will be checked when calculating the excess. The result of the check is displayed on the page ["Draft"](/docs/user-guide/en/part06_draft/part06_draft.md).