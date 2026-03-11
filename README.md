# Measuring-the-Regional-Fiscal-Multiplier
The goal is to determine whether an increase in government spending in a specific sector correlates with a statistically significant change in regional economic performance, controlling for confounding variables. 
The specific sectors will be human capital, physical capital, safety (such as police), and healthcare (such as medicaid).

For Data Aquisition I will be using the FRED API from the Federal Bank of St. Louis as well as censusapi which is from Census Bureau, giving me a robust source of data.
Most of the project will be done in R markdown since I can access the API's with ease and reading them in is a lot easier than importing everything to python code. Though somce analysis may be done in python as well as R. 

Hypothesis Testing:
H0: State-level sectoral spending is not a primary driver of GDP growth (perhaps national trends or private sector investment matter far more).

H1: At least one of those sectors has a significant impact. 

As well as doing an F-test for joint significance (which is the style of hypothesis testing I have chosen for this project), I will also find the specific p values for each Beta value (each specific sector is a beta value) IF the null happens to get rejected.
This is to find the 'heaviest lifter' in terms of rejecting the null (the one that is the largest outlier, giving us the most significant impact).

The project has a relatively simple premise but there are pitfalls that are to be considered. 
Such as time lag and endogeneity. Time lag is simple enough to resolve; I can just test the GDP growth of certain investments (like investments in education) against the GDP in 5 years time so it has enough time to actually impact the GDP. Since
Human Capital investment takes time to affect the GDP. But endogeneity is a difficult problem to overcome. There is a "chicken or egg" problem here. Does government spending cause GDP growth, or does a booming GDP give the government more tax revenue to spend?
