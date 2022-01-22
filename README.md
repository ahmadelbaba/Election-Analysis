# Election-Analysis

## Project Overview
A Colorado Board of Elections employee has given me the following tasks to complete the election audit of a recent local congressional election.
1. Calculate the total number of votes cast.
2. Get a complete list of counties in which votes where cast.
4. Calculate the total number of votes in each county.
5. Calculate the percentage of votes each county out of the total count.
6. Determine the county with highest turnout.
7. Print the Election Results to the Command line
8. Save a written Analysis to a text file.

## Resources
- Data Source: election_results.csv
- Software: Python 3.6.1, Visual Studio Code, 1.38.11

# Analysis Summary
The analysis of the election show that:

## County Results

- There were 369,711 total votes cast
- The counties were: Jefferson, Denver, Arapahoe
- The votes in each county were as per below:
  * Jefferson: 10.5% (38,855)
  * Denver: 82.8% (306,055)
  * Arapahoe: 6.7% (24,801)
- The countywith the highest turnout is: Denver

 <br /> 
 
## Candidate Results

- The candidates were: Charles Casper Stockham, Diana DeGette, Raymon Anthony Doane
- The votes for each canadidate were as per below:
  * Charles Casper Stockham: 23.0% (85,213)
  * Diana DeGette: 73.8% (272,892)
  * Raymon Anthony Doane: 3.1% (11,606)
 -  The winning candidate is: Diana DeGette

# Challenge Summary

The code developed can be reused to to anlze any election. 
This can be done in two ways:
- simply changing the data in the source .csv file name "election_results.csv" 
- or by uploading a different .csv file and changing the filename in the code below:

![Read_CSV](/Resources/Read_CSV.PNG)

The reason the code will work is because our code is flexible. Our code parses through the differen rows in our source data file to find the different "Candidates" and "Counties". The list of Candidates and Counties are note hard coded. Rather our code discovers the two lists as it goes through the rows of our data file. 

First our code declares lists in which we will store new counties/candidates as we find them (lines 18 and 22). We also declare dictionaries so we can store election results (lines 19 and 23):

![Lists](/Resources/Declaring_Lists.PNG)

Second our code parses through the rows of our source data file and dynamically adds new candidates to their respective lists as it finds them. 
- In line 51 we extract the name of the candidate from each row.
- In line 59 we check if the candidate has already been added to our list.
- In line 62 we add the candidate to our list if they have not been added before.

![Adding_to_Lists](/Resources/Adding_to_lists.PNG)

Similarly we do the same to counties. Our code parses the rows in our source data file and dynamically adds new counties to their respective lists as it finds them. 

The dynamic addition of candidates/counties relieves us from the need to hardcode candidate and county names and allows our code to accept new data and generate a comprehensive analysis.  
