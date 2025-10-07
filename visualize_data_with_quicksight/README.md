<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Visualize data with QuickSight

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-analytics-quicksight)

**Author:** Justine Jurel Valenzuela  
**Email:** valenzuela.justinejurel@gmail.com

---

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Introducing Today's Project!

In this step, I will create an S3 bucket to store the database files I downloaded. Then, I’ll modify and upload the manifest.json file to the same bucket so that Amazon QuickSight can easily access and analyze the data later.

### Tools and concepts

The services I used were Amazon S3 for storing the dataset and Amazon QuickSight for analyzing and visualizing the data.

The key concepts I learned include how to connect S3 data to QuickSight, use manifest files, create interactive dashboards, and refresh datasets to keep reports up to date.

### Project reflection

This project took me approximately 1 hour and 30 minutes to complete. The most challenging part was updating the dataset and getting QuickSight to reflect the new data correctly. It was most rewarding to see the updated dashboard display accurate and meaningful insights after all the fixes.

After this project, I plan to work on Day 3 of the AWS Beginner’s Challenge. I’ll start this project in the afternoon, as I want to complete it earlier than the expected schedule and keep building momentum in my learning journey.

---

## Upload project files into S3

S3 is used in this project to store two files, which are nextflix_titles.csv and manifest.json

I edited the manifest.json file by copying the URI of my netflix_titles.csv file, which was uploaded to my S3 bucket. After making the changes, I reuploaded the manifest file to update it.

It’s important to edit this file because it tells Amazon QuickSight where to find the dataset in S3, allowing it to access and analyze the data correctly.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_3c3cd85a)

---

## Create QuickSight account

Creating an Amazon QuickSight account is free, but new AWS Free Tier users must upgrade to a paid plan to access it. You’ll get a 30-day free trial, and you won’t be charged if you delete it before the trial ends.

Creating an account took me 5 - 10 minutes. 

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_f4ab4214)

---

## Download the Dataset

I connected my S3 bucket to Amazon QuickSight by going to the Datasets page on the left panel of the QuickSight console. Then, I clicked “New dataset” and selected Amazon S3. After that, I filled in the required information, including the data source name, and uploaded the manifest file via URL by copying the S3 URI from the S3 bucket page.

The manifest.json file was important in this step because it tells Amazon QuickSight where the data is stored and helps it understand how to read and import the dataset correctly.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_6f874996)

---

## My first visualization

To create visualizations in QuickSight, select a dataset, choose a chart type, and then drag and drop fields onto the visual to display your data.

The charts show a breakdown of the number of Netflix titles by release year. The first chart displays the total count of records for each year, while the second chart compares the count of records by release year and type, such as movies, TV shows, and others.

I created these visualizations by dragging and dropping the release_year field into the chart area to group the data and using the count of records as the measure. For the second chart, I added the type field to show a comparison between movies and TV shows released each year.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_aff3aad7)

---

## Using filters

Filters are useful for focusing on specific parts of your data, allowing you to analyze trends, compare categories, and find insights without being overwhelmed by all the information at once.

This visualization is a breakdown of Netflix titles by release year, type, and genre. It shows how many movies and TV shows were released each year, along with their distribution across different categories like Action & Adventure, TV Comedies, and Thrillers.

Here, I added a filter by “type” to focus on specific content categories, making it easier to analyze how each genre performed over time.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_c32248c5)

---

## Setting up a dashboard

As a finishing touch, I add some descriptive titles to my visualizations 

Did you know you could export your dashboard as PDFs, too? I did this by publishing my work first, then finding the export icon button on the top right side 

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Refreshing source data

In this project's extension, I downloaded fresh data that’s different from my original dataset because it provides more up-to-date and complete information for analysis.

Analyzing incomplete or outdated data can lead to inaccurate insights and misleading conclusions, which affects the reliability of the results.

Once I downloaded the new data, I updated my S3 bucket by uploading the latest CSV file to replace the old one. I also uploaded a new manifest.json file that included the updated S3 URI, so Amazon QuickSight could locate and use the new dataset correctly.

I initially couldn’t see my updated data in QuickSight, so I went to the Data tab and opened the Datasets section. Then, I edited the dataset I was using and clicked Refresh to load the new data. After that, I saved and published the changes, then went back to the dashboard to view the updated visuals.

![Image](http://learn.nextwork.org/sparkling_silver_zealous_persimmon/uploads/aws-analytics-quicksight_86415f4e3)

---

---
