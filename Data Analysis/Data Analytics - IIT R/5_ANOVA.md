Determining sample size when estimating mu:
* Z = (x̄ - µ)/σ/sqrt(n)
* Error of Estimation (tolerable error) E = x̄ - µ
* Estimated Sample Size, n = Z<sup>2</sup><sub>α/2</sub>.σ<sup>2</sup>/E<sup>2</sup>
* Estimated σ = 1/4 (range)

Similar method for,
* Determining sample size when estimating P
* Determining sample size when estimating P with no prior information

Why ANOVA (Analysis of variance)?
* We could compare the means, one by one using t-tests for difference of means. 
* Problem: Each test contains type 1 error. 
* The total type 1 error is 1 - (1-α)<sup>k</sup> where k is the number of means. 
* For example, if there are 5 means and you use α = 0.05, you must take 10 two by two comparisons. Thus the type 1 error = 1 - (0.95)<sup>10</sup> = 0.4012.
* This means, 40% of the time you will reject the null hypothesis of equal means in favor of the alternative! <br>So whenever you want to compare more than two populations, you should not go for t-tests, but ANOVA.

Hypothesis Testing with Categorical Data:
* Chi square tests can be viewed as a generalisation of Z tests of proportions. 
* Analysis of Variance (ANOVA) can be viewed as generalisation of t-tests: a comparison of differences of means across more than 2 groups. 
* Like Chi Square, if there are only two groups, the two analyses will produce identical results - thus a t-test or ANOVA can be used with 2 groups. 

Biggest usecase: Prodcution Process Inputs & Outputs
* Suppose there is a production system, where there are p controllable inputs and q uncontrollable inputs, and output is y = quality characteristic of the output product.
* We should here analyse - what combination of controllable inputs will provide better y values. 
* When you go for improving the quality of the product, almost all quality engineering techniques provide systematic reduction of process variability. 

Case Study using ANOVA

* Example, suppose I want to know which teaching methodology is more effective. 
    - Blackboard
    - Case presentation
    - PPT
* We take 3 students and in 3 situations we calculate their marks. 
* We calculate SST (overall variance - how each element is away from the overall mean). 
* Then we calculate SSB = How much is variance due to teaching methodology. 
* Finally, we calculate SSE = Variance which is inherit - i.e. uncontrollable parameters. 
* Then you calculate degrees of freedom for all the SSx. 
    - For SST, there are 9 elements. So, dof = 8.
    - For SSB, there are 3 columns i.e. teaching methodologies. So dof = 2. 
    - For SSE, there are 3 students evaluated in each teaching methodology. So, dof = (3-1) + (3-1) + (3-1) = 6. 
* We calculate f value as, f = MSB/MSE = (SSB/dof)/(SSE/dof). 
* Once you get f value, you refer to f table and then you find f-critical using the p-value obtained using level of significance.  
* Depending on whether the f value is in acceptance or rejection region, you fail to reject or successfully reject the null hypothesis.

Assumptions for ANOVA: 
* For each population, the response (dependent) variable is normally distributed. For above example, the performance of the student is the dependent variable and the independent variable is the teaching methodology. 
* The variance of the response variable, denoted σ<sup>2</sup>, is the same for all the populations. 
* The observations must be independent. 

ANOVA Types: 
* One Way ANOVA
    - F test
    - Tukey-Kramer test
* RBD (Randomize Block Design)
* Two Way ANOVA
    - Interaction Effects

General ANOVA Setting: 
* Investigator controls one or more factors of interest
    - Each factor contains two or more levels
    - Levels can be numerical or categorical
    - Different levels produce different groups
    - Think of the groups as populations
* Observe effects on the dependent variable 
    - Are the groups the same?
* Experimental design: the plan used to collect the data

Completely Randomized Design:
* Experimental units (subjects) are assigned randomly to the different levels (groups)
    - Subjects are assumed homogeneous. We are not putting high IQ students in one group and others in other group. 
