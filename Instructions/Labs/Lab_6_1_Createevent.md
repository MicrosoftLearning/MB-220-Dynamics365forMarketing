---
lab:
    title: 'Lab 6.1: Create an event'
    module: 'Module 6: Manage events'
---

# Module 6: Manage events

## Practice Lab 6.1: Create an event

# Lab Overview

## Scenario

Contoso Insurance wants to host a Business Appreciation Event as a thank you to their business customers. They plan to use Dynamics to manage the entire event process including planning, registration, and post-event follow up.

The event will take place next month at the Coho Winery in Seattle.

They plan to send an invitation email, a confirmation email for those that register, and a follow up email with a link to a survey to those that attend the event.

For this event, the Marketing Coordinator will need to:

- Create two segments – one for the invitees and one for the event attendees.

- Use Customer Voice to create a survey to gather feedback about the event.

- Create three marketing emails – an invitation, a confirmation, and a post-event follow up email with a link to a survey.

- Create a customer journey that will automate the delivery of the event content.

## Lab Overview

This lab comprises of seven exercises:

- In the first exercise, you will create the event record.

- In the second exercise, you will create the segments needed to invite contacts to the event and follow up with attendees after the event.

- In the third exercise, you will create a survey that will be sent to those that attended the event.

- In the fourth exercise, you will create the emails needed for the event.

- In the fifth exercise, you will create the customer journey to send the event communications.

- In the sixth exercise, you will register for the event.

- In the seventh exercise, you will check-in event attendees.

- In the eighth exercise, you will fill out a survey.

## What You’ll Need

- A computer with a Dynamics 365 Marketing environment

## Exercise 1: Create an in-person event

 

1. Log into Dynamics 365 Marketing.

2. Navigate to the **Events** work area.

3. Navigate to **Events** under the **Event** group.

4. Click **+New** to create a new event.

	- **Event name**: [my prefix] Contoso Insurance Business Appreciation Event. 

	- **Event type**: Demonstration.

	- **Event time zone**: Pacific.

	- **Event start date/time**: One month from today 6:00 PM.

	- **Event end date/time**: One month from today 8:00 PM.

	- In the **Location** section, in the **Building** field, select Coho Winery.

	- In the **Room** field, select St. Croix Room.

	- In the **Venue constraints** section, verify the **capacity** is set to 50.

	- Click **Save**.

5. Add a speaker to the event.

	- Navigate to the **Agenda** tab.

	- Scroll down the page to the **Speaker engagement** area.

	- Click **+ New Speaker Engagement**. 

	- On the flyout, in the **Name** field, enter Dean Halstead.

	- In the **Speaker** field, search for and select Dean Halstead.

	- Click **Save and Close**.

6. Update the event website.

	- Navigate to the **Website and form** tab.

	- Click the magnifying glass in the **Event image** field. Locate and select the coho-vineyard image then click **Select**.

	- Change **Enable CAPTCHA** to No.

7. **Save** the event record.

8. Click **Go Live** in the command bar.

9. After the event finishes going live, open the **Event URL**.

10. Review the details of the event.

## Exercise 2: Create the segments

1. Log into Dynamics 365 Marketing.

2. Navigate to the **Marketing** work area.

3. Navigate to **Segments** under the **Customers** section.

