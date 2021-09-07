---
lab:
    title: 'Lab 3.2: Create marketing websites and redirect URLs'
    module: 'Module 3: Manage marketing forms and pages'
---

# Module 3: Manage marketing forms and pages

## Practice Lab 3.2 - Create marketing websites and redirect URLs

# Lab Overview

## Scenario

Once a customer or prospect submits the form for the Cross Sell Campaign, the marketing team wants to redirect the customer to a webpage on the Contoso Insurance website. Since this page is native to their CMS system, they would like to track analytics from this page within Dynamics. They would also like to set up a redirect URL from the form submission on the Cross Sell Campaign marketing page to the website page so that they can view how the traffic is originating to that page.

The Marketing Coordinator will start by creating a marketing website for the product page on their website. This will allow the marketing team to view insights, including referring URL, from the product page within Dynamics.

Next, the Marketing Coordinator will create a redirect URL that will be used on the form for the Cross Sell Campaign marketing page in Dynamics. This URL will drive traffic to the product page on Contoso Insurance's website and they will be able to view the referring URL within Dynamics. 

Finally, the Marketing Coordinator will add the redirect URL to the marketing form for the Cross Sell Campaign. Anyone who submits the form will be redirected to the product page on Contoso Insurance's website. The marketing team will then be able to see these insights in Dynamics.

# Lab Overview

This lab compromises of three exercises:

1. In exercise one, you will create a marketing website.

2. In exercise two, you will create a redirect URL.

3. In exercise three, you will add the redirecting URL to the marketing form on the marketing page created in the previous lab.

## What you’ll need:

- A computer with a Dynamics 365 Marketing environment

# Exercise 1: Create a marketing website

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing websites** under the **Internet marketing** group.

3. Click **+New** to create a new website.

4. Name the website **[my prefix] Contoso Insurance Product Page**.

5. In the **URL** field, copy and paste this URL: [https://dynamics.microsoft.com/en-us/marketing/overview/](https://dynamics.microsoft.com/en-us/marketing/overview/)

6. Save your changes.

7. After saving, JavaScript and Form capture code will be generated for the website. 

	- Note: The next step would be to send the code to a web master for the Contoso Insurance website to embed on the webpage that will be tracked in Dynamics. Once added, the Insights tab will display analytics such as Contact name (if the visitor is a known contact), page address, referrer URL, visit duration, and timestamp.

# Exercise 2: Create a redirect URL

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing pages** under the **Internet marketing** group.

3. Open the marketing page created in the previous lab. 

4. Navigate to the **Summary** tab. Copy the **Full page URL**.

5. Navigate to **Redirect URLs** under the **Internet marketing** group.

6. Create a new **redirect URL**.

7. Name the redirect URL **[my prefix] Contoso Insurance Product Page Redirect**.

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
