---
lab:
    title: 'Lab 5.2: Create an event and an event journey'
    module: 'Module 5: Manage events'
---

# Module 5: Manage events

## Practice Lab 5.2: Create an event and an event journey

# Lab Overview

## Scenario

Contoso Insurance wants to host a Business Appreciation Event as a thank you to their business customers. They plan to use Dynamics to manage the entire event process including planning, registration, and post-event follow up.

The event will take place next month at the Coho Winery in Seattle.

They plan to send an invitation email, a confirmation email for those that register, and a follow up email with a link to a survey to those that attend the event.

For this event, the Marketing Coordinator will need to:

- Create two segments – one for the invitees and one for the event attendees.

- Create three emails – an invitation, a confirmation, and a post-event follow up email.

- Create a journey that will automate the delivery of the event content.

## Lab Overview

This lab comprises of seven exercises:

- In the first exercise, you will create the event record.

- In the second exercise, you will create the segments needed to invite contacts to the event and follow up with attendees after the event.

- In the third exercise, you will create the emails needed for the event.

- In the fourth exercise, you will create the journey to send the event communications.

- In the fifth exercise, you will register for the event.

- In the sixth exercise, you will check-in event attendees.

## What You’ll Need

- A computer with a Dynamics 365 Customer Insights - Journeys environment

## Exercise 1: Create an in-person event

1. Log into Dynamics 365 Customer Insights - Journeys.

2. Navigate to the **Event planning** work area.

3. Navigate to **Events** under the **Event** group.

4. Click **+New event** to create a new event.

	- **Event name**: Contoso Insurance Business Appreciation Event. 

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

6. Add a description to the event.

	- Navigate to the **Additional information** tab.

	- In the **Description** text box, enter the following:
	`We look forward to welcoming you to the beautiful Coho Winery to show our appreciation for your business.`

8. **Save** the event record.

9. Click **Go Live** in the command bar.

10. After the event finishes going live, open the **Event URL** in a new tab.

11. Review the website.

## Exercise 2: Create the segments

1. Log into Dynamics 365 Customer Insights - Journeys.

2. Navigate to the **Real-time marketing** area.

3. Navigate to **Segments** under the **Audience** section.

4. Create a segment for the event invitees.

	- Select **+New segment**.

	- When prompted to select a template, click **Skip.**

	- Name the segment **Business Appreciation Event Invitees**. Keep target audience as **Contact.** Select **Create.**

	- Let's try using Query Assist to use natural language to build our segment. Click the **Query Assist** tab on the right pane. In the text box, use natural language to describe a segment with the following conditions:

		- The contact's City is Bellevue, Redmond, or Seattle.
   		- The contact does not work for Humongous Insurance.
	
 	- The Result should look like: **Address 1: City** is in Seattle, Redmond, Bellevue and **Account** is not **Humongous Insurance.**
	
 	- This will work, but let's use the segment we created in a previous lab, which will capture contacts who not only have our competitor listed as their Account, but also those who have a competitor's email address. Delete the second group by using the trash can symbol.

	- Select **+ Add new** to add a new group and select **Existing segment**.

	- Change the operator to **but not.**

	- Select the **Humongous Insurance (Contact)** segment from the Segment pane.
    
    - At the bottom of the screen, click **Estimate** to calculate the segment's estimated size. Review the results. Reminder: The capacity for the venue is 50.
    
    - Click **Save**.
          
    - On the toolbar, click **Ready to use**.
    
    - Give the system time and refresh if needed. After a few minutes, reopen the segment and navigate to the **Members and Insights** tab.
    
    - Verify you see your contact record in the list.
    
    - Click the drop down next to **Save** then click **Save &amp; Close** to return to the Segment list.
    
6. Create a segment for the event attendees.

	- Select **+New Segment.**

	- Name the segment **Business Appreciation Event Attendees**. Keep **Contact** as the target audience. Click **Create.**

	- In the Natural Query Assist, type "Contacts who attended the Contoso Insurance Business Appreciation Event." The result should include "Event (Event Registration) is Contoso Insurance Business Appreciation Event."

	- Click **Save**. Then select **Ready to use.**

# Exercise 3: Create the emails

