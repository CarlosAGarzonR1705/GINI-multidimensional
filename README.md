# GINI-multidimensional

*************************************************************************
* Multidimensional Inequality Index DL
* Carlos Alberto Garzón
* Universidad de la Sabana
* 15th of july 2015
* PURPOSE: MULTIDIMENSIONAL INEQUALITY GINI INDEX CALCULATION
*************************************************************************

** clear information in the memory

cap log close
clear all
set more off

** change working folder

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/2. ECV"

*************************************************************************
** Merging year by year data bases
** 1. Sorting by Directorio, survey sequency and person sequency
** 2. Merge de data set by year
*************************************************************************

** 2024 data base 

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2024"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2024.dta"

** 2023 data base 

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2023"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2023.dta"

** 2022 data base 

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2022"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2022.dta"

** 2021 data base 

clear all

sort directorio secuencia_encuesta secuencia_p
cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2021"

use "Educacion.dta"
sort directorio secuencia_encuesta secuencia_p
save "Educacion.dta", replace
use "Salud.dta"
sort directorio secuencia_encuesta secuencia_p
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort directorio secuencia_encuesta secuencia_p
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort directorio secuencia_encuesta secuencia_p
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 directorio secuencia_encuesta secuencia_p using "Salud.dta",
drop _merge
merge 1:1 directorio secuencia_encuesta secuencia_p using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 directorio secuencia_encuesta secuencia_p using "Infancia.dta"
drop _merge

save  "merged_2021.dta"


** 2020 data base 

clear all
cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2020"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2020.dta"


** 2019 data base 
clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2019"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2019.dta"



** 2018 data base 

clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2018"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2018.dta"


** 2017 data base 

clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2017"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2017.dta"


** 2016 data base 

clear all

sort directorio secuencia_encuesta secuencia_p
cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2016"

use "Educacion.dta"
sort directorio secuencia_encuesta secuencia_p
save "Educacion.dta", replace
use "Salud.dta"
sort directorio secuencia_encuesta secuencia_p
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort directorio secuencia_encuesta secuencia_p
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort directorio secuencia_encuesta secuencia_p
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 directorio secuencia_encuesta secuencia_p using "Salud.dta",
drop _merge
merge 1:1 directorio secuencia_encuesta secuencia_p using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 directorio secuencia_encuesta secuencia_p using "Infancia.dta"
drop _merge

save  "merged_2016.dta"

** 2015 data base 
clear all

sort directorio secuencia_encuesta secuencia_p
cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2015"

use "Educacion.dta"
sort directorio secuencia_encuesta secuencia_p
save "Educacion.dta", replace
use "Salud.dta"
sort directorio secuencia_encuesta secuencia_p
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort directorio secuencia_encuesta secuencia_p
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort directorio secuencia_encuesta secuencia_p
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 directorio secuencia_encuesta secuencia_p using "Salud.dta",
drop _merge
merge 1:1 directorio secuencia_encuesta secuencia_p using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 directorio secuencia_encuesta secuencia_p using "Infancia.dta"
drop _merge

save  "merged_2015.dta"


** 2014 data base

clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2014"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2014.dta"

** 2013 data base

clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2013"

use "Educacion.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2013.dta"

** 2012 data base

clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2012"

use "Educacion.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2012.dta"

** 2011 data base

clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2011"

use "Educacion.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2011.dta"

** 2010 data base

clear all

cd "/Users/carlosgarzonriveros/Library/CloudStorage/OneDrive-DepartamentoAdministrativoparalaProsperidadSocialDPS/Unimilitar/6. Bases de datos/1. ECV/2010"

use "Educacion.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Educacion.dta", replace
use "Salud.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Salud.dta", replace
use "Fuerza de trabajo.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Fuerza de trabajo.dta", replace
use "Infancia.dta"
sort directorio SECUENCIA_ENCUESTA SECUENCIA_P
save "Infancia.dta", replace

use "Educacion.dta"
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Salud.dta",
drop _merge
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Fuerza de trabajo.dta"
drop _merge
merge 1:1 directorio SECUENCIA_ENCUESTA SECUENCIA_P using "Infancia.dta"
drop _merge

save  "merged_2010.dta"

