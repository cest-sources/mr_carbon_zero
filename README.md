# MR carbon zero
A resource for MRI institutes / radiologic institutes towards realization of carbon neutral MRI.

## Current general energy demand of MRI
The energy demand of “a **single MRI** machine in clinical use […] corresponds to **25.8 four-person households**” [[1]](#literature-references). The “daily energy consumption for a clinical MRIs  scanner in operation for 13 hours was estimated to be 363 kWh with 1.5 T units and 530 kWh with 3.0 T units”[[1]](#literature-references). 

Thus, yearly (~300 days) this sums up to **108 MWh for 1.5 T units  and 159 MWh for 3 T units**.

With almost **3000 MRI systems** in use alone in **Germany**, corresponding to the demand of approximately **75k households**, this forms a substantial contribution to the national electric energy demand and to the national carbon footprint. In addition, in case of external energy shortage MRI diagnostics cannot be performed or only using emergency generators that again **rely on external fuel resources**.

Average per examination 20 kWh ± 5 (range, 12–34 kWh).

### Helium demand and zero boil-off
MR scanners have a rather high helium demand for the cooling system as upon usage, heating of the system leads to boil-off of helium.
On old systems this helium is either gathered for external reliquefying purposes or released to the environment.
Newer generation of MRI scanners have a so-called **zero boil-off technology where the generated helium gas is locally collected and reliquefied**. The additional helium demand is therefore marginal, which is a significant cost reduction, but the energy demand of zero boil-off systems is larger.

In both cases the helium reliquification process has to be included in the energy demand calculation.

The above mentioned energy demand is most probobably from system with zero boil-off techonolgy (Skyra, Verio, Avanto Fit, Espree), but this could not be verified, as avanto system without zero boil-off exist. It is assumed that this is included for the estimations herein.

### Dynamic energy demand 
The dynamic energy demand[[1]](#literature-references)  is given by the following figures:

 - ![Dynamic Energy demand](../main/img/dynNRG-MRI_fig2.jpeg)

This shows that 
1. MRI has an high constant energy demand at both on and off times, due to the cooling
2. MRI has peaks of power demand up to 60 kWh for certain sequences (ssfp)
3. MRI has non-negligible idle energy demand during on-active times.

which is also nicely summarized here:
![Dynamic Energy demand](../main/img/dynNRG_MRI_fig7.jpeg)

## Options to save energy
### simple
- (use lower field, but at cost of performance)
- switching off the scanner as long as possible
- reduce on-active idle times 
- optimize MR sequences

### advanced 
- no cooling at night : **store helium gas and use solar power** during the daytime for condensation.
- use the generated **waste heat** as heat supply or reservoir for heat pumps. Under the assumption that 20 % of the energy (108 MWh/159 MWh at 1.5/3 T) can be re-used as heat source, this is  21 / 32 MWh unused energy annualy or **6 houshold per MRI system**.

### more advanced 
- design and usage of more effecient amplifiers
- more effcient cooling / isolation ( e.g. cryogen-free systems, but seem to have similar demand)

## Solar system and storage dimensioning
Active times are in average 13h, ca. 6am to 7 pm mostly at daytime, where local photovoltaics (PV) can contribute to the energy demand. [[2]](#literature-references) 
As depicted below on average we have 50 % PV capacity between 7 am and 4 pm  and we are above the 50 % capacity between March and October.
![Solar months](../main/img/PV_weekly_hourly_germany.jpg)
Thus, a strongly reduced external energy demand can be achieved using local photovoltaics supply. 
**In 8 of 12 months even an autarkic mode might be possible**.

With above mentioned savings we might reduce te energy demand of an advanced MRI from 159 MWh down to 80 MWh.
In Germany a **PV production of 175 to 235 kWh/sqm is possible**[[3]](#literature-references).  Using **200 kWh/sqm** as for our calculation leads to 400 sqm of needed photovoltaics to covere the average demand with the average production.
To cover the months in spring and autumn a overdimensioning of a factor two might be necessary, leading to **800 sqm**.
To use the higher PV energy of noon time for evening and morning, a **battery storage** can be used.
 - A storage of **0.5 MWh** could cover approximatley 2 days of demand and seems well suited for this. 
 - Modern Li batteries also easily cover the mentioned **peak power** demand, thus the battery also serves as a peak power buffer.
 - Moreover, the **helium liquification can be done at noon time** as well to use abundant energy, and switch off cooling at night.

## Cost of an 8/12 autarkic MRI 
base costs: PV: 210 Euro per sqm [[4]](#literature-references) , battery: ~500€ per kWh [[5]](#literature-references) 

- 800 sqm PV --------  168,000 €
- 0.5 MWh battery --- 250,000 €
- setup ----------------- 32,000 €
- ----------------------------------
- Total:-----------------450,000 €

Currently energy prices are at 42 cent per kWh. Thus, outgoing from the non-optimized demand (159 MWh), this **autarkic MRI + PV + battery system** would amortize itself within **7.7 years**. And would contribute to the heating of the building.

And too many roofs are still empty:

![Rofs](../main/img/roofs.jpg)

In the winter months one needs to buy wind energy to realize a carbon zero MRI.

## Summary - MR carbon zero
In summary we have to
1. build 800sqm PV
2. reduce active-on idle times (optimize work flow) and match active-on with solar cycle
3. don't cool at night, but recool during daytime
4. add buffer battery for mornings, evenings, and as peak-power buffer
5. get wind energy in winter
6. use generated waste heat for buildings heating ~ 10 Mwh/year
7. **Optimize MRI sequences**

![Rofs](../main/img/summary.jpg)

## Literature references

[1]	Heye T, Knoerl R, Wehrle T, Mangold D, Cerminara A, Loser M, Plumeyer M, Degen M, Lüthy R, Brodbeck D, Merkle E. The Energy Consumption of Radiology: Energy- and Cost-saving                    Opportunities for CT and MRI Operation. Radiology. 2020;295(3):593-605. https://doi.org/10.1148/radiol.2020192084 

[2] Pfenninger S, Staffell I. Long-term patterns of European PV output using 30 years of validated hourly reanalysis and satellite data. Energy. 2016;114:1251-1265. doi:10.1016/j.energy.2016.08.060 and the Supporting Info: 
https://ars.els-cdn.com/content/image/1-s2.0-S0360544216311744-mmc1.pdf

[3] https://www.ise.fraunhofer.de/content/dam/ise/de/documents/publications/studies/aktuelle-fakten-zur-photovoltaik-in-deutschland.pdf

[4] https://kostencheck.de/solaranlage-kosten-pro-m%C2%B2

[5] https://energetechsolar.com/1mwh-500v-800v-battery-energy-storage-system

