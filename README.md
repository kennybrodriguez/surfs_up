# Surfs Up

### Overview
This project focued on analyzing weather data with the intention of finding out more about the weather during the months of June and December. Investment into a surf shop was the reason for the analysis with the focus being on the viability of a shop as a yearround business. The data was provided in a SQLITE file and sqlchemy was used to connect to the database. From there the data was queried for the information on the months of June and December. Summary statistics were retrieved on this data for comparison. 


### Results
- The average temperature for June was 74.94. The average temperature in December was 71.04. This is about a 3 degree difference in the average between summer and winter, which would imply that the temperature is pretty constant throughout the year. 

![Results](/Resources/1.PNG)

- The coldest temperature in June is 64 and in December it is 56 degrees. This implies that the temperature drop in winter is minimal. 

![Results](/Resources/2.PNG)

- The hottest temperature in June is 85 and in December it is 83 degrees. This shows that temperatures can rise even in the winter months. 

### Summary
The intention of the analysis was to provide insight on the viability of a surf shop in Oahu that is open year round. The main focus was on the temperature in Oahu. We compared a summer month with a winter month (June and December) to get a sense of how different the weather is in different parts of the year. 

Overall, the temperature summary statistics ended up being quite similar. The mean for June was 74.94 and December was 71.04. This slight variance in the mean implies that it is slightly colder in December but it is minimal. This is good news for a surf shop that wants to do business year round. The plan mentioned selling ice cream at this shop and average temperatures in the 70's would mean you can sell ice cream year round. 

Lastly, the measurement table also has a column for precipitation. This could prove invaluable in seeing if an investment in a surf/ice cream shop is worth it. Two queries were provided below to help show the precipitation summary statistics for the months of June and December. This could help provide more insight on the impact rain can have on the business. 


jun_prec = session.query(Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

dec_prec = session.query(Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()