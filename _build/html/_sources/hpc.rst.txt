==========================
High Performance Computing
==========================

------------
Introduction
------------

Today we will be deploying and running a High Performance Computing (HPC) cluster by running a genomics analysis example from the `Amazon Genomics CLI <https://aws.amazon.com/genomics-cli/>`_, in individual  temporary AWS accounts provided by AWS through Event Engine.

We will be working at the command line, inside the AWS Cloud9 environment.  No previous knowledge of genomics, HPC, the AWS Console, or the command line is necessary, as all commands are provided.  However if you are familiar with any of these concepts, you are free to explore them in the provided AWS account.

.. _launch-constraint:

We will be running the workshop `Amazon Genomics CLI <https://catalog.workshops.aws/agc-pipelines/en-US>`_ to install the Amazon Genomics CLI, then run a sample workflow.  All work will be done from within an AWS Cloud9 instance, which provides a terminal environment integrated with a file explorer and text editor.  

Today we will do only the **Getting Started** and **WDL Pipeline (Option 2)** sections.  All actions necessary to deploy and run the workflow can be performed from the command line of the Cloud9 environment, though we will also visit the AWS Console to examine the resources and processes of the workflow.

Follow the instructions in sequence, and there are some notes below relevant to the various steps.

----------------------------------
Getting Started → Cloud9 Disk Size
----------------------------------

To access the command line in Cloud9, click the green '+' icon and select 'New Terminal'.

------------------------------------------------
Getting Started → Hello World → Monitor Workflow
------------------------------------------------

Press ``CTRL-C`` to interrupt the '``watch -n 5 -c agc workflow status``' command.

-----------------------
WDL Pipeline (option 2)
-----------------------

We will only run option 2 in this workshop, as it completes in around 15 minutes.  This gives us time to watch the resources start up and shut down, and to retrieve the results and log files during the workshop.  You are welcome to run the other workflows, though some of them run for considerably longer.

**Run the GATK germline SNPs and indels workflow**

There is a capitalization error in the instructions; the context is named ``onDemandCtx``, not ``OnDemandCtx``

