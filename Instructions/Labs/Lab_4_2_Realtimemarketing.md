---
lab:
    title: 'Lab 4.2: Create a journey'
    module: 'Module 4: Create segments and journeys'
---

# Module 4: Create segments and journeys

## Practice Lab 4.2 – Create a journey

# Lab Overview

## Scenario

The marketing team wants to create a real-time onboarding journey for new
business customers.

## Lab Overview 

This lab comprises of five exercises: 

-   In exercise one, you will create the first email for the real-time journey.

-   In exercise two, you will create the second email for the real-time journey.

-   In exercise three, you will create the third email for the real-time
    journey.

-   In exercise four, you will create the real-time customer real-time journey.

-   In exercise five, you will participate in the real-time journey.

## What you’ll need:

-   A computer with a Dynamics 365 Customer Insights - Journeys environment

# Exercise 1: Create email 1

The journey will consist of 3 marketing emails. Refer to the screenshots inline or
provided in the Appendix for design and content suggestions for these emails.

1.  Log into Dynamics 365 Customer Insights - Journeys.

2.  Navigate to the **Real-time marketing** work area.

3.  Under **Channels**, select **Emails.**

4.  Create the email.

    -   Click **+ New** to create a new email.

    -   From the template gallery, select **skip**.

5.  Enter details about the email.

    -   **Name**: Welcome Email 1

    -   **Subject**: Welcome to Contoso Insurance

    -   **Preview text**: We’re committed to providing you quality
        insurance.

6.  Select the **Default brand profile** as the brand profile.

7. Navigate to **Email header** and expand Compliance. Select the **Contoso Americas** compliance profile.

8.  Design the email.

    -   Refer to the screenshot of Welcome Email 1 below for design
        and content ideas. You can modify the images and content as desired, but
        you will want to include a call-to-action button in this email as it
        will be used as branching criteria within the journey.

