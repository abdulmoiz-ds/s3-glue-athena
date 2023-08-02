# S3 to Athena Data Pipeline
Here I am going to explain how I use AWS S3, AWS Glue, and AWS Athena to make a data pipeline.

## Step 1: Create a bucket
First, go to AWS Console and search "S3". Click on "S3". Then click on "Create Bucket". Give a unique name to the bucket and click on "Create Bucket".
![Screenshot (595)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/ae46f413-6fb0-44a9-8503-ef144ff4e6ed)

You will see a new bucket will be in the list. Click on the bucket and then click on "Upload" to upload the file.
![Screenshot (597)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/4c30d4c6-2c92-4aca-8bed-d9e9cee8c468)

After this, click on "Add files" and then upload a sample CSV file.
![Screenshot (598)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/5ebddaaa-9092-4c2c-8987-1335d71f538a)

Then click on "Upload".
![Screenshot (599)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/158a657b-20e6-4f69-bd54-98156a05be57)

You will see a CSV file showing in the bucket.

![Screenshot (600)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/eedd8caf-abd1-447f-9355-c00830001366)

## Step 2: Create a Crawler
Now search "Crawler" in the search bar and click on it.
![Screenshot (601)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/60d848d2-8bb3-4dda-8b74-f96097321d36)

Give a name to the Crawler.
![Screenshot (602)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/dc28341b-db49-47da-af6f-945e9c3591c9)

Click on "Next". Then click on "Add a Data Source".
![Screenshot (604)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/3b5218d6-5e99-4418-b2b3-a62def42d7a5)


Now choose the bucket you just created and click on "Choose".
![Screenshot (606)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/4c210cf5-cd97-48ea-a7be-e797aca73169)

## Step 3: Create IAM Role for Glue Crawler
Now search IAM and open it in a new tab. Click on "Roles". Then Click on "Create Role" on the Top-Rigt side. Then Search "Glue". Then Click on "Next".

![Screenshot (610)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/701efa8d-f6ef-41d6-9907-e8d285e47f48)


Now search "S3" and give FullAccess.
![Screenshot (611)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/a50bd16e-1eea-4910-a6b1-95068709fec3)

After this click on create role.

Now go back to the glue page and click on next. You will see this page. Click on the role you just created.

![Screenshot (613)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/45f5b164-bb06-4ca9-8dfe-e37a820d125f)

Now click next. Click on "Add a Database". Then create a database. Go back to the previous page and select the created database.

Then create a crawler. You have to run the crawler.
![Screenshot (618)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/8ff67baf-9d68-4994-a9bc-e7cfa2193af4)


Wait for the crawler to stop.
## Step 4: Launch Query Editor in Athena

Now search "Athena" in the search bar and click on "Launch Query Editor".

![Screenshot (621)](https://github.com/abdulmoiz-ds/s3-glue-athena/assets/74011754/0cde6917-3772-420b-96e1-99222fddcff6)

Here you can do a query. You have to create a bucket where your queries will be saved.
