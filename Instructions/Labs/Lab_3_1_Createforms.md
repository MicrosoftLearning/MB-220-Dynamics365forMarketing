---
lab:
    title: 'Lab 3.1: Create a form'
    module: 'Module 3: Create emails, forms, text messages, and push notifications'
---

# Module 3: Create emails, forms, text messages, and push notifications

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

1.  Log into Dynamics 365 Customer Insights - Journeys. Change the work area to **Real-time journeys** if you are not already in that area.

2.  Navigate to **Forms** under the **Channels** group.

3.  Select **+ New** to create a new form. Name the form `Cross Sell Campaign Form` and select **Contact** as the target audience. Select **Create**.

4.  Select **Skip**.

5.  The form designer will open, and available fields will appear in the right menu.

    - Drag the **First Name** field onto the form. (You can use the search box to find the field instead of scrolling.)
    - Return to **Fields** on the right side tabs. Next, drag **Last Name** below First Name.
    - Return to **Fields.** Drag **Email** below Last Name.

6.  Switch to the **Elements** section. Drag the **Submit** button below Email.
    - Change the **Font** size from 16px to 20px.
    - Change **Rounded corners** to 6px.
    - Change **Border** to Dotted.

7.  Make the following updates to the **First Name**, **Last Name**, and **Email** fields:
    - Remove the **Placeholder** text.
    - Set **Required** to Yes.

8.  Preview the form by selecting the **Preview and test** tab at the top of the form designer.

9.  **Save** the record and select **Check content** in the toolbar. Correct any errors if needed. 

10. Select **Publish**. Do not navigate away from the screen.


# Exercise 2: Host the form

In this exercise, we will publish the form as a standalone page.

1.  At the top of the screen, select **Publish options.** Select **Create** under **Standalone page**.

2.  **Wait** for the creation process.

3.  When the page is published, a URL will appear. Select **Open in new tab**.

4.  Fill out the form to create a new contact.
    - Under First Name, enter `John`
    - Under Last Name, enter `Doe`
    - Under Email, enter `johndoe@alpineskihouse.com`

5.  Select **Submit**.

6.  **Close** the tab.

7.  Back in the **Real-time marketing** app, select **Done**. Navigate to **Forms**, under the **Channels** group.

8.  Open the **Cross Sell Campaign Form** record. Navigate to the **Submissions** tab.

9.  Verify **John Doe** exists as a Submission. Select **John Doe** to open the new **Contact** record. 