4. Create a segment for the event invitees.

	- Select **+New** and choose **+New Dynamic Segment.**

	- When prompted to select a template, click **Skip.**

	- Name the segment **[my prefix] Business Appreciation Event Invitees**.

	- Select **Add Query Block.** (If a pop-up appears, close it.) 

	- In the first field, the **Contact** entity should be selected. If it is not, change the query entity to **Contact**. 

		- Create the following condition: **Address 1: City contains Seattle**.

		- Click **+ Add** then choose **Add condition to Contact**. 

			1. Select **Or** for the operator.

			2. Create the following condition: **Address 1: City contains Redmond**.

        - Click **+ Add** then choose **Add condition to Contact**. 

        	1. Select **Or** for the operator.
        
        	2. Create the following condition: **Address 1: City contains Bellevue**.


    - Below the conditions you just created, click **Add segment block**. 
    
    	- Change the operator to **but not**. 
    
    	- Start typing your prefix into the field and select the **[my prefix] Humongous Insurance.**
    
    - Click the arrow next to **Estimate size**. Review the results. Reminder: The capacity for the venue is 50.
    
    - Click **Save** and **check for errors**. Correct any if needed.
    
    - On the toolbar, click **Go live**.
    
    - Give the system time and refresh if needed. After a few minutes, reopen the segment and navigate to the **Members** tab.
    
    - Verify you see your contact record in the list.
    
    - Click the drop down next to **Save** then click **Save &amp; Close** to return to the Segment list.
    
5. Create a segment for the event attendees.

	- Select **+New** and choose **+New Dynamic Segment.**

	- In the template gallery, select **Attended an event** then click **Select**.

	- Name the segment **[my prefix] Business Appreciation Event Attendees**.

	- Under **Check-in**, in the event lookup field, select **[my prefix] Contoso Insurance Business Appreciation Event**.

	- Click **Save** and **check for errors**. Correct any if needed.

	- On the toolbar, click **Go live**.

 

# Exercise 3: Create the survey

1. Open a new tab in your browser.

2. Log into Customer Voice.

3. Customer Voice is composed of projects and surveys. All surveys must reside under one project.

4. Each user will see a personal dashboard specific to the user. No one else has access to your project/surveys.

5. Click **+ New project** to begin.

6. From the project template gallery, select the **Periodic customer feedback** template. Click **Next** on the bottom left of your screen. 

7. Click **See all environments.** Select the same environment as the marketing app. To determine which environment to correct, compare the URL in the pop-up window within Customer Voice with the URL of the marketing app. Ask your instructor if you are unsure which environment to select.

8. Click **Create**.

9. On left side you will see the name of the Project - Periodic customer feedback, the **Surveys** area, which shows all the surveys for that project, including the new one you just created, and the **Reports** area, which shows all the reports for the surveys within that project.

	- In the **Surveys** section, click the vertical ellipsis next to **Periodic customer feedback** then select **Rename**. Rename **to [my prefix] Business Appreciation Event Survey**. Click **Rename**.

	- This is the name you will search for when linking your survey to other marketing content for the event.

10. Click into the header of the survey. Change headline to **Contoso Insurance Business Appreciation Event Feedback.** Highlight the text then change the size to **26px** and the color to **white**. Click out of the header.

11. Hover over the header. A menu will appear on the left of the header with options. Click **Theme color.** Type in this hexadecimal color **#0076AD.**

12. Expand the **Customizations** menu on the right.

	1. Click **Satisfaction metrics.**

		- Click **Add metric** and choose **Sentiment.**

		- Click **Choose question** and select 3. What additional feedback would you like to share with us?

		- Click **Save.**

		- Close the Satisfaction metrics window.

    2. Click **Branching**.
    
    	- Click **Customize.**
    
    	- Name the rule **Satisfaction alert.** 
    
    	- Click **+Add condition.**
    
    	- Select the question: How would you rate your overall satisfaction with our company?
    
    	- In the operator area, from the drop down select is less than. 
    
    	- In the select response drop down, choose 3.
    
    	- Click **Save.**
    
    	- Close the Advanced logic window.
    
    3. Click **Branding**.
    
    	- Expand the Fonts menu.
    
    	- Change your **Header font** and **Body font** to Segoe UI.
    
    	- Close the Branding window.
    
    4. Click **Formatting**.
    
    	- Turn off **Progress bar.**
    
    	- Turn on **Shuffle questions.**
    
    	- Close the Formatting window.

13. Choose the first question.

	- Rename to: How would you rate the event?

	- Change 1 Star to: Okay

	- Change 5 Stars to: Great!

	- Click out of the question to save.

