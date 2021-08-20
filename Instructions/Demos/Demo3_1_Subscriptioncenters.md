---
demo:
    title: 'Demo 3.1: Manage subscription centers'
    module: 'Module 1: Manage marketing forms and pages'
---


# Module 3: Manage marketing forms and pages

## Demo 3.1 – Manage subscription centers

# Demo Overview

## Scenario

The marketing team wants a separate subscription center for their business customers to be able to manage their email preferences. To do so, they need to create the marketing lists they want to appear on the subscription center, a form, and the marketing page that will host the form.

They want to ensure this subscription center is used for business-centric emails going forward. They need to create a new content settings record that will be used in business-related customer journeys.

## Lab Overview

This lab compromises of four exercises:

1. In exercise one, you will create three marketing lists for business contacts to be able to opt into or out of.

2. In exercise two, you will create a form for the business subscription center.

3. In exercise three, you will create a page for the business subscription center.

4. In exercise four, you will create a content settings record and link business subscription center to it.

## What you’ll need:

- A computer with a Dynamics 365 Marketing environment

## Exercise 1: Create subscription lists

1. Log into Dynamics 365 Marketing.

2. Navigate to **Subscription lists** under the **Customers** group. 

3. Click **+ New subscription list**.

	- Name the list **Monthly Newsletters.**

	- Click Save & Close.

4. Click **+ New subscription list**.

	- Name the list **Product Updates.**

	- Click Save & Close.

5. Click **+ New subscription list**.

	- Name the list **Special Offers.**

	- Click Save & Close.

 

## Exercise 2: Create subscription center form

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing forms** under the **Internet marketing** group. 

3. Click **+ New** to create a new form.

4. Select the **heraklion** template.

5. Click the **drop-down arrow** in the header area. Name the form **Business Subscription Center Form**. Ensure the **type** is **subscription center** and that only **contacts** are updated.

6. In the **Designer** area, update the header.

	- Change the text to: “Email Preference Center.” 

	- Change the font to Segoe UI and center align.

7. From the Toolbox, locate the **Subscription lists** section.

	- Drag **Monthly Newsletters** above **Do not email**. 

		1. Change the Default value to Subscribed. Turn Prefill to On.

		2. Highlight Monthly Newsletters. Change the font to Segoe UI and font size 16.

    - Drag **Product Updates** above **Do not email**.
    
    	1. Change the Default value to Subscribed. Turn Prefill to On.
    
    	2. Highlight Monthly Newsletters. Change the font to Segoe UI and font size 16.
    
    - Drag **Special Offers** above **Do not email**.
    
    	1. Change the Default value to Subscribed. Turn Prefill to On.
    
    	2. Highlight Monthly Newsletters. Change the font to Segoe UI and font size 16.

8. From the Toolbox, drag a **divider** between **Special Offers** and **Do not email**. Adjust the width, color, and padding as desired.

9. Highlight **Do not email**. Change the font to Segoe UI and font size 16.

10. Delete **[Update subscriptions heading]**.

11. Remove **Phone**.

12. Select **First Name**.

	- Change the font to Segoe UI.

	- Remove the placeholder value.

	- Set Required to on.

	- Add a Required error message (e.g., Something went wrong. Please try again.)

	- Turn Prefill to On.

13. Select **Last Name**.

	- Change the font to Segoe UI.

	- Remove the placeholder value.

	- Set Required to on.

	- Add a Required error message (e.g., Something went wrong. Please try again.)

	- Turn Prefill to On.

14. Select **Email**.

	- Change the font to Segoe UI.

	- Remove the placeholder value.

	- Set Required to on.

	- Add a Required error message (e.g., Something went wrong. Please try again.)

	- Turn Prefill to On.

15. Make any other updates as desired.

16. **Save** and **check for errors**. Correct any if needed.

17. **Go live**.

## Exercise 3: Create subscription center page

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing pages** under the **Internet marketing** group. 

3. Click **+ New**. Click **Skip** in the template dialog box. 

4. Click the dropdown in the upper right corner. 

	- Name the page **Business Subscription Center.**

	- In the **Type** field, select **Subscription center**.

	- In the partial URL field enter **businessmanagesubscriptions**.

5. From the **Toolbox**, drag and drop an **Image** block. With the image block selected, click the magnifying glass icon under **Image source** in the **Properties** tab. Select **Contoso Insurance logo** and ensure that **Left** is selected for **Alignment**.

6. Add a **divider** below the logo. Change the color to white and add 10px padding to the top and bottom.

7. Add a **form** **block** below the **divider**. Select the **Business Subscription Center Form** you created in the previous exercise. Input the following:

	- **Success notification**: Thank you. Your submission has been received.

	- **Error message**: Something went wrong. Please try again.

	- **Redirecting URL**: http://www.contoso.com

8. **Save** and **check for errors**. Correct any if needed.

9. **Go live**. (If you receive a pop-up, click **OK**.)

## Exercise 4: Create content settings record

1. Log into Dynamics 365 Marketing.

2. Navigate to **Content Settings** under the Templates group 

3. Click **+ New**. 

4. Update the following:

	- **Name**: Business Content Settings

	- **Address main**: 4567 Main St., Seattle, WA 98052

	- **LinkedIn URL**: [https://www.linkedin.com/company/contoso12345/about/](https://www.linkedin.com/company/contoso12345/about/)

	- **Twitter URL**: [https://twitter.com/ContosoInc](https://twitter.com/ContosoInc)

	- **Facebook URL**: [https://www.facebook.com/Contoso-102137176602590/](https://www.facebook.com/Contoso-102137176602590/)

5. In the **Subscription center** field, click the **Personalization** icon.

	- Choose **Static** content.

	- Select **MarketingPage**.

	- Search for the **Business Subscription Center** page you created in the previous exercise.

	- Select **No relationship**.

	- Select **msdyncrm_full_page_url**.

	- Click **Insert**.

- **Save** and **check for errors**. Correct any if needed.

- **Go live**.
