# data_analysis_viz_stars_dataset
thestars dataset clssed stars by their color and each star had attributes that include temparature, luminosity, radius, and absolute magnitude, and color. various univariate and multivariate analysis and visualization methods were carried on this data to understand the various relations between features.
 First, we'll import pandas, a data processing and CSV file I/O library. We'll also import seaborn, a Python graphing library. current version of seaborn generates a bunch of warnings that we'll ignore. Next, we'll load the stars dataset. Using the .head() method, we check what'sin the stars data
 We then check how many examples we have of each star color using the .value_counts() method on the "Star color" feature..
 The first way we can plot things is using the .plot extension from Pandas dataframes. We'll use this to make a scatterplot of the stars features.
 We can also use the seaborn library to make a similar plot. A seaborn jointplot shows bivariate scatterplots and univariate histograms in the same figure.
 One piece of information missing in the scatterplots is what color each star is. We'll use seaborn's FacetGrid to color the scatterplot by stars.
 We can look at an individual feature in Seaborn through a boxplot. One way we can extend this plot is adding a layer of individual points on top of it through Seaborn's striplot. We'll use jitter=True so that all the points don't fall in single vertical lines above the color. Saving the resulting axes as ax each time causes the resulting plot to be shown on top of the previous axes. A violin plot combines the benefits of the previous two plots and simplifies them. Denser regions of the data are fatter, and sparser thiner in a violin plot. A final seaborn plot useful for looking at univariate relations is the kdeplot, which creates and visualizes a kernel density estimate of the underlying feature. Another useful seaborn plot is the pairplot, which shows the bivariate relation between each pair of features.
 The diagonal elements in a pairplot show the histogram by default. We can update these elements to show other things, such as a kde.
 We can quickly make a boxplot with Pandas on each feature split out by color.
 One cool more sophisticated technique pandas has available is called Andrews Curves. Andrews Curves involve using attributes of samples as coefficients for Fourier series and then plotting these.
 Another multivariate visualization technique pandas has is parallel_coordinates. Parallel coordinates plots each feature on a separate column & then draws lines connecting the features for each data sample.
 A final multivariate visualization technique pandas has is radviz Which puts each feature as a point on a 2D plane, and then simulates having each sample attached to those points through a spring weighted by the relative value for that feature.
