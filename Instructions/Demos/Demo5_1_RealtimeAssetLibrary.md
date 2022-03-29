---
demo:
    title: 'Demo 5.1: Real-time marketing asset library'
    module: 'Module 5: Manage emails and journeys in Dynamics 365 Marketing'
---


#  Module 5: Manage emails and journeys in Dynamics 365 Marketing

## Demo 5.1 - Real-time marketing asset library

# Demo Overview

## Scenario

The marketing team wants to begin using the real-time marketing capabilities.
They start by updating real-time marketing settings and uploading assets to the
real-time library.

## Lab Overview

This lab comprises of four exercises:

-   In the first exercise, you will demonstrate updating the consent center for
    marketing.

-   In the second exercise, you will demonstrate update marketing email
    settings.

-   In the third exercise, you will demonstrate copy all files over from
    outbound marketing.

-   In the fourth exercise, you will demonstrate the capabilities of the
    real-time marketing asset library.

## What You’ll Need

-   A computer with a Dynamics 365 Marketing environment

-   Seven (7) image files to be used in marketing content. These can be found in
    the AllFiles folder on GitHub in the Module_5 folder.

    1.  app store icon (png)

    2.  Contoso Insurance Welcome Kit (pdf)

    3.  Get the most out of your policy video (mp4)

    4.  google play icon (png)

    5.  shaking hands over contract (png)

    6.  person using computer (png)

    7.  person using laptop (png)

## Exercise 1: Update the consent center

1.  Log into Dynamics 365 Marketing with your admin credentials.

2.  Navigate to the **Settings** work area.  

3.  Under **Customer engagement** click on **Compliance.**

4.  Navigate to the **Real-Time consent** tab.

5.  In **Company address**, enter **1234 Main St., Seattle, WA 56789.**

6.  Click **Save.**

## Exercise 2: Update marketing email settings

1.  Log into Dynamics 365 Marketing with your admin credentials.

2.  Navigate to the **Settings** work area.  

3.  Under **Email marketing** click on **Default settings.**

4.  Open the **DefaultMktSettings**.

5.  Navigate to the **Marketing email** tab.

6.  In the **Default from email** field, enter ContosoInsurance\@contoso.com.

7.  In the **Default from name** field, enter Contoso Insurance.

8.  Click **Save.**

9.  Note: The **Default from email** domain will auto-update to the sending
    domain of your Dynamics 365 environment.

## Exercise 3: Copy files from outbound to real-time

1.  Log into Dynamics 365 Marketing with your admin credentials.

2.  Navigate to the **Outbound marketing** work area.

3.  Under **Marketing content**, select **Files.**

4.  Click **Copy all files to Real-time marketing** in the command bar.

5.  Click **Copy files.**

6.  Note: If you get an error trying to move all files, try selecting a few
    images (click the checkmark toward the top right of the image to select
    images individually). Once the images are selected, click **Copy all files
    to Real-time marketing** in the command bar then click **Copy files**.
    Repeat this for all files you want to move to real-time marketing.

## Exercise 4: Review the features of the real-time asset library

1.  Download the image files from the resource documents. Extract the files to a
    folder on your desktop.

2.  Log into Dynamics 365 Marketing with your admin credentials.

3.  Navigate to the **Real-time marketing** work area.

4.  Navigate to **Library** under the **Assets** group.

5.  Show how to upload files to the real-time asset library.

    1.  From your computer, locate the images downloaded in step 1 of this
        exercise. Select all images **except person using laptop**. (This image
        will be uploaded in a future step.) Drag and drop the files into the
        Asset library.

    2.  In the **Alt text** field, enter image.

    3.  Click **Upload now**.

    4.  Wait for the upload to complete.

6.  Describe how the real-time asset library can manage images, videos, and
    documents.

    1.  In the Asset library, select **Images**. Explain how the asset library
        supports images such as JPEG, GIF, and PNG files.

    2.  Select **Videos**. Explain how the asset library supports videos such as
        MP4, AVI, and MPEG files.

    3.  Select **Documents**. Explain how the asset library supports documents
        such as Word, PowerPoint, and PDFs.

7.  Show AI tagging.

    1.  In the Asset library, select. **All**.

    2.  Locate the **person using computer** image. Select the image by clicking
        the circle icon to the top right of the image. (A blue circle with a
        white checkmark will indicate the image is selected).

    3.  Show how AI tags are automatically generated for the image. (When an
        image is selected, properties about the image appear on the right of the
        asset library. AI tags are the second set of tags. If you don’t see any
        tags, you may need to refresh your browser. The system needs a few
        minutes after the image has been uploaded to generate tags.)

8.  Show how to version assets.

    1.  While the **person using computer** image is still selected, click
        **Replace binary** in the command bar. (This button appears toward the
        middle of the page above the Asset library header.)

    2.  From your computer, locate the **person using laptop** image and select
        it.

    3.  Wait for the upload to complete.

    4.  Click on the image. Show how the **Last modified by** now displays
        **Version 2**.
