
# Elk Migration Research Summary

## Summary 

In the Fall 2024 introductory Data Science class, my team and I researched the **migration patterns of elk** in Yellowstone National Park in relation to **environmental factors**. This project challenged me to combine disparate data sources and learn to work with a unique file type. The project was featured in class, and the project website is available [here](https://brooklynnrm.github.io/Elk-Migration.github.io/index.html). 


## Combining Data

I combined five data sources to create a unified table to make analysis easy. Each data source was documented, examined, and cleaned. Each row in the table was a single observation of a single elk with a timestamp, a location given in latitude and longitude, the temperature, rainfall, vegetation, and chemical contamination at that location. *Combining these data sets allowed us to answer our questions about elk movement in relation to the environmental factors and make surprising discoveries.* 

We discovered that **high arsenic concentrations** were reported in July and August of 2010 at the water sampling site GRTE_SNR01. At the same time, two elk had traveled around this sampling site, potentially exposing themselves to unhealthy levels of arsenic in water. Other notable markers of poor water quality that we observed included low dissolved oxygen concentrations in June and July of 2010, as well as relatively high chloride levels in October of 2010. Chloride is a chemical that may indicate the presence of lead in water, which has no safe concentration for exposure.

![arsenic](images/arsenic.png)

## Geographic Data

I learned to utilize geographic data in the form of raster files. I imported vegetation land cover data taken via satellite from the state of Wyoming. After much experimentation, I learned to use the tools in the [terra R package](https://cran.r-project.org/web/packages/terra/index.html). I reprojected the coordinates of the raster file to latitude and longitude, so that they would align with the elk's location data (also given in latitude and longitude) and the maps given in the [ggmap package](https://cran.r-project.org/web/packages/ggmap/index.html), allowing side by side comparisons of elk activity along geographic and natural borders. 

![maps](images/elk_paths.png)



# Shell Questions

1. All files in the working directory , including hidden files can be shown with `ls -a`.

2. To count the number of lines in a text file, I would use the command `wc -l data.txt`. It also works on markdown files, as demonstrated by `wc -l hello.md`, which has three lines.

3. To search for all strings matching "error" in all log files in the current directory, I would use the command `grep "error" .log`. This will return a list of each file and each line containing the word "error".

4. To make a file executable, I would use the command `chmod +x filename.sh`. `chmod` tells the terminal that we are editing permissions, `+x` adds the executable permission, and lastly the file is specified.

5. To display the last twenty lines of a log file, I would use `tail -n 20 output.log`.

6. To combine two text files, I would use the command `cat file1.txt file2.txt > combined.txt`.

7. To check for the word "Completed" in a text file and display the line containing it, I would again use the command `grep "Completed" status.txt`.

8. To sort the lines of a file in alphabetical order and save the results to a new file, I would use the command `sort file.txt > sorted_file.txt`.


# SuSiE Method Summary

The SuSiE method is a linear Bayesian approach to association analysis. The goal of the SuSiE method is to identify causal genetic variants from a large pool of potential variants. **SuSiE outperforms the simple univariate method**, because it addresses multicolinearity in the genetic data by providing credible sets of likely causal variants that are all correlated, rather than simply providing the variants with the best linear regression. A key assumption is that there are a small number of causal variants and that the rest of the variants have an effect size of zero. The SuSiE method has a hyper-parameter called scaled prior variance, which adjusts the balance between the method's sensitivity and precision.

The SuSiE method uses an iterative approach to generate its credible sets. It begins by fitting a linear regression of the variable of interest on each variant. From those linear regressions, it generates the posterior inclusion probability (the Bayesian probability that the variant in question in causal) for each variant, and notes the strength of those effects. In the next iteration, the identified effect is removed, so that other causal effects can be identified. When there are no more significant effects to identify or the algorithm has reached a pre-specified number of effects to estimate, the process terminates. For each identified effect, the variants with the largest probability of contributing to that effect are included, up until the sum of their PIP is at least 0.95 for a credible set with 95% coverage. **A larger coverage percentage will mean a larger credible set**. The credible set may be interpreted as the set of variants with at least a 95% chance of containing the true effect variant.  




 


