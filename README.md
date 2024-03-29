## NHSE Methods: Gradient boosting estimation


### About this method

Gradient boosting estimation is a machine learning methodology which uses a decision tree approach to take into account relationships between variables and outcome to generate coefficients/weights.
For more information about the method, including how is being used, when and by who, please refer to the Methods toolbox documentation on our [FutureNHS workspace](https://future.nhs.uk/DataMeth/grouphome).


### Requirements

Installation of R and Alteryx package: "gbm"


### Summary of the code

This code is developing the weights for each variables using R software. The code reads and prepares the data and then constructs the command string. Then it defines the type of target / distribution of the loss function and determines the preferred number of trees in the model, as well as further model specifications. 
When the model is run, it creates a list with the model objects and it writes out the results. Finally, summary weights are created for each variable which will be used in the Euclidean distance estimation.


### Data sources

|Variable Description | Source |
|--|--|
|The average Index of Multiple Deprivation (2010) score in the LSOAs where Trusts' patients live (Deprivation)|NHS Digital, HES|
|Number distinct patients with recorded activity on the previous year	(Patients)|NHS Digital, HES|
|Total number of finished episodes or attendances	(Attendances)|NHS Digital, HES|
|Total number of Full time equivalent Staff at the end of the financial year	(FTE staff)|NHS Digital, Workforce Statistics|
|The proportion of finished admissions where patient's diagnosis is Diseases of the digestive system (K00-K93) or Symptoms, signs and abnormal clinical and laboratory findings, not elsewhere classified (R00-R99)	(diagnosis)|NHS Digital, HES publication|
|Average percentage of daily number occupied beds overnight (Jan-March)	(Night beds)|NHS England, Unify2 data collection - KH03|
|Average percentage of daily number occupied beds day only (Jan-March) (Day beds)|NHS England, Unify2 data collection - KH03|
|The proportion of finished episodes or attendances or appointments where patient's age is ≤15	(Age 0 -15)|NHS Digital, HES|
|The proportion of finished episodes or attendances or appointments where patient's age is between 60-74	(Age 60 -74)|NHS Digital, HES|
|The proportion of finished episodes where patient didn't have a procedure or intervention	(No procedure)|NHS Digital, HES publication|
|Trust's Operating Expendes at the end of the year	(Operating expenses)|Monitor, Transparency data|
|The proportion of finished episodes or attendances or appointments where the Rural/Urban indicator is recorded as Urban	(Urban)|NHS Digital, HES databases|
|Number of open sites per Trust	(Sites)|Organisation Data Service, ODS|
|Distance from the Trust to the sea in miles	(Sea distance)|ODS to obtain Trust's postcode and doogal.co.uk to calculate distance|
|Market Forces Factor payment values	(MFF payment index)|NHS England Publications|
|Proportion of undergraduate medical students placed in any hospital Trust	(StudentStaff)|DH|
|Number of CCGs contracting with Trust	(CCGs)|NHS Digital, HES|
|Presence of non-emergency department	(Non-type 1 AE department)|NHS Digital, HES|
|Yearly average Staff sickness absence rate	(Absence Rate)|NHS Digital, Workforce Statistics|
|Number of Delayed Days during the last quarter of the financial year	(DTOCs)|NHS England, Unify2 Data Collection - MSitDT|
|Degree of specialisation (Degree of specialisation)|Calculated using HES databases|


### Authors

Felix Asamoah, Senior Analytical Manager - felix.asamoah1@nhs.net 

