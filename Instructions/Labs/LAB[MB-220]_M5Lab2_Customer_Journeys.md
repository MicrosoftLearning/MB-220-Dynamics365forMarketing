---
lab:
    title: 'Lab 5.2: Create and launch a customer journey'
    module: 'Module 5: Manage marketing emails and customer journeys'
---


Module 5: Manage marketing emails and customer journeys
=====

## Practice Lab 5.2

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

2.  Navigate to **Customer journeys** from the **Marketing execution** group. Click **+New**. When prompted to select a template, click **Skip.**

3.  Click the dorpdown carrot in the upper right corner. Name the journey **[my prefix] Contoso Request a Quote Journey**. Select today as a start
    date and 4:00 PM as the time. Set recurring as no. 

4.  Switch to the General tab. Ensure target is set to contact. Select an end date as a month from the start date.

5.  Save your changes.

6.  Switch back to the Designer tab.

7.  Define the audience for the journey.

   - Select the plus sign above **Set your audience** in the first box in the designer.
   - In the audience pane on the right, ensure Source Type = **Segment**, Segment = **Segment**, and that **Inclusion** is selected. In the Segment field, start typing your prefix and select **[my prefix] Contoso Southwest Excluding Competitors Segment**.

8. Set the date and time for the email to send. Select the plus sign between the **Start** and **End** nodes. In the **Wait for** pane on the right, select the following:
	- Duration: One week
	- Day of week: Weekdays (can use quick select or uncheck Saturday and Sunday)
	- Time of day: Mornings
	
10. Set up an email to send via the journey.

	- Select the plus sign between the **Wait for** and **End** nodes.
	- From the dropdown, select **Send an email.**
	- In the **Send an email** pane on the right, type your prefix into the field and select **alans Contoso Request a Quote Email.**
	- Expand the **Email elements** tab and select **+ Add item.** Select **Page** from the dropdown.
	- Type in your prefix into the field and select **[my prefix] Contoso Request a Quote** page.
	- Click **+Add item** again and select **Form.**
	- Type in your prefix and select **[my prefix] Contoso Request a Quote** form.
	- Expand the **Schedule** tab.
	- Using Quick Select, select **Weekdays.**
	- Using Quick Select, select **Mornings.**

11. Add a condition.
	- Between the **Send an email** and the **End** node, click the plus sign.
	- Select **If/Then.**
	- In the **Select a source** field, select **[my prefix] Contoso Request a Quote Form.** In the **Select a condition** field, select **have registration.**
	- Ensure that 1 hour is selected in **Wait up to.**

12. Set up the Yes/No branches for the condition.
	- In the **Yes** branch, click the plus sign. Select **Phone call**.
	- In the **Phone call** field, select **+New Phone-call activity marketing template.**
	- For **Name**, write **[my prefix] Requested Quote Follow-up.**
	- For **Subject**, write **Customer requested a quote.**
	- Set **Schedule type** to **Delay (in days)** and enter 0 for **Start delay.**
	- For **Start time**, enter 1 for **Hour.**
	- Click **Save and close.**

13. Save the customer journey and check for errors.

15. Go live.

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

    - In the entity field, select **Customer Journey.**

    - Set the frequency to each and the date range of a lifetime.

    - Use the lookup field to select the customer journey value.

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
