## Bootstrap probabilistic reasoning (Experimental)

For the bootstrapping approach, the averaged network sometimes does not hold directed acyclic assumptions, and the probabilistic reasoning cannot be performed. The bootReason function is implemented that performs probabilistic reasoning for each bootstrap replicate and return the mean of events, as well as difference in mean from the control level.

```R
source("utilitiesBoot.R")
bootReasonOne(
	df, # Dataframe
	20, # bootstrap number
	node=c("CENPH","NUP107"), # event nodes
	c("TP53"), # evidence node
	level=c(0, 0.25, 0.5, 0.75, 1), # evidence level
	cont=0 # control level
	)
```