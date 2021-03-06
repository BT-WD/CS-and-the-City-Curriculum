# Bias

## Learning Objectives

* SWBAT examine the ways in which data can be misused in presentation and analysis.
* SWBAT critique the intentional misuse of data.
* SWBAT recognize the unintentional misuse of data.

## Sequence

1. [Launch](#launch)
2. [Case Study 1: Bias in Reporting](#case-study-1-bias-in-reporting)
3. [Case Study 2: Bias in Interpretation](#case-study-2-bias-in-interpretation)
4. [Case Study 3: Bias in Visualization](#case-study-3-bias-in-visualization)
5. [Close](#close)

## Launch

> In this, and in many lessons throughout this unit, there may be occasion to include content warnings for students, or to swap out news sources provided for some that feel more tailored to your students' interests and emotional readiness to discuss certain topics. You know your students, and you know what level of seriousness/intensity is going to best benefit them.

**Discuss: What is an unemployment rate? Is it better for a state to have a low or high unemployment rate?**

**Follow-up: If a state has low unemployment, is it reasonable to suppose that the people who live in that state are happier (on average)?**

Consider the following Facebook post and excerpt from a [news article in the _Tennessean_ newspaper](https://www.tennessean.com/story/news/2017/07/20/tennessees-unemployment-rate-last-month-lowest-state-history-gov-bill-haslam-announced-thursday/496383001/) from 2017:

| Facebook Post |
| --- |
| <h3>Tennessee continues to be a great place to do business, and I am proud of all our state has done to create an environment for job growth.</h3><h5>--Sen. Bob Corker, TN</h5> |

| Tennessean Excerpt |
| --- |
| <h3>Haslam: June featured lowest unemployment rate in Tennessee history</h3><h5>Tennessee's unemployment rate last month was the lowest in state history, Gov. Bill Haslam announced Thursday.</h5><h5>The state had a preliminary seasonally adjusted unemployment rate of 3.6 percent in June.</h5><h5>[...]</h5><h5>Haslam said the unemployment figures came after decisions made by his administration and the state legislature. "We honestly think this is a result of the policies put in place by the state of Tennessee and the General Assembly," he said.</h5><h5>The state's previous low for unemployment rate was 3.7 percent in March 2000.</h5> |

#### Discussion Questions

- How would you describe each author's intent for writing their post/article?
- How is each author using their language to impact the reader's response?
- What data is each author including or not including that might impact the reader's response?
- What other data might be relevant for making a decision whether or not the post and excerpt are meaningful?

#### Additional Information

Now consider the following chart that shows the percent of each state's workers who are paid at or below minimum wage:

![Workers Paid At or Below Minimum Wage](./images/percent-min-wage.png)

- How could Tennessee's rank in this list contradict the analysis made by the _Tennesseean_?
- Does this data sufficiently disprove Sen. Corker's assertion that "Tennessee continues to be a great place to do business" and that Tennessee has "create[d] an environment for job growth"? Is it possible that this could still be a great place to work, even with this new information?
- How does this data complicate the _Tennessean_'s conclusions about the state's unemployment rate?
- Can you come up with a way to describe the employment situation in Tennessee that can encompass BOTH the low unemployment and the high percentage of employed workers making less than minimum wage?
- After learning this new information, what questions do you still have?

One conclusion might be that even though the state's unemployment rate is lower than it has been before, the types of jobs created in Tennessee may not be viable options for some individuals or families, since so many jobs are at or below minimum wage. With that context, it is possible to disagree with the Senator's conclusion that this is a great place to work. 

However, another conclusion is possible: We don't have *historical* data for minimum wage jobs in Tennesse - those numbers could be going down too, meaning more workers are working their way out of the minimum wage bracket. Additionally, these articles also don't say anything about the cost of living in Tennessee when compared to other locations - it could be that minimum wage in Tennessee affords someone a very different day-to-day life than it would in NYC. 

This is an example of selection bias: the senator and the newspaper each had a story they wanted to tell and chose data that supports the point the want to make. In this case, that point may just be "Tennessee is a great place for jobs!" but you, the reader, bear the responsibility to decide whether the data they present is enough information to support their point. It's also the reader's responsibility to look at the other dat given (for example, in the comments section) to determine 

#### Additional Reading

- Based on this [Quora discussion about political spin](https://www.quora.com/Whats-an-example-of-a-misleading-political-spin).

## Types of Bias in Data Science

*Bias* means believing what you want to believe and refusing to take into consideration the opinions of others. In data science, bias can manifest in a few ways:

1. *Confirmation bias* is when you either intentionally or subconsciously only pay attention to data which proves a pre-determined conclusion.
2. *Selection bias* is the group of people surveyed do not accurately reflect the larger population that a researcher assumes they do.
3. *Ignored Outliers* can introduce bias if a dataset has a few datapoints that are uncharacteristically different from most; in this case, average values can be skewed.
4. *Confounding variables* can add unintentional bias when there's something missing from the dataset that influences both the independent and dependent variables. These connections can cause a researcher to assume a cause-and-effect relationship where there isn't one.
5. *Correlation is not causation.* Just because two things follow the same trend doesn't necessarily mean one causes the other. [Spurious Correlations](https://www.tylervigen.com/spurious-correlations) has some good examples of absurd but true correlations to help prove that point.
6. *Overfitting (and underfitting)* can lead to an overly-complicated (or overly-simplistic) model to represent the data - we can examine this more closely later.

## Case Study 1: Bias in Reporting

Optional framing questions: 
- If you own something, should you be able to sell it for any price you want?
- If someone needs that thing to survive, does that change your answer?

| Passage A: ["Martin Shkreli faces antitrust suit over raising drug price 4,000%"](https://www.latimes.com/business/story/2020-01-27/martin-shkreli-sued-by-ftc-over-daraprim-drug-price) - LA Times |
| --- |
|"Pharma bro" Martin Shkreli was sued Monday by U.S. officials and the state of New York, who are accusing him of violating antitrust law when he jacked up the price of a crucial drug by 4,000% overnight in 2015.... <br> <br> The allegations are separate from what landed Shkreli behind bars, though the drug at the center of the case is the same. He???s in prison serving a seven-year sentence for defrauding investors in hedge funds he ran by lying to them about his track record and performance ??? as well as for a fraud scheme involving Retrophin Inc., a company he founded in 2011.|

| Passage B: ["???Pharma Bro??? Martin Shkreli Must Face Antitrust Suit for Now"](https://news.bloomberglaw.com/mergers-and-antitrust/pharma-bro-martin-shkreli-must-face-antitrust-suit-for-now) -  |
| --- |
|Martin Shkreli failed to convince a federal judge to dismiss an antitrust lawsuit against him April 10, about a week after reports that the imprisoned ???pharma bro??? had been placed in solitary confinement. <br> <br> Shkreli, Retrophin Inc., and two related companies are facing claims that they unlawfully shielded the blockbuster kidney drug Thiola from competition by refusing to put out samples that competing pharmaceutical companies must use, under federal law, to demonstrate the ???bioequivalence??? of their generics. <br> <br>They will now have to undergo 90 days of limited discovery to determine whether plaintiff Spring Pharmaceuticals LLC has standing to sue by virtue of the investment it made preparing to develop a generic Thiola rival, according to the ruling by Judge J. Curtis Joyner of the U.S. District Court of the Eastern District of Pennsylvania.|

#### Discussion Questions
- What facts/data/information were included in Passage A that were not included in Passage B?
- How does the inclusion / omission of these facts influence how a reader might feel about Martin Shkreli?
- Either of these ways of reporting the information that Martink Shkreli is being sued could be considered accurate:
	- Make a case for why Passage A is more accurate.
	- Make a case for why Passage B is more accurate.
- Now that we've considered the facts/data/information, how do specific word choices (adjectives, etc) in each article might influence the reader's opinion of Shkreli?
- After thinking over both cases, which do you think is the more unbiased reporting?

## Case Study 2: Bias in Interpretation

When we interpret data, we can "spin" data in quite a few ways:
> Many people will be familiar with the concept of "spin"; in popular culture, spin is "a form of propaganda to influence public opinion" (Esquire 1996;126:70), more specifically "the manipulation of language to convince the reader of the likely truth of the result." (BMJ 1995;310:985???7)

1. *Confirmation bias* (mentioned above in a slightly different context) is evaluating evidence that supports one's preconceptions differently from evidence that challenges these convictions.
2. *Rescue bias* is discounting data by finding selective faults in the experiment.
3. *"Time will tell" bias* is the phenomenon that different scientists need different amounts of confirmatory evidence.
4. *Orientation bias* is the possibility that the hypothesis itself introduces prejudices and errors and becomes a determinate of experimental outcomes.
5. *Auxiliary hypothesis bias* is introducing ad hoc modifications to imply that an unanticipated finding would have been otherwise had the experimental conditions been different.
6. *Mechanism bias* is being less skeptical when underlying science furnishes credibility for the data.

> This list is probably more comprehensive than necessary for students - feel free to narrow to the first three or four.

The following [two passages](https://www.business2community.com/government-politics/celebrating-2016-elections-history-political-spin-01672605) about a certain political candidate's great uncle are examples of a type of political spin. Each is selective about how it frames the story in order to achieve its intended outcome.

| Passage A |
| --- |
| <h5>His great-great uncle was hanged for horse stealing and train robbery in the late 1880s. He was first captured as a horse thief, but then he escaped incarceration and went on to rob trains. He was eventually re-captured and was ultimately put to death by hanging.</h5> |

| Passage B, Rewritten by the candidate's political staffers |
| --- |
| <h5>His great-great uncle was a famous cowboy in the Montana Territory. His business empire grew to include acquisition of valuable equestrian assets and intimate dealings with the Montana railroad. Beginning in 1883, he devoted several years of his life to government service, finally taking leave to resume his dealings with the railroad. In 1887, he was a key player in a vital investigation. In 1889, he passed away during an important civic function held in his honor when the platform upon which he was standing collapsed.</h5> |

#### Discussion Questions

- How do the authors' interpretations of the historical record differ?
		- What does "acquisition of valuable equestrian assets" mean in context?
		- What does "years... of governmental service" mean in context?
		- What "civic function" was "held in his honor" at the end of the excerpt?
- What would each author want the reader to think about the subject's great-great uncle?
- The fundamental data of this story is the same in both excerpts - what does this tell you about the importance of word choice in analysis?

Sometimes people interpret data differently, and that can be okay. However, if those interpretations don't also recognize the effects of inherent biases, the reader is required to make a critique of the biases which might be affecting how an author has come to their conclusions.

## Case Study 3: Bias in Visualization

Consider the three sets of data visualizations below. Each pair represents the same information.

#### Discussion Questions

- Why did the person making each of these graphs choose to represent the data the way they have?
- What message do you think that person was trying to communicate by making those choices?
- Which do you think is more biased? more unbiased?


| Visualization A | Visualization B |
| :---: | :---: |
| ![Interest Rates](./images/zbl-3.png) | ![Interest Rates](./images/zbl-4.png) |

| Visualization A | Visualization B |
| :---: | :---: |
| ![Election Map](./images/election-map-0.png) | ![Election Map](./images/election-map-1.jpg) |

| Visualization A | Visualization B |
| :---: | :---: |
| ![Gun Deaths](./images/gun-deaths-0.jpg) | ![Gun Deaths](./images/gun-deaths-1.jpg) |

#### Additional Discussion Questions

Notice that each of these pairs of visualizations represents the same data in two different ways. 
- Is there a pair among these three pairs that seems to provide two *equally helpful* ways of visualizing information?
- Are any of the six visualizations particularly *helpful* in conveying useful information?
- Are any of the six visualizations particularly *unhelpful* in conveying information?
- Do any of the six visualizations appear to be *intentionally* misleading?

## Close

Bias is complicated. It can be intentional or unintentional; it can be hidden or it can be overt. Bias is usually dangerous and harmful, but it can be incredibly difficult to get away from our own biases. Bias can be a weapon to accomplish specific ends, and bias can cause us to think narrowly.

- What are your biases?
- How can you ensure that your biases don't negatively affect your interpretation of data?
- Are there cases or situations where a certain amount of bias is healthy or helpful?
		- If you agree, present those situations/scenarios to the class. When does the bias cease to be healthy or helpful?
		- If you disagree, how would you respond to your classmates' scenarios?