*************************************************************************
*                         Calculate MIGI
*************************************************************************

**************************************************************************
**** DIMENSION 1: EDUCATION (years of schooling **************************
**************************************************************************

* INDICATOR: YEARS OF SCHOOLING
	* NOTE: People studying currently P6213S1 (2010 - 2011) P1088S1 (2012 - 2024) 
	* NOTE: People out of the scholar system P6219S1 (2010 - 2011) P8587S1 (2012 - 2024)

clear all

cd "/Users/carlosgarzonriveros/Documents/1. University/5. Working papers/Multidimensional Gini/2025 paper/Calculations"
	
** 2010 data base
	
use "merged_2010.dta"

gen study = P6213S1
replace study = 0 if P6213S1 == .
gen approbe = P6219S1
replace approbe = 0 if P6219S1 == .
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save ""merged_2010.dta", replace

** 2011 data base
	
use "merged_2011.dta"

gen study = P6213S1
replace study = 0 if P6213S1 == .
gen approbe = P6219S1
replace approbe = 0 if P6219S1 == .
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2011.dta", replace

** 2012 data base
	
use "merged_2012.dta"

gen study = P1088S1 
replace study = 0 if P1088S1 == .
gen approbe = P8587S1
replace approbe = 0 if P8587S1 == .
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2012.dta", replace

** 2013 data base
	
use "merged_2013.dta"

gen study = P1088S1 
replace study = 0 if P1088S1 == .
gen approbe = P8587S1
replace approbe = 0 if P8587S1 == .
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2013.dta", replace

** 2014 data base
	
use "merged_2014.dta"

gen study = P1088S1 
gen approbe = P8587S1
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2014.dta", replace

** 2015 data base
clear all
	
use "merged_2015.dta"

gen study = p8586 
gen approbe = p8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2015.dta", replace

** 2016 data base
clear all
	
use "merged_2016.dta"

gen study = p8586 
gen approbe = p8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2016.dta", replace

** 2017 data base
clear all
	
use "merged_2017.dta"

gen study = P8586 
gen approbe = P8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2017.dta", replace

** 2018 data base
clear all
	
use "merged_2018.dta"

gen study = P8586 
gen approbe = P8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2018.dta", replace

** 2019 data base
clear all
	
use "merged_2019.dta"

gen study = P8586 
gen approbe = P8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2019.dta", replace

** 2020 data base
clear all
	
use "merged_2020.dta"

gen study = P8586 
gen approbe = P8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2020.dta", replace

** 2021 data base
clear all
	
use "merged_2021.dta"

gen study = p8586 
gen approbe = p8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2021.dta", replace

** 2022 data base
clear all
	
use "merged_2022.dta"

gen study = P8586 
gen approbe = P8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2022.dta", replace

** 2023 data base
clear all
	
use "merged_2023.dta"

gen study = P8586 
gen approbe = P8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2023.dta", replace

** 2024 data base
clear all
	
use "merged_2024.dta"

gen study = P8586 
gen approbe = P8587
gen eduattain = study + approbe
label variable eduattain "Años Promedio de Educacion"
drop study approbe
tab eduattain

save "merged_2024.dta", replace


**************************************************************************
**** DIMENSION 2: HEALTH (Access to health care) *************************
**************************************************************************

* INDICATOR: YACCESS TO HEALTH CARE
	* NOTE: Affiliation Health System P6091 (2010 - 2012) P6090 (2013 - 2024) 
	* NOTE: Afected by disease P5665 (2010 - 2012) P5665 (2013 - 2024)
	* NOTE: Institutional attention P6143 (2010 - 2012) P8563 (2013 - 2024)

clear all

cd "/Users/carlosgarzonriveros/Documents/1. University/5. Working papers/Multidimensional Gini/2025 paper/Calculations"
	
** 2010 data base
	
use "merged_2010.dta"

gen affiliated = 0
replace affiliated = 1 if P6091 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P6143 == 1
replace treat = 1 if P6143 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2010.dta", replace
 
** 2011 data base
	
use "merged_2011.dta"

gen affiliated = 0
replace affiliated = 1 if P6091 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P6143 == 1
replace treat = 1 if P6143 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2011.dta", replace
 
** 2012 data base
	
use "merged_2012.dta"

gen affiliated = 0
replace affiliated = 1 if P6091 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P6143 == 1
replace treat = 1 if P6143 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2012.dta", replace
 
** 2013 data base
	
use "merged_2013.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2013.dta", replace

** 2014 data base
	
use "merged_2014.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2014.dta", replace
 
** 2015 data base
	
use "merged_2015.dta"

gen affiliated = 0
replace affiliated = 1 if p6090 == 1 
gen disease = 0
replace disease = 1 if p5665 == 1
gen treat = 0
replace treat = 1 if p8563 == 1
replace treat = 1 if p8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2015.dta", replace

** 2016 data base
	
use "merged_2016.dta"

gen affiliated = 0
replace affiliated = 1 if p6090 == 1 
gen disease = 0
replace disease = 1 if p5665 == 1
gen treat = 0
replace treat = 1 if p8563 == 1
replace treat = 1 if p8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2016.dta", replace

** 2017 data base
	
use "merged_2017.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2017.dta", replace

** 2018 data base
	
use "merged_2018.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2018.dta", replace

** 2019 data base
	
use "merged_2019.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2019.dta", replace

** 2020 data base
	
use "merged_2020.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2020.dta", replace

** 2021 data base
	
use "merged_2021.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2021.dta", replace

** 2022 data base
	
use "merged_2022.dta"

gen affiliated = 0
replace affiliated = 1 if p6090 == 1 
gen disease = 0
replace disease = 1 if p5665 == 1
gen treat = 0
replace treat = 1 if p8563 == 1
replace treat = 1 if p8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2022.dta", replace

** 2014 data base
	
use "merged_2022.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2022.dta", replace

** 2023 data base
	
use "merged_2023.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2023.dta", replace

** 2024 data base
	
use "merged_2024.dta"

gen affiliated = 0
replace affiliated = 1 if P6090 == 1 
gen disease = 0
replace disease = 1 if P5665 == 1
gen treat = 0
replace treat = 1 if P8563 == 1
replace treat = 1 if P8563 == 2
gen dise_treat = disease + treat 
recode dise_treat (0=0) (1=0) (2=1)
gen hc_access = affiliated + dise_treat
label variable hc_access "Acceso a salud dada necesidad"
drop affiliated disease treat dise_treat

save "merged_2024.dta", replace
 

**************************************************************************
**** DIMENSION 3: LABOR MARKET (Formal labor)    *************************
**************************************************************************

* INDICATOR: FORMAL LABOR (ACCESS TO A PENSION FUND)
	* NOTE: Affiliation Health System P6091 (2010 - 2012) P6090 (2013 - 2014) 
	* NOTE: Contribution to a pension fund P6920

	clear all

cd "/Users/carlosgarzonriveros/Documents/1. University/5. Working papers/Multidimensional Gini/2025 paper/Calculations"

** 2010 data base
	
use "merged_2010.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6091 == 2
replace occupation = 1  if P6240 == 1 & P6091 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6091 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6091 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6091 == 2 & P6920 == 1 | P6091 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2010.dta", replace
 
** 2011 data base
	
use "merged_2011.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6091 == 2
replace occupation = 1  if P6240 == 1 & P6091 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6091 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6091 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6091 == 2 & P6920 == 1 | P6091 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2011.dta", replace
 
** 2012 data base
	
use "merged_2012.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6091 == 2
replace occupation = 1  if P6240 == 1 & P6091 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6091 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6091 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6091 == 2 & P6920 == 1 | P6091 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2012.dta", replace
 
** 2013 data base
	
use "merged_2013.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2013.dta", replace
 
** 2014 data base
	
use "merged_2014.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2014.dta", replace

** 2015 data base
	
use "merged_2015.dta"

gen occupation = 0
replace occupation = .  if p6240 == .
replace occupation = 1  if p6240 == 4 & p6090 == 2
replace occupation = 1  if p6240 == 1 & p6090 == 2 & p6920 == 2
replace occupation = 2  if p6240 == 4 & p6090 == 1
replace occupation = 3  if p6240 == 3
replace occupation = 4  if p6240 == 2 
replace occupation = 5  if p6240 == 1 & p6090 == 1 & p6920 == 2
replace occupation = 6  if p6240 == 1 & p6090 == 2 & p6920 == 1 | p6090 == 1 & p6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2015.dta", replace

** 2016 data base
	
use "merged_2016.dta"

gen occupation = 0
replace occupation = .  if p6240 == .
replace occupation = 1  if p6240 == 4 & p6090 == 2
replace occupation = 1  if p6240 == 1 & p6090 == 2 & p6920 == 2
replace occupation = 2  if p6240 == 4 & p6090 == 1
replace occupation = 3  if p6240 == 3
replace occupation = 4  if p6240 == 2 
replace occupation = 5  if p6240 == 1 & p6090 == 1 & p6920 == 2
replace occupation = 6  if p6240 == 1 & p6090 == 2 & p6920 == 1 | p6090 == 1 & p6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2016.dta", replace

** 2017 data base
	
use "merged_2017.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2017.dta", replace

** 2018 data base
	
use "merged_2018.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2018.dta", replace

** 2019 data base
	
use "merged_2019.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2019.dta", replace

** 2020 data base
	
use "merged_2020.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2020.dta", replace

** 2021 data base
	
use "merged_2021.dta"

gen occupation = 0
replace occupation = .  if p6240 == .
replace occupation = 1  if p6240 == 4 & p6090 == 2
replace occupation = 1  if p6240 == 1 & p6090 == 2 & p6920 == 2
replace occupation = 2  if p6240 == 4 & p6090 == 1
replace occupation = 3  if p6240 == 3
replace occupation = 4  if p6240 == 2 
replace occupation = 5  if p6240 == 1 & p6090 == 1 & p6920 == 2
replace occupation = 6  if p6240 == 1 & p6090 == 2 & p6920 == 1 | p6090 == 1 & p6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2021.dta", replace

** 2022 data base
	
use "merged_2022.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2022.dta", replace

** 2023 data base
	
use "merged_2023.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2023.dta", replace

** 2024 data base
	
use "merged_2024.dta"

gen occupation = 0
replace occupation = .  if P6240 == .
replace occupation = 1  if P6240 == 4 & P6090 == 2
replace occupation = 1  if P6240 == 1 & P6090 == 2 & P6920 == 2
replace occupation = 2  if P6240 == 4 & P6090 == 1
replace occupation = 3  if P6240 == 3
replace occupation = 4  if P6240 == 2 
replace occupation = 5  if P6240 == 1 & P6090 == 1 & P6920 == 2
replace occupation = 6  if P6240 == 1 & P6090 == 2 & P6920 == 1 | P6090 == 1 & P6920 == 1
label variable occupation "Ocupacion formal (pago seguridad social)"

save "merged_2024.dta", replace


 

**************************************************************************
**** DIMENSION 4: CHILD CARE (Access to a child care services)    *************************
**************************************************************************

* INDICATOR: ACCESS TO CHILD CARE SERVICES

	* NOTE: Children (0-4) spend last month P6176 (2010 - 2012) P51 (2013 - 2024) 

clear all

cd "/Users/carlosgarzonriveros/Documents/1. University/5. Working papers/Multidimensional Gini/2025 paper/Calculations"

	
** 2010 data base
	
use "merged_2010.dta"

gen child_care =0
replace child_care = .  if P6176 == .
replace child_care = 5  if P6176 == 1
replace child_care = 4  if P6176 == 2
replace child_care = 3  if P6176 == 3
replace child_care = 2  if P6176 == 4
replace child_care = 1  if P6176 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2010.dta", replace

** 2011 data base
	
use "merged_2011.dta"

gen child_care =0
replace child_care = .  if P6176 == .
replace child_care = 5  if P6176 == 1
replace child_care = 4  if P6176 == 2
replace child_care = 3  if P6176 == 3
replace child_care = 2  if P6176 == 4
replace child_care = 1  if P6176 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2011.dta", replace
 
** 2012 data base
	
use "merged_2012.dta"

gen child_care =0
replace child_care = .  if P6176 == .
replace child_care = 5  if P6176 == 1
replace child_care = 4  if P6176 == 2
replace child_care = 3  if P6176 == 3
replace child_care = 2  if P6176 == 4
replace child_care = 1  if P6176 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2012.dta", replace
 
** 2013 data base
	
use "merged_2013.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2013.dta", replace
 
** 2014 data base
	
use "merged_2014.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2014.dta", replace
 
** 2015 data base
	
use "merged_2015.dta"

gen child_care =0
replace child_care = .  if p51 == .
replace child_care = 5  if p51 == 1
replace child_care = 4  if p51 == 2
replace child_care = 3  if p51 == 3
replace child_care = 2  if p51 == 4
replace child_care = 1  if p51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2015.dta", replace

** 2016 data base
	
use "merged_2016.dta"

gen child_care =0
replace child_care = .  if p51 == .
replace child_care = 5  if p51 == 1
replace child_care = 4  if p51 == 2
replace child_care = 3  if p51 == 3
replace child_care = 2  if p51 == 4
replace child_care = 1  if p51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2016.dta", replace

** 2017 data base
	
use "merged_2017.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2017.dta", replace

** 2018 data base
	
use "merged_2018.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2018.dta", replace

** 2019 data base
	
use "merged_2019.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2019.dta", replace

** 2020 data base
	
use "merged_2020.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2020.dta", replace

** 2021 data base
	
use "merged_2021.dta"

gen child_care =0
replace child_care = .  if p51 == .
replace child_care = 5  if p51 == 1
replace child_care = 4  if p51 == 2
replace child_care = 3  if p51 == 3
replace child_care = 2  if p51 == 4
replace child_care = 1  if p51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2021.dta", replace

** 2022 data base
	
use "merged_2022.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2022.dta", replace

** 2023 data base
	
use "merged_2023.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2023.dta", replace

** 2024 data base
	
use "merged_2024.dta"

gen child_care =0
replace child_care = .  if P51 == .
replace child_care = 5  if P51 == 1
replace child_care = 4  if P51 == 2
replace child_care = 3  if P51 == 3
replace child_care = 2  if P51 == 4
replace child_care = 1  if P51 == 5

label variable child_care "Acceso a servicios de cuidado infantil"

save "merged_2024.dta", replace


********* KEEP JUST VARIABLES FOR MEASUREMENT 
********* COLLAPSING BY HOUSEHOLD (MAX)
********* CALCULATE SIMPLE INEQUALITY INDICATORS

clear all

cd "/Users/carlosgarzonriveros/Documents/1. University/5. Working papers/Multidimensional Gini/2025 paper/Calculations"

** 2010 data base

use "merged_2010.dta"
keep directorio SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2010.dta"

** 2011 data base

use "merged_2011.dta"
keep directorio SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2011.dta"

** 2012 data base

use "merged_2012.dta"
keep directorio SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2012.dta"

** 2013 data base

use "merged_2013.dta"
keep directorio SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2013.dta"

** 2014 data base

use "merged_2014.dta"
keep directorio SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2014.dta"

** 2015 data base

use "merged_2015.dta"
keep directorio secuencia_encuesta secuencia_p region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2015.dta"

** 2016 data base

use "merged_2016.dta"
keep directorio secuencia_encuesta secuencia_p region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2016.dta"

** 2017 data base

use "merged_2017.dta"
keep DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2017.dta"

** 2018 data base

use "merged_2018.dta"
keep DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2018.dta"

** 2019 data base

use "merged_2019.dta"
keep DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2019.dta"

** 2020 data base

use "merged_2020.dta"
keep DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2020.dta"

** 2021 data base

use "merged_2021.dta"
keep directorio SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2021.dta"

** 2022 data base

use "merged_2022.dta"
keep DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2022.dta"

** 2023 data base

use "merged_2023.dta"
keep DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2023.dta"

** 2024 data base

use "merged_2024.dta"
keep DIRECTORIO SECUENCIA_ENCUESTA SECUENCIA_P region P3 FEX_C P6040 eduattain hc_access occupation child_care
collapse (max) eduattain hc_access occupation child_care, by(directorio)
ineqdeco eduattain 
ineqdeco hc_access
ineqdeco occupation
ineqdeco child_care

save "MDGI_2024.dta"


**** MIGI CALCULATION
**** 1. MATRIX STANDARIZATION (0-1) UNSING (DATA-MIN)/(MAX-MIN)

clear all

cd "/Users/carlosgarzonriveros/Documents/1. University/5. Working papers/Multidimensional Gini/2025 paper/Calculations"

** 2010 data base

use "MDGI_2010.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2010.dta", replace

** 2011 data base

use "MDGI_2011.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2011.dta", replace

** 2012 data base

use "MDGI_2012.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2012.dta", replace

** 2013 data base

use "MDGI_2013.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2013.dta", replace

** 2014 data base

use "MDGI_2014.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2014.dta", replace

** 2014 data base

use "MDGI_2014.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2014.dta", replace

** 2015 data base

use "MDGI_2015.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2015.dta", replace

** 2016 data base

use "MDGI_2016.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2016.dta", replace

** 2017 data base

use "MDGI_2017.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2017.dta", replace

** 2018 data base

use "MDGI_2018.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2018.dta", replace

** 2019 data base

use "MDGI_2019.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2019.dta", replace

** 2021 data base

use "MDGI_2021.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2021.dta", replace

** 2022 data base

use "MDGI_2022.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2022.dta", replace

** 2023 data base

use "MDGI_2023.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2023.dta", replace

** 2024 data base

use "MDGI_2024.dta"

foreach v of var eduattain hc_access occupation child_care { 
	su `v', meanonly 
	gen new_`v' = (`v' - r(min))/(r(max) - r(min)) 
	label var new_`v' "`var' estandarizada"
		}

