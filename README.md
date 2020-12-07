# Rainbow-Railroad-Data-for-Cause
Rainbow RailRoad is a NPO based in Torotno. Their mission is to fund LGBTQI people to escape from the countries which systematically discriminate or opress them, or even threathen their lives. The organization depends on the volunteers to create the data visualization
for fundraising campaign for their cause.

I constructed scores to show each country's level of tolerance toward peole with different sexual orientation, and visualized them in the form of the world map (blue is more tolerent and orange is less tolerent). 

This is the code I worte by Python to construct such scores. file: LGBT law.ipynb

This is the link to the final vizualization (by Tableau). https://public.tableau.com/profile/satoko.suda#!/vizhome/Rainbow_0/Dashboard1



********************
## Sorering system details, in case you are interested:

Existence of protection such as rights of civil union is +1, existence of criminal punishment is -1 multiplied by severity of sentences (1 for "up to 2 years", 10 for "death sentence", for example) if there was any arrest in past 3 years. After giving different weights to different protections or punishments, I would aggregate those points for each country to get the final score. Therefore,

Legal:All genders +2
Ages of Consent: Equal +1
Ages of Consent: Unequal -1
Illegal:Male: -1
Illegal:Female: -1

Penalising text (for each offence): -1 * (+1 for Max Sentences: 1 M to 2 Yrs
                                                      +2 for 3 to 7 Yrs
                                                      +3 for 8 to 13 Yrs
                                                      +5 for 14 to Life
                                                      +10 for Death ) * (Arrest in Past 3 Yrs (0 or +1))

Promotion or Morality (for each offence): -1* (+1 for Max Sentences: 1 M to 2 Yrs  Or Fines (No prison sentence)
                                                                 +2 for 3 to 7 Yrs
                                                                 +3 for 8 to 13 Yrs
                                                                 +5 for 14 to Life
                                                                 +10 for Death ) * (Arrest in Past 3 Yrs (0 or +1))
Ban on NGO- Yes: -1
NRHI SO inclusive -Yes +1
NRHI SO inclusive -No -1
NRHI SO inclusive -Unclear & None 0
Protection: Constitution: +5
Protection other than Constitution: +1 for each
Relationship Recognition: Marriage +5
Relationship Recognition: Cvivil +2
Relationship Recognition: Joint Adoption +2
Relationship Recognition: 2nd Parent Adoption +2

Under this scoring system,

Syrian score is : -16
Egypt: -8
Japan: 4
Canada: 13
Denmark: 17