![](https://github.com/MicrosoftLearning/MB-220-Dynamics365forMarketing/blob/master/Instructions/Labs/media/WelcomeEmail1.jpg)

Here is some sample copy for this email. You can copy and paste this into your email design. Use **Personalization**, like we used in the previous email lab, to enter dynamic content for the contact's first name.
        
```
FirstName,

Thank you for putting your trust in Contoso Insurance. We're honored to have you
as a customer and look forward to building a lasting relationship with you.

As America's \#1 insurance company, we're committed to providing quality
insurance that protects all aspects of your business.

We've put together a welcome kit that provides insight about our agency, advises
on what to do if you need to report a claim, and provides our staff's direct
contact information. Use the link below to download it.

Feel free to contact us any time at 888-888-8888 with any questions you have.
And don't forget to download our mobile app where you can view your account
history, pay your bill, and more.
```

9.  Add a button to the email.

    -   In the **Toolbox**, select **Elements** tab.

    -   Drag a **button** below the main text.

    -   Change **Link to** from URL to **File download.**

    -   Select **Choose a file** then **Browse library**. Select *Contoso
        Insurance Welcome kit* then click **Insert**.

    -   In the **Button Text** field, change it to **Click here to download the
        welcome kit.**

    -   Expand the **Style** section.

    -   Change the **button color** to \#0076ad.

10.  Preview, test, and go live with your email.

    -   Navigate to the **Preview and test** tab of your email to review your
        email.

    -   Use **Test send** to send yourself a copy. Enter your personal email address. Select the contact you created previously - the personalization will fill in this contact's first name. Be sure to check your junk folder if you do not see the email in your inbox.

    -   Make any final changes.

    -   Click **Check content**. Correct any errors if needed.

    -   Click **Ready to send.**

# Exercise 2: Create email \#2

1.  Create a new email by copying email 1.

    -   While Welcome Email 1 is open, click the drop down next to **Save** then
        select **Save as**.

    -   Update the name of the email to **Welcome Email 2** and
        click **Save and Close**.

    -   Select **View record** in the pop-up to move to your newly created email.

2.  Enter details about the email.

    -   Suggested **Subject**: Get on-demand access to your
        Contoso Insurance portal.

    -   Suggested **Preview text**: Review account information, policy details,
        submit a claim, and more.

3.  Design the email.

    -   Refer to the screenshot of Welcome Email 2 below for design
        and content ideas. You can modify the images and content as desired.

![](https://github.com/MicrosoftLearning/MB-220-Dynamics365forMarketing/blob/master/Instructions/Labs/media/WelcomeEmail2.jpg)

Here is sample copy for this email. You can copy and paste this into your email design. (Note: We recommend leaving FirstName from the first email and then replacing the rest of the copy with this.)

```
I would like to welcome you to the Contoso family! I hope you found the welcome
kit helpful and informative.

Our specialists are here to help you with all your insurance needs. We also
encourage you to setup your Contoso Insurance online account to gain 24/7 access
to: 

-   Your account information and policy details.

-   Submit a request for coverage verification, start a claim, or review prior
    claims.

-   A secure and encrypted internal messaging tool for sharing sensitive
    information.

Feel free to contact me with any questions you have.

Cheers,

John Smith, Insurance Specialist  
jsmith@contosoinsurance.com
888-888-8888
```

4.  Update the button in the email.

    -   Select the button.

    -   Change **Link to** from File download to **URL.**

    -   In the **URL field**, enter http://microsoft.com.

    -   In the **Button Text** field, change it to **Log in or Register**

    -   Expand the **Style** section.

    -   Change the **button color** to \##9B1E13.

5.  Preview, test, and go live with your email.

    -   Navigate to the **Preview and test** tab of your email to review your
        email.

    -   Use **Test send** to send yourself a copy.

        1.  Note: You do not need to fill out any of the fields other than email
            address. The remaining fields will populate based on system settings
            and the personalization default values.

        2.  Be sure to check your junk folder if you do not see the email in
            your inbox.

    -   Make any final changes.

    -   Click **Check content**. Correct any errors if needed.

    -   Click **Ready to send.**

# Exercise 3: Create email \#3

1.  Create a new email by copying email 2. Name the email **Welcome email 3.**

2.  Enter details about the email.

    -   **Subject**: Your welcome kit contains important
        information

    -   **Preview text**: Download and review your welcome kit.

3.  Design the email.

    -   Refer to the screenshot of Welcome Email 3 below for design
        and content ideas. You can modify the images and content as desired.

![](https://github.com/MicrosoftLearning/MB-220-Dynamics365forMarketing/blob/master/Instructions/Labs/media/WelcomeEmail3.jpg)

Here is sample copy for this email. You can copy and paste this into your email design. (Note: We recommend leaving FirstName from the second email and then replacing the rest of the copy with this.)

```
Thank you for putting your trust in Contoso Insurance. I'm honored to have you
as a customer and look forward to building a lasting relationship with you.

Your welcome kit provides insight about our agency, advises on what to do if you
must report a claim, and provides our staff's direct contact information. Use
the link below to download it.

Feel free to contact me with any questions you have.

Cheers,
John Smith, Insurance Specialist  
jsmith@contosoinsurance.com
888-888-8888
```

1.  Update the button in the email.

    -   Change **Link to** from URL to **File download.**

    -   Select **Choose a file** then **Browse library**. Select **Contoso
        Insurance Welcome kit** then click **Insert**.

    -   In the **Button Text** field, change it to **Click here to download the
        welcome kit.**

    -   Change the **button color** to \#0076ad.

2.  Preview, test, and go live with your email.

    -   Navigate to the **Preview and test** tab of your email to review your
        email.

    -   Use **Test send** to send yourself a copy.

    -   Make any final changes.

    -   Click **Check content**. Correct any errors if needed.

    -   Click **Ready to send.**

# Exercise 4: Create a real-time journey

1.  Log into Dynamics 365 Customer Insights - Journeys.

2.  Navigate to the **Real-time marketing** work area.

3.  Under **Engagement**, select **Journeys.**

4.  Click **+ New journey** in the command bar.

    1.  In **Name the journey**, enter Welcome Journey.

    2.  In **Choose journey type**, select Trigger-based.

    3.  In **Choose a trigger**, search for and
        select Contact Created.

    4.  Click **Create**.

5.  From the Journey settings on the right, in the **Entry** section, do the following:

    1.  Leave **Exclude by segments** blank.

    2.  In the **Repeat** section, select Immediately.

    3.  In the **Time zone** section, choose your time zone.

    4.  In **Start,** select today, 15 minutes from now.

    5.  In **End,** select tomorrow.

6.  From the Journey settings on the right, navigate to the **Goal** section.

    1.  In **The goal of this journey is,** select Send a general notification.

    2.  In **The goal is met when,** select A person clicked on at least one
        link.

    3.  In **The number of people needed,** enter 50. Leave percent selected.

7.  In the journey designer, click the **plus icon (+)** under the Contact
    Created tile.

    1.  Select **Branch based on a specific value**.

    2.  In **Display name** on the right, enter New Business Customer.

    3.  Select **Branch 1**.

    4.  In **Choose an attribute**, Search for Description (description), under Contact.

    5.  Change the value from Equals to
        Contains.

    6.  In **Value,** enter Business.

8.  Click the **plus icon (+)** under Branch 1.

    1.  Select **Send an email**.

    2.  In **Select email,** choose Welcome Email 1.

9.  Click the **plus icon (+)** under the Send an email tile.

    1.  Select **Respond to an action**.
    
    2.  To configure the **If/then branch**, under **Wait for, Choose a branch condition type** select The previous message gets an interaction.

    3.  In **Choose an interaction**, select Email Link Clicked.
    
    4.  In **What’s the time limit?,** enter 10 minutes.
    
    5.  Back on the Journey diagram: To specify the link clicked, select **create branches**.
    
    6.  Select the Attribute **Email Link Clicked**.
    
    7.  In **Branch 1, Choose a link**, select the call-to-action button from the email (e.g., Click here to download the welcome kit).  

10. In the **Yes** path, click the **plus icon (+).**

    1.  Select **Send an email**.

    2.  In **Select email,** choose Welcome Email 2.

11. In the corresponding **No** path, click the **plus icon (+).**

    1.  Select **Send an email**.

    2.  In **Select email,** choose Welcome Email 3.

12. **Save** the journey.

13. Review the journey. Make any final changes.

14. Click **Publish**. Wait for the journey to publish before moving on to Exercise 5.

# Exercise 5: Participate in the journey

1.  Log in to Dynamics 365 Customer Insights - Journeys.

2.  Navigate to the **Real-time marketing** work area.

3.  Under **Audience**, select **Contacts.**

4.  Create a new contact.

    -  Click **+ New** in the command bar.

    -  Input a fictitious first name, last name, and your email.

    -  Navigate to the **Details** tab. In the **Personal Notes** field, enter
        Business.

    -  Click **Save** in the command bar.

5. Wait a few minutes. Check your inbox to see that you have received
        Welcome Email 1 with the subject line: Welcome to Contoso
        Insurance. Be sure to check your junk folder if you do not see the email
            in your inbox.

6. Click the call-to-action button from the email (e.g., Click here to download the welcome kit).

7. Verify the PDF downloads.

8. Wait a few minutes. Check your inbox to see that you have received
        Welcome Email 2 with subject line: Get on-demand access to
        your Contoso Insurance portal. (Note: Be sure to check your junk folder if you do not see the email in your inbox.)

5.  Create a new contact.

    1.  Click **+ New** in the command bar.

    2.  Input a fictitious first name, last name, and your email.

    3.  Navigate to the **Details** tab. In the **Personal Notes** field, enter
        Business. (Note: Depending on the environment you are working in, you may
            receive a pop-up notification stating you are creating a duplicate
            contact. Select **Ignore and Save**.)

    4.  Click **Save** in the command bar.

    5.  Wait a few minutes. Check your inbox to see that you have received
        Welcome Email 1 \| subject line: Welcome to Contoso Insurance.

        1.  Note: Be sure to check your junk folder if you do not see the email
            in your inbox.

    6.  Do not take any action within the email.

    7.  Wait 10 minutes. Check your inbox to see that you have received Welcome
        Email 3 \| subject line: Your welcome kit contains important
        information.

6.  Navigate to the **Real-time marketing** work area.

7.  Under **Engagement**, select **Journeys.**

8.  Open **Welcome Journey.**

9.  Review the analytics generated from the journey.
