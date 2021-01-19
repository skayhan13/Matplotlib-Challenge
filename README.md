# Matplotlib-Challenge

## Background- The Power of Plots

What good is data without a good plot to tell the story?

So, let's take what you've learned about Python Matplotlib and apply it to a real-world situation and dataset:

While your data companions rushed off to jobs in finance and government, you remained adamant that science was the way for you. Staying true to your mission, you've joined Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. You have been tasked by the executive team to generate all of the tables and figures needed for the technical report of the study. The executive team also has asked for a top-level summary of the study results.

## Instructions

Your tasks are to do the following:

* Before beginning the analysis, check the data for any mouse ID with duplicate time points and remove any data associated with that mouse ID.

* Use the cleaned data for the remaining steps.

* Generate a summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

* Generate a bar plot using both Pandas's `DataFrame.plot()` and Matplotlib's `pyplot` that shows the total number of measurements taken for each treatment regimen throughout the course of the study.

  * **NOTE:** These plots should look identical.  Please consult the images folder for all .png's of the plots created.

* Generate a pie plot using both Pandas's `DataFrame.plot()` and Matplotlib's `pyplot` that shows the distribution of female or male mice in the study.

  * **NOTE:** These plots should look identical.

* Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Calculate the quartiles and IQR and quantitatively determine if there are any potential outliers across all four treatment regimens.

* Using Matplotlib, generate a box and whisker plot of the final tumor volume for all four treatment regimens and highlight any potential outliers in the plot by changing their color and style.

  **Hint**: All four box plots should be within the same figure. Use this [Matplotlib documentation page](https://matplotlib.org/gallery/pyplots/boxplot_demo_pyplot.html#sphx-glr-gallery-pyplots-boxplot-demo-pyplot-py) for help with changing the style of the outliers.

* Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

* Generate a scatter plot of mouse weight versus average tumor volume for the Capomulin treatment regimen.

* Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. Plot the linear regression model on top of the previous scatter plot.

* Look across all previously generated figures and tables and write at least three observations or inferences that can be made from the data. Include these observations at the bottom of notebook.

Here are some final considerations:

* You must use proper labeling of your plots, to include properties such as: plot titles, axis labels, legend labels, _x_-axis and _y_-axis limits, etc.

* See the [starter workbook](Pymaceuticals/pymaceuticals_starter.ipynb) for help on what modules to import and expected format of the notebook.

* In the very last cell of the notebook you will find the following in markdown format:

* Data Analysis Findings:
1. Based on the "Summary Statistics" Dataframe we can draw some assumptions about the drug regimen, Capomulin.  Capomulin has results with the lowest standard deviation meaning that it captured findings closest to a normal distribution. Capomulin also delievered the most promising results of the mouse trial as it shrunk the tumor volume more than any other drug regimen.

2. There appears to be a positive correlation between a mouse's weight and the tumor volume.  This correlation can prove that the two entities appear to be directly proportional.  I use the word "appear" as opposed to "is" because there are a few points that do not lie on the linear regression line, and the r-squared value is 0.70.  The closer the r-squared value is to 1, then the better fit the regression line is said to be.  This idea of weight and tumor volume sharing a directly proportional relationship does intuitively make sense, and I was expecting to see this correlation before starting my data anaylsis.

3. Finally, the two most tested drugs in this trial were: Capomulin and Ramicane. This helps to explain why these two drug regimens experienced nearly identical mean and median values, and the lowest standard deviations.  They had the most occurences of being tested.  A conclusion that can be drawn from this fact and studied further is whether these two drug regimens had more funding in comparison to the other regimens. Data on funding would need to be provided to us in order to conduct this analysis.
