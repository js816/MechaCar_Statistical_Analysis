# Loading the libraries
library(dplyr) 
library(tidyverse)

# Deliverable 1

mpg_data <- read.csv('MechaCar_mpg.csv') # Reading in the csv file

# Performing multiple linear regression
lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD,data=mpg_data) # Generating linear regression
summary(lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD,data=mpg_data)) # Generating the summary statistics


# Deliverable 2
coil_data <- read.csv('Suspension_Coil.csv') # Reading in the suspension coil data as a data frame

# 2 Creating data frame with summaries from the coil data
total_summary <- coil_data %>%
  summarize(mean = mean(PSI),
            med = median(PSI),
            var = var(PSI),
            stdv = sd(PSI))

# 3 Creating data frame with grouped_by summaries from the coil data
lot_summary <- coil_data %>%
  group_by(Manufacturing_Lot) %>%
  summarize(mean = mean(PSI),
            med = median(PSI),
            var = var(PSI),
            stdv = sd(PSI))
