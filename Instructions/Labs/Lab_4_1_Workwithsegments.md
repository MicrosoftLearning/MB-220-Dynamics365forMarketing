---
lab:
    title: 'Lab 4.1: Work with segments'
    module: 'Module 4: Manage segments and subscription centers'
---

# Module 4: Manage segments and subscription centers

## Practice Lab 4.1: Work with segments

# Lab Overview

## Scenario

The first step in setting up the Cross Sell Campaign will be to create the segments for the journey.

The Marketing Coordinator will start by creating a segment for all current, business contacts. The marketing team is also aware that their competitors will occasionally fill out forms on the Contoso Insurance website, so they want to make sure to exclude competitor contacts from all marketing campaigns. 


## Lab Overview

This lab compromises of three exercises:

1. In exercise one, you will create a dynamic segment for all competitors from Humongous Insurance. 

2. In exercise two, you will create a dynamic segment for all active, business contacts and exclude competitor contacts.

3. In exercise three, you will create your own contact record to be able to participate in the customer journey.


## What you’ll need:

- A computer with a Dynamics 365 Marketing environment


# Exercise 1: Create a dynamic segment

1.  Log into Dynamics 365 Marketing. Change to the **Outbound marketing** area, in the **Change area** drop-down menu.

2.  Navigate to **Segments** under the **Customers** group. 

3.  Select **+New** and choose **+New Dynamic Segment.**

4.  When prompted to select a Segment Template, select **Skip**.

5.  In the **Name** segment located in the middle of the screen, enter `Humongous Insurance`

6.  On the right, next to Undo/Redo, make sure **Natural view** is selected.

7.  Select **Add query block** (If a pop-up appears, close it.) 

8.  In the first field, the entity **Contact** should be selected. If it is not, change the query entity to **Contact**. 

	- Create the following condition: Company Name **is** Humongous Insurance.

9.  Select **+ Add** then choose **Add condition to Contact**. 

	- Select **Or** for the operator.

	- Create the following condition: Email **contains** humongousinsurance.

10. Select **+ Add** then choose **Add condition to Contact**. 

	- Select **And** for the operator.

	- Create the following condition: Status **is** Active.

11. Select **Save** and then select **check for errors** in the toolbar. Correct any if needed. 

12. Select **Go live** in the toolbar. 

13. Select the **Members** tab. 

	- Verify you see contacts with a Humongous Insurance email or Humongous company name. 

	- Note: You may need to refresh or wait a few minutes before the contacts appear. 


# Exercise 2: Create a dynamic segment with an exclusion segment

1.  Log into Dynamics 365 Marketing.

2.  Navigate to **Segments** under the **Customers** group. 

3.  Select **+ New** and choose **+ New Dynamic Segment.**

4.  When prompted to select a Segment Template, select **Skip**.

5.  Name the segment `Business Customers`

6.  Select **Add query block** (If a pop-up appears, close it.) 

7.  In the first field, the entity **Contact** should be selected. If it is not, change the query entity to **Contact**. 

	- Create the following condition: Status **is** Active.

8.  Select **+ Add** and select **Add condition to Contact**. 

	- Select **And** for the operator.

	- Create the following condition: Description **contains** Business.

9.  Below the conditions you just created, click **Add segment block**. 

	- Change the operator to **but not**. 

	- Start typing **Hum** and select the **Humongous Insurance** record.

10. Select **Save** and then select **check for errors** in the toolbar. Correct any if needed.

11. Select **Go live** in the toolbar. 

12. Select the **Members** tab. 

	- Verify you do not see any contacts with a Humongous Insurance email. 

    **Note:** You may need to refresh or wait a few minutes before the contacts appear. 


# Exercise 3: Create a contact

To participate in the journey, you will need to set yourself up as a contact. Because the segment previously created is dynamic, once you create the contact record and fill out the description field, it should automatically appear in the segment.

1.  Log into Dynamics 365 Marketing.

2.  Navigate to **Contacts** under the **Customers** group. 

3.  Select **+New**.

4.  In the **First Name** field, enter a generic first name.

5.  In the **Last Name** field, enter a generic last name.

6.  In the **Job Title** field, enter Finance Director or CFO. 

7.  In the **Email** field, enter your email.

8.  In the **Address: City** field, enter `Seattle`

9.  In the **Address: State/Province** field, enter `Washington`. Select **Done**. 

10. Navigate to the **Details** tab. In the **Personal Notes** field, enter Business.

11. Select **Save &amp; Close**. 

12. Navigate back to **Segments**. Open the **Business Customers** segment. Verify the contact you created appears.

    **Note:** You may need to refresh or wait a few minutes before the contact appears.