14. Delete the second question (Based on your experience with our company…)


15. Add a new question.

	- Click **+Add new.**

	- Choose **Rating.**

	- Question name: How would you rate the date and time of the event?

	- Mark as **required.**

	- Click the 3 dots to see more settings then select **Label**.

	- 1 Star: Okay

	- 5 Starts: Great!

	- Click out of the question to save.

16. Add a new question.

	- Click **+Add new.**

	- Choose **Rating.**

	- Question name: How would you rate the location of the event?

	- Mark as **required.**

	- Click the 3 dots to see more settings then select **Label**.

	- 1 Star: Okay

	- 5 Starts: Great!

	- Click out of the question to save.

17. Add a new question.

	- Click **+Add new.**

	- Choose **Choice.**

	- Question name: What did you think about the event length?

	- Mark as **required.**

	- Option 1: Too long

	- Option 2: Too short

	- Click **+ Add option.**

	- Option 3: Just right

	- Click out of the question to save.

18. Select “What additional feedback would you like to share with us?” and move to the end of the survey by clicking the down arrow until it appears at the end.

	- Click out of the question to save.

19. Your survey is automatically saved and is now available for selection in Dynamics 365 Marketing areas such as emails and journeys.

20. Click **All Projects** on the left menu.

21. Locate the **Periodic customer feedback** project. Click the vertical ellipsis next to **Periodic customer feedback** then select **Rename**. Rename to **Post Event Surveys**. Click **Rename**.

 

# Exercise 4: Create the marketing emails

1. Log into Dynamics 365 Marketing.

2. Create event email #1.

	- Navigate to **Marketing emails** under the **Marketing execution** group.

	- Open **[my prefix] Cross Sell Campaign Email 3**.

	- Click the drop down next to **Save** then choose **Save as**.

	- **Name**: [my prefix] Business Appreciation Event Invite.

	- **Subject:** You’re invited!

	- Click **Save and Close**. A pop up will appear at the bottom of the email that says Your changes were saved. Click View record to open the new email. Otherwise navigate to the Marketing emails list and open **[my prefix] Business Appreciation Event Invite**.

	- Change the image to: coho-vineyard

	- Update the alt text for the image to: Coho Vineyard

	- Change the header to: Hi {{contact.firstname}}, 

	- Change the body to:

            We appreciate your business and, as a thank you, want to invite you to a special Business Appreciation Event.
            
            Join us at the beautiful **Coho Winery** for cocktails and dinner.
            
            **July 15, 2021 6:00 PM - 8:00 PM**

    - Add a button below the text.
    
    	- **Link to**: Event
    
    	- **Event**: Click **Change View**. Choose **My Active Events.** Select [my prefix] Contoso Insurance Business Appreciation Event
    
    	- **Button text**: REGISTER NOW
    
    	- **Font**: Segoe UI
    
    	- **Font size**: 18 px
    
    	- **Button color**: #1a658c
    
    	- **Outer spacing** **– Top**: 20px
    
    - Make any other changes as desired.
    
    - **Save**.
    
    - **Preview** the email.
    
    - **Go live**. Correct any errors if needed.

3. Create event email #2.

	- While **[my prefix] Business Appreciation Event Invite** email is still open, click the drop down next to **Save** then choose **Save as**.

	- **Name**: [my prefix] Business Appreciation Event Confirmation.

	- **Subject:** Thanks for registering!

	- Click **Save and Close.**

	- Open the email.

	- Change the image to: reserved

	- Update the alt text for the image to: Reserved image

	- Change the header to: Thanks for registering!

	- Change the body to:

 
            We look forward to seeing you at our upcoming Business Appreciation Event.                     
            
            **Coho Winery**
            
            **July 15, 2021 6:00 PM - 8:00 PM**

    - Update the button.
    
    	- **Link to**: Add to calendar
    
    	- What should be added to calendar: Only the event
    
    	- **Event**: [my prefix] Contoso Insurance Business Appreciation Event
    
    	- **Button text**: ADD TO CALENDAR

    - Make any other changes as desired.
    
    - **Save**.
    
    - **Preview** the email.
    
    - **Go live**. Correct any errors if needed.