1. Log into Dynamics 365 Customer Insights - Journeys.

2. Create event email #1.

	- Navigate to **Emails** under the **Channels** group.

	- Open **Cross Sell Campaign Email 3**.

	- Click the drop down next to **Save** then choose **Save as**.

	- **Name**: Business Appreciation Event Invite.

	- **Subject:** You’re invited!

	- Click **Save and Close**. A pop up will appear that says Your changes were saved. Click View record to open the new email. Otherwise navigate to the emails list and open **Business Appreciation Event Invite**.

	- Change the image to: coho-vineyard

	- Update the alt text for the image to: Coho Vineyard

	- Change the header to: Hi {{Firstname}}, 

	- Change the body to:

            We appreciate your business and, as a thank you, want to invite you to a special Business Appreciation Event.
            
            Join us at the beautiful Coho Winery for cocktails and dinner.
            
            December 1, 2023 6:00 PM - 8:00 PM

    - Add a button below the text.
    
    	- **Link to**: Event
    
    	- **Event**: Click the magnifying glass. Select Contoso Insurance Business Appreciation Event.
    
    	- **Button text**: REGISTER NOW
    
    	- **Font**: Segoe UI
    
    	- **Font size**: 18 px
    
    	- **Button color**: #1a658c
    
    - Make any other changes as desired.
    
    - **Save**.
    
    - **Preview** the email.
    
    - Select **Ready to send.**

3. Create event email #2.

	- While **Business Appreciation Event Invite** email is still open, click the drop down next to **Save** then choose **Save as**.

	- **Name**: Business Appreciation Event Confirmation.

	- **Subject:** Thanks for registering!

	- Click **Save and Close.**

	- Open the email by clicking **View record** in the pop-up.

	- Change the header to: Thanks for registering!

	- Change the body to:
 
            We look forward to seeing you at our upcoming Business Appreciation Event.                     
            
            **Coho Winery**
            
            **December 1, 2023 6:00 PM - 8:00 PM**

    - Update the button.
    
    	- **Link to**: Add to calendar
    
    	- **What should be added to calendar**: Only the event
    
    	- **Event**: Contoso Insurance Business Appreciation Event
    
    	- **Button text**: ADD TO CALENDAR

    - Make any other changes as desired.
    
    - **Save**.
    
    - **Preview and test** the email.
    
    - Select **Ready to send.** Correct any errors if needed.

4. Create event email #3.

	- While **Business Appreciation Event Confirmation** email is still open, click the drop down next to **Save** then choose **Save as**.

	- **Name**: Business Appreciation Event Thank You

	- **Subject:** Thanks for attending our Business Appreciation Event!

	- Click **Save and Close.**

	- Open the email by clicking View Record in the pop-up.

	- Change the image to: thank-you

	- Update the alt text for the image to: Thank you image

	- Remove the header text

	- Change the body to:

            Hi {{Firstname}},            
            
            Thanks for attending our Business Appreciation Event. We value your business and hope this event was a great way of showing our appreciation. We look forward to continuing helping you with all your insurance needs!
    
    - Make any other changes as desired.
    
    - On the toolbar, click **Save**.
    
    - **Preview and test** the email.
    
    - On the toolbar, click **Ready to send.** Correct any errors as needed.

# Exercise 5: Create the journey

We will create two journeys - the first will include the invitation and confirmation emails. The second will include the post-event email.

1. Log into Dynamics 365 Customer Insights - Journeys.

2. Navigate to **Journeys** under the **Engagement** group.

3. Click **+New journey.** Name the journey "Business Appreciation Event Invites." Select a segment-based journey. Select **Business Appreciation Event Invitees** as the segment.

