# gettsim_wochenbericht

## Motivation
Dieses Repository soll eine Übersicht über die Module und Tools in [GETTSIM](https://github.com/iza-institute-of-labor-economics/gettsim) schaffen, um zu evaluieren inwiefern eine Analyse zur Verteilungswirkung der Mütterrente mit GETTSIM anstelle von STSM möglich wäre. Zum Vergleich werden Wochenberichte aus [2014](/literature/DIW_Wochenbericht%2014-20-1.pdf) und[2018](/literature/DIW_Wochenbericht18-28-1.pdf) herangezogen.


## Vergleich 

>Dazu enthält das STSM komplexe Simulationsmodule zu Einkommensteuer
>und Solidaritätszuschlag, zu den Sozialversicherungsbeiträgen
>sowie zu den wesentlichen Sozialtransfers (Arbeitslosengeld I,
>Wohngeld, Elterngeld, Kindergeld, Kinderzuschlag, Grundsicherung).


| STSM | GETTSIM |
| ---- | ---- |
| Einkommenssteuer | [Einkommenssteuer](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/taxes/eink_st.py) |
| Sozialbeiträge | [Sozialbeiträge](https://github.com/iza-institute-of-labor-economics/gettsim/tree/main/src/_gettsim/social_insurance_contributions)<br>Krankenversicherung, Rentenversicherung, Pflegeversicherung, Arbeitslosenversicherung |
| Solidaritätszuschlag | [Solidaritätszuschlag](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/taxes/soli_st.py) |
| Arbeitslosengeld I | [Arbeitslosengeld I](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/arbeitsl_geld.py) |
| Grundsicherungsleistungen | [Bürgergeld](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/arbeitsl_geld_2/arbeitsl_geld_2.py) |
| Wohngeld | [Wohngeld](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/wohngeld.py) |
| Elterngeld | [Elterngeld](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/elterngeld.py) |
| Kindergeld | [Kindergeld](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/kindergeld.py) |
| Kinderzuschlag | [Kinderzuschlag](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/kinderzuschl/kinderzuschl.py) |
| Witwenrente | Die Witwenrente ist noch gar nicht implementiert und es scheint auch unrealistisch, dass das noch rechtzeitig passiert.<br>Es gibt allerdings schon einen ersten Aufschlag zur Implementierung. Vielleicht könnte man also eine geforkte GETTSIM Variante mit einer provisorischen Witwenrente für die Analyse verwenden. |
| Rentenarten | [Altersrente](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/rente.py)<br>[Altersrente für (besonders) langjährige Versicherte](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/rente.py)<br>[Grundsicherung im Alter](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/grunds_im_alter.py)<br>[Grundrente](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/grundrente.py)<br>[Erwerbsminderungsrente](https://github.com/iza-institute-of-labor-economics/gettsim/blob/main/src/_gettsim/transfers/erwerbsm_rente.py) |



## Datenaufbereitung SOEP -> GETTSIM
Für die Aufbereitung der SOEP Daten, um sie in GETTSIM zu verwenden, gibt es vom IZA ein eigenes [Soep-Data](https://github.com/iza-institute-of-labor-economics/soep-data) Repository. In dem Repo wird pytask genutzt, um die Daten zu reinigen und so umzubenennen das sie problemlos in GETTSIM genutzt werden können. Ggf. müssten einige Tools noch an die aktuelle SOEP-Welle angepasst werden. 