### DATA PREPROCESSING

With this first commit I would like to begin a series of points regarding data preprocessing because 
I see it as a fundamental step for later dealing or apply with any algorithm to extract any conclusion from them. I hope you find this articles useful.

But firstly I would like to name a few buzz words regarding what I would like to write about: Data preparation, cleaning, pre-processing, cleansing, wrangling... These words refer to the same topic, which is a set of steps or activities to pre- model data.

As an example, we can show two definitions of the Wikipedia to grasp an idea of what I wrote about above
 
 - [Data cleansing](https://en.wikipedia.org/wiki/Data_cleansing) Data cleansing or data cleaning is the process of detecting and correcting (or removing) corrupt or inaccurate records from a record set, table, or database and refers to identifying incomplete, incorrect, inaccurate or irrelevant parts of the data and then replacing, modifying, or deleting the dirty or coarse data.[1] Data cleansing may be performed interactively with data wrangling tools, or as batch processing through scripting.
 
 - [Data wrangling](https://en.wikipedia.org/wiki/Data_wrangling), sometimes referred to as data munging, is the process of transforming and mapping data from one "raw" data form into another format with the intent of making it more appropriate and valuable for a variety of downstream purposes such as analytics. A data wrangler is a person who performs these transformation operations. This may include further munging, data visualization, data aggregation, training a statistical model, as well as many other potential uses. Data munging as a process typically follows a set of general steps which begin with extracting the data in a raw form from the data source, "munging" the raw data using algorithms (e.g. sorting) or parsing the data into predefined data structures, and finally depositing the resulting content into a data sink for storage and future use

#### Step 1: Preparing for the Preparation

Around this topic could be a great discussion if it belongs or not to machine learning 
process but undoubtedly it belongs to the ecosystem of understanding machine learning.

In order to undestand better the concept to transmit, firstly we can have a look at the image

![alt text](https://github.com/vanalex/data-preprocessing/blob/master/images/CRISP-DM.png)

As we can see in the image the process of data preparation covers many steps but for our purpose 
it can be summarized as follows:
 - Selection
 - Preprocessing
 - Transformation
 
### Step 2: Exploratory data analysis

Before working with data, it is a key aspect of any process related to data to understand it, and 
a key point to this is EDA. In words of [Chlow Mawer](https://www.svds.com/value-exploratory-data-analysis/?utm_campaign=KDNuggets%20Blog&utm_source=KDNuggets) : 
 - At a high level, EDA is the practice of using visual and quantitative methods to understand 
   and summarize a dataset without making any assumptions about its contents. It is a crucial 
   step to take before diving into machine learning or statistical modeling because it provides 
   the context needed to develop an appropriate model for the problem at hand and to correctly 
   interpret its results.
 
So, before applying any algorithm to our data we should have a look at our data to have more 
insight about it. Here are some steps according to Chlow Mawer to get this insight
 - Univariate visualization of and summary statistics for each field in the raw dataset
 - Bivariate visualization and summary statistics for assessing the relationship between each variable in the dataset and the target variable of interest (e.g. time until churn, spend)
 - Multivariate visualizations to understand interactions between different fields in the data
 - Dimensionality reduction to understand the fields in the data that account for the most variance between observations and allow for the processing of a reduced volume of data
 - Clustering of similar observations in the dataset into differentiated groupings, which by collapsing the data into a few small data points, patterns of behavior can be more easily identified 
 
The article author stresses the importance of visualization instead of only using summarization alone.

# Step3: Dealing with missing values

In this topic I can recommend you the next:

    - dropping instances
    - dropping attributes
    - imputing the attribute mean for all missing values
    - imputing the attribute median for all missing values
    - imputing the attribute mode for all missing values
    - using regression to impute attribute missing values
    
MAybe you can follow other ways to deal with the commented missing values but the listed ones are tried, tested and most 
importantly, are the commonly used approach.

# Step 4: Dealing with outliers

There is no strategy to remove or to maintain them at all. Even if you hear someone telling you that you should follow a fixed
strategy always, this is not true. Outliers are situation dependant.

Depending on the concrete situation, outliers can be the result of poor data collection or they can be really good anomalous 
data. So the approaching to outliers is not focused to a particularly strategy. From this article [Analysis factor](http://www.theanalysisfactor.com/outliers-to-drop-or-not-to-drop/)  

    
    One option is to try a transformation. Square root and log transformations both pull in high numbers. 
    This can make assumptions work better if the outlier is a dependent variable and can reduce the impact 
    of a single point if the outlier is an independent variable. 
    
Here also you can follow some discussion regarding outliers:
    - [§ mehotds to deal with outliers](https://www.neuraldesigner.com/blog/3_methods_to_deal_with_outliers)
    - [Removing Outliers Using Standard Deviation in Python](https://www.kdnuggets.com/2017/02/removing-outliers-standard-deviation-python.html)     
    - [Remove Outliers in Pandas DataFrame using Percentiles](https://stackoverflow.com/questions/35827863/remove-outliers-in-pandas-dataframe-using-percentiles)
    
# Step 5: Dealing with Imbalanced Data
This is a problem that is more common that you think. Maybe you have a robust dataset, with no missing values, with outliers but
maybe if you a have a deeper look, you notice that 90% percent of the instances belong to one class and the others to another. 
Or even worse, 95% to 5%, or could even worse.

To deal with this there some strategies:

- [Learning from Imbalanced Classes](https://www.svds.com/learning-imbalanced-classes/?utm_source=kdnuggets&utm_medium=blog&utm_campaign=learning%20from%20imbalanced%20classes)
- [7 Techniques to Handle Imbalanced Data](https://www.kdnuggets.com/2017/06/7-techniques-handle-imbalanced-data.html)

There is a good explanation of why we can have at the end imbalanced data. As stated in the last link:

    Data used in these areas often have less than 1% of rare, but “interesting” events (e.g. fraudsters using credit cards, 
    user clicking advertisement or corrupted server scanning its network). However, most machine learning algorithms do not 
    work very well with imbalanced datasets. The following seven techniques can help you, to train a classifier to detect 
    the abnormal class.
    
# Step 6: Transformations

According to Wikipedia

    In statistics, data transformation is the application of a deterministic mathematical function to each point in a data 
    set — that is, each data point zi is replaced with the transformed value yi = f(zi), where f is a function. Transforms are 
    usually applied so that the data appear to more closely meet the assumptions of a statistical inference procedure that is to 
    be applied, or to improve the interpretability or appearance of graphs.
    
This is one of the most important tasks of data preparation and it requires more sophisticated methods than others viewed 
previously.

Many ways of doing transformations exist but instead of giving a list of steps, it is better to have a few examples to better 
grasp the concept

    - One-hot encoding "transforms categorical features to a format that works better with classification and regression 
    algorithms" (taken from the first link below). See a discussion of the one-hot transformation below, as well as an 
    approach using Pandas
        - [One hot encoding discussion](https://www.quora.com/What-is-one-hot-encoding-and-when-is-it-used-in-data-science/answer/H%C3%A5kon-Hapnes-Strand)
        - [One hot encoding in python](https://stackoverflow.com/questions/37292872/how-can-i-one-hot-encode-in-python)  
     
    - Log distribution transformation if the non-linear model can be turned into a linear model.
        - [log transformation](https://stats.stackexchange.com/questions/18844/when-and-why-should-you-take-the-log-of-a-distribution-of-numbers)
        
# Step 7: Finishing touches and Moving ahead

Here normally you have some options to proceed with the data that has beed cleaned

    - If you want to use the cleaned data to feed a machine learning algorithm in order to build model, then you probably need
      to use a proper strcuture to use any machine learning algorithm. Normally from a dataframe to numpy ndarray or matrix.
    
    - You will need then a proper knowledge of what algorithm to use.
    
    - Or maybe [you want to save the data into any database](https://stackoverflow.com/questions/39939716/writing-a-pandas-dataframe-to-mysql)
    
    - [Or maybe you want to continue with the data preparation](https://github.com/vanalex/tidy-data-python)         