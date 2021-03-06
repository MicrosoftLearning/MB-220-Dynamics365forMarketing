---
lab:
    title: 'Lab 2.1: Work with segments'
    module: 'Module 2: Manage segments and lists'
---


Module 2: Manage segments and lists
======

## Practice Lab 2.1 - Work with segments

Lab Overview
============

Scenario
--------

As Contoso continues preparing their nurture campaign, they need to define the
audience that will participate in the customer journey.

Lab Overview
------------

This lab compromises of three exercises:

1.  In exercise one, you will create a contact and create a dynamic segment that will pull those contacts.

2.  In exercise two, you will create two segments – one of your competitors and
    another one to pull in all contacts from the southwest except your
    competitors.

3.  In exercise three, you will create and configure a subscription center page
    and update the system content settings.

 What you’ll need:
------------------

-   A computer with a Dynamics 365 Marketing environment

Exercise 1: Create a dynamic segment 
=====================================

Contoso wants to target contacts who live in the southwest. You previously
uploaded a list of contacts into the system. Now you need to create a segment
pulling in specific contacts. The segment is what will be used in the customer
journey to interact with your intended audience.

1.  Log into Dynamics 365 Marketing.

2. Navigate to **Contacts** in the left menu, in the **Customers** group. Click **+New.** For **First Name**, enter your alias. For **Last Name**, enter **Test.**

3. In **Address 1: State/Province**, enter California, Arizona, or Texas. Fill in the other fields with fictional information (as many as you'd like). Do not enter any personally identifiable information.

4. Click **Save and close.** You should be able to see your new contact record in the view.

2.  Navigate to **Segments** in the left menu, in the **Customers** group. Select **+New** and choose **+New Dynamic Segment.**

3.  When prompted to select a Segment Template, click **Skip.** 

4.  In the **Definition** tab, name the segment **[my prefix] Contoso Southwest Segment**. 

5.  Select **Add Query Block.** (If a pop-up appears, close it.) In the first field, the entity **Contact** should be selected. If it is not, change the query entity to Contact. Add the following statements:

    - Address 1: State/Province **equals** California 
    
    - Click +Add and select **Add condition to Contact** using **OR**

    - Address 1: State/Province **equals** Arizona
    
    - Click +Add and select **Add contion to Contact** using **OR**

    - Address 1: State/Province **equals** Texas

6.  Save and check for errors. Correct any if needed.

7.  Go live.

8.  Give the system time and refresh if needed. After a few minutes, reopen the segment and navigate to the **Members** tab. Ensure the contact you created earlier in the exercise is listed in the view. 

Exercise 2: Create a segment using union, exclude, or intersect logic
=====================================================================

During further analysis of the contacts, it was found that a few are from a
competitive company, Relecloud. You will want to create a dynamic query pulling
in anyone that comes from Relecloud. You then want to create a new segment using
the exclude logic to make sure these contacts are not included in your customer
journey.

2.  Click **Segments** in the left menu to return to the main segment view.

    - Create a new segment by clicking **+New** and selecting **+New Dynamic Segment.**
    
    - When prompted to select a template, click **Skip.**

    - Name the segment **[my prefix] Relecloud Suppression Segment.**

3. Generate a statement so that the Contact’s Account is Relecloud And Contacts All.

    - Click **Add Query Block.** (If a pop-up appears, close it.)
    
    - **Contact** should be selected as the query entity.
    
    - Create the following condition: Company Name **equals** Relecloud.

    - Save and check for errors. Correct any if needed.

    - Go live.

3.  Create a segment for all your southwest contacts except your competitors.

    - Return to the main segment view by clicking **Segments** in the left menu. Create a new segment by clicking **+New** and selecting **+New Dynamic Segment.**
    
    - When prompted to select a template, click **Skip.**

    - Name the segment **[my prefix] Contoso Southwest Excluding Competitors Segment**.

    - Select **Add segment block.**

    - Start by typing your prefix into the Segment field. Select the **[my prefix] Contoso Southwest Segment** segment from Exercise 1.

    - Click **Add Segment Block** again. Change the modifier to **but not**. Start typing your prefix into the field and select the **[my prefix] Relecloud Suppression Segment** segment.

    - Save and check for errors. Correct any if needed.

    - Click on the **Members** tab. You should see contacts from the selected states, but no members of the Relecloud company.

Exercise 3: Create subscription center page and update system content settings
==============================================================================

Since Contoso is new to Dynamics 365 Marketing, you will need to create a
subscription center page for anyone to be able to opt out of communications from
Contoso.

1. From the left menu, select **Subscription lists** from the **Customers** group.

4.  Select **+New subscription list.**

    - Name the list **[my prefix] Contoso Subscription List**.

    - Click **Save.**

5.  Add the subscription list to a subscription form.
    
    - Navigate to **Marketing Forms** under the **Internet marketing** group.  Create a new form using the heraklion
        template.

    - Click the **Summary** tab. Name the form **[my prefix] Contoso Subscription Form**. From the header, ensure the type is subscription
        center and that only contacts are updated.

    - Return to the **Designer** tab. Update the header to: “Please update your preferences below." Center
        align and change the font to Segoe UI.

    - Update the font for First Name, Last Name, Phone, and Email to Segoe UI.

    - Make First Name, Last Name, and Email required.

    - From the Toolbox, drag the **[my prefix]] Contoso Subscription List** above Do not email.
        Change the Label to Contoso Newsletter and select prefill. Change the font of Contoso newsletter and do not email to Segoe UI.

    - Remove [Update subscriptions heading].

    - Save and check for errors. Correct any if needed.

    - Go live.

6.  Create a new marketing page.

    - Navigate to **Marketing pages** from the Internet marketing group. Click **+New**. When prompted to select a template, click **Skip.**

    - Click the dropdown in the upper right corner. Name the page **[my prefix] Contoso Subscription Page** with a type of subscription
        center and enter the partial URL as **[myprefix]subscription**. It should look like the following: **mollycsubscription.**

    - Drag and drop an Image block. With the image block selected, click the magnifying glass icon under **Image source** in the Properties tab. Select **Contoso logo** and ensure that **Center** is selected for **Alignment**.

    - Return to the **Toolbox** tab. Drag and drop a Form block below the image. Start by typing in your prefix into the search box and select the **[my prefix] Contoso
        Subscription Form** you just created. Input the following:

        1.  Success notification: Thank you. Your submission has been received.

        2.  Error message: Something went wrong. Please try again.

        3.  Redirecting URL: http://www.contoso.com

    - Save and check for errors. Correct any if needed.

    - Go live. (If you recieve a pop-up, click OK.)

7.  Update content settings.

    - Navigate to **Content Settings** in the Templates group and select the
        default content settings record. You will need to stop the entity record
        before you can update. Add the following:

        1.  Address main: 4567 Main St. Seattle, WA 98052

        2.  LinkedIn URL: https://www.linkedin.com/company/contoso12345/about/

        3.  Twitter URL: https://twitter.com/ContosoInc

        4.  Facebook URL: https://www.facebook.com/Contoso-102137176602590/

        5.  Subscription center: Use the edit assist option to select the
            Contoso Subscription Page you just created. Be sure to select the
            FullPageURL.

    - Save and check for errors. Correct any if needed.

    - Go live.
