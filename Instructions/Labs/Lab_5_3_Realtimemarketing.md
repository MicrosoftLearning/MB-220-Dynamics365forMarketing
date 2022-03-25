---
lab:
    title: 'Lab 5.3: Real-time marketing'
    module: 'Module 5: Manage emails and journeys in Dynamics 365 Marketing'
---

# Module 5: Manage emails and journeys in Dynamics 365 Marketing

## Practice Lab 5.4 – Real-time marketing

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

-   A computer with a Dynamics 365 Marketing environment

# Exercise 1: Create email \#1

The journey will consist of 3 marketing emails. Refer to the screenshots inline or
provided in the Appendix for design and content suggestions for these emails.

1.  Log into Dynamics 365 Marketing.

2.  Navigate to the **Real-time marketing** work area.

3.  Under **Channels**, select **Emails.**

4.  Create the email.

    -   Click **+ New** to create a new email.

    -   From the template gallery, select **skip**.

5.  Enter details about the email.

    -   Suggested **Name**: [my prefix] Welcome Email 1

        1.  Enter this at the top left of the email designer.

    -   Suggested **Subject**: [my prefix] Welcome to Contoso Insurance

        1.  To add a subject and preview text, click the section in the middle
            of the designer that includes the From address and Subject Line
            placeholder to display the **Email header** on the right.

        2.  Note: All students in the course will create the same emails and
            journey. This means you will receive emails from other students’
            journeys. We suggest you include your prefix in the subject line of
            the email to identify which one you created.

    -   Suggested **Preview text**: We’re committed to providing you quality
        insurance.

6.  Design the email.

    -   Refer to the screenshot of Welcome Email 1 below for design
        and content ideas. You can modify the images and content as desired, but
        you will want to include a call-to-action button in this email as it
        will be used as branching criteria within the journey.

