=========
Analytics
=========

We will be using `Data Engineering Immersion Day <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US>`_ in AWS Workshop Studio.  We will be doing only parts of the immersion day, which are outlined below along with some notes you will need to complete the workshop.

* `Introduction <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/100-introduction>`_
   * `Workshop at an AWS Event <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/100-introduction/30-region-selection>`_: Use these instructions to log in using Event Engine.  The event hash will be provided to you.
* Omit Lab: Streaming Data Analytics
* `Lab: Ingestion with DMS <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/400>`_
   * **Omit** options 1 and 2
   * `Option 3: Skip DMS Lab <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/400/450-skip-dms>`_
      * For this step you will need the name of the S3 bucket created within your account.
      * In the AWS Console, visit the [S3 Console](https://s3.console.aws.amazon.com/s3/buckets).  It's helpful to keep the S3 console open in a separate browser tab.
      * Identify and click on the bucket containing the string **dmslabs3bucket**
      * Note the full name of the bucket (**mod-xxx-dmslabs3bucket-xxx**)
      * Now proceed with opening the AWS CloudShell, and paste in the bucket name in the `aws s3 cp` command in the  **Copy Data across from staging Amazon S3 bucket to your S3 bucket** section.  This command will copy 1.9 GB of CSV data to your bucket.
* `Lab: Transforming data with Glue <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/600>`_
   * We will use the **New** AWS console, so the appearance and some of the order of steps differs from the workshop instructions.
   * `Data Validation and ETL <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/600/610-glue-data-validation-etl>`_
      * Create Glue Crawler for initial full load data
      * Step 6: Is now contained within step 7.
      * Step 12: Is now contained within step 13.
      * Step 13: Creating a new database will open a new tab.  After creating the new database, return to the **Set output and scheduling** tab and refresh the **Target database** field to be able to select your newly-created database.
      * Step 16: **Add new columns only** is under the **Advanced options** dropdown
   * Data Validation Exercise
      * Step 3: To rename the columns with Edit Schema, we will temporarily use the 'old' Glue console.
      * On the left navigation menu of the Glue console, expand **Legacy pages** and select **Tables (legacy)** to gain access to the **Edit Schema** button for the **person** table.
   * **Omit** the other sections (Incremental Data Processing with Hudi, Glue Job Bookmark, Glue Workflows)
* `Lab: Query and Visualize <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/800>`_
   * `Athena and Quicksight <https://catalog.us-east-1.prod.workshops.aws/workshops/976050cc-0606-4b23-b49f-ca7b8ac4b153/en-US/800/810-athena-quicksight>`_
      * In the Data Engineering Immersion Day instructions, expand the section **Get Started using Athena** to set up a query result location.
      * The procedure to set up a query result location in S3 has changed from the workshop instructions.  Follow the link **Learn More** from the **Getting Started** box on the Athena front page, to follow the [Getting Started](https://docs.aws.amazon.com/athena/latest/ug/getting-started.html) instructions on how to set up a query result location.
      * You will create a new folder `athenaquery` at the top level of the bucket, alongside the `tickets` folder.  So the S3 location string will look like `s3://mod-xxx-dmslabs3bucket-xxx/athenaquery/`
      * Once you have created the query result location, proceed with the instructions starting with '`1. In the Query Editor...'
