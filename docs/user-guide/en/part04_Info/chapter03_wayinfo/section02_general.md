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