
==========#########==========#########==========#########==========#########

## project description

This project divides the US into population clusters based on census tract
centroids and then profiles the census characteristics of each cluster.

## project plan

#### plan structure

This project follows a three draft structure:
+ D1 (Rough Draft) - Build the initial rough draft of the code
  – Address technical/architectural challenges early, confirming feasibility
  – Make a fully functional prototype
+ D2 (Improved Draft) - Use hindsight and polish to improve prototype draft
  – Incorporate lessons learned / hindsight into the revised design
  – Remove technical debt
  – Polish output
+ D3 (Optimization) - Identify and mitigate pain points in the code
  – Find faster / more resource efficient alternative approaches
  – Across projects, D3 is lower priority
    – Better to have three projects at D2 than two projects at D3

Each project
+ PP  (Plan Project) – Plan the features and ordering of the project code
  – Outline plan in the README file, but do not waste time over-documenting
  – Set up the Notebook script with corresponding sections
  – Acquire data (if the code itself does not do data acquisition)
  – Initialize an GitHub repository
  – Learn any necessary secondary skills
+ RD  (Refine Data) – Convert raw data into a form suitable for model
+ MD  (Model Data) – Deploy models on the refined data
  – Generate model results
  – Determine the quality of model results
+ EMR (Enrich Model Results) – Contextualize model with supplemental data
  – Partition secondary data to match model results
  – Calculate statistics for each partition
+ PVD (Prepare Visualization Data) – Generate results extracts for visuals
+ RV  (Render Visualization) – Visual results
+ UGP (Update GitHub Portfolio) –  Showcase project in GitHub portfolio

#### task tracking matrix

   | D1| D2| D3|
   |:- |:- |:- |
PP | X |   |   |
GD | X |   |   |
RD | X |   |   |
MD | X |   |   |
EMR| X |   |   |
PVD| X |   |   |
RV | X |   |   |
UGP| X |   |   |
W  | 55| 30| 15|

   Total Progress: (55 * 8.0 + 30 * 0.0 + 15 * 0.0) / (100 * 8) = 55%
Priority Progress: (55 * 8.0 + 30 * 0.0 + 00 * 0.0) / (085 * 8) = 65%

KEY:
X = 100% Complete
/ = ≥50% Complete


#### to-dos and notes (for draft 2)
+ Change the KNN to use a precomputed geographic distance matrix
+ Scale tract-level potus vote to match national totals
+ Change census profile vars to be potus, education, life expectency, income per cap.
    + This correspond to HDI + politics
+ Do agglom, then agglom within agglom, instead of agglom + dbscan
+ Use land area to discard the most isolated points (can also use ML if necessary)
+ Change the clustering approach to iterate through k number of clusters
    + OR Make cluster k decision-making search for 95% solutions
+ Mask Canada and Mexico from map (also clip the overflow on the elbow chart)

## directory layout

Project directories are lettered to indicate sequences, and code scripts are
numbered for the same reason.
+ A_Input - Original input data.  It should be read but never written.
+ B_Progress - Contains intermediate data as needed.
+ C_Output - Project's final products (tables and visualizations)
+ Z_Admin - Contain context and planning documentation as needed.

## data sources
+ data.census.gov (2020 census; census tract level)
    + tract centroids (.dbf files)
    + total households and households with income ≥$200,000 (table DP03)
    + total population, ≥65 years old, and non-hispanic white (table DP05)
+ electionlab.mit.edu/data (2020 potus election data)
    + total voters and republican voters (county presidential election returns)
