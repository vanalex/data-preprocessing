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