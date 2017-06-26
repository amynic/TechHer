# TechHer: Let your Data tell you the Real Story: Advanced Analytics on Azure

During this hands on lab at TechHer UK June 2017 we will be using the **Azure Data Lake Analytics** and **Azure Machine Learning** services with some sample datasets.

### Pre-requistes:
* [An Azure Subscription](https://azure.microsoft.com/en-gb/free/)
* [Azure Storage Explorer](http://storageexplorer.com/)
* [ADLcopy tool](https://www.microsoft.com/en-us/download/details.aspx?id=50358)

Please download the Azure Storage Explorer and ADLCopy tools from the links above

## Azure Data Lake Analytics

**Dataset used: datasets/simpsons_text_analysis.csv**

Lets get started by creating an Azure Data Lake Analytics account

1. **Create an account**
    1. Sign in to the Azure portal.
    2. Click **New > Data + analytics > Data Lake Analytics**.
    3. Select values for the following items: 
        1. **Name:** The name of the Data Lake Analytics account. *[Techher_initials]*
        2. **Subscription:** The Azure subscription used for the account.
        3. **Resource Group:** The Azure resource group in which to create the account. *[Techher_initials]*
        4. **Location:** The Azure datacenter for the Data Lake Analytics account. *[North Europe]* 
        5. **Data Lake Store:** The default store to be used for the Data Lake Analytics account. The Data Lake Store account and the Data Lake Analytics account must be in the same location. *[Create new data lake store]*
        6. **Pricing Tier:** Set as Pay-as-you-go
    4. Select Pin to Dashboard
    5. Click Create. 


Once created you will see the screen below load. Have a look around and then click on **'Sample Scripts'** to walk you through some query and process examples for Azure Data Lake Analytics in the Azure Portal.

![ADLA Portal](images\samplescripts.JPG)

Once loaded click 'Sample Data Missing' and 'U-SQL Advanced Analytics Extensions' to download the data and extensions needed to run the sample.

![ADLA Portal](images\aslasamplesetup.JPG)

This download will take a couple of minutes

![ADLA Portal](images\samplesinprogress.JPG)

![ADLA Portal](images\samplecompleted.JPG)

Once completed and you see the green icons above, now choose **'Query a TSV file'** and read through the U-SQL job.

![ADLA Portal](images\newusqljob.JPG)

Lets take a look at the datasets being used that are stored in your Azure Data Lake Store account. To do this select 'Data Explorer' at the top of the screen.

Your Azure Data Lake Store will load. Given the input schema given in the query - find the file and view the data

``` FROM @"/Samples/Data/SearchLog.tsv" ```

![ADLA Portal](images\dataexplorer.JPG)

![ADLA Portal](images\inputdata.JPG)

Once you have viewed the data, close the storage windows by clicking the 'X' in the top right of each blade until you only have the 'New U-SQL Job' blade

Now choose submit job using 'Submit Job' button at the top of the blade.

Once submitted you will see a blade with the job details and the progress of the job.

![ADLA Portal](images\jobsubmitted.JPG)

Once the job is running the blade will also produce a job graph - showing the breakdown of the query (input files, output files, extract and aggregate processes)

![ADLA Portal](images\querydesign.JPG)

Once the job summary shows the process as complete, the job graph is green and explains how much data (in rows) was written to the output file. Now click the tab 'Output' and select the SearchLog_output.tsv file to review the output data

![ADLA Portal](images\jobcomplete.JPG)
![ADLA Portal](images\selectoutput.JPG)



## Azure Machine Learning

**Dataset used:**
