**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group: 10      |
|-----------------|
|J. Ty|   
|Kairos|   
|Luis|   
|Sayma|

# Table of Contents
1. [Introduction](#introduction)
2. [Assessment Using Reliability Growth Testing](#par1)
3. [Assessment Using Reliability Demonstration Chart](#par2)
4. [Comparison of Results](#par3)
5. [Discussion on Similarity and Differences of the Two Techniques](#par4)
6. [How the team work/effort was divided and managed](#par5)
7. [Difficulties encountered, challenges overcome, and lessons learned](#par6)
8. [Comments/feedback on the lab itself](#par7)


# Introduction<a name="introduction"></a>
In this lab, we explored and analyzed integration test data using different reliability assessment tools. More specifically, we looked at Reliability Growth Testing (RGT) and Reliability Demonstration Charts (RDC). Using these two methods, we analyzed the resulting graphs/data from various datasets. Our RGT analysis looked at algorithms such as Geometric and Littlewood and Varral’s Bayesian Reliability. Our RDC analysis looked at failure intensity objectives.

# Assessment Using Reliability Growth Testing<a name="par1"></a>

In order to perform Reliability Growth Testing, we used Dataset 1, and used the Geometric and Littlewood and Varral's Bayesian Reliability models to test the dataset twice.
All of the reliability growth testing was performed on `SRTAT`.

*Figures 1-3* below shows our results when using the Geometric Model.

*Figure 1: Geometric Model Result on Dataset 1*

![Alt text](/media/geomodel.png?raw=true "Geometric Model Result")

*Figure 2: Geometric Analysis on Dataset 1*

![Alt text](/media/geoanalysis.png?raw=true "Geometric Analysis")

*Figure 3: Geometric Prediction on Dataset 1*

![Alt text](/media/geoprediction.png?raw=true "Geometric Prediction")

*Figures 4-6* below shows our results when using the Littlewood and Varral's Bayesian Reliability Model.

*Figure 4: Littlewood and Varral's Bayesian Reliability Model Result on Dataset 1*

![Alt text](/media/lvmodel.png?raw=true "Littlewood and Varral's Bayesian Reliability Model Result")

*Figure 5: Littlewood and Varral's Bayesian Reliability Analysis on Dataset 1*

![Alt text](/media/lvanalysis.png?raw=true "Littlewood and Varral's Bayesian Reliability Analysis")

*Figure 6: Littlewood and Varral's Bayesian Reliability Prediction on Dataset 1*

![Alt text](/media/lvprediction.png?raw=true "Littlewood and Varral's Bayesian Reliability Prediction")

# Assessment Using Reliability Demonstration Chart<a name="par2"></a> 
In order to create a Reliability Demonstration Chart, we used Dataset 1 and used `SRTAT` to create the model.

*Figure 7: Reliability Demonstation Chart with Default MTTF*

![Alt text](/media/rdcorig.png?raw=true "RDC Default MTTF")

This RDC has a MTTF of the default value provided by the program. With this value the test data passes the reliability tests and do not need to be tested further.


*Figure 8: Reliability Demonstation Chart with Minimum MTTF*

![Alt text](/media/rdcmin.png?raw=true "RDC Min MTTF")

This RDC has a MTTF of the minimum value that is accepted. To find the failures per second to use to get the minimum MTTF, we first divided the normalized measure by the failure time, then since `normalized measure=failure time*failure/s` and `normalized measure=failure time/MTTF` we can find the MTTF by finding the inverse of  failure time. In our case this was *2.88/8*, leading to .36 failures per second, and a MTTF of 2.8.


*Figure 9: Reliability Demonstation Chart with Half the Minimum MTTF*

![Alt text](/media/rdchalf.png?raw=true "RDC Half MTTF")

This RDC has a MTTF of half the minimum value found. This causes the data to need to continue testing, as the failure data is betwee the *accept* and *reject* lines. We found the failures per second to use by halving the minimum MTTF.


*Figure 10: Reliability Demonstation Chart with Double the Minimum MTTF*

![Alt text](/media/rdcdouble.png?raw=true "RDC Double MTTF")

This RDC has a MTTF of double the minimum value found. This causes the data to still be accepted, as the failure data is past the *accept* line. We found the failures per second to use by doubling the minimum MTTF.

# Comparison of Results<a name="par3"></a>

Reliability Growth Testing (RGT) is able to show time elapsed from start of the system against the failure number. This allows us to predict approximately when the next failure is likely to occur. Based on the graph plotted by SRTAT, it would seem that the intervals between the failures are increasing, which could mean that the SUT is becoming increasingly reliable as time passes.

On the other hand, the Reliability Demo Chart (RDC) is able to show whether a failure intensity objective of the system under test has been met, based on cumulative failure observations. Based on the graph plotted by SRTAT, it would seem that the SUT is acceptable.

Both results are able to show that the SUT from dataset 1 is sufficiently reliable based on our group’s parameters. The actual acceptability of the SUT will ultimately depend on the customer’s reliability requirements.

# Discussion on Similarity and Differences of the Two Techniques<a name="par4"></a>

The similarity between the two techniques lies in the fact that both of them are able to give us insightful information in the form of graphs regarding the reliability of the SUT. Both techniques require a proper dataset of time between failures and failure count in order to generate the graphs.

The difference in the two techniques is that RGT is mainly used to graphically visualize how often the failures are happening, as well as predicting when the next failure is likely to occur; while RDC is able to definitely tell whether the SUT is acceptable based on the given parameters. These two techniques serve different functions in telling us the reliability of the SUT and should be used in tandem in order to draw useful conclusions of the SUT.

# How the team work/effort was divided and managed<a name="par5"></a>

Our team started off with all of us trying to convert the data files for the datasets. We then split into pairs and worked on the two parts of the assignment concurrently, where we analyzed the results of each method (RGT vs RDC) and summarized our findings for the group.

Overall, the work and effort was divided and managed equally amongst the group members.

# Difficulties encountered, challenges overcome, and lessons learned<a name="par6"></a>

The main difficulty encountered by the team is familiarizing ourselves with the SRTAT software. The software requires a certain formatted file type, which was not directly provided in the lab documents. This meant that we had to have a good understanding of the software in order to correctly format the documents to carry out with the rest of the lab. We managed to overcome this by reading up on SRTAT and comparing the given datasets with the sample datasets to ensure that the format is correct.

# Comments/feedback on the lab itself<a name="par7"></a>

Overall, the lab provided us with hands-on experience in testing the reliability of the SUT based on failure datasets. The skillset to generate models and graphs based on given datasets can be extremely helpful in our future careers as software engineers, since various reliability tests will be carried out on SUT.

