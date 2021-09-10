---
lab:
    title: 'Lab 3.1: Create marketing forms and pages'
    module: 'Module 3: Manage marketing forms and pages'
---

# Module 3: Manage marketing forms and pages

## Practice Lab 3.1 - Create marketing forms and pages

# Lab Overview

## Scenario

For the cross-sell campaign, the marketing team wants to direct contacts to a marketing page with a marketing form. The purpose of the page will be to encourage business customers to fill out the form to schedule a review of their current coverage and learn about additional services available.

The Marketing Coordinator will start by creating the marketing form and then create a marketing page and add the form to the page.

## Lab Overview

This lab compromises of two exercises:

1. In exercise one, you will create a marketing form.

2. In exercise two, you will create a marketing page and embed the marketing form on the page.

## What you’ll need:

- Access to a Dynamics 365 Marketing environment

# Exercise 1: Create a marketing form

 

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing forms** under the **Internet marketing** group.

3. Click **+ New** to create a new form.

4. From the template gallery, select **rhodes**.

5. Expand the carrot next to **Draft** in the upper right corner. 

	- Name the form **[my prefix] Cross Sell Campaign Form**. 

	- Confirm the **Form Type** is **Landing page** and that it is set to update **Contacts and leads.**

6. Save your changes.

7. Navigate to the **Summary** tab. Change the **Prefill fields** field to **Yes**.

8. Navigate back to the **Designer** tab. 

9. Remove the **[Form heading].**

10. Move the **Remember me** checkbox below the **Email** field. Highlight **Remember Me** and change the font to Segoe UI and the size to 16.

11. Add the following fields to the form: Company Name, Job Title, and Industry.

	- Select **Toolbox** on the right. In the **Fields** section, click in the search box. 

	- Search for **Company Name**. Once it appears select it so that it appears with the other fields. Drag and drop the **Company Name** field below the **Email** field.

	- Select **Toolbox** on the right. In the **Fields** section, click in the search box. Search for **Job Title**. Once it appears select it so that it appears with the other fields. Drag and drop the **Job Title** field below the **Email** field.

	- Select **Toolbox** on the right. In the **Fields** section, click in the search box. Search for **Industry**. Once it appears select it so that it appears with the other fields. Drag and drop the **Job Title** field below the **Email** field.

12. Make the following updates to the form fields:

	- First Name

		1. Change **font** to Segoe UI and size to 14.

		2. Remove the **Placeholder** text.

		3. Set **Required** to on.

		4. Add a **Required error message** (e.g., Something went wrong. Please try again.)

		5. Set **Prefill** to on.

    - Last Name
    
    	1. Change **font** to Segoe UI and size to 14.
    
    	2. Remove the **Placeholder** text.
    
    	3. Set **Required** to on.
    
    	4. Add a **Required error message** (e.g., Something went wrong. Please try again.)
    
    	5. Set **Prefill** to on.
    
    - Email
    
    	1. Change **font** to Segoe UI and size to 14.
    
    	2. Remove the **Placeholder** text.
    
    	3. Set **Required** to on.
    
    	4. Add a **Required error message** (e.g., Something went wrong. Please try again.)
    
    	5. Set **Prefill** to on.
    
    - Company Name
    
    	1. Change **font** to Segoe UI and size to 14.
    
    	2. Set **Required** to on.
    
    	3. Add a **Required error message** (e.g., Something went wrong. Please try again.)
    
    - Job Title
    
    	1. Change **font** to Segoe UI and size to 14.
    
    	2. Set **Required** to on.
    
    	3. Add a **Required error message** (e.g., Something went wrong. Please try again.)
    
    - Industry
    
    	1. Change **font** to Segoe UI and size to 14.
    
    	2. Set **Required** to on.

13. Preview the form by selecting the **Preview** tab at the top of the form designer underneath the main tabs.

14. Click **Save** and click **check for errors** in the toolbar. Correct any if needed.

12. Click **Go live** in the toolbar.

 

# Exercise 2: Create a marketing page and embed a form

1. Navigate to **Marketing pages** under the **Internet marketing** group.

2. Click **+ New** to create a new page.

3. From the template gallery, select **product page 2. (Layout enabled)**

4. Expand the carrot next to **Draft** in the upper right corner. 

	- Name the page **[my prefix] Cross Sell Campaign Page**. 

	- Confirm this page is designated as a **landing page**. 

	- In the **Partial URL** field, enter **[myprefix]reviewcoverage**.

5. Save your changes.

6. Remove the **Fabrikam** text block. From the **Toolbox**, drag an **image** element where the text was. Navigate to the image gallery and select the **Contoso Insurance logo**.

7. Change About Us to Business.

8. Change Our product to Residential.

9. Remove “Articles | Try for free - >.”

10. Remove “Marketing automation”.

11. Change “A short headline goes here” to “We’ve got you covered.”

12. Change the paragraph below the headline to: “Your business is unique. Your insurance should be, too. Contoso provides a variety of insurance options that cover every aspect of your business, big or small. Our agents can review your current coverage, discuss your business goals, and recommend additional options that ensure your employees and assets are protected.”

13. From the **Toolbox**, drag an **image** element below the paragraph. Navigate to the image gallery and select **insurance-agent**. Change the Height/Width sizing to Auto.

14. Click the form block. In the **Marketing form** field, begin typing **your prefix** and select the form you created in the previous exercise. If your form does not appear, save your marketing page and navigate to your form to ensure it is **Live**.

15. Add a **text element** above the form. Add “Contact us to schedule your coverage review.” Change the font size to 18.

16. Make any other changes to the page as desired.

17. Suggested edits:

	- Remove the About Us section.

	- Remove the image section.

	- Remove the Our product section.

	- Remove the 01 Email Campaigns section.

	- Remove the Read our latest articles section.

	- Remove the 3-column section.

	- Remove the next 3-column section.

	- Remove Fabrikam.

	- Move the grey divider above Follow us on social media. Add 15px padding to the bottom of the divider.

	- Remove the menu section.

	- Update social media icon links.

		1. Select the **Facebook** icon. In the **Link** field, copy and paste [https://www.facebook.com/Contoso-Insurance-Agency-100458384785914/community/](https://www.facebook.com/Contoso-Insurance-Agency-100458384785914/community/) 

		2. Select the **LinkedIn** icon. In the **Link** field, copy and paste [https://www.linkedin.com/company/contoso/about/](https://www.linkedin.com/company/contoso/about/)

		3. Select the **Twitter** icon. In the **Link** field, copy and paste [https://twitter.com/ContosoInc](https://twitter.com/ContosoInc) 

18. Save your changes.

19. **Preview** the page.

20. Click **Save** and click **check for errors** in the toolbar. Correct any if needed.

12. Click **Go live** in the toolbar. A pop-up will show up. Click **OK**. 

22. Navigate to the **Summary** tab and open the **Full page URL** to view your page. It may take a moment for all content to appear.

23. If you would like to make changes, stop the page, make your updates. Click **Check for errors** and then click **Go live** again.