4. Create event email #3.

	- While **[my prefix] Business Appreciation Event Confirmation** email is still open, click the drop down next to **Save** then choose **Save as**.

	- **Name**: [my prefix] Business Appreciation Event Thank You.

	- **Subject:** Thanks for attending our Business Appreciation Event!

	- Click **Save and Close.**

	- Open the email.

	- Change the image to: thank-you

	- Update the alt text for the image to: Thank you image

	- Remove the header text

	- Change the body to:

 

            Hi {{contact.firstname}},            
            
            Thanks for attending our Business Appreciation Event. We value your business and hope this event was a great way of showing our appreciation. If you don’t mind, please take a few minutes to fill out this brief survey so that we can further improve future events such as this one.            
            
            We look forward to continuing helping you with all your insurance needs!

    - Update the button.
    
    	- **Link to**: Survey
    
    	- **Event**: [my prefix] Business Appreciation Event Survey
    
    	- **Button text**: TAKE SURVEY
    
    - Make any other changes as desired.
    
    - On the toolbar, click **Save**.
    
    - **Preview** the email.
    
    - On the toolbar, click **Go live**. Correct any errors if needed.

 

# Exercise 5: Create the customer journey

The journey will have two tracks - the first will include the invitation and confirmation emails. The second track will include the post-event email with the link to the survey. 

1. Log into Dynamics 365 Marketing.

2. Navigate to **Customer Journeys** under the **Marketing execution** group.

3. Click **+New.** Select **Skip** from the list of customer journey templates.

4. Navigate to the **General** tab.

	- **Name** the journey [my prefix] Business Appreciation Event Journey.

	- Ensure **Target** is set to Contact.

	- Set the **Start date and time** to today’s date 1 hour ago.

	- Set the **End date and time** to 3 days after the event end date.

	- Set the **Time zone** to your time zone.

	- Change the **Content settings** to Business Content Settings. 

	- Save your changes.

5. Switch back to the **Designer** tab.

