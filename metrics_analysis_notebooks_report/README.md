README.md
# Single User Test
The single user test result analysis notebook is based on naming standard of ScaleFactor_Pattern_Scenario_Query_Cache_Run when exporting data from DAX Studio.

* Options for ScaleFactor: 10,100,1000
* Options for Pattern: DL,DQ,MIR,CM (Which stands for Direct Lake, DirectQuery, Mirroring, Composite Model)
* Options for Scenario: S1,S2,S3
* Options for Query: Q1,Q2,Q3,Q4,Q5
* Options for Cache: C,W,H,HH 
* Options for Run:R1,R2,R3,R4

So 10_DL_S1_Q1_C_R1 is Direct Lake test on Scale Factor 10 for Scenario 1 Query 1 under cold cache Run 1

If you were to conduct your own test and use a different naming standard, update the code in single_user_test_result_analysis.ipynb to reflect your own naming standard.


# Load Test
The load test result analysis notebook is based on naming standard of Pattern-ScaleFactor-Run when naming load tests.


* Options for Pattern: db_cm,db_dq,fab_dl,fab_mirror
* Options for ScaleFactor: 10,100,1000
* Options for Run:01,02,03

So db_cm_10_01 is Composite Model test on Scale Factor 10 Run 1

If you were to conduct your own test and use a different naming standard, update the code in load_test_result_analysis.ipynb to reflect your own naming standard.