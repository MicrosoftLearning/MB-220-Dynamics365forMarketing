---
lab:
    title: 'Lab 5.3: Create marketing websites and redirect URLs'
    module: 'Module 5: Manage emails and journeys in outbound marketing'
---

# Module 5: Manage emails and journeys in outbound marketing

## Practice Lab 5.3: Create marketing websites and redirect URLs

# Lab Overview

## Scenario

Once a customer or prospect submits the form for the Cross Sell Campaign, the marketing team wants to redirect the customer to a webpage on the Contoso Insurance website. Since this page is native to their CMS system, they would like to track analytics from this page within Dynamics. 

The Marketing Coordinator will start by creating a marketing website for the product page on their website. This will allow the marketing team to view insights on it.

# Lab Overview

This lab compromises of one exercise:

1. In exercise one, you will create a form and host it on a webpage.


## What you’ll need:

- A computer with a Dynamics 365 Marketing environment

# Exercise 1: Create a marketing website

1. Log into Dynamics 365 Marketing. Ensure you are in the **Real-time marketing** section.

2. Navigate to **Forms** under the **Channels** group.

3. Click **+New** to create a new form.

4. Name the form **Contoso Insurance Product Page**. Select **Contact** as the target audience.

6. Click **Create.**

# Exercise 2: Create a redirect URL

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing pages** under the **Internet marketing** group.

3. Open the marketing page created in the previous lab. 

4. Navigate to the **Summary** tab. Copy the **Full page URL**.

5. Navigate to **Redirect URLs** under the **Internet marketing** group.

6. Create a new **redirect URL**.

7. Name the redirect URL **Contoso Insurance Product Page Redirect**.

8. In the **Original URL** field, copy and paste this URL: [https://dynamics.microsoft.com/en-us/marketing/overview/](https://dynamics.microsoft.com/en-us/marketing/overview/)

9. Save your changes.

10. Copy the **Redirecting URL** and paste somewhere for you to use in the next exercise.

# Exercise 3: Add the redirecting URL to the marketing form

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing pages** under the **Internet marketing** group.

3. Open the marketing page created in the previous lab. 

4. Click **Edit** in the command bar. Click **OK** in the pop up.

5. Select the form. In the **Properties** on the right, paste the redirect URL record you copied from the previous exercise into the **Redirect URL** field.

6. Save your changes.

7. Navigate to the **Summary** tab. Open the **Full page URL**.

8. Fill out the form using the following details.

	- **First Name**: Enter a fictious name.

	- **Last Name**: Enter a fictious name.

	- **Email**: Enter a fictious email.

	- **Company**: Enter a fictious company name.

	- **Title**: Select any.

	- **Industry**: Select any.

	- Click **Submit**.

9. After you submit, ensure the redirect URL takes you to: [https://dynamics.microsoft.com/en-us/marketing/overview/](https://dynamics.microsoft.com/en-us/marketing/overview/).

10. Return to Dynamics 365 Marketing.

11. Select **Leads** under the **Lead management** group. 

12. You should see the lead in the view.

	- Note: It may take a few minutes to show up. Refresh the page after a few minutes if your lead is not showing.