6. Define the first track for the customer journey.

	- Click **Set audience.** On the properties pane on the right, in the un-named field under Inclusion, click on the magnifying glass. Select **[my prefix] Business Appreciation Event Invitees**.

	- Click on the plus sign between Start and End arrows. Select **Send an email** from the menu.

	- Click the **Send an email** tile. On the properties pane on the right, in the email field, click on the magnifying glass. Select the **[my prefix] Business Appreciation Event Invite**.

		- Expand the **Email elements** tab and select **+ Add item.** Select **Event**. In the lookup field, choose **[my prefix] Contoso Insurance Business Appreciation Event**.

    - Click on the plus sign next to **Send an email.** Select **If/then** from the menu.
    
    - Click the **If/then** tile.
    
    	- In the **Conditions** field, select **[my prefix] Contoso Insurance Business Appreciation Event**.
    
    	- In the **Select a condition** field, select **has been registered**.
    
    	- **Wait up to** 7 Day.
    
    - In the **Yes** branch, click the plus sign. Select **Send an email**.
    
    	- In the **Email** field on the right, select **[my prefix] Business Appreciation Event Confirmation**.
    
    - In the **No** branch, click the plus sign. Select **Send an email**.
    
    	- In the **Email** field on the right, select **[my prefix] Business Appreciation Event Invite**.
    
    	- Expand the **Email elements** tab and select **+ Add item.** Select **Event**. In the lookup field, choose **[my prefix] Contoso Insurance Business Appreciation Event**.
    
    	- Click on the plus sign next to **Send an email.** Select **If/then** from the menu.
    
    	- Click the **If/then** tile.
    
    		1. In the **Conditions** field, select **[my prefix] Contoso Insurance Business Appreciation Event**.
    
    		2. In the **Select a condition** field, select **has been registered**.
    
    		3. **Wait up to** 7 Day.
    
    - In the **Yes** branch, click the plus sign. Select **Send an email**.
    
    	1. In the **Email** field on the right, select **[my prefix] Business Appreciation Event Confirmation**.`

7. Define the second track for the customer journey.

	- Below the audience tile, click **+ Add swimlane.**

	- Click **Set Audience.** On the **properties** pane on the right, in the un-named field under **Inclusion**, click on the magnifying glass. Select **[my prefix] Business Appreciation Event Attendees**.

	- Click on the plus sign between Start and End arrows. Select **Wait until** from the menu.

	- Click the **Wait until** tile. Choose today’s date, on the closest ½ hour from now.

		- Note: In an actual event campaign, you would set this to the day after the event. You are setting it to today so that you will receive the email during this lab.

    - Click on the plus sign next to the **Wait until** tile. Select **Send an email** from the menu.
    
    - Click the **Send an email** tile. On the **properties** pane on the right, in the **email** field, click on the magnifying glass. Select the **[my prefix] Business Appreciation Event Thank You**.
    
    	- Expand the **Email elements** tab and select **+ Add item.** Select **Customer Voice survey**. In the lookup field, choose **[my prefix] Business Appreciation Event Survey**.

8. Click **Save** in the command bar. 

9. **Check for errors** and address as needed.

10. Click **Go live** in the command bar. You may receive a warning that the journey is set to start in the past, and this is OK.

# Exercise 6: Register for the event

1. Navigate to your email account. 

2. Locate the email from **Contoso Insurance** with a subject line of **You’re invited!**

	- Open the email. Click the CTA button.

	- This will open the event website page.

	- Review the details of the event.

	- Click on Dean Halstead’s profile picture to display his bio.

	- Click **Register now**.

	- **First name**: enter the same name as the contact record you created in Lab 2.1.

	- **Last name**: enter the same name as the contact record you created in Lab 2.1.

	- **Email address**: enter the same email as the contact record you created in Lab 2.1.

	- Click **Check out**.

3. Navigate to your email account. 

4. Verify you receive a new email from **Contoso Insurance** with a subject line of **Thanks for registering!**

	- Open the email.

	- Click the **Add to calendar** CTA.

	- Verify a browser opens with an ics file for download. Open the ics file and review the invitation details.

	- Note: This will only work in Outlook. The Add to calendar functionality does not currently work for other email clients such as Gmail.

# Exercise 7: Check in event attendees

The day of the event, a representative from Contoso Insurance would check in attendees as they arrive to the event. There are two ways to check-in attendees – manually or by scanning a QR code. For this exercise, you will be checking the attendees in manually.

1. Log into Dynamics 365 Marketing.

2. Navigate to the **Events** work area.

3. Navigate to **Events** under the Event group.

4. Open **[my prefix] Contoso Insurance Business Appreciation Event**.

5. Navigate to the **Registration and attendance** tab. Scroll down to the **Event registrations** area to see who has registered.

6. On the left, under the checkmark icon, click next to the attendee you want to check in. A checkmark will appear, and the record will be highlighted blue.

7. Click **Check in registrations**. A box will appear and ask if you want to check in the selected registrations. Select **OK**.

8. Scroll down the page to the **Event Check-ins** section and verify you see the check-in record.

# Exercise 8: Fill out a survey

1. Navigate to your email account. 

2. Locate the email from **Contoso Insurance** with a subject line of **Thanks for attending our Business Appreciation Event!**

	- Reminder: You set a wait step prior to the send of this email within the customer journey, so if you don’t see the email yet, it may not have sent yet. You can log back into Dynamics, navigate to the customer journey, click on Business Appreciation Follow Up email 

3. Open the email. Click the CTA button.

4. Fill out the survey.
