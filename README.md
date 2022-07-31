# ANA-505-Week-4-Activity
Week 4 Assignment on dplyr package in R


#Week 4: dplyr package


mydata <- data.frame(HairEyeColor)


head(mydata,10)


install.packages("dplyr")
library(dplyr)


select(mydata, Hair, Sex)


mydata_hair_sex <- select(mydata, Hair = Hair, Sex = Sex)


mydata_hair_sex <- select(mydata_hair_sex, -Sex)


rename(mydata, Gender = Sex)


mydata[,"Gender"] <- NA
mydata


mydata_male <- filter(mydata, Sex == "Male")
mydata_male <- select(mydata_male, Sex)
mydata_male


group_by(mydata, Sex)

#After you run it, write the total here:592

total=mutate(mydata, total=cumsum(Freq))
total


mydata_female <- filter(mydata, Sex == "Female")
mydata_female <- select(mydata_female, Sex)
mydata_female


bind_rows(mydata_male,mydata_female)


mydata_eye<- arrange(mydata, desc(Eye))
mydata_eye

