# The most effective drug regimen for squamous cell carcinoma (*Challenge 5*)

This repository contains the analysis of a study of 10 treatments for squamous cell carcinoma (SCC), a common form of skin cancer, in 248 mice.

## Authors

Daniel Ramón Murillo Antuna: [@daniel-r-murillo-antuna](https://www.github.com/daniel-r-murillo-antuna)

## Repository and project description

The effectiveness of anti-cancer medications is one of the most important topics in the pharmaceutical industry. In this mini-project, I pretended to be a senior data analyst for the fictional company Pymaceuticals, Inc, which specialises in anti-cancer medications. They have been recently screening for potential treatments for SCC and gave me access to the data of their most recent study.

### Study's purpose:

The study aimed to compare the performance of the company's drug of interest Capomulin against other treatments. It followed 248 mice with SCC tumours, which received a treatment that included one of 10 different drug regimens —*Capomulin was one of those drugs*. The tumour development was observed and measured over 45 days.

### Summary of the study's conclusions:

1. Capomulin was one of the most effective drugs against SCC, particularly when compared to Ketapril. However, although Capomulin showed very promising results, Ramicane seemed to be more effective at treating SCC.
2. Neither the number of mice tested nor the sex of the mice had an effect on how well each drug performed.
3. About the four most promising drugs, Capomulin, Ramicane, Infubinol, and Ceftamin —*as defined by the company*—, the final tumour volumes of all the mice tested with Capomulin and Ramicane were consistently smaller than those of Infubional and Ceftamin.
4. Although Capomulin works, its tumour-shrinking effects might take time to show.
5. There is a significant relationship between mouse weight and tumour volume; both rise together.

### Study conclusions explained with the results of the analysis:

1. ***Capomulin was one of the most effective drugs against SCC, particularly when compared to Ketapril. However, although Capomulin showed very promising results, Ramicane seemed to be more effective at treating SCC***: Based on the summary statistics, the results were very consistent. Ketapril was the drug with the poorest results, as its mean (55.24 mm<sup>3</sup>) and median (53.70 mm<sup>3</sup>) tumour volume throughout the study were the greatest. This means that the tumours treated with this drug were generally the largest. It also had the highest variability of all the drugs, since its was the most spread; the tumour volume values were overall farther from the mean than the other drugs —*the variance was 68.55 mm<sup>3</sup>, and the standard deviation was 8.28 mm<sup>3</sup>*. On the other hand, Capomulin seemed to have a much lower mean (40.68 mm<sup>3</sup>) and median (41.56 mm<sup>3</sup>) tumour volume. This means that the tumours treated with this drug were mainly much smaller. It also showed a much lower variability because the data was less spread; the tumour volume values were substantially clustered closer to the mean than all but one of the drugs —*the variance was 24.95 mm<sup>3</sup>, and the standard deviation was 4.99 mm<sup>3</sup>*. The drug that surpassed Capomulin's results was Ramicane. The latter seemed to have the most consistent results, as it had the lowest mean (40.22 mm<sup>3</sup>) and median (40.67 mm<sup>3</sup>) tumour volume. This means that the tumours treated with this drug were generally the smallest. Ramicane also had the lowest variability, since the data was the least spread; the tumour volume values were broadly clustered closest to the mean —*the variance was 23.49 mm<sup>3</sup>, and the standard deviation was 4.85 mm<sup>3</sup>*. If the company were to repeat the study, Ketapril's tumour volume would vary the most, as it showed the greatest standard error of the mean (0.60 mm<sup>3</sup>) —*the standard error also suggests that Ketapril's true mean tumour volume value size lies between 54.64 mm<sup>3</sup> and 55.84 mm<sup>3</sup>*. Capomulin would vary much less because it had a much lower standard error of the mean (0.33 mm<sup>3</sup>) —*the standard error shows that Capomulin's true mean tumour volume value size would be between 40.35 mm<sup>3</sup> and 41.01 mm<sup>3</sup>*. Nevertheless, Ramicane would vary the least because it had the lowest standard error of the mean (0.32 mm<sup>3</sup>) —*the standard error indicates that Ramicane's true mean tumour volume value size would lie between 39.9 mm<sup>3</sup> and 40.54 mm<sup>3</sup>*.

2. ***Neither the number of mice tested nor the sex of the mice had an effect on how well each drug performed***: This is because a bar chart, which was plotted to compare the number of mice to the administered drugs by counting how many time points were tested for each regimen, revealed, as expected, that Capomulin had the highest number of mice tested. Ramicane was a very close second —*each drug, Capomulin and Ramicane, were tested on over 200 mice*—, and Ketrapril came third with just below 200 mice. Contrarily, Propriva had the lowest number of tested mice —*just below 150*. A pie chart was plotted to compare the overall distribution of female and male mice in the study. The distribution was even: 51% males and 49% females.

3. ***About the four most promising drugs, Capomulin, Ramicane, Infubinol, and Ceftamin —as defined by the company—, the final tumour volumes of all the mice tested with Capomulin and Ramicane were consistently smaller than those of Infubional and Ceftamin***: This conclusion was reached by creating a graph with four boxplots, one per regimen. The graph showed the distribution of the final tumour volume for all mice in each treatment group, and confirmed an even distribution across drugs, although there was one outlier in the Infubinol distribution. The quartiles and the interquartile range were calculated in order to create that graph.

4. ***Although Capomulin works, its tumour-shrinking effects might take time to show***: That was concluded after looking at a line plot of a random mouse that was treated with Capomulin. The line plot compared the tumour volume and all the time points in the study. The mouse selected had the ID number *l509*. Initially, the tumour volume increased until time point 20. However, after that time point, the volume steadily decreased.

5. ***There is a significant relationship between mouse weight and tumour volume; both rise together***: That was found after generating a scatter plot that compared tumour volume and mouse weight for the Capomulin treatment. The plot showed that as the weight rose, so did the tumour volume. Nonetheless, a correlation needed to be ran to statistically prove whether this trend was significant. The correlation was run. The tumour volume and mouse weight were found to be strongly correlated (*r*(23) = .84, p < .01), which means that their relationship was statistically significant.

### More technical information about how the data was treated before the analysis:

*Part 1*: I received 2 original datasets, one of them contained each mouse's metadata and the other one had the study results. I merged both datasets to create a new Pandas DataFrame, screened the data, and found one duplicated mouse, whose ID number was *g989*. The duplicated information was removed. Altogether, there were 248 mice in the clean DataFrame.

### How the analysis was conducted:

- *Part 2*: I calculated the summary statistics: mean, median, variance, standard deviation, and standard error of the mean.

- *Part 3*: I looked at the number of mice tested among the administered drugs and the sex of the mice overall.

- *Part 4*: I calculated the quartiles and interquartile range, and determined outliers in order to graph four boxplots and look at the distribution of the 4 most promising drugs.

- *Part 5*: I generated a line plot to look at the final tumour volume of a random mouse over all the time points in the study. I also created a scatter plot to find a relationship between mouse weight and tumour volume.

- *Part 6*: I ran a Pearson's correlation to prove whether mouse weight and tumour volume were related.

### Improvements for future analyses:

For future analyses, I would suggest to look at the sex proportions of the mice for each drug regimen to confirm whether different regimens had different proportions. I would also generate more line graphs for a larger sample of random mice to more certainly conclude that the Capomulin's positive effects take time to show. Finally, I would look at maybe a correlation matrix of all the variables tested to confirm whether there are more relationships that need to be analysed.

Contents of the repository:

### The *Pymaceuticals* folder:

It contains a folder that has the two original datasets and a Jupyter Notebook with the data cleanup and the analysis.

## Data Reference

The ficitonal data was generated by [Mockaroo](https://mockaroo.com/), LLC (2022). Realistic Data Generator.

```#Thank you for reading me!```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)



















