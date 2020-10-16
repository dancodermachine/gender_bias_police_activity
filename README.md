# Analyzing Gender Bias on Police Activity

On a normal day in the United States, law enforcement produces more than 50,000 traffic stops. To
understand the interactions between police officers and the public during these traffic stops, a team
named The Stanford Open Policing Project is collecting the data [1] [2] and making it available for free.

This dataset contains information from the state of Rhode Island State. The objective of this project is
to discover if gender bias exists on search conductions, the type of search and the outcomes of each
search. The work that will be done is using descriptive statistic (describing the sample data). This
project does not try to infer from the data.

The analysis was done using the following python packages: Pandas, NumPy, Seaborn, Matplotlib, Os,
Sys, Requests

## Definitions:

violation:

1. Speeding: Drive above speed limit.
2. Equipment: Violations that are not classified when a car is parked or in movement (e.g. no
    current safety check sticker). [3]
3. Moving violation: It occurs when a traffic law is violated by a vehicle in motion (e.g. running a
    stop line) [4]
4. Registration/plates: Issues with car registration/plate. [5]
5. Seat belt: Not using seat belts.

search_conducted:

1. Inventory Search: It is a warrantless search of a lawfully impounded vehicle conducted by
    police. Exception the 4th Amendment (police are barred from conducting unreasonable
    searches and seizures). [6]
2. Probable Cause: Concrete evidence of the crime (e.g. car speeding)
3. Reasonable Suspicion: A police officer should be allowed to stop and briefly detain a car if,
    based on police’s training and experience, there is a reason to believe that the individual is
    engaging in criminal activity (e.g. an open beer can next to the driver). [7]
4. Protective Frisk: Official can pass hands over (someone) in a search of hidden weapons, drugs,
    or other items.
5. Incident to arrest: Official can warrantless search the car of an arrested person. [8]


## Do genders commit different violations?

65.81% of women traffic stops are for speeding, 13.82% for moving violation, 10.52% for equipment
violation, 4.44% for problems on the registration of car or plates, 2.43% for not using seat belt. In
contrast, 52.22% of men traffic stops are for speeding, 20.61% for moving violation, 13.42% for
equipment violation, 4.22% for problems on the registration of car or plates and 3.63% for not using
seat belt. This does not mean that females speed more often than males or that men have more
moving violations than women, however, since we did not consider the number of stops or drivers.


## Does gender affect whose vehicle is searched?

The percentage of people to be searched given that are male and have been stopped by a
registration/plates violation is 10.88%. On the other hand, the percentage of people to be searched
given that are female and have been stopped by a registration/plates is 5.49%. The percentage of
people to be searched given that are male and have been stopped by an equipment violation is 7.15%.
On the other hand, the percentage of people to be searched given that are female and have been
stopped by an equipment violation is 4.1%. The percentage of people to be searched given that are
male and have been stopped by a seat belt violation is 3.51%. On the other hand, the percentage of a
people to be searched given that are female and have been stopped by a seat belt violation is 1.73%.
This shows that males are being searched almost as twice as often as females during a
registration/plates, equipment and seat belt violation.

The percentage of people to be searched given that are male and have been stopped by a moving
violation is 6.15%. On the other hand, the percentage of people to be searched given that are female
and have been stopped by a moving violation is 4%. The percentage of people to be searched given
that are male and have been stopped by speeding violation is 2.79%. On the other hand, the
percentage of a people to be searched given that are female and have been stopped by speeding
violation is 0.83%. Men are searched 2% more than women in both of these categories.

Overall, men are being searched more than women for all violations.


## Is there gender bias on each type of search?

10.1% of men are searched due to a reasonable suspicion, almost as twice as women (5.92%). 9 .4 4 %
of men are searched due to protective frisk, around 2% more than women (7.46%). 36.79% of men
are searched due to a probable cause, around 4% more than women (32.68%). 12.66% of men’s
searches end up in inventory, around 5% less than women (17.54%). 48.47% of men’s cars are
searched due to an arrest, around 6% less than women (54.61%).

For ‘reasonable suspicion’, ‘protective frisk’ and ‘probable cause’ categories, men have a higher rate.
However, in the ‘inventory’ and ‘incident to arrest’ categories, women have a higher rate.


