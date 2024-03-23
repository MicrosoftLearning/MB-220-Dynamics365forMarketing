---
lab:
    title: 'Lab 4.1: Create a segment'
    module: 'Module 4: Create segments and journeys'
---

# Module 4: Create segments and journeys

## Practice Lab 4.1: Work with segments

# Lab Overview

## Scenario

The first step in setting up the Cross Sell Campaign will be to create the segments for the journey.

The Marketing Coordinator will start by creating a segment for all current business contacts. The marketing team is also aware that their competitors will occasionally fill out forms on the Contoso Insurance website, so they want to make sure to exclude competitor contacts from all marketing campaigns. 

## Lab Overview

This lab compromises of three exercises:

1. In exercise one, you will create a segment for all competitors from Humongous Insurance. 

2. In exercise two, you will create a segment for all active business contacts and exclude competitor contacts.

3. In exercise three, you will create your own contact record to be able to participate in the journey.


## What you’ll need:

- A computer with a Dynamics 365 Customer Insights - Journeys environment

# Exercise 1: Create a segment

1.  Log into Dynamics 365 Customer Insights - Journeys. Ensure you are in the **Real-time journeys** area.

2.  Navigate to **Segments**, under the **Audience** group. 

3.  Select **+New Segment**.

4.  In the **Name the segment** box, enter `Humongous Insurance` Select **Contact** as the target audience.

7.  Let's use **Copilot** to build the new segment. In **Query Assist**, enter `Contacts with account "Humongous Insurance"` and select **Create**.

8.  In the **Query Assist** pane, the **Result** will appear. Verify the Result reads **Account  Is  Humongous Insurance**. Since this looks like a result that will satisfy our segment requirements, select **Use**.

9.  Copilot builds the condition in the **Segment Designer** pane. The **Group 1** condition will read "Account **Is** Humongous Insurance".

10. We want to add another condition to the segment. We will build this condition ourselves. Select **+Add new** to add a new group and select **Attribute group**.

11. Change the operator from **and also** to **or**. 

    - In the Attribute pane, start typing **Email**. Expand **Contact**. Select the plus button next to the field and add it to **Group 2**.

    - Create the following condition: Email **contains** `humongousinsurance`

12. Select **Save**.

13. Select **Ready to use** in the toolbar.

14. Select the **Members and Insights** tab. 

	- Verify you see contacts with a Humongous Insurance email or Humongous company name. 

	- Note: You may need to refresh or wait a few minutes before the contacts appear. 


# Exercise 2: Create a segment with exclusion

1.  Log into Dynamics 365 Customer Insights - Journeys. Ensure you are in the **Real-time marketing** section.

2.  Navigate to **Segments** under the **Audience** group. 

3.  Select **+ New Segment**.

4.  Name the segment `Business Customers`. Keep **Contact** selected as target audience.

6.  Let's use Copilot to create our segment again. In the Query Assist text box, type "Contact who description contains business."

7.  Click **Create.**

8.  Review the Result. It should say "Description contains business." Select **Use.**

9.  In the Elements pane, select the **Segments** tab. You should see the Humongous Insurance segment you created in Exercise 1. (If your segment is not in the pane, your segment may still be building.)

10.  Select the plus sign next to the Humongous Insurance segment. It will create a new Group 2.

11. Change the operator to **but not.** This will create a segment that includes all contacts with "Business" in their Description *except* those from your competitor, Humoongous Insurance.

12. Select **Save** and then select **Ready for use.**

12. Wait for your segment to build.

13. Select the **Members and insights** tab. Verify you do not see any contacts with a Humongous Insurance email. 


# Exercise 3: Create a contact

To participate in the journey, you will need to set yourself up as a contact. 

1.  Log into Dynamics 365 Customer Insights - Journeys and ensure you are in the **Real-time marketing** section.

2.  Navigate to **Contacts** under the **Audience** group. 

3.  Select **+New**.

4.  In the **First Name** field, enter a generic first name.

5.  In the **Last Name** field, enter a generic last name.

6.  In the **Job Title** field, enter Finance Director.

7.  In the **Email** field, enter your email.

8.  In the **Address 1: City** field, enter `Seattle`

9.  In the **Address: State/Province** field, enter `Washington`. 

10. Navigate to the **Details** tab. In the **Personal Notes** field, enter Business.

11. Select **Save &amp; Close**. 

12. Navigate back to **Segments**. Open the **Business Customers** segment. Verify the contact you created appears.

    **Note:** You may need to refresh or wait a few minutes before the contact appears.