4. Select **A one-time journey with a static audience**.

	- Set the **Start date and time** to today’s date a half hour in the future.

	- Set the **Time zone** to your time zone.

	- Select **Create.**

	- Click on the plus sign between Start and Exit arrows. Select **Send an email** from the menu.

	- Click the **Email** tile. On the properties pane on the right, in the email field, click on the magnifying glass. Select the **Business Appreciation Event Invite**.

    - Click on the plus sign under to **Send an email.** Select **Wait for trigger.**
    
    - Click the **If/then branch** tile.
    
    	- In the **Choose a branch condition type**, select **A trigger is activated.**
    
    	- In the **Choose a trigger** field, select **Marketing Event Registration Created**. 
  
       	- Select **+Add condition.** Expand **Marketing event registration created** and select **Marketing Event Reference.** From the dropdown list, select the first option, **Condition on Marketing Event Reference.**
    
	- Change the modifier to **Equals** and select **Contoso Insurance Business Appreciation Event** from the lookup.

      	- Set the time limit as **7 days.**
    
    - In the **Yes** branch, click the plus sign. Select **Email**.
    
    	- In the **Email** field on the right, select **Business Appreciation Event Confirmation**.
    
    - In the **No** branch, click the plus sign. Select **Send an email**.
    
    	- In the **Email** field on the right, select **Business Appreciation Event Invite**.
    
    	- Click on the plus sign below **Send an email.** Select **Respond to an action** from the menu.
    
    	- Click the **If/then** tile.
    
    		    	- In the **Choose a branch condition type**, select **A trigger is activated.**
    
    			- In the **Choose a trigger** field, select **Marketing Event Registration Created**.
  
       			- Select **+Add condition.** Expand **Marketing event registration created** and select **Marketing Event Reference.** From the dropdown list, select the first option, **Condition on Marketing Event Reference.**
    
			- Change the modifier to **Equals** and select **Contoso Insurance Business Appreciation Event** from the lookup.

      			- Set the time limit as **7 days.**
    
    - In the **Yes** branch, click the plus sign. Select **Send an email**.
    
    	1. In the **Email** field on the right, select **Business Appreciation Event Confirmation**.

   - Select **Save.** Then select **Publish.**

7. Define the second journey for event attendees.

	- Return to the journeys view and select **+ New journey.** Name the journey **Business Appreciation Event Follow-up.** Select a segment-based journey and select **Business Appreciation Event Attendees** as the segment. Set the time zone to your time zone and select the start date in half an hour. (Note: In an actual event campaign, you would set this to the day after the event. You are setting it to today so that you will receive the email during this lab.)

    - Select **Create.**
    
    - Click the plus sign beneath the segment tile. Select **Send an email** from the menu.
    
    - I **email** field, click on the magnifying glass. Select the **Business Appreciation Event Thank You**.

8. Click **Save** in the command bar. 

9. Click **Publish.**

# Exercise 6: Register for the event

1. Navigate to your email account. 

2. Locate the email from **Contoso Insurance** with a subject line of **You’re invited!**

	- Open the email. Click the button.

	- This will open the event website page.

	- Review the details of the event.

	- Click on Dean Halstead’s profile picture to display his bio.

	- Click **Register now**.

	- **First name**: enter the same name as the contact record you created.

	- **Last name**: enter the same name as the contact record you created.

	- **Email address**: enter the same email as the contact record you created.

	- Click **Check out**.

3. Navigate to your email account. 

4. Verify you receive a new email from **Contoso Insurance** with a subject line of **Thanks for registering!**

	- Open the email.

	- Click the **Add to calendar** button.

	- Verify a browser opens with an ics file for download. Open the ics file and review the invitation details.

# Exercise 7: Check in event attendees

The day of the event, a representative from Contoso Insurance would check in attendees as they arrive to the event. There are two ways to check-in attendees – manually or by scanning a QR code. For this exercise, you will be checking the attendees in manually.

1. Log into Dynamics 365 Customer Insights - Journeys.

2. Navigate to the **Event Planning** work area.

3. Navigate to **Events** under the Event group.

4. Open **Contoso Insurance Business Appreciation Event**.

5. Navigate to the **Registration and attendance** tab. Scroll down to the **Event registrations** area to see who has registered.

6. On the left, under the checkmark icon, click next to the attendee you want to check in. A checkmark will appear, and the record will be highlighted blue.

7. Click **Check in registrations**. A box will appear and ask if you want to check in the selected registrations. Select **OK**.

8. Scroll down the page to the **Event Check-ins** section and verify you see the check-in record.

# Exercise 8: Open the final email

1. Navigate to your email account. 

2. Locate the email from **Contoso Insurance** with a subject line of **Thanks for attending our Business Appreciation Event!**
 
3. Open the email. 
