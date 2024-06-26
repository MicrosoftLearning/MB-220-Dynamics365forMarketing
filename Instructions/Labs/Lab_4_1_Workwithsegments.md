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

The Marketing Coordinator will start by creating a segment for all current business contacts.

## Lab Overview

This lab compromises of three exercises:

1. In exercise one, you will create a segment for all competitors from Humongous Insurance. 

2. In exercise two, you will create a segment for all active business contacts.

3. In exercise three, you will create your own contact record to be able to participate in the journey.


## What you’ll need:

- A computer with a Dynamics 365 Customer Insights - Journeys environment

# Exercise 1: Create a segment

1.  Log into Dynamics 365 Customer Insights - Journeys. Ensure you are in the **Real-time journeys** area.

1.  Navigate to **Segments**, under the **Audience** group. 

1.  Select **+New Segment**.

1.  In the **Name the segment** box, enter `Humongous Insurance` Select **Contact** as the target audience. Select **Create.**

1. Select **Add a new group** in the segment designer. First, we will choose an **Attribute block.**

1. From the **Attributes** pane, expand **Contact** and select **Account.** Add item to the existing group.

1. In the lookup in Group 1, select **Humongous Insurance.**
   
1. The **Group 1** condition will read "Account **Is** Humongous Insurance".

10. We want to add another condition to the segment. Select **+Add new** to add a new group and select **Attribute group**.

11. Change the operator from **and also** to **or**. 

    - In the Attribute pane, start typing **Email**. Expand **Contact**. Select the plus button next to the field and add it to **Group 2**.

    - Create the following condition: Email **contains** `humongousinsurance`

12. Select **Save**.

13. Select **Ready to use** in the toolbar.

14. Select the **Members and Insights** tab. 

	- Verify you see contacts with a Humongous Insurance email or Humongous company name. 

	- Note: You may need to refresh or wait a few minutes before the contacts appear. 


# Exercise 2: Create another segment

1.  Log into Dynamics 365 Customer Insights - Journeys. Ensure you are in the **Real-time marketing** section.

2.  Navigate to **Segments** under the **Audience** group. 

3.  Select **+ New Segment**.

4.  Name the segment `Business Customers`. Keep **Contact** selected as target audience.

5. Add a new group and select **Create attribute group.** In the Attributes pane, expand **Contact** and add **Description** to Group 1.

6. In the segment designer, change the qualifier to **Contains**. For the value, enter "Business."

7. Select **Save** and then select **Ready for use.**

8. Wait for your segment to build.

9. Select the **Members and insights** tab to view your segment members.


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
