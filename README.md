# neural-network-challenge-1
# What data was collected (column headers)
payment_history	float64
location_parameter	float64
stem_degree_score	float64
gpa_ranking	float64
alumni_success	float64
study_major_code	float64
time_to_completion	float64
finance_workshop_score	float64
cohort_ranking	float64
total_loan_score	float64
financial_aid_score	float64
credit_ranking	int64

# What other types of data were considered
Gender and minority scores were entertained but based on Supreme Court rulings about college admissions, it was decided not to use these types of 
data in the calculation.  Other than that, no other data elements were considered.

# Featurs and Nodes
I used 11 features and 6 nodes in the first hidden layer, and 3 nodes in the second hidden layer.  This decision was based on the relevant columns of data
which I felt all were needed to accurately calculate the loan score.
# Scale and model
I used the Standard Scaler to scale the model, then did a Sequential model. Here are my results:
Model: "sequential"
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━┓
┃ Layer (type)                         ┃ Output Shape                ┃         Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━┩
│ dense (Dense)                        │ (None, 6)                   │              72 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dense_1 (Dense)                      │ (None, 3)                   │              21 │
├──────────────────────────────────────┼─────────────────────────────┼─────────────────┤
│ dense_2 (Dense)                      │ (None, 1)                   │               4 │
└──────────────────────────────────────┴─────────────────────────────┴─────────────────┘
 Total params: 97 (388.00 B)
 Trainable params: 97 (388.00 B)
 Non-trainable params: 0 (0.00 B)
None
## Types of Filtering and what I selected
There are three types of filtering.  They are:
Filter Type	    Basis for Recommendation	                        Example Use Case
Collaborative	User interactions and preferences of similar users	Movie recommendations on Netflix based on ratings by similar users
Content-Based	Attributes or properties of the items	            Suggesting books similar to ones you've read
Context-Based	External factors and specific user scenarios	    Restaurant suggestions based on your current location and time of day

I selected Context-Based filtering for the following reasons:  
1. by considering the specific context in which each student is situated, the loan can be tailored to each student's circumstances
2. factors like success rate of the institution and location can greatly influence the potential outcome for the student,
    which makes the scoring more relevant and accuratel
3. as contextual factors change, like a student's GPA or payment history, the model can make adjustments to the student's loan score.
