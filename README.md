# gettsim_wochenbericht
Dieses Repository soll eine Übersicht über die Module und Tools in GETTSIM schaffen, um zu evaluieren inwiefern eine Analyse zur Verteilungswirkung der Mütterrente mit GETTSIM anstelle von STSM möglich wäre. Zum Vergleich werden Wochenberichte aus [2014](/literature/DIW_Wochenbericht%2014-20-1.pdf) und[2018](/literature/DIW_Wochenbericht18-28-1.pdf) herangezogen.


## Datenaufbereitung fürs SOEP
Für die Aufbereitung der SOEP Daten, um sie in GETTSIM zu verwenden, gibt es vom IZA ein eigenes [Soep-Data](https://github.com/iza-institute-of-labor-economics/soep-data) Repository. In dem Repo wird pytask genutzt, um die Daten zu reinigen und so umzubenennen das sie problemlos in GETTSIM genutzt werden können. Ggf. müssten einige Tools noch an die aktuelle SOEP-Welle angepasst werden. 