# Pump It Up: Data Mining the Water Table

Introduction

This project is based on the competition Driven Data had published about water pumps, in Tanzania, a large country that suffers from access to good quality water. The main project idea is to identify which pumps are functional, which need some repairs, and which don't work at all. The metric used for this competition is “Accuracy” for calculating the precision of the model.

The result of the project was uploaded to score the predictions, which generated a response in the 66th percentile of 5282 entries. I scored 0.7411 while the best was 0.8294.

Distribution of Labels
The labels in this dataset are simple. There are three possible values:

functional - the waterpoint is operational and there are no repairs needed
functional needs repair - the waterpoint is operational, but needs repairs
non functional - the waterpoint is not operational


Dataset description

The data for the training has 59,400 rows and 40 columns without the label that comes in a separate file, in the case of testing data it has 14,850 rows. The name of the target is status_group that has three possible values:
1)	functional 
2)	non-functional
3)	functional but it needs to repair

Exploratory Data Analysis (EDA)
Data Set Variables:
population - Population around the well
public_meeting - True/False
recorded_by - Group entering this row of data
scheme_management - Who operates the waterpoint
scheme_name - Who operates the waterpoint
permit - If the waterpoint is permitted
construction_year - Year the waterpoint was constructed
extraction_type - The kind of extraction the waterpoint uses
extraction_type_group - The kind of extraction the waterpoint uses
extraction_type_class - The kind of extraction the waterpoint uses
management - How the waterpoint is managed
management_group - How the waterpoint is managed
payment - What the water costs
payment_type - What the water costs
water_quality - The quality of the water
quality_group - The quality of the water
quantity - The quantity of water
quantity_group - The quantity of water
source - The source of the water
source_type - The source of the water
source_class - The source of the water
waterpoint_type - The kind of waterpoint
waterpoint_type_group - The kind of waterpoint

Our expansive variable set distills into four distinct potential determinants for the state of water pumps:
1)	Oversight
2)	Location
3)	Population of village
4)	Water quality


I also wanted to create a variable for the age of the water well. To do this I turned both the construction_year and date_recorded into date type variables. The difference between the two was given the name duration.

I also used the two variables water_quality and management to capture the remaining variation due to upkeep and water quality.

Show table of model results
I used a random forest classification model.

Proof of Submission

<img width="468" alt="image" src="https://github.com/jconns/Pump-It-Up-Data-Mining-the-Water-Table/assets/48659723/a242c33b-4e69-4f80-86c7-b56ce78d2353">

