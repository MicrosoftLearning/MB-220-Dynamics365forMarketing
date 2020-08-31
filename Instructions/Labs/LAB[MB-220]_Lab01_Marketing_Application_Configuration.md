---
lab:
    title: 'Lab: Prepare Marketing environment'
    module: 'Module 1: Marketing Application Configuration'
---


# Module 1: Marketing Application Configuration
## Practice Lab 1: Prepare Marketing Environment 
----

Lab Overview
============

Scenario
--------

Contoso is an insurance company that has outgrown their single-send marketing
software and is looking to obtain a more holistic view of their marketing
efforts to help facilitate sales.

Contoso already has Dynamics 365 customer engagement apps. Because of its
seamless integration, the marketing department decides to move forward with
Dynamics 365 Marketing.

Contoso already has email templates they have been using in their previous
software. They want to transfer their marketing assets along with their contact
list to the new system.

Lab Overview
------------

This lab compromises of two exercises:

1.  In the first exercise, you will upload image files to be used in marketing
    pages and emails.

2.  In the second exercise, you will import accounts and contacts to Dynamics
    365 Marketing from csv files.

 What you’ll need:
------------------

-   A computer or VM with a Dynamics 365 Marketing environment

-   10 image files to be used in marketing content and 2 csv files containing
    Contoso contact and account data. These can be found in the AllFiles folder on GitHub, or may be distributed directly by your MCT.

    -   briefcase.png

    -   contosologo.png

    -   facebook.png

    -   flood.png

    -   heroemail.jpg

    -   heropage.jpg

    -   linkedin.png

    -   safebox.png

    -   travel.png

    -   twitter.png

    -   Contoso Accounts.csv

    -   Contoso Contacts.csv

Exercise 1: Upload marketing content 
=====================================

Contoso wants to use the same images from their current system. To so do, you
will need to upload the marketing assets to Dynamics 365 for Marketing.

1.  Download the image files from the resource documents. Extract the files to a
    folder on your desktop.

2.  Navigate to home.dynamics.com and sign in with your user credentials. Record the characters before the "@" symbol in your email address - it should be a first name and a last initial. These characters will become your "alias" throughout the course. Write them down somewhere you'll be able to access throughout the course.

**Important:** Please be aware that this tenant and the Dynamics 365 organization will be shared with the other students in your classroom, like employees would share a tenant when using the Dynamics 365 instance belonging to their organization. Do not use any PII (personally identifiable information) when creating records. It is also good practice to use your username prefix (ex., **mollyc**) in front of all records, data, apps, workflows, etc. you create.

3.  From the list of the available apps, select **Marketing.** The Marketing app will open. In the left menu, navigate to **Files** in the Marketing Content section and click the + Upload
    button to open the upload files window. Add the 10 image files.

4.  While the upload window is open, add the keywords “logo” and “contoso” to
    the contosologo image file. Since this is a new system, keywords will need
    to be created instead of selected. When you’re done adding keywords, finish
    the upload.

5.  Ensure 10 images files uploaded.

6.  Using the search bar, type “con” and hit enter. Ensure the Contoso logo
    appears in the search results.

Exercise 2: Import accounts and contacts
========================================

Contoso was using their old system to email their marketing contacts. These
contacts need to move into Dynamics 365 for Marketing, but they need to be
differentiated from sales contacts. To do that, you will need to import them as
marketing-only contacts. Before you can import the contacts, you will need to
import the companies they are associated with first.

**Note:** Please be aware that depending on your authorized lab hoster, your
hosted lab may not have Microsoft Excel to open and view the csv import files.
The files can still be imported successfully, but you may not be able to view
them before importing.

1.  Download the csv files from the resource documents. Extract the files to a
    folder on your desktop.

2.  Since these are Accounts, you can upload them directly in the Accounts
    section.

3. Click the Gear icon in the upper right corner to access Advanced Settings. Select **Data Management** and then select **Imports.**

4.  Click **Import Data** and select the **Contoso Accounts** file. 

5.  Select quotation mark for the data delimiter settings. Select **Next**. When prompted with **Select Data Map**, hit **Next.**

6.  Select **Account** for the entity and click **Next.** Select **Col1** for the Account Name field.

7.  Finish the import.

    -  Note: Some accounts may already exist in the system, so the import may
        show both successes and errors. That is expected and you can continue
        onto the next step.

8.  Repeat this process for the **Contoso Contacts** file, selecting the **Contact** entity as the target entity instead. All options will be the same until you reach the **Map Fields** window.

11. Map the column headings to the corresponding fields in Dynamics 365 for
    Marketing:
	- Last Name = Last Name

    -  Company Name = Company Name (Lookup)

    -  Email = Email

    -  First Name = First Name
    
    - Gender = Gender (Option Set)

    -  Marketing Contacts = Marketing Only (Two Options)
    	- Empty = Ignore
	- Yes = Yes
	- Press OK.

    -  State = Address 1: State/Province

12. Finish the import.

13. Navigate to the contacts setting to view your new contacts.
