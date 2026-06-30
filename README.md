## Research
https://docs.google.com/document/d/18KgChC6qzngcY5tHbvzZDImq3opYi2hnKpBRUSOYS7s/edit?tab=t.0

## Notes
This dataset contains outliers, null values, and some technical anomalies. It is expected that participating teams will apply oil and gas domain knowledge

**Part 1** will be data science based perhaps no domain knowledge things, just basic way of data cleaning, no constraints check, an intuitive way of filling missing values, just the basic stuff, maybe outlier removal as well

**Part 2** will be listening to constraints, domain knowledge of generating features, etc. It will include all of part 1 + extra basically. Something to note, there's 3 geological anomalies in 3 features, perhaps some constraints are violated based on provided range in the about the dataset part or something like that.

## Plan
### Phase 1 - 19th June - 20th June
### Phase 1 A
**KC & AJ** - In depth research and understanding of all features and empirical formulas related to this part of geology combined with dataset exploration (EDA) to understand what the organizers mean about "correct geological anomalies or inconsistencies in at least three (3)
dataset features"

### Phase 1 B
**Damola** - Start Basic Data Cleaning check in notebook for train data (this checks will apply to Part 1 and Part 2). You can reference this [notebook](https://github.com/pithun/2024-SPE-DSEATS-Datathon-Open-Solution/blob/master/2nd-Place/Submissions/Chigozie_Udoh_2024_DSEATS_Datathon_5272808.ipynb)

Specifically, do;
1. Column name shortening
2. Data Type check (ensure correct data types are assigned)
3. Consistency check for text columns (ensure trap_type for example has the different trap types with same name. e.g we shouldn't have DOME and dome)
4. Missing Data check (you have to suggest ways to fill missing values)
5. Duplicate check
6. Outlier Detection (Feel free to use a model like Isolation Forest for this later on)
7. Any extra stuff is highly welcomed

### Phase 1 C
**Udoh**  - Slides preparation + Review/Support 1A and Review 1B

### Phase 2 - 21st June
Brainstorm Session to get clarity on what to do with dataset regarding part 2

### Phase 3 - 21st June to 24th June
- **Everyone** - Feature Engineering and Modelling Brainstorming
- **KC** - Review Slides Template
- **Udoh and Damola** - FE and Modelling Execution
- **AJ** - FE and Modelling Support

### Phase 4  - 25th June to 26th June
**Everyone** - Populating Slides based on part you worked on

### Phase 5 - 27th June to 28th June
Individual reviews to confirm that results make sense