![](https://github.com/MicrosoftLearning/MB-220-Dynamics365forMarketing/blob/master/Instructions/Labs/media/WelcomeEmail1.jpg)

    -   Here is some sample copy for this email. You can copy and paste this
        into your email design.

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

1.  Add personalization.

    -   Note: Dynamic content functions differently than outbound marketing. To
        add personalization in real-time, follow these steps:

    -   Highlight FirstName then click **Personalization** in the text toolbar.

    -   Wait for the **Personalization** window to load.

    -   Click **Select a data field** then select **Contact**.

    -   Select **First Name**.

    -   In **Default value** enter **Valued Customer.**

    -   Click **Save**.

2.  Add a button to the email.

    -   In the **Toolbox**, select **Elements** tab.

    -   Drag a **button** below the main text.

    -   Change **Link to** from URL to **File download.**

    -   Select **Choose a file** then **Browse library**. Select *Contoso
        Insurance Welcome kit* then click **Insert**.

    -   In the **Button Text** field, change it to **Click here to download the
        welcome kit.**

    -   Expand the **Style** section.

    -   Change the **button color** to \#0076ad.

3.  Preview, test, and go live with your email.

    -   Navigate to the **Preview and test** tab of your email to review your
        email.

    -   Use **Test send** to send yourself a copy.

        1.  Note: You do not need to fill out any of the fields other than
            email. The remaining fields will populate based on system settings
            and the personalization default values.

        2.  Be sure to check your junk folder if you do not see the email in
            your inbox.

    -   Make any final changes.

    -   Click **Check content**. Correct any errors if needed.

    -   Click **Ready to send.**

# Exercise 2: Create email \#2

1.  Create a new email by copying email 1.

    -   While Welcome Email 1 is open, click the drop down next to **Save** then
        select **Save as**.

    -   Update the name of the email to **[my prefix] Welcome Email 2** and
        click **Save and Close**.

    -   Select **View record** in the pop-up at the bottom of the screen to move
        to your newly created email record.

2.  Enter details about the email.

    -   Suggested **Subject**: [your prefix] Get on-demand access to your
        Contoso Insurance portal

        1.  Note: All students in the course will create the same emails and
            journey. This means you will receive emails from other students’
            journeys. We suggest you include your prefix in the subject line of
            the email to identify which one you created.

    -   Suggested **Preview text**: Review account information, policy details,
        submit a claim, and more.

3.  Design the email.

    -   Refer to the screenshot of Welcome Email 2 below for design
        and content ideas. You can modify the images and content as desired.

![](https://github.com/MicrosoftLearning/MB-220-Dynamics365forMarketing/blob/master/Instructions/Labs/media/WelcomeEmail2.jpg)

    -   Here is sample copy for this email. You can copy and paste this into
        your email design.

    -   Note: We recommend leaving FirstName from the first email and then
        replacing the rest of the copy with this:

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

**John Smith**  
Insurance Specialist  
<jsmith@contosoinsurance.com>888-888-8888

1.  Update the button in the email.

    -   Select the button.

    -   Change **Link to** from File download to **URL.**

    -   In the **URL field**, enter http://microsoft.com.

    -   In the **Button Text** field, change it to **Log in or Register**

    -   Expand the **Style** section.

    -   Change the **button color** to \#595959.

2.  Preview, test, and go live with your email.

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

1.  Create a new email by copying email 2.

    -   While Welcome Email 2 is open, click the drop down next to **Save** then
        select **Save as**.

    -   Update the name of the email to **[my prefix] Welcome Email 3** and
        click **Save and Close**.

    -   Select **View record** in the pop-up at the bottom of the screen to move
        to your newly created email record.

2.  Enter details about the email.

    -   Suggested **Subject**: [your prefix] Your welcome kit contains important
        information

        1.  Note: All students in the course will create the same emails and
            journey. This means you will receive emails from other students’
            journeys. We suggest you include your prefix in the subject line of
            the email to identify which one you created.

    -   Suggested **Preview text**: Download and review your welcome kit.

3.  Design the email.

    -   Refer to the screenshot of Welcome Email 3 below for design
        and content ideas. You can modify the images and content as desired.

![](https://github.com/MicrosoftLearning/MB-220-Dynamics365forMarketing/blob/master/Instructions/Labs/media/WelcomeEmail3.jpg)

    -   Here is sample copy for this email. You can copy and paste this into
        your email design.

    -   Note: We recommend leaving FirstName from the second email and then
        replacing the rest of the copy with this:

Thank you for putting your trust in Contoso Insurance. I'm honored to have you
as a customer and look forward to building a lasting relationship with you.

Your welcome kit provides insight about our agency, advises on what to do if you
must report a claim, and provides our staff's direct contact information. Use
the link below to download it.

Feel free to contact me with any questions you have.

Cheers,

**John Smith**  
Insurance Specialist  
<jsmith@contosoinsurance.com>888-888-8888

1.  Update the button in the email.

    -   In the **Toolbox**, select **Elements** tab.

    -   Drag a **button** below the main text.

    -   Change **Link to** from URL to **File download.**

    -   Select **Choose a file** then **Browse library**. Select *Contoso
        Insurance Welcome kit* then click **Insert**.

    -   In the **Button Text** field, change it to **Click here to download the
        welcome kit.**

    -   Change the **button color** to \#0076ad.

2.  Preview, test, and go live with your email.

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

# Exercise 4: Create a real-time journey

1.  Log into Dynamics 365 Marketing.

2.  Navigate to the **Real-time marketing** work area.

3.  Under **Engagement**, select **Journeys.**

4.  Click **+ New journey** in the command bar.

    1.  In **Name the journey**, enter [my prefix] Welcome Journey.

    2.  In **Choose journey type**, select Event-based.

    3.  In **Which event triggers the start of this journey?**, search for and
        select Contact Created.

    4.  Click **Create**.

5.  From the Journey settings on the right, in the **Start** section, click
    **Edit.**

    1.  Leave **Exclude by segments** blank

    2.  In the **Repeat** section, select Immediately.

    3.  In the **Time zone** section, choose your time zone.

    4.  In **Start,** select today, 15 minutes from now.

    5.  In **End,** select tomorrow.

    6.  Scroll back to the top and select the **back arrow** next to **Start**
        to return to the Journey settings.

6.  From the Journey settings on the right, in the **Goal** section, click
    **Set**.

    1.  In **The goal of this journey is,** select Send a general notification.

    2.  In **The goal is met when,** select A person clicked on at least one
        link.

    3.  In **The number of people needed,** enter 50. Leave percent selected.

    4.  Click the **back arrow** next to **Goal** to return to the Journey
        settings.

7.  In the journey designer, click the **plus icon (+)** under the Contact
    Created tile.

    1.  Select **Branch based on a specific value**.

    2.  In **Display name** on the right, enter New Business Customer.

    3.  Click **Incomplete condition**.

    4.  Verify **Contact** is selected.

    5.  In **Select an attribute,** choose Description.

    6.  In **Select Condition Operator,** change the value from Equals to
        Contains.

    7.  In **Value,** enter Business.

8.  Click the **plus icon (+)** in the Yes path.

    1.  Select **Send an email**.

    2.  In **Select email,** choose [your prefix] Welcome Email 1.

9.  Click the **plus icon (+)** under the Send an email tile.

    1.  Select **Respond to an action**.

    2.  In **Branch off this,** select [your prefix] Welcome Email 1.

    3.  In **Wait for,** select Email Link Clicked.

    4.  In **Which link?,** select the call-to-action button from the email
        (e.g., Click here to download the welcome kit).

    5.  In **What’s the time limit?,** enter 10 minutes.

10. In the **Yes** path, click the **plus icon (+).**

    1.  Select **Send an email**.

    2.  In **Select email,** choose [your prefix] Welcome Email 2.

11. In the corresponding **No** path, click the **plus icon (+).**

    1.  Select **Send an email**.

    2.  In **Select email,** choose [your prefix] Welcome Email 3.

12. **Save** the journey.

13. Review the journey. Make any final changes.

14. Click **Publish**.

# Exercise 5: Participate in the journey

1.  Log in to Dynamics 365 Marketing.

2.  Navigate to the **Outbound marketing** work area.

3.  Under **Customers**, select **Contacts.**

4.  Create a new contact.

    1.  Click **+ New** in the command bar.

    2.  Input a fictitious first name, last name, and your email.

    3.  Navigate to the **Details** tab. In the **Personal Notes** field, enter
        Business.

    4.  Click **Save** in the command bar.

    5.  Wait a few minutes. Check your inbox to see that you have received
        Welcome Email 1 \| subject line: [my prefix] Welcome to Contoso
        Insurance.

        1.  Note: Be sure to check your junk folder if you do not see the email
            in your inbox.

    6.  Click the call-to-action button from the email (e.g., Click here to
        download the welcome kit).

    7.  Verify the PDF downloads.

    8.  Wait a few minutes. Check your inbox to see that you have received
        Welcome Email 2 \| subject line: [my prefix] Get on-demand access to
        your Contoso Insurance portal.

        1.  Note: Be sure to check your junk folder if you do not see the email
            in your inbox.

5.  Create a new contact.

    1.  Click **+ New** in the command bar.

    2.  Input a fictitious first name, last name, and your email.

    3.  Navigate to the **Details** tab. In the **Personal Notes** field, enter
        Business.

        1.  Note: Depending on the environment you are working in, you may
            receive a pop-up notification stating you are creating a duplicate
            contact. Select **Ignore and Save**.

    4.  Click **Save** in the command bar.

    5.  Wait a few minutes. Check your inbox to see that you have received
        Welcome Email 1 \| subject line: Welcome to Contoso Insurance.

        1.  Note: Be sure to check your junk folder if you do not see the email
            in your inbox.

    6.  Do not take any action within the email.

    7.  Wait 10 minutes. Check your inbox to see that you have received Welcome
        Email 3 \| subject line: [my prefix] Your welcome kit contains important
        information.

6.  Navigate to the **Real-time marketing** work area.

7.  Under **Engagement**, select **Journeys.**

8.  Open **[my prefix] Welcome Journey.**

9.  Review the insights generated from the journey.
