<h1><b><font color="#cc0000"><i>AB_testing</i></font></b></h1>





<h1>1- Overview and business problem</h1>

<br>
<p><font size="3">A/B testing is a controlled experiment in which two or more variants of a given condition are randomly presented to different groups of individuals, with the goal of determining which variation produces the best response or outcome. It is commonly used in computer science, psychology, marketing, and other areas to test the effectiveness of different versions of a product, message, or treatment.</br>
    
In this project, A/B testing will be applied to evaluate two distinct scenarios: conversion rate evaluation and gross revenue evaluation.</font></p>

<br>
<ol>
   <li><font size="3"><i>Evaluating conversion rate</i>
     <br><br>Conversion rate is a metric that measures the percentage of website visitors or marketing campaign participants who perform a desired action, such as making a purchase, filling out a form, or signing up for a newsletter. It is an important indicator for evaluating the effectiveness of a marketing or sales strategy. In this session, the main objective is to evaluate the difference between two web pages (A and B) from the perspective of the conversion rate.<br></font></li>
    <p><font size="3">The current conversion rate of the main page A is 12%. Therefore, it is proposed to test a challenger page B that could increase the website's conversion rate and, consequently, increase revenue. For page B to be considered successful in the test, it is expected to have a conversion rate of 14%. However, it is necessary to validate this hypothesis from the point of view of the experimentally collected data.</font></p>
      
   
  <li><font size="3"><i>Evaluating gross revenue</i>
     <br><br>Gross revenue is the total value of a company's sales before subtracting costs, expenses, and taxes. It is the total revenue obtained by the company from the sale of its products or services. It is important to note that gross revenue does not represent the net profit of the company, as it does not take into account the necessary deductions for calculating this indicator. In this session, the main objective is to evaluate the difference between two business strategies (A and B) from the perspective of gross revenue.<br></font></li>
    <p><font size="3">Strategy A presents an average gross revenue that is different in each of the countries where the test was conducted. Therefore, it is proposed to test a challenger strategy B that could increase the company's gross revenue. For strategy B to be considered successful in the test, it is expected to provide a 63% increase in gross revenue. However, it is necessary to validate this hypothesis from the point of view of the experimentally collected data.</font></p>
</ol>



<h1>2- Assumptions</h1>

<br>
<p><font size="3">The following are some of the key assumptions for A/B testing.</font></p></br>
<ol>
  <li><font size="3">Random assignment: Participants in the A/B test must be randomly assigned to either the control group (version A) or the treatment group (version B) to ensure that the groups are comparable in terms of their characteristics.</font></li><br>
  <li><font size="3">Large sample size: The larger the sample size, the more reliable the results of the A/B test will be. A larger sample size also helps to reduce the impact of outliers or random fluctuations in the data.</font></li><br>
  <li><font size="3">Independence of observations: The observations in the A/B test should be independent of each other, meaning that the behavior of one participant should not influence the behavior of another participant.</font></li><br>
  <li><font size="3">Normality of data: The data should be normally distributed to allow for valid statistical tests to be conducted. If the data is not normally distributed, a non-parametric test may be used instead.</font></li><br>
  <li><font size="3">Homogeneity of variance: The variance of the data in the control and treatment groups should be roughly equal. If the variances are significantly different, this can affect the results of the statistical tests and make it harder to draw meaningful conclusions.</font></li><br>  
</ol>





<h1>3- Data description</h1>

<br>
<ol>
   <li><font size="3"><i>Evaluating conversion rate</i>
     <br><br>The tabular dataset used for evaluating gross revenue has the following descriptors:<br></font></li><br>
<ul>
  <li><font size="3"><b>user_id - </b>Unique user identifier.</font></li><br>
  <li><font size="3"><b>timestamp - </b>Data of data collection.</font></li><br>
  <li><font size="3"><b>group - </b>Group to which the user was assigned in the experiment (control or treatment).</font></li><br>
  <li><font size="3"><b>landing_page - </b>The page that was chosen for display to the user (old_page and new_page). It is dependent on the group (control or treatment).</font></li><br>
  <li><font size="3"><b>converted - </b>Indicates whether the user converted or not (0 or 1).</font></li><br>
</ul>
   <li><font size="3"><i>Evaluating gross revenue</i>
     <br><br>The tabular dataset used for evaluating gross revenue has the following descriptors:<br></font></li><br>
<ul>
  <li><font size="3"><b>uid - </b>Unique user identifier.</font></li><br>
  <li><font size="3"><b>country - </b>Corresponding country of the user.</font></li><br>
  <li><font size="3"><b>gender - </b>Gender of the user (M or F)..</font></li><br>
  <li><font size="3"><b>spent - </b>Gross revenue generated by the user (in a specific currency).</font></li><br>
  <li><font size="3"><b>purchases - </b>Number of purchases made by the user.</font></li><br>
  <li><font size="3"><b>date - </b>Date of data collection (ranging from 2015-01 to 2019-01)..</font></li><br>
  <li><font size="3"><b>group - </b>Group to which the user was assigned in the experiment (control or treatment).</font></li><br>
  <li><font size="3"><b>device - </b>Device used by the user (Internet or App).</font></li><br>  
