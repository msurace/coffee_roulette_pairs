# Generate Coffee Roulette pairings

Generate rounds of pairs with no repeating names within each round, and no repeating pairs between rounds.

## Usage

1. Update names.csv with the names of participants, and include any unwanted pairings in unwantedpairs.csv in two columns.

1. Run the code, which outputs pairs for each round such that everyone participates in each round.

NB the parameter alpha (0.0 < alpha < 1.0) determines how many rounds are generated, and how long the code takes to execute. It's default value is 0.7, and can be decreased if desired.  
NB the code may be terminated early, in which case any rounds which have already been generated will be present.
