---
lab:
    title: 'Lab: Prepare Marketing environment'
    module: 'Module 1: Marketing Application Configuration'
---


# Module 1: Marketing Application Configuration
## Practice Lab 1: Prepare Marketing Environment 
----

## Important notice re: tenants - temporary workaround

As of January 23, 2020, WWL is unable to provide students with pre-provisioned Dynamics 365 access, and is working on a solution that should be available in the next 4-6 weeks. As a workaround, we are recommending using Dynamics 365 Trial accounts. Each student will be responsible for requesting these. To help students in getting the Dynamics 365 tenants (including Marketing), M365 tenants will be provided through the Authorized Lab Hosters. This is a short-term solution and we will keep all stakeholders including Learning Partners and MCTs updated as progress is made and advise as a more permanent solution timeline for pre-provisioning Dynamics 365 access for lab use is established. Please work with your Authorized Lab Hoster for provisioning of the M365 Tenants for the students and follow the instructions below to use the M365 tenant to secure a Dynamics 365 trial for your appropriate application.
 
1. Using your provided M365 credential, log into https://admin.microsoft.com/ and accept the terms.
2. Once you’ve logged in successfully, access https://trials.dynamics.com/Dynamics365/marketing.
3. Under “Work email,” enter the email address from the M365 tenant. Under “phone number,” enter your own phone number.
4. Select Get Started.
5. You will be prompted to enter your password for the on.microsoft.com account. Enter the password provided for the M365 tenant.
6. If you are prompted to accept terms and conditions, accept them. Your environment may take a few minutes to provision.

Lab Overview
============

Scenario
--------

Contoso is an insurance company that has outgrown their single-send marketing
software and are looking to obtain a more holistic view of their marketing
efforts to help facilitate sales.

Contoso already has Dynamics 365 for Customer Engagement. Because of its
seamless integration, the marketing department decides to move forward with
Dynamics 365 for Marketing.

Contoso already has email templates they have been using in their previous
software. They want to transfer their marketing assets along with their contact
list to the new system.

Lab Overview
------------

This lab compromises of two exercises:

1.  In the first exercise, you will upload image files to be used in marketing
    pages and emails.

2.  In the second exercise, you will import accounts and contacts to Dynamics
    365 for Marketing from csv files.

 What you’ll need:
------------------

-   A computer with a Dynamics 365 for Marketing environment

-   10 image files to be used in marketing content and 2 csv files containing
    Contoso contact and account data:

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

2.  Log into Dynamics 365 for Marketing.

3.  Navigate to Files in the Marketing Content section and click the + Upload
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

2.  Log into Dynamics 365 for Marketing.

3.  Since these are Accounts, you can upload them directly in the Accounts
    section. However, for this exercise, we are going to import them from the
    Settings area. Navigate to the Advanced Settings menu and the Import Data
    section.

4.  The import entity will be account and the file type is csv.

5.  Select quotation mark for the delimiter settings.

6.  Map the column headings to the corresponding fields in Dynamics 365 for
    Marketing:

    -  Account Name = Company Name

7.  Finish the import.

    -  Note: Some accounts may already exist in the system, so the import may
        show both successes and errors. That is expected and you can continue
        onto the next step.

8.  Contacts can be uploaded directly in the Contacts section. However, for this
    exercise, we are going to import them from the Settings area. Navigate to
    the Advanced Settings menu and the Import Data section.

9.  The import entity will be contact and the file type is csv.

10. Select quotation mark for the delimiter settings.

11. Map the column headings to the corresponding fields in Dynamics 365 for
    Marketing:
	- Last Name = Last Name

    -  Company Name = Company Name (Lookup)

    -  Email = Email

    -  First Name = First Name

    -  Marketing Contacts = Marketing Only (Two Options)

        1.  Yes = Yes

        2.  Click OK

    -  State = Address 1: State/Province

12. Finish the import.

13. Navigate to the contacts setting to view your new contacts.