## Does gender affect who gets a ticket?

The percentage of people getting a ticket given that are female and stopped due to speeding is 95.22%,
around 1% more than males. The percentage of people getting a ticket given that are female and
stopped due to a seat belt violation is 83.22%, around 1.5% more than males. The percentage of
people getting a ticket given that are female and stopped due to a moving violation is 83.23%, around
3% less than men. The percentage of people getting a ticket given that are female and stopped due to
an equipment violation is 71.53%, around 5% less than men. ‘Other’ violation is not considered in this
study.

For “speeding”, “seat belt” and “registration/plates” categories, there is not much difference on who
gets a ticket due to gender. However, for “moving violation” and “equipment” categories, males have
higher citation rates.


## Does gender affect who gets a warning?

The percentage of people getting a warning given that are female and committed a speeding violation
is 4.01%, around the same for males (3.62%). The percentage of people getting a warning given that
are female and have been stopped due to a seat belt violation is 14.53%, around 3% more than men.
The percentage of people getting a warning given that are female and have been stopped due to a
registration/plates violation is 5.02%, the same for males. The percentage of people getting a warning
given that are female and have been stopped due to a moving violation is 9.46%, around 2% more
than men. The percentage of people getting a warning given that are female and have been stopped
due to an equipment violation is 15.99%, around 3% more than men.

For a seat belt, equipment and moving violation, the rate for women is higher than men. Interestingly,
for speeding and registration/plates violation, the rate for both sexes are the similar.


## Does gender affect if the driver gets arrested?

The percentage of people getting arrested given that are female and have committed a speeding
violation is 0.58%, three times less than men. The percentage of people getting arrested given that
are female and have been stopped due to a seat belt violation is 1.38%, around 1% less than men. The
percentage of people getting arrested given that are female and have been stopped due to a
registration/plates violation is 7.77%, around 1% less than men. The percentage of people getting
arrested given that are female and have been stopped due to a moving violation is 5.45%, around the
same for men. The percentage of people getting arrested given that are female and have been stopped
due to an equipment violation is 4.72%, around the same for men.

For a speeding, seat belt, equipment and registration/plates violation, the rate for men are higher
than women. Interestingly, for equipment and moving violation, the rate for both sexes are the similar.

# References

[1] T. S. O. P. Project, "Standford Open Policing," [Online]. Available: https://openpolicing.stanford.edu/data/. 
[2] E. Pierson, C. Simoiu, J. Overgoor, S. Corbett-Davies, D. Jenson, A. Shoemaker, V. Ramachandran, P. Barghouty, C. Phillips, R. Shroff and S. Goel, "A large-scale analysis of racial disparities in police," Nature Human Behaviour, vol. 4, pp. 736-745, 2020.
[3] H. S. Judiciary, "courts.state.hi.us," [Online]. Available: https://www.courts.state.hi.us/self-
help/traffic/moving_citations#:~:text=An%20equipment%20violation%20is%20a,as%20moving% 20or%20parking%20violations.. [Accessed 10 15 2020].
[4] F. l. w. a. editors, "findlaw.com," 20 06 2016. [Online]. Available: https://www.findlaw.com/hirealawyer/choosing-the-right-lawyer/traffic-
violations.html#:~:text=A%20moving%20violation%20occurs%20whenever,to%20parking%20or%20faulty%20equipment.. [Accessed 15 10 2020].
[5] https://www.oakgov.com/, "https://www.oakgov.com/," [Online]. Available: https://www.oakgov.com/courts/district-courts/52-2/traffic/Pages/license-registration- violations.aspx. [Accessed 15 10 2020].
[6] M. Law, "minicklaw.com," 24 01 2014. [Online]. Available: https://www.minicklaw.com/inventory-search-vehicle-legal/#:~:text=An%20inventory%20search%20is%20a,a%20variety%20of%20administrative%20functions.. [Accessed 15 10 2020].
[7] Probable Cause vs Reasonable Suspicion. [Film]. United States: Jules St James, 2019.
[8] "wikipedia.org," [Online]. Available: https://en.wikipedia.org/wiki/Searches_incident_to_a_lawful_arrest. [Accessed 15 10 2020].
