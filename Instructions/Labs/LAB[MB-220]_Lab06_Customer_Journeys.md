---
lab:
    title: 'Lab: Create and launch a customer journey'
    module: 'Module 6: Customer Journeys'
---


Module 6: Customer Journeys
=====

## Practice Lab 6

Lab Overview
============

Scenario
--------

Now that all the components have been created, Contoso is ready to execute their
marketing campaign to nurture their existing contacts and acquire new customers.
You now need to create a customer journey and bring in all the marketing
elements created in previous labs. You will also update the lead scoring model
you created earlier to also score on interaction data.

Lab Overview
------------

This lab compromises of three exercises:

1.  In exercise one, you will create an outbound customer journey utilizing all
    the marketing components you created in the previous labs.

2.  In exercise two, you will update the lead scoring model created in Lab 4 to
    include interaction data.

3.  In exercise three, you will launch your outbound customer journey.

 What you’ll need:
------------------

-   A computer with a Dynamics 365 Marketing environment

Exercise 1: Create an outbound customer journey
===============================================

You will need to create a new customer journey. Within the customer journey, you
will add a segment, which defines the audience that will be targeting by journey
along with the marketing email that directs contacts to the marketing form and
page you created.

1.  Log into Dynamics 365 Marketing.

2.  Navigate to **Customer Journeys** from the **Marketing execution** group. Click **+New**. When prompted to select a template, click **Skip.**

3.  Click the dorpdown carrot in the upper right corner. Name the journey **[my prefix] Contoso Request a Quote Journey**. Select today as a start
    date and 4:00 PM as the time. Set recurring as yes.

4.  Switch to the General tab. Ensure target is set to contact. Set the recurrence count and recurrence interval
    both to 1.

5.  Save your changes.

6.  Switch back to the Designer tab.

7.  Define the audience for the journey.

   - Drag a segment tile from the Toolbox onto the canvas. Switch to the
        Properties tab and name the tile Contoso Contacts. On the
        segmen tilet, select the arrow down button to expose the child segment.
        Select the child segment and name it Contoso Southwest. In the segment
        field, search for the **[my prefix] Contoso Southwest Excluding Competitors Segment**
        you created in Lab 4 by starting to type in your prefix.
	
- From the Toolbox select the scheduler tile and drag it to the right of
        the segment tile. In the properties, set the following:

    1. Tile Name: One week

    2.  Scheduler type: Date and time

    3.  Date and Time: One week from your current date

    4.  Permitted Times (need to expand): Weekdays 8:00 AM – 5:00 PM (17:00)

8.  Set up the email and marketing page for the journey.

    - From the Toolbox, select the marketing email message tile and drag it to
        the right of the scheduler tile.

    - In the properties, name the email tile Contoso Request a Quote Email.

    - In the marketing email message field, search for your prefix and add the **[my prefix] Contoso Request a Quote Email** you created in Lab 5.

    - From the Toolbox, select the marketing page tile and drag and drop it on top of the
        the email tile.

    - On the email tile, select the arrow down button to expose the marketing
        page tile.

    - Select the marketing page sub-tile and in the properties, name the tile
        Contoso Request a Quote Page.

    - In the marketing page field, search for your prefix and add the **[my prefix] Contoso Request a Quote Page**
        you created in Lab 3.

9.  Add a trigger.

    - From the Toolbox, select the trigger tile and drag it to the right of
        the email tile.

    - In the properties, name the trigger **Requested a quote?**

    - Set the timeout to 14 days.

    - Add a new rule by clicking **+New** next to **Set rules.**

        1.  Source: Contoso Request a Quote Page

        2.  Condition: Trigger_Condition_UserRegistered

	- **Note:** When you add a trigger tile, two paths will automatically appear – a positive path, denoted with a checkmark and a negative path, denoted with an x. This scenario will only use the positive path.

10.  Add an activity.

    - From the Toolbox, select the activity tile and drag it to the positive
        path for the Request a quote trigger.

    - In the properties, name the action Notify Owner.

    - Set the Activity type to task.

    - In the Activity tile, select + New. On the pop out add the following:

        1.  Name: Notify Owner

        2.  Owner: your personal user account (should be default)

        3.  Subject: A quote has been requested

    - Save and close.

11.  Save the journey.

