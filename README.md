# Computational Political Science

Spring 2021  
david.broska\@zu.de

### Course Information

Classes on Tuesdays 16:30-19:00 (Big Blue Button link on [ILIAS](https://learning.zu.de/goto.php?target=crs_19944&client_id=ilias))

| Session |  Date  | Topic                                                  |               Assignment               |
|:-------:|:------:|:-------------------------------------------------------|:--------------------------------------:|
|    1    | Feb 02 | [Overview and key concepts](#session-1)                |                   \-                   |
|    2    | Feb 09 | [Preprocessing and descriptive statistics](#session-2) |   [Formative](#formative-assignment)   |
|    3    | Feb 16 | [Dictionary methods](#session-3)                       |                   \-                   |
|    4    | Feb 23 | [Machine learning (for texts)](#session-4)             | [Summative 1](#summative-assignment-1) |
|    5    | Mar 02 | [Supervised scaling models for texts](#session-5)      |                   \-                   |
|    6    | Mar 09 | [Unsupervised scaling models for texts](#session-6)    | [Summative 2](#summative-assignment-2) |
|    7    | Mar 16 | [Similarity and clustering](#session-7)                |                   \-                   |
|    8    | Mar 23 | [Topic models](#session-8)                             | [Summative 3](#summative-assignment-3) |
|   \-    |   \-   | *Break*                                                |                   \-                   |
|    9    | Apr 13 | [Retrieving data from the web](#session-9)             |                   \-                   |
|   10    | Apr 20 | [Published applications](#session-10)                  |                   \-                   |
|   11    | Apr 27 | [Project Presentations](#session-11)                   |                   \-                   |

### Course Description

Digital technologies and the relentless shift towards digital modes of communication bring fundamental changes to societies. This transformation challenges the integrity of privacy and information on the web, stipulates regulatory oversight, and necessitates decision-makers to find ways in which technological change can broadly benefit society. For social scientists, these and related topics create fascinating lines of inquiry.

However, the digital transformation does not only create new research topics. The increase in computing power, online communication, and the abundance of data also expands the ways in which we study social phenomena. This course provides an overview of useful quantitative methods to collect and analyze data from online resources.

For example, participants gain hands-on experience with computer-assisted data collection (web scraping) and the use of databases with SQL. In line with the burgeoning interest of political scientists in natural language processing, we also cover methods to analyze large text corpora. These techniques include, but are not limited to, extracting features of texts such as content categories, word counts, dictionary counts, or parts of speech. Statistical methods are used to draw inferences about the texts or their authors. Political scientists have used those methods to track public opinion on social media, reveal censorship through government agencies, or infer political ideology from speeches and party manifestos.

This course does not solely focus on the application of methods. We will also discuss the advantages and caveats of the above techniques to build an intuition for assessing their respective strengths, weaknesses, and trade-offs. This will be done by studying applications of the above-mentioned methods in published academic work exploring various sociopolitical phenomena.

There are no strict prerequisites for this course but basic R programming skills - or the eagerness to learn - are expected. For applications in quantitative text analysis, we will use the [quanteda](https://quanteda.io/) package for R.

### Assessment

The overall goal of this course is to let participants enrich their methodological repertoire and strengthen their skills in conducting computational social science research. Participants will therefore be responsible for carrying out their own small-scale research project on a topic of their interest using some of the methods presented in this course. Three coding assignments are intended to lay the foundation for the final project: participants practice the creation and analysis of textual data using content analytic and statistical software.

-   Project (70%)
-   Assignments (30%)

### Resources

-   [base R cheat sheet](https://rstudio.com/wp-content/uploads/2016/05/base-r.pdf)
-   [quanteda cheat sheet](https://muellerstefan.net/files/quanteda-cheatsheet.pdf)
-   [regular expressions in R cheat sheet](https://rstudio.com/wp-content/uploads/2016/09/RegExCheatsheet.pdf)

### Credits

I am indebted to Prof. Kenneth Benoit, Dr. Pablo Barbará, and Dr. Blake Miller who developed an introductory course for quantitative text analysis at the London School of Economics. I also thank Dr. David Zimmerman for preparing an excellent introduction to programming in R. I have adapted a large proportion of these materials for the Computational Political Science course.

------------------------------------------------------------------------

## Schedule

### Session 1

**Overview and key concepts**

We will familiarize ourselves with the key themes and concerns of the seminar, discuss organizational aspects of the course, and start thinking about the promises of computational methods. There is no mandatory reading for this session but you can look into the following articles to get an overview of some of the key themes of this course.

*Reading:*

-   Lazer, D., A. Pentland, L. Adamic, S. Aral, A.-L. Barabasi, D. Brewer, N. Christakis, et al. 2009. "Computational Social Science." *Science* 323 (5915): 721–23. <https://doi.org/10.1126/science.1167742>.
-   Grimmer, Justin, and Brandon M. Stewart. 2013. "Text as Data: The Promise and Pitfalls of Automatic Content Analysis Methods for Political Texts." *Political Analysis* 21 (3): 267–97. <https://doi.org/10.1093/pan/mps028>.

------------------------------------------------------------------------

### Session 2

**Preprocessing and descriptive statistics**

This session introduces methods for characterizing and comparing texts by statistical measures. We will also cover common techniques for preparing textual data for quantitative analyses. This will be followed by a coding session in which participants have the opportunity to apply the methods presented before.

Please download and install base [R](https://cran.microsoft.com/) and [RStudio](https://rstudio.com/products/rstudio/download/) Desktop before this session. This [tutorial](https://www.datacamp.com/community/tutorials/installing-R-windows-mac-ubuntu) provides instructions on installing the software.

If you haven't done so already, please make sure to install the following R packages through `install.packages(c("quanteda","stringr", "ggplot2"))`. Please contact me in advance if you run into technical problems. I'm happy to help.

#### Formative Assignment

This assignment does *not* count towards the final degree. Instead, it is meant to give you an opportunity to familiarize yourself with the questions and the structure of the assignments in the following weeks. You can work on this assignment on your own or in teams of two. If you submit the assignment you will be provided with feedback. Please send the .Rmd file and the compiled .html document to david.broska\@zu.de.

**Deadline**: Feb 22, 23:59:59

------------------------------------------------------------------------

### Session 3

**Dictionary methods**

Dictionary methods allow researchers to link words in a document with a concept of interest. This session introduces the idea behind dictionary methods, means to test their validity, and guidelines for refinement.

During the practical part of this session, we will apply commonly used dictionaries to conduct sentiment analyses.

*Reading:*

-   Hancock, Jeffrey T., David I. Beaver, Cindy K. Chung, Joey Frazee, James W. Pennebaker, Art Graesser, and Zhiqiang Cai. 2010. "Social Language Processing: A Framework for Analyzing the Communication of Terrorists and Authoritarian Regimes." Behavioral Sciences of Terrorism and Political Aggression 2 (2): 108–32. <https://doi.org/10.1080/19434471003597415>.

------------------------------------------------------------------------

### Session 4

**Machine learning for texts: Classification I**

This session offers an introduction to machine learning methods for texts, particularly for classifying documents. We will discuss the Naive Bayes model which is one of the most popular classifiers.

Hands-on work gives participants the opportunity to apply the Naive Bayes classifier in R.

*Reading:*

-   Evans, Michael, Wayne McIntosh, Jimmy Lin, and Cynthia Cates. 2007. "Recounting the Courts? Applying Automated Content Analysis to Enhance Empirical Legal Research." *Journal of Empirical Legal Studies* 4 (4): 1007–39. <https://doi.org/10.1111/j.1740-1461.2007.00113.x>.

#### Summative assignment 1

The first summative assignment will be released after Session 4 and amounts to 10% of the overall grade for the course. You are expected to work on this assignment on your own. Please send the .Rmd file and the compiled .html document to david.broska\@zu.de.

**Deadline**: Mar 08, 23:59:59

------------------------------------------------------------------------

### Session 5

**Machine learning for texts: Classification II**

Building on our knowledge about classification methods, we will discuss ways to evaluate the performance of classifiers. In particular, we look at precision, recall, accuracy, and F1. 

We will also introduce regularization for quantitative text analysis, particularly Lasso and Ridge regression.

The computer exercise is about classifying names using Naive Bayes and Lasso regression.


------------------------------------------------------------------------

### Session 6

**Supervised and unsupervised scaling models for texts**

In this session, we will build upon the Naive Bayes classifier and introduce the Wordscores method of Laver, Benoit, and Garry (2003) for scaling latent characteristics.

We will also discuss unsupervised methods based on parametric (Wordfish) and non-parametric approaches (Correspondence analysis).

During the computer exercise, we scaling methods from the quanteda package to place political texts on an ideological scale.

*Reading:*

-   Laver, Michael, Kenneth Benoit, and John Garry. 2003. "Extracting Policy Positions from Political Texts Using Words as Data." *American Political Science Review* 97 (2): 21.
-   Lowe, Will, and Kenneth Benoit. 2013. "Validating Estimates of Latent Traits from Textual Data Using Human Judgment as a Benchmark." *Political Analysis* 21 (3): 298–313. <https://doi.org/10.1093/pan/mpt002>.



#### Summative assignment 2

The second summative assignment will be released after Session 6 and amounts to 10% of the overall grade for the course. You are expected to work on this assignment on your own. Please send the .Rmd file and the compiled .html document to david.broska\@zu.de.

**Deadline**: Mar 15, 23:59:59

------------------------------------------------------------------------

### Session 7

**Similarity and clustering**

In this session, we will look at metrics to quantify the distance and similarity between documents. We will also introduce hierarchical and k-means clustering for textual data.

During the computer exercise, we will use these methods to build a basic recommendation engine for movies. We will also identify similar political speeches using clustering techniques.

------------------------------------------------------------------------

### Session 8

**Topic models**

Topic models are machine learning techniques that provide a systematic framework to analyze large sets of unstructured textual data. By constructing clusters of words, this method allows researchers to identify topics in a collection of texts. Topic models can also be used as a classifier to automatically sort documents into a set of categories.

During the practical part of the session, we will learn how to use the Latent Dirichlet Allocation (LDA) model and the Structural Topic Model (STM).

*Reading:*

-   Blei, David M. 2012. "Probabilistic Topic Models." *Communications of the ACM* 55 (4): 77–84. <https://doi.org/10.1145/2133806.2133826>.

-   Roberts, Margaret, Brandon Stewart, Dustin Tingley, Christopher Lucas, Jetson Leder-Luis, Shana Kushner Gadarian, Bethany Albertson, and David G. Rand. 2014. "Structural Topic Models for Open-Ended Survey Responses." *American Journal of Political Science* 58 (4): 1064–82.

#### Summative assignment 3

The third summative assignment will be released after Session 8 and amounts to 10% of the overall grade for the course. You are expected to work on this assignment on your own. Please send the .Rmd and the compiled .html document to david.broska\@zu.de.

**Deadline**: Apr 12, 23:59:59

------------------------------------------------------------------------

### Session 9

**Retrieving data from the web**

In this session, we will cover techniques to turn web data into text or numbers, also known as web scraping. We will learn how to retrieve data via APIs, scrape documents in XML, and parse content from websites with non-static components with Selenium.

------------------------------------------------------------------------

### Session 10

**Published applications**

At this point, the course will have covered some of the most widely used techniques for quantitative text analysis. In this session, we will be discussing applications of these methods in published academic work. The goal is to strengthen our intuition for assessing their respective strengths, weaknesses, and trade-offs.

The literature discussed in this session is also meant to inspire participants for their final projects. Please feel free to suggest published applications of the methods covered in this course that you find particularly interesting and worth discussing in greater detail.

*Reading:*

-   Schwemmer, Carsten, and Sebastian Jungkunz. 2019. "Whose Ideas Are Worth Spreading? The Representation of Women and Ethnic Groups in TED Talks." *Political Research Exchange* 1 (1): 1–23. <https://doi.org/10.1080/2474736X.2019.1646102>.

-   Karell, Daniel, and Michael Freedman. 2019. "Rhetorics of Radicalism." *American Sociological Review* 84 (4): 726–53. <https://doi.org/10.1177/0003122419859519>.

------------------------------------------------------------------------

### Session 11

**Project Presentations**

During this session, participants will be asked to give a brief presentation on their proposed course project. This presentation does not count towards the final degree. Instead, it is meant to be an opportunity to get informal feedback from your peers. The audience might also be helpful in resolving difficulties that may arise, be they related to your research topic, data collection, or methods for analysis.

Participants are encouraged to be as specific as possible about their research topic, relevant literature, and the research question (or the set questions) that the proposed research project is expected to answer. To convince your audience about the feasibility of the project, it is advisable to identify potential sources for data collection and appropriate methods for analysis.
