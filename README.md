
==========#########==========#########==========#########==========#########

## project description

This project divides the US into population clusters based on census tract
centroids and then profiles the census characteristics of each cluster.

## project plan

#### plan structure

This project follows a three draft structure:
+ D1 (Rough Draft) - Build the initial rough draft of the code
  - Address key technical/architectural challenges early, confirming feasibility
  – Make a fully functional prototype
+ D2 (Improved Draft) - Use hindsight and polish to improve the prototype draft
  – Incorporate lessons learned / hindsight into the revised design
  – Remove technical debt
  – Polish output
+ D3 (Optimization) - Identify and mitigate pain points in the code
  – Compare alternative designs to find the fastest / most resource efficient
  – Across projects, D3 is lower priority
    – Better to have three projects at D2 than two projects at D3

Each project
+ PP  (Plan Project) – Plan the features and ordering of the project code
  – Outline the plan in the README file, but do not waste time over-documenting
  – Set up the Notebook script with corresponding sections
  – Acquire data (if the code itself does not do data acquisition)
  – Initialize an GitHub repository
  – Learn any necessary secondary skills
+ RD  (Refine Data) – Convert raw data into a form suitable for model
+ MD  (Model Data) – Deploy models on the refined data
  – Generate model results
  – Determine the quality of model results
+ EMR (Enrich Model Results) – Use secondary data to contextualize model results
  – Partition secondary data to match model results
  – Calculate statistics for each partition
+ PVD (Prepare Visualization Data) – Generate results extracts for visualization
+ RV  (Render Visualization) – Visual results
+ UGP (Update GitHub Portfolio) – Update GitHub portfolio to showcase project

#### task tracking matrix

   |Imp|Dra|Opt|
   |:- |:- |:- |
PP |  X|   |   |
RD |   |   |   |
MD |   |   |   |
AMR|   |   |   |
PVD|   |   |   |
RV |   |   |   |
UGP|   |   |   |
High-Priority Progress:|1 of 14|(07%)
Total Progress:|1 of 21|(05%)

#### to-dos and notes
– Determine if project is suitable for AWS

## directory layout

Project directories are lettered to indicate sequences, and code scripts are
numbered for the same reason.
+ A_Input - Original input data.  It should be read but never written.
+ B_Progress - Contains intermediate data as needed.
+ C_Output - Tables and visualizations that are the project's final products.
+ Z_Admin - Contain context and planning documentation as needed.
