## bulk cargo
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