save "MDGI_2024.dta", replace


******************************************************************************
**************** MULTIDIMENSIONAL GINI INDEX CALCULATION *********************
******************************************************************************

clear all

cd "/Users/carlosgarzonriveros/Documents/1. University/5. Working papers/Multidimensional Gini/2025 paper/Calculations"

**********************************
*** 2010 data base
*** If beta equal cero
**********************************

use "MDGI_2010.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2010.dta", replace

**********************************
*** 2011 data base
*** If beta equal cero
**********************************

use "MDGI_2011.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2011.dta", replace

**********************************
*** 2012 data base
*** If beta equal cero
**********************************

use "MDGI_2012.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2012.dta", replace

**********************************
*** 2013 data base
*** If beta equal cero
**********************************

use "MDGI_2013.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2013.dta", replace

**********************************
*** 2014 data base
*** If beta equal cero
**********************************

use "MDGI_2014.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2014.dta", replace

**********************************
*** 2015 data base
*** If beta equal cero
**********************************

use "MDGI_2015.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2015.dta", replace


**********************************
*** 2016 data base
*** If beta equal cero
**********************************

use "MDGI_2016.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2016.dta", replace


**********************************
*** 2017 data base
*** If beta equal cero
**********************************

use "MDGI_2017.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2017.dta", replace


