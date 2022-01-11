# Election Analysis
Analyzing Colorado congressional district election results via Python.

## Overview of Election Audit
A Colorado Board of Elections employee has given the following tasks to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candiates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.
6. Calculate the total voter turnount for each county that participated in the congressional district election.
7. Calculate the percentage of votes that each county received out of the total.
8. Determine which county had the highest voter turnount.

## Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.63.2

## Election-Audit Results
The analysis of the election saw that:
- There were 369,711 votes cast in the election.
- The candidates were:
    - Diana DeGette
    - Charles Casper Stockham
    - Raymon Anthony Doane
- The candidate results were:
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
    - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
    - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.
- The voter turnount for each county in this precinct was:
    - Denver County received 82.8% of the vote and 306,055 number of votes.
    - Jefferson County received 10.5% of the vote and 38,855 number of votes.
    - Arapahoe County received 6.7% of the vote and 24,801 number of votes.
- The county in this congressional precinct with the largest voter turnount was:
    - Denver County, which generated 82.8% of the vote and 306,055 number of votes.

## Election-Audit Summary
By expanding the election audit to include voter turnount by county, we can further conclude where voter turnount may be high or low, and further target the necessary infrustructure and resources to ensure that there's equal opportunity for all citizens to have their voice heard in future elections.  While we have a distribution of percentage of votes by county compared against total votes cast, it would also be helpful to pull in total number of eligible voters by county, to see the compliance of votes cast against total eligible amount of votes that can be cast.  We would need to slightly alter our code to ensure a field such as "total_voters = 0" is initialized to track a total voter count, as well as ensure it's worked in to any further downstream lines of code.

In addition, it would be helpful to understand the distribution of votes by candidate in each eligible county.  We only see the vote total, but not how those votes allocated across each candidate.  By adding an if-statement to the code, we should be able to also understand how each candidate performed by county as well.

The majority of this code can also be widely replicated to not only include this single congressional district, but also other election levels as well such as future municipal, state or even federal elections.  This would just require slightly tweaking the code to ensure we're defining the accurate voting level hierarchy (ex: if we're looking at analyzing a federal election across states instead of a state election by county, we would want to define the list, dictionay syntax of "county_options = [], county_votes = {}" and instead write it out as "state_options = [], state_votes = {}").
