---
lab:
    title: 'Lab 2.1: Work with segments'
    module: 'Module 2: Manage segments and lists'
---

# Module 2: Manage segments and lists

## Practice Lab 2.1 - Work with segments

 

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

1. Log into Dynamics 365 Marketing.

2. Navigate to **Segments** under the **Customers** group. 

3. Select **+New** and choose **+New Dynamic Segment.**

4. When prompted to select a Segment Template, click **Skip.**

5. In the **Name** segment located in the middle of the screen, enter **[my prefix] Humongous Insurance.**

6. On the right, next to Undo/Redo, make sure **Natural view** is selected.

7. Select **Add Query Block.** (If a pop-up appears, close it.) 

8. In the first field, the entity **Contact** should be selected. If it is not, change the query entity to **Contact**. 

	- Create the following condition: Company Name **is** Humongous Insurance.

9. Click **+ Add** then choose **Add condition to Contact**. 

	- Select **Or** for the operator.

	- Create the following condition: Email **contains** humongousinsurance.

10. Click **+ Add** then choose **Add condition to Contact**. 

	- Select **And** for the operator.

	- Create the following condition: Status **is** Active.

11. Click **Save** and click **check for errors** in the toolbar. Correct any if needed.

12. Click **Go live** in the toolbar.

13. Click on the **Members** tab. 

	- Verify you see contacts with a Humongous Insurance email or Humongous company name.

	- Note: You may need to refresh or wait a few minutes before the contacts appear.

# Exercise 2: Create a dynamic segment with an exclusion segment

1. Log into Dynamics 365 Marketing.

2. Navigate to **Segments** under the **Customers** group. 

3. Select **+New** and choose **+New Dynamic Segment.**

4. When prompted to select a Segment Template, click **Skip.**

5. Name the segment **[my prefix] Business Customers.**

6. Select **Add Query Block.** (If a pop-up appears, close it.) 

7. In the first field, the entity **Contact** should be selected. If it is not, change the query entity to **Contact**. 

	- Create the following condition: Status **is** Active.

8. Click **+Add** and select **Add condition to Contact**.

	- Select **And** for the operator.

	- Create the following condition: Description **contains** Business.

9. Below the conditions you just created, click **Add segment block**. 

	- Change the operator to **but not**. 

	- Start typing your prefix into the field and select the **[my prefix] Humongous Insurance**.

10. Click **Save** and click **check for errors** in the toolbar. Correct any if needed.

12. Click **Go live** in the toolbar.

12. Click on the **Members** tab. 

	- Verify you do not see any contacts with a Humongous Insurance email.

	- Note: You may need to refresh or wait a few minutes before the contacts appear.

# Exercise 3: Create a contact

To participate in the journey, you will need to set yourself up as a contact. Because the segment previously created is dynamic, once you create the contact record and fill out the description field, it should automatically appear in the segment.

1. Log into Dynamics 365 Marketing.

2. Navigate to **Contacts** under the **Customers** group. 

3. Select **+New**.

4. In the **First Name** field, enter [my prefix].

5. In the **Last Name** field, enter a generic last name.

6. In the **Job Title** field, enter Finance Director or CFO.

7. In the **Email** field, enter your email.

8. Click the edit icon in the **ADDRESS** section.

9. In the **Address: City** field, enter Seattle.

10. In the **Address: State/Province** field, enter Washington.

11. Navigate to the **Details** tab. In the **Personal Notes** field, enter Business.

12. Click **Save &amp; Close**.

13. Navigate back to **Segments**. Open the **[my prefix] Business Customers** segment. Verify the contact you created appears.

	- Note: You may need to refresh or wait a few minutes before the contact appears.

 