12.  Check for errors and correct any if needed. Note: You may get a warning
    about the recurring journey is set to start in the past. The first iteration
    will start immediately, but future iterations will run in relation to the
    specified start date.

13.  Copy the customer journey URL and paste in a text editor. You will need this
    information in the next exercise.

Exercise 2: Update lead scoring model with interaction data
===========================================================

The lead scoring module you created in Lab 2 scored contacts based on
demographic data. Now that the marketing page and customer journeys have been
created, you can update the scoring model to also score on interaction data.

Note: In this exercise, you will need to the record IDs for the customer journey
and marketing page you created in previous exercises. You will need to navigate
to each item and copy and paste the ID somewhere you can easily reference it.
You can find the ID by navigating to the item and reviewing the URL. The ID
follows &id= towards the end of the URL.

Example customer journey URL:
https://\<orgname\>.crm.dynamics.com/main.aspx?appid=6fd89d4b-06b5-e811-a972-00d3af34c4b&pagetype=entityrecord&etn=msdyncrm_customerjourney&id=34e63989-683f-e911-a987-000d3af3d307

Example customer journey ID: 34e63989-683f-e911-a987-000d3af3d307

1.  Log into Dynamics 365 Marketing.

2.  Navigate to **Scoring Models** in the **Lead management** section of the left menu. Open the **[my prefix] Contoso Southwest Outreach
    Model** you created in Lab 2.

3.  Click stop from the command bar. Click OK in the pop up. Wait until the
    status reason has changed from Stopping to Draft. This may take several minutes. You can check the status by clicking the **Refresh** button in the command bar.

4.  Add a score for completing the customer journey.

    - Drag a condition from the Toolbox below Southwest Demographic. Name the
        condition Journey Completed.

    - On the condition tile, select the arrow down button to expose the child
        condition. Select the child condition and name it Journey Completed.

    - In the entity field, select **Trigger workflow activity contact processed.**

    - Set the frequency to each and the date range of a lifetime.

    - In the Expression 1 section, set the following:

        1.  Field: Customer journey iteration ID

        2.  Operator: =

        3.  Value: Copy and paste the ID of the customer journey you created in
            Exercise 1 of this lab

    - From the Toolbox, drag an action to the right of the Journey Completed
        condition and increase the score to 100.

5.  Add score for opening an email.

    - From the Toolbox, drag a condition below Journey Completed. Name
        the condition Email Opened.

    - On the condition tile, select the arrow down button to expose the child
        condition. Select the child condition and name it Email Opened.

    - In the entity field, select Email opened.

    - Set the frequency to each and the date range of a lifetime.

    - Delete the expression box.

    - From the Toolbox, drag an action to the right of the Email Opened
        condition and increase the score to 5.

6.  Add a score for clicking on an email.

    - From the Toolbox, drag a condition below Email Opened. Name the
        condition Email Clicked.

    - On the condition tile, select the arrow down button to expose the child
        condition. Select the child condition and name it Email Clicked.

    - In the entity field, select Email clicked.

    - Set the frequency to each and the date range of a lifetime.

    - Delete the expression box.

    - From the Toolbox, drag an action to the right of the Email Clicked
        condition and increase the score to 10.

7.  Add a score for a page visit.

    - From the Toolbox, drag a condition to the canvas below Email Clicked.
        Name the condition Page Visited.

    - On the condition tile, select the arrow down button to expose the child
        condition. Select the child condition and name it Page Visited.

    - In the entity field, select Website visited.

    - Set the frequency to each and the date range of a lifetime.

    - In the Expression 1 box, set the following:

        1.  Field: Page Address

        2.  Operator: =

        3.  Value: Copy and paste the ID of the marketing page you created in
            Lab 3 Exercise 2

    - From the Toolbox, drag an action to the right of the Page Visited
        condition and increase the score to 25.

8.  Save and check for errors. Correct any as needed.

9.  Go live.

Exercise 3: Go live with the customer journey
=============================================

Now that you have updated the lead scoring model, you are ready to kick off the
customer journey.

1.  Log into Dynamics 365 Marketing.

2.  Navigate to **Customer journeys** in the **Marketing execution** section of the left menu.

3.  Select the **[my prefix] Contoso Request a Quote** customer journey you created in Exercise
    1.

4.  Click go live from the command bar.
