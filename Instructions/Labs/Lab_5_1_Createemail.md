---
lab:
    title: 'Lab 5.1: Create a marketing email'
    module: 'Module 5: Manage marketing emails and customer journeys'
---

# Module 5: Manage marketing emails and customer journeys

## Practice Lab 5.1: Create a marketing email

# Lab Overview

## Scenario

For this campaign, the marketing team wants to upsell current customers with additional services. They plan to send a three-email series. The first email will promote some of the company’s more specialized offerings. The second email is intended to encourage customers to visit a marketing page and fill out a marketing form. The third email is a confirmation email once the form has been submitted.

## Lab Overview

This lab compromises of one exercise:

1. In this exercise, you will create a marketing email using an email template.

2. In this exercise, you will create a marketing email by copying another email.

3. In this exercise, you will create a marketing email by copying another email.

## What you’ll need:

- A computer with a Dynamics 365 Marketing environment

# Exercise 1: Create an email from a template

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing emails** under the **Marketing execution** group. 

3. Click **+New** to create a new email.

4. From the template gallery, select **2 column layout**.

5. In the upper left corner, name the email **[my prefix] Cross Sell Campaign Email** 

6. Select the **From Name/Subject** box in the designer to display the **Email** header details on the right.

	- Type the following in the **Subject**: “Ensure all aspects of your business are covered”.

	- Expand **Send settings**. Change the **From name** to Contoso Insurance.

7. Click anywhere on the sides of the email in the designer to display the **Toolbox**. In the **Toolbox**, switch to the **General styles** tab.

	- Note: The details in this section affect the entire email. If you add new text elements to the email, it will default to the font, size and color listed here. You can then updated those elements as needed.

	- Change the **Font family** to Segoe UI. 

	- Change the **body text color** to: #404040.

	- Change the **email background** color to #CCCCCC.

8. Select the first section.

	- When you select, it will default to the column, click the arrow icon to go up to the section. Change the **Section background color** to white.