</ul>
</ol>


<h1>4- Solution strategy</h1>

<ol>
   <li><font size="3"><i>Evaluating conversion rate</i><br></font></li><br>
<ol>
  <li><font size="3">Initial data check, verification of NAs, duplicate data, unique IDs, conversion of data formats, correct correspondence between landing page and group.</font></li><br>
  <li><font size="3">Calculation of sample size based on the evaluated KPI and the values for group A and the expected value for group B.</font></li><br>
  <li><font size="3">Hypothesis testing (frequentist) on the resulting dataset from the calculated sample size.</font></li><br>
  <li><font size="3">Bayesian test on the dataset provided for the experiment..</font></li><br>
  <li><font size="3">Comparison between frequentist test and Bayesian test..</font></li><br>
</ol>
   <li><font size="3"><i>Evaluating gross revenue</i><br></font></li><br>
<ol>
  <li><font size="3">Initial data check, verification of NAs, duplicate data, unique IDs, conversion of data formats, correct correspondence between landing page and group.</font></li><br>
  <li><font size="3">Calculation of sample size based on the evaluated KPI and the values for group A and the expected value for group B.</font></li><br>
  <li><font size="3">Checking the distribution of the data.</font></li><br>
  <li><font size="3">Hypothesis test (frequentist) conducted by country..</font></li><br>
  <li><font size="3">Bayesian test, also performed by country.</font></li><br>
  <li><font size="3">Comparison of frequentist test vs Bayesian test.</font></li><br>
</ol>
</ol>



<h1>5- Statistical tests applied</h1>

<ol>
   <li><font size="3"><i>Evaluating conversion rate</i><br></font></li><br>
<ul>
  <li><font size="3">Chi-square</font></li><br>
  <li><font size="3">Binary Bayesian test</font></li><br>
</ul>
   <li><font size="3"><i>Evaluating gross revenue</i><br></font></li><br>
<ul>
  <li><font size="3">Shapiro test</font></li><br>
  <li><font size="3">Kolmogorov-Smirnov</font></li><br>
  <li><font size="3">Mann-Whitney test</font></li><br>
  <li><font size="3">Welch's test</font></li><br>
  <li><font size="3">t test</font></li><br>
  <li><font size="3">t test unequal variances</font></li><br>
  <li><font size="3">DeltaLognormal DataTest</font></li><br>
</ul>
</ol>    
    
    
    
    
<h1>6- Results</h1>

<br>
<ol>
   <li><font size="3"><i>Evaluating conversion rate</i>
     <br><br>The figure below shows the results for the conversion rate evaluation from the frequentist (chi-square) and Bayesian (binary) tests perspective. The respective tests were applied to the same dataset as the experiment time progressed (y-axis) and the sample size increased.<br></font></li>
    <p><font size="3">From the chi-square test perspective, it was not possible to observe a significant p-value as the experiment time advanced, while in the Bayesian test, it is possible to notice, a few days before the experiment is concluded, that the challenger page B does not perform better than page A in terms of conversion rate. Therefore, it would be possible to terminate the experiment in less time compared to the frequentist test, saving resources for the organization.</font></p>

<img src="https://drive.google.com/uc?export=view&id=1iF1x4nqH1id81ihulq-zSiHCq5j98yyM" style="width: 650px; max-width: 100%; height: auto" title="Click to enlarge picture" />   
   
    
    
    
  <li><font size="3"><i>Evaluating gross revenue</i>
     <br><br>Since there are several countries in the revenue evaluation dataset, Spain was chosen to display the comparative image between the frequentist and Bayesian tests.<br></font></li>
    <p><font size="3">The figure on the left shows a trend of the p-value staying below 0.05 as the experiment progresses, indicating that from that point onwards there are significant differences between business strategies A and B. On the other hand, the figure for the Bayesian test on the right shows the high risk associated with stating that strategy A is less than B, represented by the dotted blue line, while the dotted yellow line represents the lower risk of stating that strategy B is better than A. It can be observed that, over the course of the experiment, this risk tends to decrease more when compared to the risk of stating that strategy A is better.</font></p>
</ol>


<img src="https://drive.google.com/uc?export=view&id=1Z0MvOtofB10ciZtfBLmcdfxT6TO8ZUbn" style="width: 650px; max-width: 100%; height: auto" title="Click to enlarge picture" />




<h1>7- Conclusions</h1>

<br>
<p><font size="3">Text here.</font></p>
<br>

    
    
