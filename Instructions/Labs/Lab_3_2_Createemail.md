---
lab:
    title: 'Lab 3.2: Create an email'
    module: 'Module 3: Create emails, forms, text messages, and push notifications'
---

# Module 3: Create emails, forms, text messages, and push notifications

## Practice Lab 3.2: Create an email

# Lab Overview

## Scenario

For this campaign, the marketing team wants to upsell current customers with additional services. They plan to send a three-email series. The first email will promote some of the company’s more specialized offerings. The second email is intended to encourage customers to fill out a form. The third email is a confirmation email once the form has been submitted.

## Lab Overview

This lab compromises of one exercise:

1. In this exercise, you will create an email using an email template.

2. In this exercise, you will create an email by copying another email.

3. In this exercise, you will create an email by copying another email.

## What you’ll need:

- A computer with a Dynamics 365 Customer Insights - Journeys environment

# Exercise 1: Create an email from a template

1. Log into Dynamics 365 Customer Insights - Journeys. Ensure you are in the **Real-time marketing** area.

2. Navigate to **Emails** under the **Channels** group. 

3. Click **+New** to create a new email.

4. From the template gallery, select **1-2 column.** 

5. In the upper left corner, name the email **Cross Sell Campaign Email**.

6. Select the **From Name/Subject** box in the designer to display the **Email** header details on the right.

	- Type the following in the **Subject**: “Ensure all aspects of your business are covered”.

	- Change the **From name** to Contoso Insurance.

7. In the **Toolbox**, switch to the **General styles** tab.

	- Note: The details in this section affect the entire email. If you add new text elements to the email, it will default to the font, size and color listed here. You can then updated those elements as needed.

	- Change the **Font family** to Segoe UI. 

	- Change the **body text color** to: #404040.

	- Change the **email background** color to #CCCCCC.

8. Select the first section. Change the **Section background color** to white.

