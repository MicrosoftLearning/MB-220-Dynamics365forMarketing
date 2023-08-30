---
lab:
    title: 'Lab 3.1: Create a form'
    module: 'Module 3: Manage forms'
---

# Module 3: Manage forms

## Practice Lab 3.1 - Create a form

# Lab Overview

## Scenario

For the cross-sell campaign, the marketing team wants to direct contacts to a webpage with a form. The purpose of the page will be to encourage business customers to fill out the form to schedule a review of their current coverage and learn about additional services available.

The Marketing Coordinator will start by creating the form. Then, they will configure the form hosting.

## Lab Overview

This lab compromises of two exercises:

1. In exercise one, you will create a form.

2. In exercise two, you will host the form.

## What you’ll need:

- Access to a Dynamics 365 Customer Insights - Journeys environment.


# Exercise 1: Create a form

1.  Log into Dynamics 365 Customer Insights - Journeys. Change the work area to **Real-time marketing** if you are not already in that area.

2.  Navigate to **Forms** under the **Channels** group.

3.  Select **+ New** to create a new form. Name the form **Cross Sell Campaign Form** and select **Lead** as the target audience. Click **Create.**

4.  The form designer will open, and available fields will appear in the right menu.
- Drag the **First Name** field onto the form. (You can use the search box to search for the field instead of scrolling.)
 - Return to **Fields**. Next, drag **Last Name** below First Name.
 - Return to **Fields.** Drag **Email** below Last Name.
 - Below Email, add three more fields: **Company Name, Job Title,** and **Industry (option set)**.

5. Select the **Industry** field on the form. In the Placeholder text field, enter "Select industry...".

10. Switch to the **Elements** section. Drag the **Submit** button below Email.
	- Change the font size from 16px to 20px.
	- Change Rounded corners to 6px.
	- Change Border to dotted.

13. Make the following updates to the First Name, Last Name, Email, Company Name, and Job Title fields:
	- Remove the Placeholder text.
	- Set **Required** to Yes.

15. Preview the form by selecting the **Preview and test** tab at the top of the form designer.

16. **Save** the record and select **Check content** in the toolbar. Correct any errors if needed. 

12. Select **Publish**. Do not navigate away from the screen.

# Exercise 2: Host the form

A pop-up window will appear with two options for publishing your form. In this exercise, we will publish the form as a standalone page.

1. Select **Create** under Create new standalone page.

2. The creation process may take a second.

3. When your page is published, a URL will appear. Select **Open in new tab.**

4. Fill out the form for a new lead.
	- Under First Name, enter **John.**
	- Under Last Name, enter **Doe.**
	- Under Email, enter **johndoe@alpineskihouse.com.**
	- Under **Company**, enter **Alpine Ski House.**
	- Under **Job Title,** enter **Account Manager.**
	- Under **Industry,** select **Entertainment Retail.**

5. Select **Submit.**

6. You can now close the tab.
7. Back in the **Real-time marketing** section, navigate to **Forms** in the **Channels** section.
8. Select the **Cross-Sell Campaign Form**. Navigate to the **Submissions** tab.
9. You should now see **John Doe** as a submission. Select John Doe to navigate to the new **Lead** record.
