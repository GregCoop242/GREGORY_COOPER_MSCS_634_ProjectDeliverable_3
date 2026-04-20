## GREGORY_COOPER_MSCS_634_ProjectDeliverable_3


#Classification

Both the Decision Tree and k-NN models learn to predict flight delays using only pre flight scheduling features no post flight leakage. The tuned Decision Tree generally achieves slightly better F1 and AUC than the baseline, with GridSearchCV identifying the depth and pruning settings that generalize best.

Real-world use case: An airline operations system could run this model on the day's scheduled departures to flag highr isk flights for pre-emptive gate changes or crew reallocations.

#Clustering

K-Means separates flights into four operationally meaningful groups based on departure time, route distance, and taxi time. Clusters with late-evening departures and longer taxi times consistently show higher delay rates matching real-world experience with cascading delays across a day's operations.

Real-world use case: Airlines could target delay reduction initiatives (faster ground operations, buffer time adjustments) specifically at the high risk cluster rather than applying blanket policies.

#Association Rules

Apriori surfaces patterns like {Summer, Evening, Long-Haul} → Delayed and {Morning, Short-Haul, Weekday} → On-Time with confidence well above baseline delay rates. These rules quantify common knowledge in a data-driven, actionable way.

Real-world use case: Travelers can use such patterns to choose lower risk flight windows. Airlines can use them in dynamic pricing flagging historically delay-prone combinations for operational scrutiny.
