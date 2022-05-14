# tree_prune_model

This R code is a simple model for initiating a starting population of urban trees and modelling the changes in tree biomass taking into account pruning rates, pruning frequencies and mortality rates.  The variables for the model have come from real data for 8 tree species in the cities of Taranto and Florence, Italy.

The model is part of the data analysis for the research paper: Speak, A.F., Salbitano, F. (2022) "The impact of pruning and mortality on the provision of urban tree ecosystem services"

Prunerate = the number of years between pruning events
Pruneadjust = a factor that adjusts the pruning severity i.e. 0.8 reduces the pruning variables by 20%
Mortrate = percentage of trees that die each year

The variables for crown width (CWID) and height (H) come from the measured trees in the cities of Taranto and Florence
The gapfactor variables are derived from averaging gapfactors measured using a hemispherical camera lens and the Winscanopy software
GF1 is from Winter1 and thus represents the gapfraction directly after pruning
GF2 is from Winters 2 to 4 and represents the normal gapfraction for the species
CWIDfact is used to reduce the crown width by a species specific value at each pruning event
CWIDnew and Hnew are the crown widths and heights of new replacement trees and are set at 1m and 2m respectively for all species
GR is the tree growth rate. Values are derived from Russo et al. (2014) for Pinus, Quercus, and Tilia genera.  THe other genera values come from discussions with the gardening departments of the two cities and online tree information. THey represent a moderate growth rate of 0.3m for Ficus, Ligustrum and Nerium and a moderate to high growth rate of 0.4m for Platanus.
CGR is the crown growth rate and is set at 0.4m

The crown volume is calculated using the formula
Crown Volume = H*(CWID/2)^2*π*(1-GF)


Russo, A., Escobedo, F.J., Timilsina, N., Schmitt, A.O., Varela, S., Zerbe, S., 2014. Assessing urban tree carbon storage and sequestration in Bolzano, Italy. Int. J. Biodivers. Sci. Ecosyst. Serv. Manag. 10 (1), 54e70.