**********************************
*** 2018 data base
*** If beta equal cero
**********************************
clear all

use "MDGI_2018.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2018.dta", replace


**********************************
*** 2019 data base
*** If beta equal cero
**********************************

clear all

use "MDGI_2019.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2019.dta", replace


**********************************
*** 2020 data base
*** If beta equal cero
**********************************

use "MDGI_2020.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2020.dta", replace


**********************************
*** 2021 data base
*** If beta equal cero
**********************************

clear all

use "MDGI_2021.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
*gen ind_WmB1   = d_WmB0 / max_indB0
*gen ind_WmB1_1 = (d_WmB0-1) / max_indB0
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2021.dta", replace


**********************************
*** 2022 data base
*** If beta equal cero
**********************************

clear all

use "MDGI_2022.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
*gen ind_WmB1   = d_WmB0 / max_indB0
*gen ind_WmB1_1 = (d_WmB0-1) / max_indB0
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2022.dta", replace


**********************************
*** 2023 data base
*** If beta equal cero
**********************************

clear all

use "MDGI_2023.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
*gen ind_WmB1   = d_WmB0 / max_indB0
*gen ind_WmB1_1 = (d_WmB0-1) / max_indB0
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)

save "MDGI2_2023.dta", replace


**********************************
*** 2024 data base
*** If beta equal cero
**********************************

