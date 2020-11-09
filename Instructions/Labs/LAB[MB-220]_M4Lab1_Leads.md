---
lab:
    title: 'Lab 4.1: Lead scoring'
    module: 'Module 4: Manage leads, accounts, and contacts'
---


Module 4: Manage leads, accounts, and contacts
=======

## Practice Lab 4.1: Lead scoring

Lab Overview
============

Scenario
--------

Contoso has several new marketing initiatives for the year. One of those
includes upselling insurance to existing customers. In order to target their
audience and send the appropriate customers to sales, they want to create a lead
scoring model based on demographic data.

Lab Overview
------------

This lab compromises of one exercise:

1.  In this exercise you will create a lead scoring model to score leads based
    on demographic data.

 What you’ll need:
------------------

-   A computer with a Dynamics 365 Marketing environment

Exercise 1: Create a lead scoring model for demographic data 
=============================================================

Contoso is interested in expanding their services to specific industries in the
southwest region. You will need to create a lead scoring model that will
increase scores based on industry and state.

The scoring model will be on a grading scale of 1-100 as follows:

- 0-24 - Cool

- 25-59 - Warm

- 60-99 - Hot

---

1.  Log into Dynamics 365 Marketing.

2.  Navigate to the Lead Management section in the left menu and select **Scoring Models**. Click +New.

3.  Switch to the **Summary** tab. Name the model **[my prefix] Contoso Southwest Outreach Model**.
    Set the target to **Contact** and save.

4.  Switch back to the Design tab. On the right, navigate to **Grades**. Input 100
    as your sales ready score. Add three new grades:

    - Cool 0-24

    - Warm 25-59

    - Hot 60-99

5.  Navigate to the **Toolbox**. Drag a Condition onto the canvas. Name the
    condition Industry Demographic.

6.  On the condition tile, select the arrow down button to expose the child
    condition. Select the child condition and name it Industry. In the entity
    field, select Lead. Add the following expressions:

    - Industry = Business Services

    - Industry = Entertainment Retail

    - Industry = Eating and Drinking Places
    
    - **Note:** You may have the option to select from two Industry fields. Pick the one that has Values as option sets, not empty fields.

7.  Navigate back to the toolbox and add an Action to the right of the Industry
    Demographic condition. In the action, increase the score by 15.

8.  In the toolbox, drag a new condition below Industry Demographic and name it
    Southwest Demographic.

9.  On the condition tile, select the arrow down button to expose the child
    condition. Select the child condition and name it Southwest States.

10. Since our state field lives on the contact level, we will have to make a
    transcendental jump from lead to contact. In the entity field, type Lead
    and select it. Add a period and then select Parent contact. Your entity
    field will look like this: **Lead.Parent contact**. Add the following
    expressions:

    1.  Address 1: State/Province = Texas

    2.  Address 1: State/Province = Arizona

    3.  Address 1: State/Province = California

11. Navigate back to the toolbox and add an Action to the right of the Southwest
    Demographic condition. In the action, increase the score by 25.

12. Save and check for errors. Correct any as needed.

13. Go live.