* Only one factor or independent variable (that's why it is called one-way ANOVA). Here teaching methodology is the one way variable and the student performance is the one way variable. 
    - With two or more levels (groups)  
* Analysed by one-factor analysis of variance (one-way ANOVA).

ANOVA Steps (one-way): 
* Ho = all means are equal <br> Ha = not all population means are equal
* Assume that a simple random sample of size n<sub>j</sub> has been selected from each of the k populations or treatments. For the resulting sample data, let <br> x<sub>ij</sub> = value of observation i for treatment j <br> n<sub>j</sub> = number of observations for treatment j <br> x̄<sub>j</sub> = sample mean for treatment j <br> s<sup>2</sup><sub>j</sub> = sample variance for treatment j <br> s<sub>j</sub> = sample standard deviation for treatment j 
* Between-Treatments Estimate of Population Variance σ<sup>2</sup>: The estimate of σ<sup>2</sup> based on the variation of the sample means is called the mean square due to treatments and is denoted by MSTR. <br> MSTR = summation(j = 1 to k) n<sub>j</sub>.(x̄<sub>j</sub> - mean_of_all(x̄<sub>j</sub>))<sup>2</sup>/k-1 <br> Here numerator is called the sum of squares due to treatments (SSTR) and denominator is the degrees of freedom associated with SSTR. 
* Within-Treatments Estimate of Population Variance σ<sup>2</sup>: The estimate of σ<sup>2</sup> based on the variation of the sample observations within each sample is called mean square error (MSE). <br> MSE = summation(from j = 1 to k) (n<sub>j</sub> - 1)s<sup>2</sup><sub>j</sub>/n<sub>T</sub> - k <br> Numerator is called the sum of squares due to error (SSE) and the denominator is called degrees of freedom associated with SSE. 
* Comparing the variance estimates: The F test
    - If the null hypothesis is true and the ANOVA assumptions are valid, the sampling distributions of MSTR/MSE is an F distribution with MSTR dof equal to k-1 and MSE dof equal to n<sub>T</sub> - k. 
    - If the means of the k populations are not equal, the value of MSTR/MSE will be inflated because MSTR overestimates σ<sup>2</sup>. 
    - Hence, we will reject Ho if the resulting value of MSTR/MSE appears to be too large to have been selected at random from the appropriate F distribution. 
* Create the ANOVA Table
* SST divided by its degrees of freedom n<sub>T</sub> - 1 is the overall sample variance that would be obtained if we treated the entire set of observations as one data set. 
* With the entire data set as one sample, the formula for computing the total sum of squares, SST, is: <br> SST = SSTR + SSE <br>
* Anova can be viewed as the process of partitioning the the total sum of squares and the degrees of freedom into their corresponding sources: treatments and error.
* Dividing the sum of squares by the appropriate dof provides the variance estimates and the F-value used to test the hypothesis of equal proportion means. 

Situation: Designing Engineering Experiments

* Experimental design methods are also useful in engineering design activities, where new products are developed and existing ones are improved. 
* By using designed experiments, engineers can determine which subset of the process variables has the greatest influence on process performance. 
* The results of an experiment can lead to:
    - Improved process yield 
    - Reduced variability in the process and closer conformance to nominal or target requirements
    - Reduced design and development time
    - Reduced cost of operation
* Every experiment involves a sequence of activities: 
    - Conjecture: the original hypothesis that motivates the experiment
    - Experiment: the test performed to investigate the conjecture. 
    - Analysis: the statistical analysis of the data from the experiment
    - Conclusion: what has been learned about the original conjecture from the experiment. Often the experiment will lead to a revised conjecture and a new experiment, and so on. 

The completely randomized single-factor experiment example: 
* A manufacturer of paper that is used for making grocery bags is interested in improving the tensile strength of the product. 
* Product engineer thinks that tensile strength is a function of the hardwood concentration in the pup and the range of hardwood concentrations of practical interest is between 5 and 20%. 
* A team of engineers responsible for the study decides to investigate four levels of hardwood concentration: 5%, 10%, 15%, and 20%. 
* They decide to make up to six test specimen at each concentration level, using a pilot plant. 
* All 24 specimens are test on a lab tensile tester, in random order. The data from the experiment is shown in the following table: 

Tensile Strength of Paper in psi unit:
| Concentration | Ob 1 | Ob 2 | Ob 3 | Ob 4 | Ob 5 | Ob 6 | Total | Avg | 
| -- | -- | -- | -- | -- | -- | -- | -- | -- |
| 5 | 7 | 8 | 15 | 11 | 9 | 10 | 60 | 10.00 | 
| 10 | 12 | 17 | 13 | 18 | 19 | 15 | 94 | 15.67 | 
| 15 | 14 | 18 | 19 | 17 | 16 | 18 | 102 | 17.00 | 
| 20 | 19 | 25 | 22 | 23 | 18 | 20 | 127 | 21.17 |
|  |  |  |  |  |  |  | 383 | 15.96 | 

* This is the typical data for single factor experiment. It seems clearly as we increase the concentration, the tensile strength of paper is increasing. 
* We can use the ANOVA to test the hypothesis that different hardwood concentrations do not affect the mean tensile strength of the paper. We will use α = 0.01. 
* The sum of squares are computed as: <br> SST = 512.96 <br> SSTR = 382.79 <br> SSE = SST - SSTR = 130.17.
* F value = 19.6. Using the p-value = 3.59 e-6, we get F critical value = 4.94. 
* We reject Ho and conclude that hardwood concentration in the pulp significantly affects the mean strength of the paper. 

Multiple Comparisons Following the ANOVA (Post-Hoc Analysis): 
* When the null hypothesis is rejected in the ANOVA, we know that some of the treatment or factor level means are different. 
* But ANOVA doesn't identify which means are different. 
* Methods for investigating this issue are called multiple comparison methods. Two ways to do this. 
    - Fisher's Least Significant Difference (LSD) Test
    - Tuckey-Kramer Test

Fisher's LSD Test:
* The Fischer LSD test compares all pairs of means with the null hypotheses Ho = µ<sub>i</sub> - µ<sub>j</sub> for all i ≠ j using the t-statistic. <br> to = (ȳ<sub>i</sub> - ȳ<sub>j</sub>)/sqrt(2*MSE/n)
* Assuming a two-sided alternative hypothesis, the pair of means i and j would be declared significantly different if | (ȳ<sub>i</sub> - ȳ<sub>j</sub>) | > LSD, where LSD is calculated as <br> LSD = t<sub>α/2, a(n-1)</sub>.sqrt(2MSE/n).
* If the sample sizes are different in each treatment, the LSD is defined as <br> LSD = t<sub>α/2, a(n-1)</sub>.sqrt(MSE*(1/n<sub>i</sub> + 1/n<sub>j</sub>)).

On our problem: 
* We will apply Fisher LSD test to the hardwood concentration experiment. There are a = 4 means, n = 6, MSE = 6.51 and t<sub>0.025, 20</sub> = 2.086. The treatment means are: <br> ȳ<sub>1</sub> = 10.00 psi <br> ȳ<sub>2</sub> = 15.67 psi <br> ȳ<sub>3</sub> = 17.00 psi <br> ȳ<sub>4</sub> = 21.17 psi
* The value of LSD is: <br> LSD = t<sub>0.025, 20</sub>.sqrt(2.MSE/n) = 3.07
* Therefore any pair of treatment averages that differ by more than 3.07 implies that the corresponding pair of treatment means are different. 
* In this problem, we see that there are significant differences between all pairs of means except 2 and 3. This implies, that 10 and 15% hardwood concentration produce approximately the same tensile strength and that all other concentration levels tested produce different tensile strengths.  

Tuckey-Kramer Test: 
* Tells which population means are significantly different. 
* Done after rejection of equal means in ANOVA. 
* Allows pair-wise comparisons.
* Compare absolute mean differences with critical range.

Steps to Tuckey-Kramer Test: 
*  Critical Range = Q<sub>U</sub>sqrt(MSW/2(1/n<sub>j</sub> + 1/n<sub>j'</sub>)) where <br> Q<sub>U</sub> = Value from studentized range distribution with c and n-c degrees of freedom for the desired level of α <br> MSW = Mean Square Within n<sub>j</sub> and n<sub>j'</sub>, sample sizes from groups j and j'

On our problem:
1. Compute absolute mean differences: <br> | x̄<sub>1</sub> - x̄<sub>2</sub> | = 5.67 <br> | x̄<sub>1</sub> - x̄<sub>3</sub> | = 7 <br> | x̄<sub>2</sub> - x̄<sub>3</sub> | = 1.33 <br> | x̄<sub>1</sub> - x̄<sub>4</sub> | = 11.17 <br> | x̄<sub>2</sub> - x̄<sub>4</sub> | = 5.5 <br> | x̄<sub>3</sub> - x̄<sub>4</sub> | = 4.17 <br>
2. Find the Q<sub>U</sub> value from the table with c = 4 and (n-c) = (24-4) = 20 degrees of freedom for the desired level of α = 0.05. <br> Q<sub>U</sub> = 3.96, using Q table. 
3. Compute Critical Range: <br> Critical Range = Q<sub>U</sub>sqrt(MSW/2(1/n<sub>j</sub> + 1/n<sub>j'</sub>)) = 4.124
4. Other than | x̄<sub>2</sub> - x̄<sub>3</sub> |, all of the absolute mean differences are greater than critical range. Therefore, there is significant difference between each pair of means, except 10% concentration and 15% concentration at the 5% level of significance. 

Intro to Randomized Block Design (RBD):
* A completely randomized design (CRD) is useful when the experimental units are homogeneous. 
* If the experimental units are heterogenous, blocking is often used to form homogeneous groups. 

Why RBD?
* A problem can arise whenever differences due to extraneous factors (ones not considered in the experiment) cause the MSE term in this ratio to become large. 
* In such cases, the F value in equation can become small, signaling no difference among treatments means when in fact such a difference exists.
* Experimental studies in business often involve experimental units that are highly heterogeneous; as a result, randomized block designs are often employed. 
* Blocking in experimental design is similar to stratification in sampling. 
* The purpose of RBD is to control some of the extraneous sources of variation by removing such variation from the MSE term. 
* This design tends to provide a better estimate of the true error variance and leads to a more powerful hypothesis test in terms of the ability to detect differences among treatment means. 

Situation: Air Traffic Controller Stress Test
* A study measuring the fatigue and stress of air traffic controllers resulted in proposals for modification and redesign of the controller's work station. 
* After consideration of several designs for the work station, three specific alternatives are selected as having the best potential for reducing controller stress.
* The key question is: To what extent do the three alternatives differ in terms of their effect on controller stress?
* In a completely randomized design, a random sample of controllers would be assigned to each work station alternative. However, controllers are believed to differ substantially in their ability to handle stressful situations. 
* What is high stress to one controller might be only moderate or even low stress to another. Hence, considering the within-group source of variation (MSE), we must realise that this variation includes both - random error and error due to individual controller differences. 
* In fact, managers expected controller variability to be a major contributor to the MSE term. 

Data of the controllers:

| | Sys A | Sys B | Sys C |
| -- | -- | -- | -- |
| Controller 1 | 15 | 15 | 18 |
| Controller 2 | 14 | 14 | 14 |
| Controller 3 | 10 | 11 | 15 |
| Controller 4 | 13 | 12 | 17 |
| Controller 5 | 16 | 13 | 16 |
| Controller 6 | 13 | 13 | 13 |

* After performing ANOVA on this dataset, we get treatment means as: <br> x̄<sub>1</sub> = 13.5 <br> x̄<sub>2</sub> = 13 <br> x̄<sub>3</sub> = 15.5 <br> If you will finish the ANOVA, you will not reject the null hypothesis and might believe that all the means are sample. 

ANOVA Table for the randomized block design with k treatments and b blocks look like: 

| Source of Variation | Sum of Squares | Degrees of Freedom | Mean Square | F | p value |
| -- | -- | -- | -- | -- | -- |
| Treatments | SST | k - 1 | MSTR = SSTR/k-1 | MSTR/MSE | p |
| Blocks | SSB | b - 1 | MSB = SSB/b-1 | | |
| Error | SSE | (k-1)(b-1) | MSE = SSE/(k-1)(b-1) | | |
| Total | SST | n<sub>T</sub> - 1 | | | |

RBD Steps on the problem
0. Terminology: <br> x<sub>ij</sub> = value of the observation corresponding to treatment j in block i <br> x̄<sub>.j</sub> = sample mean of the jth treatment <br> x̄<sub>i.</sub> = sample mean of the ith block <br> x̄ = overall sample mean 
1. Compute the SST <br> SST = 70
2. Compute the SSTR <br> SSTR = 21
3. Compute the SSB <br> SSB = k.summation(from i = 1 to b) (x̄<sub>i.</sub> - x̄)<sup>2</sup> = 30
4. Compute SSE <br> SSE = SST - SSTR - SSB = 19
5. F<sub>0.025</sub> = 5.46 and F<sub>0.01</sub>
 = 7.56 (from p-values). Our F value = 10.5/1.9 = 5.53
6. We reject the null hypothesis in this case. With introduction of RBD, our decision is completely changed. 

Conclusion to above problem solution

* Note that the ANOVA table shown provides an F value to test for treatement effects but not for blocks.
* The reason is that the experiment was designed to test a single factor - work station design. 
* The blocking based on individual stress differences was conducted to remove such variation from the MSE term. 
* However, the study was not designed to test specifically for individual differences in stress. 

Factorial Experiment: 
* A factorial experiment is an experiment design that allows simultaneous conclusions about two or more factors. 
* The term factorial is used because the experimental conditions include all possible combinations of the factors. 
* The effect of a factor is defined as the change in response produced by a change in the level of the factor. It is called a main effect because it refers to the primary factors in the study. 
* For example, for 'a' levels of factor A and 'b' levels of factor B, the experiment will involve collecting data on 'ab' treatment combinations. 
* Factorial experiments are the only way to discover interactions between variables. 

Example of Two Factor Factorial Experiment: 
* As an illustration of a two-factor factorial experiment, we will consider a study involving the CAT, a standardized test used by Grad schools of business to evaluate an applicant's ability to pursue a graduate program in that field. 
* Scores on CAT range from 200 to 800, with higher scores implying higher aptitude. 
* In an attempt to improve students' performance on the CAT, a major university is considering offering the following three CAT prep programs:
    - A three hour review session covering the types of questions generally asked on the CAT. 
    - A one-day program covering relevant exam material, along with the taking and grading of a sample exam. 
    - An intensive 10 week course involving the identification of each student's weaknesses and the setting up of individualized programs for improvement. 
* So, Factor 1 => 3 treatments: Three hour review, one day program, 10 week course. Before selecting the prep program to adopt, further study will be conducted to determine how the proposed programs affect CAT scores. 
* The CAT is usually taken by students from three colleges. 
    - Colleges of Business & Commerce
    - Colleges of Engineering
    - Colleges of Arts & Social Sciences
* Therefore, Factor 2 => 3 treatments: Business & Commerce, Engineering, Arts & Social Sciences. This is an experiment that whether a student's undergrad college affects the CAT score. 
* This gives us 9 treatment combinations for the two factor CAT experiment. 

| | Business | Engineering | Arts |
| -- | -- | -- | -- |
| 3 hr review | 1 | 2 | 3 |
| One day program | 4 | 5 | 6 |
| 10 week course | 7 | 8 | 9 |

* In experimental design terminology, the sample size of two for each treatment combination indicates that we have two _replications._ 

Data for 2 students/treatment for this CAT experiment (total 18 observations): 

| | Business | Engineering | Arts |
| -- | -- | -- | -- |
| 3 hr review | 500<br>580 | 540<br>460 | 480<br>400 |
| One day program | 460<br>540 | 560<br>620 | 420<br>480 |
| 10 week course | 560<br>600 | 600<br>580 | 480<br>410 |

* We want answers to these questions: 
    - Main effect (factor A): Do the prep program differ in terms of effect on CAT scores?
    - Main effect (factor B): Do the undergrad colleges differ in terms of effect on CAT scores? 
    - Interaction effect (factor A and B): Do students in some colleges do better on one type of prep program whereas others do better on a different type of prep program?
* The term _interaction_ refers to a new effect that we can now study because we used a factorial experiment. If the interaction effect has a significant impact on the CAT scores, we can conclude that the effect of the type of prep program depends on the undergrad college. 

Two way ANOVA
* Table structure
* Terminology
* Computation (straightforward)

Back on the problem: 
* SST = 82450
* SSA = 6100
* SSB = 45300
* SSAB = 11200
* SSE = SST - SSA - SSB - SSAB = 19850
* F<sub>A</sub> = 1.38, F<sub>B</sub> = 10.27, F<sub>A</sub> = 1.27
* p<sub>A</sub> = 0.299, p<sub>B</sub> = 0.005, p<sub>AB</sub> = 0.350

Conclusion on the problem:
* We accept null hypothesis on Prep program and interaction effect and we reject null hypothesis on college.
* So, there is no interaction, there is no effect of prep program, but there is an effect of the college background they belong to. 
* What we are concluding is: The college they belong to matters, it is an important variable. We are not saying, engineering students will perform better or arts students may not perform better. 

[ ----------- PRACTICAL ---------- ]