9. Update the logo.

	- Select the image on the designer.

	- On the right, click the placeholder image. Select **Replace** then choose **Browse library**.

	- Select the Contoso logo then click **Select**.
	
	- Replace the **Alt text** with **Contoso icon**.

	- On the right, click the **Link to** drop down then select **URL** then enter [www.microsoft.com](http://www.microsoft.com/).

	- In the **Size and alignment** section, if **Auto width** is checked, uncheck it. Enter **150px** by **50px**. Note you may have to click the unlink icon between width and height to set both.

10. Update the image.

	- Select the image in the section below the logo.

	- Select **Replace image** and **Browse library.**

	- Select the **Hero page** image.

12. Select the text section below the logo. 

	- Navigate to the section. 

	- Change the **Section background color** to white.

	- Update the header text.

		1. Put your cursor at the start of the header text then click the **Personalization** icon in the toolbar. Select **First name** from the dropdown. Ensure **Contact** is selected and select **Choose.**

		2. Add a **comma** and a space after {{Firstname}}.

        2. Change “A short headline goes here to: “**we’ve got you covered**.” 
        
        3. Highlight the text, make it **bold** and change the **font size** to 26.
        
    - Change “Customize your email...” to “With customized packages, we have insurance options to protect all aspects of your business.”
        
    - Highlight the text and change the **font size** to 18.

13. Select the two-column section below the text.

	- Navigate to the section. Change the **Section background color** to white.

	- In the left column, make the following updates:

		1. Select **Image placeholder**. Navigate to the image library and select the **briefcase icon**. 

		2. Replace the **Alt text** with: Briefcase icon.

		3. In **Link to** field, select **URL**. Enter [https://dynamics.microsoft.com/].

		4. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 150px by 150px. (Note: You may need to click the unlink icon between the width and height to be able to adjust both.)

    - In the right column under the sub header, make the following updates:
    
    	1. Select **Image placeholder**. 
    
    		1. Navigate to the image library and select the **safebox icon**.
    
    		2. Replace the **Alt text** with: Safebox icon.
    
    		3. In **Link to** field, select **URL**. Enter [https://dynamics.microsoft.com/].
    
    		4. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 150px by 150px. (Note: You may need to click the unlink icon between the width and height to be able to adjust both.

14. Select the next two-column section.

	- Navigate to the section. Change the **Section background color** to white.

	- In the left column, make the following updates:

		1. Select **Image placeholder**. 

			1. Navigate to the image library and select the stop-icon.

			2. Replace the **Alt text** with: Stop icon.

			3. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 150px by 150px.

			4. In **Link to** field, select **URL**. Enter [https://dynamics.microsoft.com/].

16. Select the section with the social icons.

	- Navigate to the section. Change the **Section background color** to white.

17. Select the section with the copyright information.

	- Navigate to the section. Change the **Section background color** to white.

	- Update the copyright from Company Inc. to Contoso Insurance.

18. Make any other changes as desired.

19. On the toolbar, click **Save**.

20. Select **Preview and test**.

	- In the Preview personalization pane, enter the first name of the contact you created. Select the contact to watch the personalization change.

	- Preview the email on all screen sizes.

21. Click **Ready to send.** Click the notification bar to view the errors. 3 errors should be thrown:
	- From email
	- Reply to email
	- Purpose

22. Let's fix these errors and get the email ready for sending.
    - Return to the Design tab.
    - Expand the **Brand profile** section and select the **Default brand profile.**
    - From email will be filled with a default sender email for your organization's domain. 
    - Select the **Email header** section from the right pane. Under **Compliance profile,** select **Contoso Americas.** The Purpose should automatically update to **Commercial.**

24. Click the arrow next to **Check content**. Choose both **Accessibility checker** and **Spam checker** to see if there are any other issues within the email. Mitigate any other issues as you see fit. 

25. On the toolbar, click **Ready to send.**.

# Exercise 2: Create an email by copying an email

1. Log into Dynamics 365 Customer Insights - Journeys. Ensure you are in the **Real-time marketing** area.

2. Navigate to **Emails** under the Channels group. 

3. Open the email you created in the Exercise 1.

4. In the command bar, click the drop-down arrow next to **Save**. Choose **Save as**.

5. In the **Quick Create** menu on the right, name the email **Cross Sell Campaign Email 2**.

6. In the **Subject** field, enter “Is your business fully covered?”

7. Click **Save and Close**. A pop up will appear that says Your changes were saved. Click **View record** to open the new email. Otherwise navigate back to **Emails** and open **Cross Sell Campaign Email 2**.

9. On the designer, change the header text to: “**{{Firstname}}, let’s review your coverage.**” 

10. Change the copy below the header to: “From increasing your online operations to adjusting the setup of your offices, your business needs may have changed considerably this past year. Let's review your policy to ensure you are getting all the coverage you need.”

12. Select the next two-column section. Change the **Layout** from 2 to 1:2.

     -	In the left column, make the following updates:
    	1. Remove the text.
    	2. Remove the button.
     
     - In the right column, make the following updates:

    	1. Remove the image. 
    
    	2. Remove BUSINESS INTERRUPTION.
    
    	3. Change the text to:
    
            *“It's important to have a partner who understands your business. We are so pleased with our experience at Contoso Insurance. They found us the coverage we needed at a great price.”
            ‎  
            ‎-David P.  
            ‎Small Business Owner*

        4. Change the **font size** to 16 and **italicize**.

14. Update the button.

	- Select the button. 

	- Change **Link to** to URL.

	- Enter [https://dynamics.microsoft.com/].

	- Change the **Button text** to REVIEW MY COVERAGE.

	- Expand **Size and alignment**. Switch **Fit to text** to Off. Change the width to 200px. 

15. On the toolbar, click **Save**.

16. **Preview** the email.

17. Click **Check content**. Correct any errors if needed.

18. On the toolbar, click **Ready to send**.

# Exercise 3: Create an email by copying an email

1. Log into Dynamics 365 Customer Insights - Journeys. Ensure you are in the **Real-time marketing** area.

2. Navigate to **Emails** under the Channels group. 

3. Open the email you created in the Exercise 2.

4. In the command bar, click the drop-down arrow next to **Save**. Choose **Save as**.

5. In the **Quick Create** menu on the right, name the email **Cross Sell Campaign Email 3**.

6. In the **Subject** field, enter “Thanks for contacting us!”

7. Click **Save and Close**. A pop up will appear at the upper right that says Your changes were saved. Click **View record** to open the new email. Otherwise navigate to the Emails list and open **Cross Sell Campaign Email 3**.

8. Change the header text to: “Thanks for contacting us!”

9. Change the copy below the header to: 

            We are excited to review your coverage and see what additional services may benefit your business.
            
            An agent will be contacting you shortly to schedule a review of your current coverage.

10. Remove the two-column section.

11. On the toolbar, click **Save**.

12. **Preview** the email.

13. Click **Check content**. Correct any errors if needed.

14. On the toolbar, click **Ready to send**.
