# EPU-Interwar-Austria

Following the approach by Baker et al. 2016, the EPU index will be based on German-speaking newspapers only and reflect uncertainty. Using the Anno database, the primary newspaper sources for the construction of the index are Neues Wiener Joural, Wiener Zeitung, Neue Freie
Presse, Neues Wiener Tagblatt (Tages-Ausgabe), and Arbeiter Zeitung for the national level. To
also capture regional sentiment, the following newspapers are used: Vorarlberger Volksblatt, Grazer
Volksblatt, K¨arntner Zeitung, Linzer Volksblatt, Allgemeiner Tiroler Anzeiger, and Salzburger
Chronik. All newspapers are analysed from January 1913 until December 1937. The reason
for the cut-off year is that the newspapers Neues Wiener Journal and Neue Freie Presse were
disestablished either due to mergers or due to Nazi politics.  Although other newspapers could certainly also classify as necessary to consider, the above-mentioned newspapers were considered the most important ones. To classify as relevant for EPU, at least one term of three categories must appear in the article. The categories for the terms are displayed in the table below.

| **Term - Economic**                                                                                     | **Term - Uncertainty**                   |
|---------------------------------------------------------------------------------------------------------|------------------------------------------|
| Wirtschaft, wirtschaftlich, Unternehmen, Industrie, Notenbank, Geldpoli-
tik, Kronen, Schilling, Banksatz, Inflation, Budget, Defizit, Haushaltsde-
fizit, Politik, Regulierung, Krieg, Gesetz, Steuer, Reparationen, Repa-
rationszahlungen, Krise, Schulden, Devisen, Zahlungsbilanz, Gelden-
twertung, Preissteigerung, Preise, Devisenhandel, Kredite, Kaufkraft,
Wertverlust, Valuta, Valuten, Geldwert, Gold, Teuerung, Aufschlag,
Wertpapiere, Währung | unischer |

To control for differing article volume and coverage over time and newspaper, Baker et al. 2016 propose the following approach. Firstly, for each newspaper, the raw EPU counts are scaled by the total number of articles appearing per month to obtain a relative EPU frequency count. With this first step, any variations in the volume of articles for each of the newspapers are accounted for. Secondly, the relative EPU frequency count is standardized per newspaper to the unit standard deviation from 1913 to 1937. As some newspapers have a higher coverage of policy-related issues than others, this step limits the variability and ensures an equal weight of the newspapers in the index. As a third and last step, the resulting series is subsequently normalized to the mean of 100 across all six newspapers by month, resulting in the overall monthly Austrian EPU index. Formally, the computation can be described as follows:

- \( i \) = newspaper
- \( t \) = time
- \( n \) = number of newspapers
- \( \sigma \) = unit standard deviation

```plaintext
X_{it} = (epu count_{it}) / (total_{it})
Y_{it} = X_{it} / σ_{i}
Z_{t} = (∑ Y_{it} from i=1 to n) / n
M = Average Z_{t} over T
EPU_{t} = Z_{t} / M
---