9. Update the logo column. 

	- Select the column with the logo. Expand the **Spacing** section. Change the **Left** **Inner spacing** to 20px. Set the others to 10 px.

	- Select the image on the designer.

	- On the right, click the placeholder image, select **Replace** then choose **Browse library**.

	- Select the **contoso-insurance-logo** then click **Select**.

	- On the right, click the **Link to** drop down then select **URL** then enter [www.microsoft.com](http://www.microsoft.com/).

	- In the **Size and alignment** section, if **Auto width** is checked, uncheck it. Enter **150px** by **50px**. Note you may have to click the unlink icon between width and height to set both.

10. Update the Date column.

	- Select the column with the **Date** text. Expand the **Spacing** section. Uncheck **Set equal for all sides**. Change the **Top** and **Right Inner spacing** to 20px.

	- Highlight **Date** in the top right column then type “View in browser”. Highlight View in browser then click the **link icon** in the text toolbar.

	- In the **Link** field, click on the assist edit icon **{ }**.

	- Under **Dynamic content**, select **Message** in the **entity** field. 

	- Select **No relationship** in the next field then **ViewAsWebpageURL** in the last field

	- Click **Insert**. Click **OK**.

	- Change the **font size** to 14px.

11. Select the text section below the logo. 

	- Navigate to the section. 

	- Change the **Section background color** to white.

	- Expand the **Spacing** section. Change the **Inner spacing** to 20px.

	- Update the header text.

		1. Put your cursor at the start of the header text then click the **{ Personalization }** icon in the toolbar.

			1. Under **Dynamic content**, select **Contact**. 

			2. Select **No relationship**.

			3. Select **First Name**.

			4. Click **Insert**.

			5. Add a **comma** and a space after {{contact.firstname}},

        2. Change “A short headline goes here to: “**we’ve got you covered**.” 
        
        3. Highlight the text, make it **bold** and change the **font size** to 26.
        
    - From the **Toolbox**, drag a **Divider** below {{contact.firstname}}, we’ve got you covered. 
        
		1. Change the size to **10px**.
	
		2. Click the **color selector** then select **Custom**. Change **Transparency** to 100. 
        
    - Change “This section is perfect….” to “With customized packages, we have insurance options to protect all aspects of your business.”
        
    - Highlight the text and change the **font size** to 18.

12. Select the two-column section below the text.

	- Navigate to the section. Change the **Section background color** to white.

	- Expand the **Spacing** section. Change the **Inner spacing** to 15px.

	- In the left column, make the following updates:

		1. Select **Image placeholder**. 

			1. Navigate to the image library and select the **umbrella icon**. 

			2. Replace the **Alt text** with: Umbrella icon.

			3. In **Link to** field, select **URL**. Enter [https://dynamics.microsoft.com/en-us/marketing/overview/](https://dynamics.microsoft.com/en-us/marketing/overview/) 

			4. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 150px by 150px.

				1. Note: You may need to click the unlink icon between the width and height to be able to adjust both.

        2. Change Headline or title to UMBRELLA. **Bold** and **center** the text.

        3. Update “This content could describe…” to “An additional layer of coverage that protects your business from things that may not be included in your standard policy such as legal fees, medical bills or damage expenses.” **Center** the text.

        4. Remove the **Link text**.

    - In the right column under the sub header, make the following updates:
    
    	1. Select **Image placeholder**. 
    
    		1. Navigate to the image library and select the **computer icon**.
    
    		2. Replace the **Alt text** with: Computer icon.
    
    		3. In **Link to** field, select **URL**. Enter [https://dynamics.microsoft.com/en-us/marketing/capabilities/](https://dynamics.microsoft.com/en-us/marketing/capabilities/)
    
    		4. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 150px by 150px.
    
    			1. Note: You may need to click the unlink icon between the width and height to be able to adjust both.
    
        2. Change Headline or title to: CYBER. **Bold** and **center** the text.
        
        3. Update “This content could describe…” to “Cyber insurance protects your business from malware, cyber-attacks and data loss. If your business does anything online, then you need cyber insurance.” **Center** the text.
        
        4. Remove the **Link text**.

13. Select the next two-column section.

	- Navigate to the section. Change the **Section background color** to white.

	- Expand the **Spacing** section. Change the **Inner spacing** to 15px.

	- In the left column, make the following updates:

		1. Select **Image placeholder**. 

			1. Navigate to the image library and select the stop-icon.

			2. Replace the **Alt text** with: Stop icon.

			3. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 150px by 150px.

			4. In **Link to** field, select **URL**. Enter [https://dynamics.microsoft.com/en-us/marketing/resources/](https://dynamics.microsoft.com/en-us/marketing/resources/) 

        2. Change Headline or title to: COMMERCIAL CRIME. **Bold** and **center** the text.
        
        3. Update “This content could describe…” to “Whether it’s crimes committed by someone from outside of the business or your employees, commercial crime insurance can help protect your company from significant losses due to criminal activities.” **Center** the text.
        
        4. Remove the **Link text**.

    - In the right column, make the following updates:

    	1. Select **Image placeholder**. 
    
    		1. Navigate to the image library and select the **shop icon**. 
    
    		2. Replace the **Alt text** with: Business shop icon.
    
    		3. In **Link to** field, select **URL**. Enter [https://dynamics.microsoft.com/en-us/marketing/pricing/](https://dynamics.microsoft.com/en-us/marketing/pricing/)
    
    		4. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 150px by 150px.
        
        2. Change Headline or title to: BUSINESS INTERRUPTION. **Bold** and **center** the text.
        
        3. Update This content could describe… to “An additional layer of coverage that protects your business from things that may not be included in your standard policy such as legal fees, medical bills, damage expenses, and more.” **Center** the text.
        
        4. Remove the **Link text**.

14. Delete the final two column section.

15. Select the section with the button. 

	- Navigate to the section. Change the **Section background color** to white.

	- Expand the **Spacing** section. Change the **Inner spacing** to 25px for all sides.

	- Set all **Outer spacing** to 0px.

	- Select the button.

		1. In the **Link to** field, select URL.

		2. In the **URL** field, enter [https://dynamics.microsoft.com/en-us/marketing/overview/](https://dynamics.microsoft.com/en-us/marketing/overview/) 

		3. In the **Button text** field, enter LEARN MORE.

		4. Change the **Font** to Segoe UI, size 20px.

		5. Change the **button color** to #1a658c.

		6. Expand **Size and alignment**.

		7. Change the **Width** to 275px and the **Height** to 50px.

		8. Expand **Spacing**.

		9. Uncheck the box next to **Outer spacing**. Change the **Bottom** spacing to 40px.

16. Select the section with the social icons.

	- Navigate to the section. Change the **Section background color** to white.

17. Select the section with the copyright information.

	- Navigate to the section. Change the **Section background color** to white.

	- Update the copyright from Microsoft Dynamics to Contoso Insurance.

18. Make any other changes as desired.

19. **Save**.

20. Select **Preview and test**.

	- Change the **Preview** as to **[your contact]**.

	- Change the **content settings** to: **Business Content Settings**.

	- Preview the email on all screen sizes.

21. Click **Check content**. Correct any if needed.

22. Click the arrow next to **Check** **content**. Choose both **Accessibility checker** and **Spam checker** to see if there are any other issues within the email.

23. **Go live**.

 

# Exercise 2: Create an email by copying an email

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing emails** under the Marketing execution group. 

3. Open the email you created in the Exercise 1.

4. In the command bar, click the drop-down arrow next to **Save**. Choose **Save as**.

5. In the **Quick Create** menu on the right, name the email **[my prefix] Cross Sell Campaign Email 2**.

6. In the **Subject** **field,** enter “Is your business fully covered?”

7. Click **Save and Close**. A pop up will appear at the bottom of the email that says Your changes were saved. Click **View record** to open the new email. Otherwise navigate to the Marketing emails list and open **[my prefix] Cross Sell Campaign Email 2**.

8. Select the **From Name/Subject** box in the designer to display the Email header details on the right. Expand **Send settings**. Verify the **From name** is Contoso Insurance.

9. On the designer, change the header text to: “**{{contact.firstname}}, let’s review your coverage.**” 

10. Change the copy below the header to: “From increasing your online operations to adjusting the setup of your offices, your business needs may have changed considerably this past year. Let's review your policy to ensure you are getting all the coverage you need.”

11. Remove the first two-column section.

12. Select the next two-column section.

	- Navigate to the section. Change the **Layout** from 2 to 1:2.

	- In the left column, make the following updates:

		1. Select the current image. 

			1. Navigate to the image library and select **customer-review-icon**. 

			2. Replace the **Alt text** with: Customer review icon.

			3. In the **Size and alignment** section, uncheck **Auto width**. Change the size to 100px by 100px.

			4. In the **URL** field, remove the link.

        2. Remove: COMMERCIAL CRIME.
    
        3. Remove: Whether it’s crimes committed…

    - In the right column, make the following updates:

    	1. Remove the image. 
    
    	2. Remove BUSINESS INTERRUPTION.
    
    	3. Change “An additional layer of coverage…” to:
    
            *“It's important to have a partner who understands your business. We are so pleased with our experience at Contoso Insurance. They found us the coverage we needed at a great price.”
            ‎  
            ‎-David P.  
            ‎Small Business Owner*

        4. Change the **font size** to 16 and **italicize**.

13. Update the button.

	- Select the button. 

	- Change **Link to** to Marketing page.

	- Select the marketing page you created in a previous lab.

	- Change the **Button text** to REVIEW MY COVERAGE.

	- Expand **Size and alignment**. Change the width to 300px. 

14. **Save**.

15. **Preview** the email.

16. Click **Check content**. Correct any errors if needed.

17. **Go live**.

 

# Exercise 3: Create an email by copying an email

1. Log into Dynamics 365 Marketing.

2. Navigate to **Marketing emails** under the Marketing execution group. 

3. Open the email you created in the Exercise 2.

4. In the command bar, click the drop-down arrow next to **Save**. Choose **Save as**.

5. In the **Quick Create** menu on the right, name the email **[my prefix] Cross Sell Campaign Email 3**.

6. In the **Subject** **field,** enter “Thanks for contacting us!”

7. Click **Save and Close**. A pop up will appear at the bottom of the email that says Your changes were saved. Click **View record** to open the new email. Otherwise navigate to the Marketing emails list and open **[my prefix] Cross Sell Campaign Email 3**.

8. Select the **From Name/Subject** box in the designer to display the Email header details on the right. Expand **Send settings**. Verify the **From name** says Contoso Insurance.

9. From the **Toolbox**, drag an **Image** element above the header. 

	- Navigate to the library and select the **agent-email-icon**.

	- Add **Alt text** with: Agent icon.

	- Leave **Auto width** On.

	- Expand the **Spacing** section. Uncheck **Set equal for all sides**. Change **Bottom** to 30px.

10. Change the header text to: “Thanks for contacting us!”

11. Change the copy below the header to: 

            We are excited to review your coverage and see what additional services may benefit your business.
            
            An agent will be contacting you shortly to schedule a review of your current coverage.

12. Remove the two-column section.

13. Move the divider in the button section below the copy. Expand the **Spacing** section. Change the **Top** spacing to 40px.

14. Remove the **button** section.

15. **Save**.

16. **Preview** the email.

17. Click **Check content**. Correct any errors if needed.

18. **Go live**.
