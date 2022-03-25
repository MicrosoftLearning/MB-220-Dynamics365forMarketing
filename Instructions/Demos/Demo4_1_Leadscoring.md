---
demo:
    title: 'Demo 2.1: Lead scoring'
    module: 'Module 2: Manage customers in Dynamics 365 Marketing'
---


# Module 2: Manage customers in Dynamics 365 Marketing

## Demo 2.1: Lead scoring

# Demo Overview

## Scenario

Sales and marketing work together to define scoring models that will help the sales teams identify the most promising leads. They decide they need two models.

The first model they want will be based on demographic data. They want to give higher scores to leads associated with Transportation and Financial industries. They also want to give higher scores to leads with key terms in their related contact titles such as Owner, CFO, Controller, or Finance Director. 

Second, they want score leads based on interaction with the content the marketing team is sending them. The model will be increase lead scores based on emails opened, forms submitted, events attended, and more.

The Marketing Coordinator creates both models within Dynamics 365 Marketing.

## Lab Overview

This lab compromises of two exercises:

1. In this exercise, you will create a lead scoring model based on demographic data.

2. In this exercise, you will create a lead scoring model based on behavioral data.

## What you’ll need:

- A computer with a Dynamics 365 Marketing environment

## Exercise 1: Create a lead scoring model for demographic data

1. Log into Dynamics 365 Marketing.

2. Navigate to **Scoring Models** under the **Lead** **Management** group.

3. Click **+New**.

4. Switch to the **Summary** tab. 

	- Name the model **Demographic Model**. 
	- Ensure target is set to **Contact** and save.

5. Switch back to the **Design** tab. 

6. On the right, navigate to **Grades**. Input 100 as your sales ready score. 

	- Click **+New**.
		1. Grade: Low
		2. From: 0
		3. To: 24
    - Click **+New**.
    	1. Grade: Medium
    	2. From: 25   
    	3. To: 59   
    - Click **+New**.    
    	1. Grade: High    
    	2. From: 60    
    	3. To: 100
7. Click **Save**.

8. Increase the lead score 20 points for being associated to the **Transportation** industry.

	- From the **Toolbox**, drag a **Condition** onto the canvas. Name the condition **Transportation Industry.**
	- On the condition tile, select the arrow down button to expose the child condition. Select the child condition.
		1. Name the child condition **Transportation Industry**. 
		2. In the entity field, select **Lead** and select it.
		3. Add the following expression: **Industry = Transportation**.
    - From the **Toolbox**, drag an **Action** to the right of the **Transportation Industry** condition. In the action, increase the score by **20**.

9. Increase the lead score 20 points for being associated to the Financial industry.

	- From the Toolbox, drag a **Condition** onto the canvas below the **Transportation Industry** condition. Name the condition **Financial Industry.**

	- On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

		1. Name the child condition **Financial Industry**. 
		2. In the entity field, select **Lead** and select it.
		3. Add the following expression: **Industry = Financial**.
    - From the **Toolbox**, drag an **Action** to the right of the **Financial Industry** condition. In the action, increase the score by **20**.

10. Increase the lead score 30 points for job title of Owner.

	- From the Toolbox, drag a **Condition** onto the canvas below the Financial Industry condition. Name the condition **Job Title contains Owner.**

	- On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

		1. Name the child condition **Owner**. 
		2. In the entity field, select **Lead** and select it. Add a period and then start typing “con”. Select **Parent contact**. Your entity field will look like this: **Lead.Parent contact**. 
		3. Add the following expression: **Job Title contains Owner**.

    - From the **Toolbox**, drag an **Action** to the right of the **Job Title contains Owner** condition. In the action, increase the score by **30**.

11. Increase the lead score 25 points for job title of CFO.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the **Job Title** **contains Owner** condition. Name the condition **Job Title contains CFO.**

	- On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

		1. Name the child condition **CFO**. 

		2. In the entity field, select **Lead** and select it. Add a period and then start typing “con”. Select **Parent contact**. Your entity field will look like this: **Lead.Parent contact**. 

		3. Add the following expression: **Job Title contains CFO**.

    - From the **Toolbox**, drag an **Action** to the right of the **Job Title contains CFO** condition. In the action, increase the score by **25**.

12. Increase the lead score 20 points for job title of Controller.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the **Job Title contains CFO** condition. Name the condition **Job Title contains Controller.**

	- On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

		1. Name the child condition **Controller**. 
		2. In the entity field, select **Lead** and select it. Add a period and then start typing “con”. Select **Parent contact**. Your entity field will look like this: **Lead.Parent contact**. 
		3. Add the following expression: **Job Title contains Controller**.

    - From the **Toolbox**, drag an **Action** to the right of the **Job Title contains Controller** condition. In the action, increase the score by **20**.

13. Increase the lead score 10 points for job title of Director.

	- From the Toolbox, drag a **Condition** onto the canvas below the **Job Title contains Controller** condition. Name the condition **Job Title contains Director.**

	- On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

		1. Name the child condition **Director**. 
		2. In the entity field, select **Lead** and select it. Add a period and then start typing “con”. Select **Parent contact**. Your entity field will look like this: **Lead.Parent contact**. 
		3. Add the following expression: **Job Title contains Director**.

    - From the **Toolbox**, drag an **Action** to the right of the **Job Title contains Director** condition. In the action, increase the score by **10**.

