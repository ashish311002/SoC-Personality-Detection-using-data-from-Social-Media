# SoC 2022: Personality Detection using data from Social Media
Week-1: Learned about various useful libraries such as Pandas, NumPy, Scipy etc. Assignment 1 is based on the application of these libraries to the questions.<br/>
Week-2: Learned about Linear Regression and Regression in multiple variables. Assignment 2 is based on the application of Linear Regression to the given Dataset.<br/>
Week-3: Learned about K Means Clustering Algorithm and applied it to the various datasets given. Implemented the Clustering algorithm from Scratch.<br/>
Link to the notebook of FinalImplementation:https://colab.research.google.com/drive/1rk2niv9t7OronuwjgSi7ufP-EcOJiXEZ#scrollTo=Tn3wh1R-Qv6J<br/>
Downloaded the dataset containing the survey result which was conducted on Social Media from Kaggle. Perforemed EDA on this dataset to find out which countries had the most participation and which countries had the least participation. By using EDA I also found out how many people were there corresponding to a given rating of a question. Finally after cleaning the data by dropping the unnecessary columns as well as any NaN values that existed I got the final dataframe on which I applied the kmeans method of the sklearn.cluster module. Using this function I divided this unlabelled data into 5 clusters and calculated the mean of all the character traits in a cluster to identify what is the major character trait in the cluster.<br/>
Link to the Kaggle dataset:https://drive.google.com/file/d/17NrQWl8E_kgxPxvITKbelQb-DMKvVMWW/view?usp=sharing<br/>
Could not upload it in the repo since the size of the dataset is greater than 25 MB. <br/>
The specification of the dataset(containing details about various columns) is given below:<br/>
This data was collected (2016-2018) through an interactive on-line personality test.<br/>
The personality test was constructed with the "Big-Five Factor Markers" from the IPIP. https://ipip.ori.org/newBigFive5broadKey.htm
Participants were informed that their responses would be recorded and used for research at the beginning of the test, and asked to confirm their consent at the end of the test.

The following items were presented on one page and each was rated on a five point scale using radio buttons. The order on page was was EXT1, AGR1, CSN1, EST1, OPN1, EXT2, etc.
The scale was labeled 1=Disagree, 3=Neutral, 5=Agree<br/>

EXT1	I am the life of the party.<br/>
EXT2	I don't talk a lot.<br/>
EXT3	I feel comfortable around people.<br/>
EXT4	I keep in the background.<br/>
EXT5	I start conversations.<br/>
EXT6	I have little to say.<br/>
EXT7	I talk to a lot of different people at parties.<br/>
EXT8	I don't like to draw attention to myself.<br/>
EXT9	I don't mind being the center of attention.<br/>
EXT10	I am quiet around strangers.<br/>
EST1	I get stressed out easily.<br/>
EST2	I am relaxed most of the time.<br/>
EST3	I worry about things.<br/>
EST4	I seldom feel blue.<br/>
EST5	I am easily disturbed.<br/>
EST6	I get upset easily.<br/>
EST7	I change my mood a lot.<br/>
EST8	I have frequent mood swings.<br/>
EST9	I get irritated easily.<br/>
EST10	I often feel blue.<br/>
AGR1	I feel little concern for others.<br/>
AGR2	I am interested in people.<br/>
AGR3	I insult people.<br/>
AGR4	I sympathize with others' feelings.<br/>
AGR5	I am not interested in other people's problems.<br/>
AGR6	I have a soft heart.<br/>
AGR7	I am not really interested in others.<br/>
AGR8	I take time out for others.<br/>
AGR9	I feel others' emotions.<br/>
AGR10	I make people feel at ease.<br/>
CSN1	I am always prepared.<br/>
CSN2	I leave my belongings around.<br/>
CSN3	I pay attention to details.<br/>
CSN4	I make a mess of things.<br/>
CSN5	I get chores done right away.<br/>
CSN6	I often forget to put things back in their proper place.<br/>
CSN7	I like order.<br/>
CSN8	I shirk my duties.<br/>
CSN9	I follow a schedule.<br/>
CSN10	I am exacting in my work.<br/>
OPN1	I have a rich vocabulary.<br/>
OPN2	I have difficulty understanding abstract ideas.<br/>
OPN3	I have a vivid imagination.<br/>
OPN4	I am not interested in abstract ideas.<br/>
OPN5	I have excellent ideas.<br/>
OPN6	I do not have a good imagination.<br/>
OPN7	I am quick to understand things.<br/>
OPN8	I use difficult words.<br/>
OPN9	I spend time reflecting on things.<br/>
OPN10	I am full of ideas.<br/>

The time spent on each question is also recorded in milliseconds. These are the variables ending in _E. This was calculated by taking the time when the button for the question was clicked minus the time of the most recent other button click.

dateload  :  The timestamp when the survey was started.<br/>
screenw    : The width the of user's screen in pixels<br/>
screenh    : The height of the user's screen in pixels<br/>
introelapse :The time in seconds spent on the landing / intro page<br/>
testelapse : The time in seconds spent on the page with the survey questions<br/>
endelapse  : The time in seconds spent on the finalization page (where the user was asked to indicate if they has answered accurately and their answers could be stored and used for research. Again: this dataset only includes users who answered "Yes" to this question, users were free to answer no and could still view their results either way)
IPC       :  The number of records from the user's IP address in the dataset. For max cleanliness, only use records where this value is 1. High values can be because of shared networks (e.g. entire universities) or multiple submissions<br/>
country    : The country, determined by technical information (NOT ASKED AS A QUESTION)<br/>
lat_appx_lots_of_err :   approximate latitude of user. determined by technical information<br/>
long_appx_lots_of_err: approximate longitude of user
