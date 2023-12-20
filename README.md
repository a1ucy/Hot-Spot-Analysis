# Hot-Spot-Analysis
In this project, you will perform numerous spatial queries on a huge database that contains geographic information and the real-time locations of the customers of a well-known taxi company.
Objectives
Learners will be able to:
● Set up Apache Spark and use dataframes within it to manage data operations.
● Write some simple Scala code then identify how to run it.
● Interact with geospatial data and run queries on it.
Technology Requirements
● Apache Spark 2.3.1
● SparkSQL
● Scala
● Java8
● Hadoop 3.0
Project Description
You will be utilizing Scala and Apache Spark in this project to create a solution that can extract crucial data from the provided dataset, which can then be used to make operational and strategic choices. The technology gives the client access to statistically significant geographic locations, which it can utilize to plan its operations in advance and improve customer service.
Please review the introductory video regarding Project 2 before beginning. This is located in your course Welcome and Start Here section.
● Project 2: Hot Spot Analysis Introduction Video
Directions
In this project, you are required to do spatial hot spot analysis. In particular, you need to complete two different hot spot analysis tasks.
Tasks:
1. Hot Zone Analysis
This task will need to perform a range join operation on a rectangle datasets and a point dataset. For each rectangle, the number of points located within the rectangle will be obtained. The hotter rectangle means that it includes more points. So this task is to calculate the hotness of all the rectangles.
Download the required templates (attached in the Coursera Project Overview page). 2. Hot Cell Analysis
This task will focus on applying spatial statistics to spatio-temporal big data in order to identify statistically significant spatial hot spots using Apache Spark. The topic of this task is from ACM SIGSPATIAL GISCUP 2016.
● Problem Definition page
● Submit Format page
● Special requirement (different from GIS CUP)
As stated in the Problem Definition page, in this task, you are asked to implement a Spark program to calculate the Getis-Ord statistic of NYC Taxi Trip datasets. We call it "hot cell analysis"
To reduce the computation power need, we made the following changes:
1. Theinputwillbe"yellow_trip_sample_100000.csv"dataset.
2. Eachcellunitsizeis0.01*0.01intermsoflatitudeandlongitudedegrees. 3. YouonlyneedtoconsiderPick-upLocation.
Coding Template Specification:
Input Parameters:
1. Outputpath(Mandatory)
2. Taskname:"hotzoneanalysis"or"hotcellanalysis"
3. Taskparameters:(1)Hotzone(2parameters):nyctaxidatapath,zonepath(2)Hotcell(1 parameter): nyc taxi data path
Example:
Note:
1. Thenumber/orderoftasksdonotmatter.
2. But,thefirst7ofourfinaltestcaseswillbehotzoneanalysis,thelast8willbehotcell analysis.
Input Data Format:
The main function/entrance is "cse512.Entrance" scala file.
1. Pointdata:TheinputpointdatasetisthepickuppointofNewYorkTaxitripdatasets.Thedata format of this phase is the original format of NYC taxi trip which is similar from Phase 2. But the coding template already parsed it for you. Find the data in the .zip file (attached in the Coursera Project Overview page, titled “...Yellow Trip Sample 100000”).
2. Zonedata(onlyforhotzoneanalysis):at"src/resources/zone-hotzone"ofthetemplate
3. Hot Zone Analysis:
The input point data can be any small subset of the NYC taxi dataset.
Hot Cell Analysis:
The input point data is a sample dataset like "yellow_trip_sample_100000.csv."
Output Data Format: Hot Zone Analysis:
All zones with their count, sorted by "rectangle" string in an ascending order.
Hot Cell Analysis
The coordinates of top 50 hottest cells sorted by their G score in a descending order. ● Note: Do not output G score.
Example answers:
An example input and answer are put in "testcase" folder of the coding template
Where you need to make changes:
Do not delete any existing code in the coding template unless you see this "You need to change this part."
Hot Zone Analysis:
In the code template:
1. Youneedtochange"HotzoneAnalysis.scala”and“HotzoneUtils.scala".
2. Thecodingtemplatehasloadedthedataandwrittenthefirststep,rangejoinquery,foryou. Please finish the rest of the task.
3. TheoutputDataFrameshouldbesortedbyyouaccordingtothe"rectangle"string.
Hot Cell Analysis:
In the code template,
1. Youneedtochange"HotcellAnalysis.scala”and“HotcellUtils.scala".
2. Thecodingtemplatehasloadedthedataanddecidedthecellcoordinate,x,y,zandtheirmin and max. Please finish the rest of the task.
3. TheoutputDataFrameshouldbesortedbyyouaccordingtoG-score.Thecodingtemplatewill take the first 50 to output. Do not output G-score.
