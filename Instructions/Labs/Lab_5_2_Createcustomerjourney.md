---
lab:
    title: 'Lab 5.2: Create and launch a customer journey'
    module: 'Module 5: Manage marketing emails and customer journeys'
---

# Module 5: Manage marketing emails and customer journeys

## Practice Lab 5.2 – Create and launch a customer journey

# Lab Overview

## Scenario

Now that all the components for the Cross Sell Campaign have been created, the Marketing Coordinator is ready to create the journey and kick off the campaign.

The journey will consist of three emails. The first email will be sent out immediately. The second email will be sent out one week later. The first email is informational, promoting specialized offerings. The second email has a CTA driving the customer to a marketing page with a marketing from. If the customer fills out the form, they will receive a third email thanking them for their submission and letting them know an agent will contact them shortly. At the same time, a task will be created and assigned to an agent, notifying them of the form submission. If the customer does not fill out the form, they will receive an additional email.

## Lab Overview

This lab compromises of three exercises:

1. In exercise one, you will create an outbound customer journey adding all the marketing components you created in the previous labs.

2. In exercise two, you will interact with the campaign components (emails, page, form).

## What you’ll need:

- A computer with a Dynamics 365 Marketing environment

# Exercise 1: Create an outbound customer journey

 

1. Log into Dynamics 365 Marketing.

2. Navigate to **Customer journeys** under the **Marketing execution** group. 

3. Click **+New**. When prompted to select a template, select **Simple Email Journey**.

4. Navigate to the **General** tab.

	- Name the journey **[my prefix] Cross Sell Campaign Journey**. 

	- Ensure **target** is set to **Contact**. 

	- Set the **Start date and time** to today’s date 1 hour ago.

	- Set the **End date and time** to one month from today.

	- Set the **Time zone** to your time zone.

	- Change the **Content settings** to Business Content Settings. 

	- Save your changes.

5. Switch back to the **Designer** tab.

6. Define the audience for the journey.

	- Select the plus sign above **Set audience** in the first box in the designer.

	- In the audience pane on the right, ensure **Source Type** = **Segment**.

	- **Segment** = Segment.

	- **Inclusion** is selected. 

	- In the **field below Inclusion**, start typing your prefix and select **[my prefix] Business Customers**.

7. Set up the first email in the journey.

	- Select the plus sign after the segment. Select **Send an Email**.

	- In the **Email** field on the right, select **[my prefix] Cross Sell Campaign Email 1**.

8. Add a wait step.

	- Select the plus sign after the first email. Select **Wait for**.

	- In the **Wait for** pane on the right, select the following: 

		1. **Duration**: Select 1 hour.

			1. Note: In a real-world campaign, this would typically be set to a longer duration such as 3 days or 1 week. You are setting to 1 hour so that you will receive the email during this lab.

9. Set up the second email in the journey.

	- Select the plus sign after the segment. Select **Send an Email**.

	- In the **Email** field on the right, select **[my prefix] Cross Sell Campaign Email 2**.

	- Expand the **Email elements** tab and select **+ Add item.** Select **Form**. In the lookup field, choose **[my prefix] Cross Sell Campaign** **Form**.

10. Add an if/then condition. 

	- After email 2, click the plus sign. Select **If/Then**.

		1. In the **Conditions** field, select **[my prefix] Cross Sell Campaign Form**.

		2. In the **Select a condition** field, select **have registration**.

		3. **Wait up to** 7 days.

11. Set up the Yes path. 

	- In the **Yes** branch, click the plus sign. Select **Send an email**.

		1. In the **Email** field on the right, select **[my prefix] Cross Sell Campaign Email 3**.

    - After the email, click the plus sign. Select **Task**. 
    
    	1. In the **Task** field, select **Follow up with customer**. 
    
    	2. Assign to: **Contact owner**.

12. Set up the No path. 

	- In the **No** branch, click the plus sign. Select **Send an email**.

		1. In the **Email** field on the right, **select** **[my prefix] Cross Sell Campaign Email 2**.

		2. Expand the **Email elements** tab and select **+ Add item.** Select **Form**. In the lookup field, choose **[my prefix] Cross Sell Campaign** **Form**.

    - After the email, click the plus sign. Select **If/Then**.
    
    	1. In the **Conditions** field, select **[my prefix] Cross Sell Campaign Form**.
    
    	2. In the **Select a condition** field, select **have registration**.
    
    	3. **Wait up to** 1 hour.
    
    	4. In the **Yes** branch, click the plus sign. Select **Send an email**.
    
    		1. In the **Email** field on the right, select **[my prefix] Cross Sell Campaign Email 3**.
    
        5. After the email, click the plus sign. Select **Task**.
        
        	1. In the **Task** field, select **Follow up with customer**. 
        
        	2. Assign to: **Contact owner**.

13. **Save**.

14. **Check for errors**. Correct any as needed. Note: You will receive a warning that the journey uses 1 or more emails multiple times and that it starts in the past. These are OK and your journey will still go live.

15. **Go live**.  
‎

# Exercise 2: Interact with the outbound campaign components

Note: You will need to wait one hour after going live with the customer journey before completing this exercise. This will give time for the first and second emails within the journey to go out.

1. Navigate to your email account. 

2. Locate the email from **Contoso Insurance** with a subject line of **Ensure all aspects of your business are covered**. (You may need to check your junk folder.) 

	- Open the email. Click one or two links within the email.

3. Locate the second email from **Contoso Insurance** with a subject line of **Is your business fully covered?**

	- Open the email. Click the CTA button.

	- Fill out the form.

		1. In the **First Name** field, enter the same name as the contact record you created in Lab 2.1.

		2. In the **Last Name** field, enter the same name as the contact record you created in Lab 2.1.

		3. In the **Email** field, enter the same email as the contact record you created in Lab 2.1.

		4. In the **Company Name** field, enter a fictitious company name.

		5. In the **Job Title** field, enter the same title as the contact record you created in Lab 2.1.

		6. In the **Industry** field, select Transportation or Financial.

		7. Click **Submit**.

4. Locate the third email from **Contoso Insurance** with a subject line of **Thanks for contacting us!**

	- Open the email.

