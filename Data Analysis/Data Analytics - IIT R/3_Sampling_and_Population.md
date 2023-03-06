Two Types of Statistics:
* Descriptive: Collecting, presenting & describing data
* Inferential: Drawing conclusions and/or making decisions concerning a population based only on sample data

Sampling:
* Need for sampling:
    - Less time consuming than a census
    - Less costly than a census
    - Based on appropriate samples, we can obtain information about population with sufficiently high precision
    - Because the research is destructive and sampling can be done by damaging only a part
    - If assessing the population is not possible, sampling is the only option
* Methods of sampling:
    - Random:
        * Simple random
        * Stratified random
        * Systematic
        * Cluster 
    - Non-random
        * Convenience
        * Judgement
        * Quota
        * Snowball
* Errors in Sampling

Describing a sampling distribution
- If the population is normal
- If the population is not normal
    * Central Limit Theorem

Acceptance Intervals:
* Goal: Determine a range within which sample means are likely to occur, given a population mean and variance. 
* By the Central Limit Theorem (CLT), we know that the distribution of X is approximately normal if n is large enough, with mean µ and standard deviation σ.
* Let z<sub>α/2</sub> be the z-value that leaves area α/2 in the upper tail of the normal distribution, then µ ± z<sub>α/2</sub>.σ is the interval that includes X with probability 1 - α. 

Idea of sampling distribution:
* Sampling distribution of mean
* Sampling distribution of proportion
* Sampling distribution of variance

Chi-squared Distribution: Family of distributions, depending on the degrees of freedom, usually n-1.
* Degrees of freedom
* Examples of chi-squared distribution

Confidence Intervals:
* For population mean
    - when population variance is known
    - when population variance is unknown
* For population proportion
* For variance of a normal population

Estimators

* An estimator of a population parameter is 
    - a random variable that depends on sample information
    - whose value provides an approximation to the unknown parameter
* A specific value of that random variable is called an estimate.
* Types:
    - Point estimate: A single number
    - Interval estimate: provides additional info about variability
* Unbiasedness: A point estimator is said to be an unbiased estimator of the population parameter if the expected value or mean of the sampling distribution is equal to population parameter.
    - The mean x-bar is the unbiased estimator of mu. 
* Bias = E(sampling parameter) - population parameter
* If P(a < θ < b) = 1 - α, then the interval from a to b is called 100(1-α)% confidence interval of θ and the quantity (1-α) is called the confidence level of the interval. 

Margin of error:
* ME = z<sub>α/2</sub>.σ/sqrt(n)
* Reducing the margin of error: 
    - the population standard deviation can be reduced 
    - the sample size is increased
    - the confidence level is decreased
* z<sub>α/2</sub> is called as Reliability Factor. 

Students's t Distribution

* If the population standard deviation σ is unknown, we can substitute the sample standard deviation, s. 
* But this introduces extra uncertainity, since s is variable from sample to sample. So, we use the t distribution instead of the normal distribution. 
* Assumptions: 
    - Population standard deviation is unknown
    - Population is normally distributed
    - If population is not normal, use large sample
* Confidence Interval Estimate = x̄ ± t<sub>n-1, α/2</sub>.S/sqrt(n)
* Here, ME = t<sub>n-1, α/2</sub>.S/sqrt(n)
* Confidence Intervals for proportion
* Confidence Intervals for Variance

Finite Population Correction Factor
* When the number of elements in the population is countable and small, we say it is a finite population. 
* If the sample size is more than 5% of the population size (and sampling is without replacement) then a finite population correction factor must be used when calculating the standard error. 
* Assume the population size is large enough to apply the CLT.  
* Apply the finite population correction factor when estimating population variance. <br> finite population correction factor = N-n/N-1
* Calculating confidence interval for population mean, proportion and variance when the population is finite (use correction factor).

[NO PRACTICAL]