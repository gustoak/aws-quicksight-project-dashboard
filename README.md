<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Visualize data with QuickSight

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-analytics-quicksight)

**Author:** Gustavo Carvalho  
**Email:** gustavo.carvalho.br@gmail.com

---

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Introducing Today's Project!

n this project, I’m going to demonstrate step by step how to work with AWS and QuickSight. First, I’ll upload a dataset into an S3 bucket, then I’ll create an Amazon QuickSight account and connect that dataset to it. After that, I’ll build different graphs, charts, and analyses, and finally, I’ll publish a dashboard full of insights.

I’m doing this project to learn how to use Amazon QuickSight for data visualization and to get more comfortable working with AWS services in practice.

### Tools and concepts

In the AWS Analytics QuickSight project, I learned to use Amazon S3 to store and update data and Amazon QuickSight to create interactive dashboards. I practiced dynamic visualizations, filters and interactivity, descriptive titles, and how to **publish and export dashboards. I also explored ML features to detect patterns and make predictions, transforming raw data into clear and shareable analyses.


### Project reflection

It took me about 1 hour to complete the AWS Analytics QuickSight project, including setting up the data in S3, creating and customizing the dashboards in QuickSight, adding interactivity and titles, and publishing/exporting the final dashboards.

The next project I plan to do is the AWS Analytics Redshift project. I plan to start it next week.

---

## Upload project files into S3

The two files I stored in my S3 bucket are:

- The dataset file in CSV format.
- The manifest.json file, which tells QuickSight how to read and interpret the dataset.

I changed the S3 URL inside the manifest.json file to point to the exact location of my dataset, the netflix_titles.csv file I had just uploaded into the bucket.

I edited this file because Amazon QuickSight needs the correct S3 path in order to find and read the dataset. Without updating the URL, QuickSight wouldn’t know where my data is stored.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_3c3cd85a)

---

## Create QuickSight account

No, opening a QuickSight account can be free if you use the free trial. Just make sure to avoid optional upgrades that could charge your AWS account.

It usually takes a few minutes for the account to be set up and ready to use, depending on AWS processing time.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_f4ab4214)

---

## Download the Dataset

I visited the Datasets page in Amazon QuickSight to connect my S3 bucket. From there, I selected New dataset, chose S3 as the source, and provided the source name along with the manifest.json file URL from my S3 bucket so QuickSight could properly understand and visualize the data.

The manifest.json file is needed because it acts like a map that tells QuickSight how to read and interpret your dataset. It describes important details such as the file locations, structure, and format of your data in S3. Without the manifest.json, QuickSight wouldn’t know how to properly organize and display the information in charts, tables, or dashboards.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_6f874996)

---

## My first visualization

I create visualizations on QuickSight by using the dataset fields shown in the left-hand panel and dragging them into the visual editor. For example, you can drag a field like release_year into the axis section to create a chart. QuickSight then lets you choose the chart type (bar, line, pie, donut, etc.), apply filters, sort, group data, and customize the appearance.

Once you build one visualization, you can add more visuals, resize or move them around, and combine them into a dashboard for easier analysis and presentation

The visualization you uploaded contains two charts built in Amazon QuickSight using the Netflix dataset:

Donut Chart (left): This chart shows the count of Netflix titles grouped by release year. Each segment of the donut represents a different year, and the size of the slice indicates how many movies and TV shows were released in that year. The large central number (8.81K) represents the total number of records in the dataset.

Bar Chart (right) : This chart provides a breakdown of Netflix titles by release year and type (Movie, TV Show, Other). The horizontal bars show the count of titles per year, with colors distinguishing between Movies, TV Shows, and Other. This lets you compare not just how many titles were released each year, but also the proportion of movies versus TV shows.

 Overall, these visuals together highlight the growth and distribution of Netflix content over time and reveal the balance between movies and TV shows released in recent years.

I created the visualization in Amazon QuickSight by using the Netflix dataset fields from the left-hand panel. For the donut chart, I dragged the release_year field into the Value section to show the count of titles per year. For the bar chart, I dragged release_year into the Y-Axis heading and type into the Group/Color heading to compare Movies and TV Shows across each year. I then adjusted the chart types, resized the visuals, and arranged them together on a dashboard for clearer analysis.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_aff3aad7)

---

## Using filters

Enable interactivity: Filters let the user explore different views of the same dataset. For example, in this chart of Count of Title by Listed_in, you could filter to see only TV Comedies or only Thrillers instead of all categories together.

Help refine the visualization: By showing only the categories that matter (e.g., TV Dramas), the chart becomes clearer and easier to read.

Improve visualization performance: With fewer data points displayed, the dashboard loads faster and is more responsive.

Assist in identifying patterns or outliers: If you filter to specific genres or years, you might notice trends (like comedies being more common than dramas) or unusual spikes.

Make the dashboard more dynamic: Different stakeholders can apply their own filters, such as focusing on genres, countries, or release years, depending on their needs.

This visualization is a horizontal bar chart showing the count of Netflix titles by category (Listed_in field).

The chart compares three categories: TV Comedies, Thrillers, and TV Dramas.
TV Comedies have the highest count (close to 70 titles).
Thrillers come next, with slightly fewer titles than comedies (around 65).
TV Dramas have the lowest count (about 35 titles).

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_c32248c5)

---

## Setting up a dashboard

I used Amazon S3 to store and update my dataset and QuickSight to create and manage visualizations. I learned to refresh data, add clear chart titles, and make dashboards interactive for better usability. I also practiced publishing dashboards for sharing and exporting them as PDFs for documentation. This step taught me how to turn raw data into a polished, shareable product ready for decision-making.

Open your dashboard in QuickSight.
Look at the top right corner of the screen, and click the Export icon (it usually looks like a small download symbol).
From the options, select Generate PDFs.
Wait for QuickSight to process your dashboard.
When the green banner appears indicating the PDF is ready, click Download.

Now you have a PDF version of your dashboard that’s ready to share or include in documentation.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_6c7f7ef0)

---

## Refreshing source data

In this project’s extension, we downloaded fresh data that differs from the original dataset because it contained rows with empty Country data. Analyzing incomplete data carries the risk of generating inaccurate insights, which can lead to incorrect business decisions that cost the company time, effort, and money.

Once we downloaded new data, we had to update our S3 bucket because it is still storing the previous version of the data (i.e. the one with country data missing). We also uploaded a new monifest.json file that points to our updated dataset name. This makes sure that QuickSight is now pulling in data from the uploaded dataset, and not the version with missing data.

We initially couldn’t see our updated data in QuickSight, so we had to visit the dataset in the DataSets page in QuickSight and perform a full reset of our data!

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-analytics-quicksight_86415f4e3)

---

---
