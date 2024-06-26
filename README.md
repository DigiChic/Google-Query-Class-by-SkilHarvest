# Google Query 

**Documentation Outline**
- [Project overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools for analysis](#tools-for-analysis)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Results](#results)

  
# Project overview
This data looks at Google Query which was the first module treated at the SkilHarvest Data Analysis class.

What is Google Query? 

Google Query is like a magical treasure chest for numbers and words.

**What does it do?**
- It helps you find answers to tricky questions about data.
- You tell it what you want, and it digs through piles of information to find just the right stuff.


# Data Sources
- The data used was provided by the SkilHarvest Instructor, Mr. TeeDee
- Here is pictorial view of the cross-section of the data

![stationarysupplies](stationarysupplies.png)

  
# Tools for analysis
- Google Sheets [You can find it here](https://docs.google.com/spreadsheets/u/0/?ec=asw-sheets-hero-goto)

# Data Cleaning and Preparation
- Data cleaning is the process of fixing or removing incorrect, corrupted, incorrectly formatted, duplicate, or incomplete data within a dataset
- Clean data ensures that the data analysed is consistent and can be analysed accurately
- The data used was clean and then analysed

# Results
- The questions and answers from the data set is as listed below
  
1. Show Sales rep of binder items and pencil
   
```
=QUERY(A:H, "SELECT B, C WHERE C = 'Pen Set' OR C = 'Binder' ", 1)
```

![question1](question1.png)


2. Show sales of binder items and pencil in 2015

```
=QUERY(A:H,"SELECT C,F,H WHERE (C = 'Binder' OR C = 'Pencil') AND F = 2015",1)
```
![question2](question2.png)

3. Sales in Central and East region in 2014

```
=QUERY(A:H, "SELECT A,F,H WHERE (A = 'East' OR A = 'Central') AND F = 2014", 1)
```
![question3](question3.png)

4. Sales in August and September 2014

```
=QUERY(A:H, "SELECT C,E,F,H WHERE (E = 'Aug' OR E = 'Sep') AND F = 2014 ", 1)
```
![question4](question4.png)

5. Show sales of items that start with Pen, include their region, sales rep and year

```
=QUERY(A:H, "SELECT A, B, C, F, H WHERE C LIKE 'Pen%' ", 1)
```
![question5](question5.png)

6. Show sales of items that end with ‘sk’, include their region, sales rep and year

```
=QUERY(A:H, "SELECT A, B, C, F WHERE C LIKE '%sk' ", 1)
```
![question6](question6.png)