14. Increase the lead score 5 points for job title of Finance.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the Job Title contains Director condition. Name the condition **Job Title contains Finance.**

	- On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

		1. Name the child condition **Finance**. 
		2. In the entity field, select **Lead** and select it. Add a period and then start typing “con”. Select **Parent contact**. Your entity field will look like this: **Lead.Parent contact**. 
		3. Add the following expression: **Job Title contains Finance**.

    - From the **Toolbox**, drag an **Action** to the right of the **Job Title contains Finance** condition. In the action, increase the score by **5**.

15. **Save**.

16. **Check for errors**. Correct any as needed.

17. **Go live**.

 

# Exercise 2: Create a behavioral lead scoring model

1. Log into Dynamics 365 Marketing.

2. Navigate to **Scoring Models** under the **Lead Management** group.

3. Click **+New**.

4. Switch to the **Summary** tab. 

	- Name the model **Behavioral Model**. 
	- Ensure target is set to **Contact** and save.

5. Switch back to the **Design** tab.

6. On the right, navigate to **Grades**. Input 30 as your sales ready score. 

	- Click **+New**.

		1. Grade: Low
		2. From: 0
		3. To: 19

    - Click **+New**.
    
    	1. Grade: Medium
    	2. From: 20
    	3. To: 39
    
    - Click **+New**.
    
    	1. Grade: High
    	2. From: 40  
    	3. To: 100

7. Increase the lead score 1 point for any email opened.

	- From the **Toolbox**, drag a **Condition** onto the canvas. Name the condition **Email Opened.**
		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.
			1. Name the child condition **Email Opened**.
			2. In the entity field, select **Email opened** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Custom.
			5. **Last**: 60 Day.
			6. Delete Expression 1.
    - From the **Toolbox**, drag an **Action** to the right of the **Email** **Opened** condition. In the action, increase the score by **1**.

8. Increase the lead score 5 points for any email clicked.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the E**mail Opened** condition. Name the condition **Email Clicked.**

		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

			1. Name the child condition **Email Clicked**.
			2. In the entity field, select **Email clicked** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Custom.
			5. **Last**: 60 Day.
			6. Delete Expression 1.

    - From the **Toolbox**, drag an **Action** to the right of the **Clicked Email** condition. In the action, increase the score by **5**.

9. Decrease the lead score 20 points for an unsubscribe.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the **Email Clicked** condition. Name the condition **Unsubscribe.**

		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.
			1. Name the child condition **Unsubscribe**.
			2. In the entity field, select **Marketing list** **unsubscribed** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Lifetime.
			5. Delete Expression 1.

    - From the **Toolbox**, drag an **Action** to the right of the **Unsubscribe** condition. In the action, decrease the score by **20**.

10. Increase the lead score 20 points for a form submission.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the **Unsubscribe** condition. Name the condition **Form submitted.**

		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.
			1. Name the child condition **Form submitted**.
			2. In the entity field, select **Form submitted** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Custom.
			5. **Last**: 6 Month.
			6. Delete Expression 1.

    - From the **Toolbox**, drag an **Action** to the right of the **Form submitted** condition. In the action, increase the score by **20**.

11. Increase the lead score 5 points for a website visit.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the Form submitted condition. Name the condition **Website visited.**

		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.
			1. Name the child condition **Website visited**.
			2. In the entity field, select **Website visited** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Custom.
			5. **Last**: 6 Month.
			6. Delete Expression 1.

    - From the **Toolbox**, drag an **Action** to the right of the **Website visited** condition. In the action, increase the score by **5**.

12. Increase the lead score 10 points for an event registration.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the **Website visited** condition. Name the condition **Event registration.**

		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

			1. Name the child condition **Event registration**.
			2. In the entity field, select **Event registration** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Custom.
			5. **Last**: 1 Year.
			6. Delete Expression 1.

    - From the **Toolbox**, drag an **Action** to the right of the **Event registration** condition. In the action, increase the score by **10**.

13. Increase the lead score 20 points for event attendance.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the Event registration condition. Name the condition **Event attendance.**

		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

			1. Name the child condition **Event check-in**.
			2. In the entity field, select **Event check-in** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Custom.
			5. **Last**: 1 Year.
			6. Delete Expression 1.

    - From the **Toolbox**, drag an **Action** to the right of the **Event attendance** condition. In the action, increase the score by **20**.

14. Decrease the lead score 10 points for a cancelled registration.

	- From the **Toolbox**, drag a **Condition** onto the canvas below the **Event attendance** condition. Name the condition **Cancelled registration.**

		1. On the condition tile, select the arrow down button to expose the child condition. Select the child condition.

			1. Name the child condition **Cancelled registration**.
			2. In the entity field, select **Event registration cancelled** and select it.
			3. **Frequency**: Each.
			4. **Date range**: Custom.
			5. **Last**: 1 Year.
			6. Delete Expression 1.

    - From the **Toolbox**, drag an **Action** to the right of the **Cancelled registration** condition. In the action, decrease the score by **10**.

15. **Save**.

16. **Check for errors**. Correct any as needed.

17. **Go live**.
