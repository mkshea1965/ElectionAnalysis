# ElectionAnalysis
The purpose of this analysis is to help a Colorado Board of Elections employee named Tom in completing an audit of the tabulated results of Colorodo's U.S. Congressional precinct. Tasks completed for this audit included reporting the total number of votes cast, the total number of votes for each candidate, the percentage of votes cast for each candidate, and the winner of the election according to popular vote (i.e. the person with the largest number of votes). Tom's manager had asked us to develop a code in Pyhton so that the code could be modified with minimal work and applied to other elections audits. By using Python to automate the auditing process, the election can be certified more quickly than when using Excel, saving the Colorado Board of Elections time, resources, and from excessive media coverage.

## Overview of Election Audit

## Election-Audit Results

- How many votes were cast in this congressional election?
    - 369,711

- Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
    - County Votes:
        - Jefferson: 10.5% (38,855)
        - Denver: 82.8% (306,055)
        - Arapahoe: 6.7% (24,801)

- Which county had the largest number of votes?
    - Denver

- Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
    - Candidate:
        - Charles Casper Stockham: 23.0% (85,213)
        - Diana DeGette: 73.8% (272,892)
        - Raymon Anthony Doane: 3.1% (11,606)

- Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
    - Election Results:
        - Winner: Diana DeGette
        - Winning Vote Count: 272,892
        - Winning Percentage: 73.8%

## Election-Audit Summary
In conclusion, the script produced for the Colorodo Board of Elections can be minimally modified to apply to any election, depending on the data file the election data is coming from. One example of modifying the script includes changing lines 8-9 of PyPoll_Challenge.py:

  8  # Add a variable to load a file from a path.
  9  file_to_load = os.path.join("Resources", "election_results.csv")
  
We could change the file_to_load variable to any csv file as long as we know the file path and how to correctly manipulate it relative to the script's location. 

This change would cause further script changes due to the different indexes of column and row categories in the new csv file. For example, we can change the index of the code below (lines 47-51 of PyPoll_Challenge.py) to align with another csv file's approriate headers.

    47 # Get the candidate name from each row.
    48    candidate_name = row[2]
    49
    50    # 3: Extract the county name from each row.
    51    county_name = row[1]

Utilizing this script can save not only the Colorado Board of Elections time and other resources, but it can save other Board of Elections time as well.
