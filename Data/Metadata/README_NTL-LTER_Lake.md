# NTL-LTER Lake Datasets

## Summary

These datasets were downloaded and prepared for use in the Environmental Data
Exploration course at Duke University, Fall 2026.

The datasets contain observations from several lakes in the North Temperate Lakes
District in Wisconsin, USA. Data were collected as part of the Long-Term Ecological
Research program established by the National Science Foundation.

## Database Information

Data were collected by the North Temperate Lakes Long-Term Ecological Research program
(NTL-LTER). More information about the program is available at
<https://lter.limnology.wisc.edu/about/overview>.

NTL-LTER data are archived in the Environmental Data Initiative (EDI) Data Portal. The
datasets were located through the [NTL-LTER Data
page](https://lter.limnology.wisc.edu/data/) and downloaded from their individual EDI
data-package pages.

EDI requires users to sign in before accessing package files. Users may sign in with an
EDI, Google, Microsoft, GitHub, or ORCID account.

The following Cascade Project datasets were downloaded:

* [Cascade Project at North Temperate Lakes LTER Core Data Carbon 1984–2023](https://portal.edirepository.org/nis/mapbrowse?packageid=knb-lter-ntl.350.8)
* [Cascade Project at North Temperate Lakes LTER Core Data Nutrients 1991–2019](https://portal.edirepository.org/nis/mapbrowse?packageid=knb-lter-ntl.351.5)
* [Cascade Project at North Temperate Lakes LTER Core Data Physical and Chemical Limnology 1984–2016](https://portal.edirepository.org/nis/mapbrowse?packageid=knb-lter-ntl.71.5)

For each package, the CSV data file was downloaded from the EDI repository. The files
were saved locally as `NTL-LTER_Lake_Carbon_Raw.csv`,
`NTL-LTER_Lake_ChemistryPhysics_Raw.csv`, and `NTL-LTER_Lake_Nutrients_Raw.csv` for
instructional use in the Environmental Data Exploration course.

The filenames identify these as raw source data; no values were altered when the files
were renamed.

Data were accessed September 14, 2026. Because EDI packages may be revised
independently, users downloading these data later should consult the package page for
the latest revision, date range, metadata, usage license, and recommended citation.

## Dataset Columns

The tables below provide a practical guide to the columns used in the course files.
Missing measurements are recorded as `NA`. Consult the metadata supplied with each EDI
package for the authoritative definitions, units, analytical methods, and
quality-control notes.

Several identification columns occur in more than one dataset:

| Column       | Description                                                       |
|--------------|-------------------------------------------------------------------|
| `lakeid`     | Short code used to identify the lake.                             |
| `lakename`   | Full name of the lake.                                            |
| `year4`      | Four-digit year in which the sample was collected.                |
| `daynum`     | Day of the year, ranging from 1 to 365 or 366.                    |
| `sampledate` | Calendar date on which the sample was collected.                  |
| `depth`      | Sampling depth below the water surface, in meters.                |
| `depth_id`   | Identifier for the sampling depth or position in a depth profile. |
| `comments`   | Notes about sampling conditions, methods, or individual records.  |

### Carbon dataset columns

File: `NTL-LTER_Lake_Carbon_Raw.csv`

| Column       | Description                                                        |
|--------------|--------------------------------------------------------------------|
| `lakeid`     | Short code used to identify the lake.                              |
| `lakename`   | Full name of the lake.                                             |
| `year4`      | Four-digit sampling year.                                          |
| `daynum`     | Day of the year.                                                   |
| `sampledate` | Sampling date.                                                     |
| `depth`      | Sampling depth below the water surface, in meters.                 |
| `depth_id`   | Identifier for the sampling depth.                                 |
| `tpc`        | Total particulate carbon concentration.                            |
| `tpn`        | Total particulate nitrogen concentration.                          |
| `DIC_mg`     | Dissolved inorganic carbon concentration expressed in mg C/L.      |
| `DIC_uM`     | Dissolved inorganic carbon concentration expressed in µmol/L.      |
| `air_pco2`   | Partial pressure of carbon dioxide measured in air above the lake. |
| `water_pco2` | Partial pressure of carbon dioxide measured in surface water.      |
| `doc`        | Dissolved organic carbon concentration.                            |
| `absorbance` | Light absorbance measured at 440 nm.                               |

### Nutrient dataset columns

File: `NTL-LTER_Lake_Nutrients_Raw.csv`

| Column or group                 | Description                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------|
| `lakeid`, `lakename`            | Lake identifiers.                                                                                          |
| `year4`, `daynum`, `sampledate` | Sampling year, day of year, and date.                                                                      |
| `depth`, `depth_id`             | Sampling depth and depth identifier.                                                                       |
| `tn_ug`                         | Total nitrogen concentration.                                                                              |
| `tp_ug`                         | Total phosphorus concentration.                                                                            |
| `no23`                          | Nitrate concentration; the measurement may include nitrate plus nitrite, as specified in the EDI metadata. |
| `nh34`                          | Ammonium concentration.                                                                                    |
| `po4`                           | Orthophosphate concentration.                                                                              |
| `comments`                      | Notes associated with the sample or measurement.                                                           |

Nutrient variable names include abbreviated chemical names. Units are not consistent
across every nutrient, so they should be checked in the EDI metadata before values are
compared or converted.

### Physical and chemical limnology dataset columns

File: `NTL-LTER_Lake_ChemistryPhysics_Raw.csv`

| Column or group                 | Description                                                        |
|---------------------------------|--------------------------------------------------------------------|
| `lakeid`, `lakename`            | Lake identifiers.                                                  |
| `year4`, `daynum`, `sampledate` | Sampling year, day of year, and date.                              |
| `depth`, `depth_id`             | Sampling depth and depth identifier.                               |
| `wtemp`.                        | Water temperature in degrees Celsius.                              |
| `dissolved_oxygen`              | Dissolved oxygen concentration and oxygen-saturation measurements. |
| `irradiance`                    | Light measured underwater at the sampling depth.                   |
| `deck_irradiance`               | Reference light measured on the deck of the sampling boat.         |

The two irradiance columns are paired measurements. `irradianceWater` describes the
light available within the water column, whereas `irradianceDeck` records the incoming
reference light above the water.

## Data Content Information

From the NTL-LTER site:

### Carbon

Data on dissolved organic and inorganic carbon, particulate organic matter, partial
pressure of CO2 and absorbance at 440nm. Samples were collected with a Van Dorn sampler.
Organic carbon and absorbance samples were collected from the epilimnion, metalimnion,
and hypolimnion. Inorganic samples were collected at depths corresponding to 100%, 50%,
25%, 10%, 5%, and 1% of surface irradiance, as well as one sample from the hypolimnion.
Samples for the partial pressure of CO2 were collected from two meters above the lake
surface (air) and just below the lake surface (water). Sampling frequency: varies;
number of sites: 14

Detailed field and laboratory protocols can be found in the Cascade Methods Manual,
found here:
<https://cascade.limnology.wisc.edu/public/public_files/methods/CascadeMa>... POC, PON
and DOC: 1. 100 - 300 ml (Typically ~200mL for PML, 150 metalimnion and 75 – 100 for the
hypolimnion) of lake water from each depth was filtered through 153 um mesh to remove
large zooplankton. Water was then filtered through a precombusted 25mm GF/F filter (0.7
um pore size) at less than 200 mm Hg pressure. Filters were placed in drying oven at 60
C to dry for at least 48 hours. 20mL of filtered water was stored in a scintillation
vial and acidified with 200uL of 2N H2SO4 for DOC analysis. Blank samples for POC and
DOC were prepared with deionized water to control for contamination. All samples were
sent to the Cary Institute of Ecosystem Studies for analysis.

Absorbance: 60ml of water was filtered through a 25mm GF/F filter and refrigerated until
it was able to be run. Samples were warmed up to room temperature and run on a
spectrophotometer in a 10cm glass cuvette. The spectrophotometer was set to 440nm and
blanked with deionized water. The cuvette was rinsed once with sample water and then
filled and absorbance was measured.

DIC: Water was sampled with a van dorn and taken back to the lab. 10 mL subsamples were
taken with syringes and 200 uL of 2N H2SO4 and 20 mL of helium gas were added to the
syringe. Syringes were shaken for one minute and 10 mL of the helium headspace was
injected into a Gas Chromatograph with Thermal Conductivity Detector to determine DIC
concentration.

PCO2: Air PCO2 was measured by filling a syringe with air from two meters above the lake
surface and running though the GC. Water PCO2 was measured by filling a two liter bottle
with lake surface water and replacing 60 mL of water with atmospheric air for headspace.
The bottle was shaken for 100 seconds and two subsamples of the headspace were taken and
run though a GC in the lab.

### Nutrients

Physical and chemical variables are measured at one central station near the deepest
point of each lake. In most cases these measurements are made in the morning (0800 to
0900). Vertical profiles are taken at varied depth intervals. Chemical measurements are
sometimes made in a pooled mixed layer sample (PML); sometimes in the epilimnion,
metalimnion, and hypolimnion; and sometimes in vertical profiles. In the latter case,
depths for sampling usually correspond to the surface plus depths of 50percent,
25percent, 10percent, 5percent and 1percent of surface irradiance. The 1991-1999
chemistry data was obtained from the Lachat auto-analyzer. Like the process data, there
are up to seven samples per sampling date due to Van Dorn collections across a depth
interval according to percent irradiance. Voichick and LeBouton (1994) describe the
autoanalyzer procedures in detail. Nutrient samples were sent to the Cary Institute of
Ecosystem Studies for analysis beginning in 2000. The Kjeldahl method for measuring
nitrogen is not used at IES, and so measurements reported from 2000 onwards are Total
Nitrogen.

Methods for 1984-1990 were described by Carpenter and Kitchell (1993) and methods for
1991-1997 were described by Carpenter et al. (2001).

Carpenter, S.R. and J.F. Kitchell (eds.). 1993. The Trophic Cascade in Lakes. Cambridge
University Press, Cambridge, England.

Carpenter, S.R., J.J. Cole, J.R. Hodgson, J.F. Kitchell, M.L. Pace,D. Bade, K.L.
Cottingham, T.E. Essington, J.N. Houser and D.E. Schindler. 2001. Trophic cascades,
nutrients and lake productivity: whole-lake experiments. Ecological Monographs 71:
163-186.

#### Units

| Variable          | Description                 | Typical Units                | Notes                                                                     |
|-------------------|-----------------------------|------------------------------|---------------------------------------------------------------------------|
| **TP**            | Total Phosphorus            | **µg P/L**                   | Includes dissolved + particulate P; measured after digestion.             |
| **SRP (PO₄³⁻-P)** | Soluble Reactive Phosphorus | **µg P/L**                   | Also called "orthophosphate."                                             |
| **TN**            | Total Nitrogen              | **mg N/L**                   | Sum of organic + inorganic N; may be converted from Kjeldahl + NO₃⁻/NO₂⁻. |
| **NO₃⁻-N**        | Nitrate Nitrogen            | **mg N/L**                   | Sometimes reported in µg/L; check dataset metadata.                       |
| **NH₄⁺-N**        | Ammonium Nitrogen           | **mg N/L**                   | Filtered sample, colorimetric or autoanalyzer method.                     |
| **SiO₂**          | Dissolved Silica            | **mg Si/L** or **µmol Si/L** | Used in productivity and diatom studies.                                  |
| **DOC**           | Dissolved Organic Carbon    | **mg C/L**                   | Often accompanies nutrient datasets.                                      |

### Physical and chemical limnology

Physical and chemical variables are measured at one central station near the deepest
point of each lake. In most cases these measurements are made in the morning (0800 to
0900). Vertical profiles are taken at varied depth intervals. Chemical measurements are
sometimes made in a pooled mixed layer sample (PML); sometimes in the epilimnion,
metalimnion, and hypolimnion; and sometimes in vertical profiles. In the latter case,
depths for sampling usually correspond to the surface plus depths of 50percent,
25percent, 10percent, 5percent and 1percent of surface irradiance.

Methods for 1984-1990 were described by Carpenter and Kitchell (1993) and methods for
1991-1997 were described by Carpenter et al. (2001).

Carpenter, S.R. and J.F. Kitchell (eds.). 1993. The Trophic Cascade in Lakes. Cambridge
University Press, Cambridge, England.

Carpenter, S.R., J.J. Cole, J.R. Hodgson, J.F. Kitchell, M.L. Pace,D. Bade, K.L.
Cottingham, T.E. Essington, J.N. Houser and D.E. Schindler. 2001. Trophic cascades,
nutrients and lake productivity: whole-lake experiments. Ecological Monographs 71:
163-186.

## Naming conventions and file formats

Files are named according to the following naming convention:
`databasename_datatype_details_stage.format`, where:

**databasename** refers to the database from where the data originated

**datatype** is a description of data

**details** are additional descriptive details, particularly important for processed
data

**stage** refers to the stage in data management pipelines (e.g., raw, cleaned, or
processed)

**format** is a non-proprietary file format (e.g., .csv, .txt)

## Additional Information and Support

For more information, please contact **Luana Lima** (lmm89@duke.edu)
