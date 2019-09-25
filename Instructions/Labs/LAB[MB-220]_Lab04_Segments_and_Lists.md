---
lab:
    title: 'Lab: Work with segments'
    module: 'Module 4: Segments and Lists'
---


Module 4: Segments and Lists
======

## Practice Lab 4

Lab Overview
============

Scenario
--------

As Contoso continues preparing their nurture campaign, they need to define the
audience that will participate in the customer journey.

Lab Overview
------------

This lab compromises of three exercises:

1.  In exercise one, you will create a dynamic segment to pull in all contacts
    from the southwest.

2.  In exercise two, you will create two segments – one of your competitors and
    another one to pull in all contacts from the southwest except your
    competitors.

3.  In exercise three, you will create and configure a subscription center page
    and update the system content settings.

 What you’ll need:
------------------

-   A computer with a Dynamics 365 for Marketing environment

Exercise 1: Create a dynamic segment 
=====================================

Contoso wants to target contacts who live in the southwest. You previously
uploaded a list of contacts into the system. Now you need to create a segment
pulling in specific contacts. The segment is what will be used in the customer
journey to interact with your intended audience.

1.  Log into Dynamics 365 for Marketing.

2.  Navigate to Segments and create a new segment.

3.  Name the segment Contoso Southwest Segment. Ensure the type is dynamic.

4.  Navigate to the Definition tab.

5.  Add the following statements:

    - Contact Address 1: State/Province is California OR

    - Contact Address 1: State/Province is Arizona OR

    - Contact Address 1: State/Province is Texas

6.  Save and check for errors. Correct any if needed.

7.  Go live.

8.  Give the system time, come back and ensure your members match the contacts
    you uploaded.

Exercise 2: Create a segment using union, exclude, or intersect logic
=====================================================================

During further analysis of the contacts, it was found that a few are from a
competitive company, Relecloud. You will want to create a dynamic query pulling
in anyone that comes from Relecloud. You then want to create a new segment using
the exclude logic to make sure these contacts are not included in your customer
journey.

1.  Log into Dynamics 365 for Marketing.

2.  Navigate to Segments and create a suppression segment for your competitors.

    - Create a new segment.

    - Name the segment Relecloud Suppression Segment.

    - Ensure type is dynamic.

    - Navigate to the Definition tab.

    - Generate a statement so that: Contact’s Account is Relecloud And
        Contacts All\*.

        - Note: When choosing an account, begin typing the name and then
            select it (instead of manually typing the entire name).

    - Save and check for errors. Correct any if needed.

    - Go live.

3.  Create a segment for all your southwest contacts except your competitors.

    - Create a new segment.

    - Name the segment Contoso Southwest Excluding Competitors Segment.

    - Change type to compound.

    - Navigate to Definition tab.

    - Select the Contoso Southwest Segment from Exercise 1, exclude the
        Relecloud Suppression Segment you just created.

    - Save and check for errors. Correct any if needed.

    - Go live.

Exercise 3: Create subscription center page and update system content settings
==============================================================================

Since Contoso is new to Dynamics 365 for Marketing, you will need to create a
subscription center page for anyone to be able to opt out of communications from
Contoso.

1.  Log into Dynamics 365.

2.  Navigate to Surveys from the app selector menu.

3.  Under the Marketing work area, select Marketing Lists.

4.  Create a subscription list.

    - Navigate to Marketing Lists and create a new list.

    - Name the list Contoso Subscription List and set the Subscription to
        True.

    - Save your changes.

5.  Add the subscription list to a subscription form.

    - Navigate to Marketing Forms and create a new form using the herakloin
        template.

    - Name the form Contoso Subscription Form. Ensure the type is subscription
        center and that only contacts are updated.

    - Update the header to: “Please update your preferences below”. Center
        align and change the font to Seqoe UI.

    - Update the font for First Name, Last Name, Phone, and Email to Seqoe UI.

    - Make First Name, Last Name, and Email required.

    - From the Toolbox, drag the Contoso Subscription List above Do not email.
        Change the Label to Contoso Newsletter and select prefill.

    - Remove [Update subscriptions heading].

    - Save and check for errors. Correct any if needed.

    - Go live.

6.  Create a new marketing page.

    - Navigate to Marketing Pages and create a new page using the blank
        template.

    - Name the page Contoso Subscription Page with a type of subscription
        center and enter the partial URL as subscription.

    - Drag and drop an Image block. Add the Contoso logo and center align.

    - Drag and drop a Form block below the image. Search for the Contoso
        Subscription Form you just created. Input the following:

        1.  Confirmation message: Thank you. Your submission has been received.

        2.  Error message: Something went wrong. Please try again.

        3.  Redirecting URL: http://www.contoso.com

    - Save and check for errors. Correct any if needed.

    - Go live.

7.  Update content settings.

    - Navigate to Content Settings in the Templates section and select the
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
