# EPU-Interwar-Austria
Following the approach by Baker et al. 2016, the EPU index will be based on German-speaking newspapers only and reflect uncertainty. Using the Anno database, the primary newspaper sources for the construction of the index are Neues Wiener Joural, Reichspost, Wiener Zeitung, Neue Freie Presse, Neues Wiener Tagblatt (Tages-Ausgabe), Illustrierte Kronen-Zeitung from January 1900 until December 1940. Although other newspapers could certainly also classify as necessary to consider, the above mentioned newspaper were considered the most important ones \textcolor{red}{SOURCE}. To classify as relevant for EPU, at least one term of three categories must appear in the article. The categories for the terms are displayed in Table \ref{table:1}. 
\begin{table}[h]
\centering
\caption{Index keywords} \label{tab:keywords}
\begin{tabularx}{\linewidth}{ | X | X |}
 \hline \hline
 Term - Economic & Wirtschaft, wirtschaftlich, Unternehmen, Industrie, Zentralbank, Geldpolitik, Kronen, Schilling, Banksatz, Inflation, Budget, Defizit, Haushaltsdefizit, Politik, Regulierung, Krieg, Gesetz, Steuer, Reparationen, Reparationszahlungen\\
 \hline
 Term - Uncertainty & Unsicherheiten, Unsicherheit, unischer\\
 \hline 
\end{tabularx}
\label{table:1}
\end{table}


To control for differing article volume and coverage over time and newspaper, Baker et al. 2016 propose the following approach. Firstly, for each newspaper, the raw EPU counts are scaled by the total number of articles appearing per month to obtain a relative EPU frequency count. With this first step, any variations in the volume of articles for each of the newspapers are accounted for. Secondly, the relative EPU frequency count is standardised per newspaper to the unit standard deviation from 1900 to 1940. As some newspapers have a higher coverage of policy-related issues than others, this step limits the variability and ensures an equal weight of the newspapers in the index.  As a third and last step, the resulting series is subsequently normalised to the mean of 100 across all six newspapers by month, resulting in the overall monthly Austrian EPU index. Formally, the computation can be described as follows:\\

$i=$ newspaper; $t=$ time; $n=$ number of newspapers; $\sigma=$ unit standard deviation
$$
\begin{gathered}
X_{i t}=\frac{\text { epu count }_{i t}}{\text { total }_{i t}} ; \\
Y_{i t}=\frac{X_{i t}}{\sigma_{i}} ; \\
Z_{t}=\frac{\sum_{i}^{n} Y_{i t}}{n} ; \\
M=\text { Average } Z_{t} \text { over } T ; \\
\text { EPU}_{t}=\frac{Z_{t}}{M}
\end{gathered}
$$