clear all
use "MDGI_2024.dta"

*** Is important replace dots for zeros when posible

foreach v of var new_eduattain new_hc_access new_occupation new_child_care { 
	replace `v' = 0.1 if (`v' >= .)
	replace `v' = 0.1 if (`v' == 0)

		}

*** First Stage: aggregation function across dimension (Wm)

gen WmB0  = new_eduattain^(1/4) * new_hc_access^(1/4) * new_occupation^(1/4) * new_child_care^(1/4)
sort WmB0
gen d_WmB0 = _n 
egen max_indB0 = max(d_WmB0)
gen ind_WmB0 = max_indB0 - d_WmB0

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB0d2 = (((ind_WmB0 / max_indB0)^2)-(((ind_WmB0 - 1)/max_indB0)^2)) * WmB0
gen WnB0d3 = (((ind_WmB0 / max_indB0)^3)-(((ind_WmB0 - 1)/max_indB0)^3)) * WmB0
gen WnB0d4 = (((ind_WmB0 / max_indB0)^4)-(((ind_WmB0 - 1)/max_indB0)^4)) * WmB0
gen WnB0d5 = (((ind_WmB0 / max_indB0)^5)-(((ind_WmB0 - 1)/max_indB0)^5)) * WmB0

tabstat  WnB0d2 WnB0d3 WnB0d4 WnB0d5, stat(sum)


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
*gen ind_WmB1   = d_WmB0 / max_indB0
*gen ind_WmB1_1 = (d_WmB0-1) / max_indB0
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB2 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)


save "MDGI2_2024.dta", replace


*** Third Stage: Calculate Mu(xj)

use "MDGI_2010.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2011.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2012.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2013.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2014.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2015.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2016.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2017.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2018.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2019.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2020.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2021.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2022.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2023.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care
use "MDGI_2024.dta"
summarize new_eduattain new_hc_access new_occupation new_child_care


**********************************
*** If beta equal minus one
**********************************


*** First Stage: aggregation function across dimension (Wm)

gen WmB1 = ((1/4) * new_eduattain^(-1) + (1/4) * new_hc_access^(-1) + (1/4) * new_occupation^(-1) + (1/4) * new_child_care^(-1))^(1/(-1))
sort WmB1
*gen ind_WmB1   = d_WmB0 / max_indB0
*gen ind_WmB1_1 = (d_WmB0-1) / max_indB0
gen d_WmB1 = _n 
egen max_indB1 = max(d_WmB1)
gen ind_WmB1 = max_indB1 - d_WmB1

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB1d2 = (((ind_WmB1 / max_indB1)^2)-(((ind_WmB1 - 1)/max_indB1)^2)) * WmB1
gen WnB1d3 = (((ind_WmB1 / max_indB1)^3)-(((ind_WmB1 - 1)/max_indB1)^3)) * WmB1
gen WnB1d4 = (((ind_WmB1 / max_indB1)^4)-(((ind_WmB1 - 1)/max_indB1)^4)) * WmB1
gen WnB1d5 = (((ind_WmB1 / max_indB1)^5)-(((ind_WmB1 - 1)/max_indB1)^5)) * WmB1

tabstat  WnB1d2 WnB1d3 WnB1d4 WnB1d5, stat(sum)

**********************************
*** If beta equal minus two
**********************************
*** First Stage: aggregation function across dimension (Wm)

gen WmB2 = = ((1/4) * new_eduattain^(-2) + (1/4) * new_hc_access^(-2) + (1/4) * new_occupation^(-2) + (1/4) * new_child_care^(-2))^(1/(-2))
sort WmB2
gen d_WmB1 = _n 
egen max_indB2 = max(d_WmB2)
gen ind_WmB2 = max_indB2 - d_WmB2

*** Second Stage: aggregation function across persons (Wn)

*** Delta = 2, 3, 4, y 5

gen WnB2d2 = (((ind_WmB2 / max_indB2)^2)-(((ind_WmB2 - 1)/max_indB2)^2)) * WmB2
gen WnB2d3 = (((ind_WmB2 / max_indB2)^3)-(((ind_WmB2 - 1)/max_indB2)^3)) * WmB2
gen WnB2d4 = (((ind_WmB2 / max_indB2)^4)-(((ind_WmB2 - 1)/max_indB2)^4)) * WmB2
gen WnB2d5 = (((ind_WmB2 / max_indB2)^5)-(((ind_WmB2 - 1)/max_indB2)^5)) * WmB2

tabstat  WnB2d2 WnB2d3 WnB2d4 WnB2d5, stat(sum)
