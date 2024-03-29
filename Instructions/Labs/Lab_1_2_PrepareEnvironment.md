---
lab:
    title: 'Lab 1.2: Prepare Customer Insights - Journeys environment'
    module: 'Module 1: Configure Dynamics 365 Customer Insights - Journeys'
---

# Module 1: Configure Dynamics 365 Customer Insights - Journeys

## Lab 1.2: Prepare Customer Insights - Journeys Environment

# Lab Overview

# Scenario

Contoso Insurance is a company that sells insurance to both residential and business customers. 
During their annual review, the sales & marketing teams observe a year over year decrease in the number of services sold to each business customer. The marketing team decides to put together a cross sell campaign to encourage current business customers to purchase additional services. 

They plan to send a series of emails with a call to action for the customer to fill out a marketing form that will result in a phone call from a sales rep. They plan to run this campaign for 2 months.

For this campaign, the Marketing Coordinator will need to:

- Build a segment of current business customers that will participate in the campaign.

- Manage business customers' consent levels to be able to opt into and out of marketing communications.

- Build the content for the campaign including the marketing emails and marketing forms, and host the forms.

- Build the journey that will automate the delivery of the campaign content.

Sales would like a way to prioritize the leads generated from this campaign based on their marketing engagement activities. The sales and marketing teams work together to define the scoring criteria and point system for this campaign. The Marketing Coordinator will then create the model within Dynamics 365 Customer Insights - Journeys. 

As part of the journey, an agent will be assigned a task each time a lead submits the marketing form. For each lead, the agent will have visibility to all the marketing emails they received and be able to see what marketing activities they interacted with. They can also review the lead score based on the model the sales and marketing team put in place. 

After the campaign ends, the marketing team will review the insights from their content to determine which content was most effective and what components should be utilized in future campaigns.

To get started, the Marketing Coordinator needs to upload the digital assets that will be used in the campaign. They also need to upload any new sales contacts the company has acquired recently and update details for existing contacts and accounts.

## Lab Overview

This lab compromises of two exercises:

1. In the first exercise, you will upload image files to be used in marketing pages and emails. These files will be uploaded to the real-time asset library.

2. In the second exercise, you will update details for existing contacts within Dynamics 365 Customer Insights - Journeys. 

3. In the third exercise, you will create a task template that will be used in the journey.

4. In the fourth exercise, you will configure the default brand profile to be used in your marketing assets (like emails).

## What you’ll need:

- A computer or VM with a Dynamics 365 Customer Insights - Journeys environment

- 12 image files to be used in marketing content. These can be found in the AllFiles folder on GitHub under Labs/Content Images.

# Exercise 1: Upload marketing assets

1.  Download the image files (.png files) from the resource documents. Extract the files to a folder on your desktop. 

2.  Log into Dynamics 365 Customer Insights - Journeys with your **admin** credentials. 

3.  By default, you should be in the **Real-time journeys** area. Confirm that you are in the **Real-time journeys** area by opening the **Area selector** in the bottom left of the screen.

4.  In the left menu, navigate to the **Assets** section. Select **Library.** Select the **+ New** button to open the upload files window. 

5.  Select **+ Add files**, locate the 12 .png files on your local computer, and select them. 

6.  While the upload window is open, add a `logo` **tag** to contosologo.png

7.  Select **Upload**. Ensure 12 images files uploaded - a green checkmark with **Done** will appear for each file. Select **Done**.

8.  Using the Filter search box, enter `con` By default, this filter searches by the file name. Verify the Contoso Insurance logo appears in the search results. 

These files will now be available for users to incorporate into their marketing operations. 


# Exercise 2: Update existing contacts

In an upcoming lab, students will build segments for a marketing campaign and an in-person event. The demo contact records need to be updated in order to populate those segments. The steps below will allow the students to build segments for competitors, business contacts, and contacts living in the Seattle area.

1.  Log into Dynamics 365 Customer Insights - Journeys with your **admin** credentials.

2.  From the left navigation, select **Contacts**, under the **Audience** group.

3.  Open the contact **Alva Tharaldsen**. 

	- Under **Account Name**, select **Bellows College.** You will then navigate to the Bellows College account record.

	- Scroll down to the **Contacts** subgrid. All Contacts associated with Bellows College are listed here. Select all contacts in the list using the three dots menu and **Select**. Check all the contacts in the list. 

	- On the **Contacts** subgrid three dots menu, select **Edit**.
 
	- On the **Details** tab, locate the **Personal Notes** field. Enter `Business` in the field. Select **Save**.  

	- Select one of the contacts. Navigate to the **Details** tab. Verify “Business” appears in the **Personal Notes** field. 

4.  Navigate to the **Contacts** entity under the **Audience** group. (If you are not alraeady in the **Real-time marketing** area, switch areas.)

5.  Set a filter on **Company Name**. 

	- Select the drop-down arrow next to **Company Name**. Select **Filter by**. Choose **Equals** then select **Lucerne Publishing**, **Southridge Video**, and **Wingtip Toys**. Select **Apply**. 

	- Select all contacts for those 3 accounts. 

	- Select **Edit** in the command bar. Enter the following: 

		- Address 1: City: `Bellevue`

		- Address 1: State/Province: `Washington`

		- Details > Personal Notes: `Business`

		- Select **Save**. 

6.  Change the filter on **Company Name**.

	- Select the drop-down arrow next to **Company Name**. Select **Filter by**. Remove the current values then select **Adatum Corporation**, **Fourth Coffee**, and **Northwind Traders**. Select **Apply**. 

	- Select all contacts for those 3 accounts.

	- Select **Edit** in the command bar. Enter the following:

		- Address 1: City: `Redmond`

		- Address 1: State/Province: `Washington`

		- Details > Personal Notes: `Business`

		- Select **Save**. 

7.  Change the filter on **Company Name**.

	- Select the drop-down arrow next to **Company Name**. Select **Filter by**. Remove the current values then select **The Phone Company**, **Trey Research**, and **Wide World Importers**. Select **Apply**.

	- Select all contacts for those 3 accounts.

	- Select **Edit** in the command bar. Enter the following:

		- Address 1: City: `Seattle`

		- Address 1: State/Province: `Washington`

		- Details > Personal Notes: `Business`

		- Select **Save**. 

8.  Change the filter on **Company Name**.

	- Select the drop-down arrow next to **Company Name**. Select **Filter by**. Remove the current values then select **Fabrikam, Inc.**, **Munson’s Pickles and Preserves Farm**, and **Adventure Works Cycles**. Select **Apply**.

	- Select all contacts for those 3 accounts.

	- Select **Edit** in the command bar. Enter the following:

		- Details > Personal Notes: `Business`

		- Select **Save**. 


# Exercise 3: Create a task template

1.  Log into Dynamics 365 Customer Insights - Journeys with your **admin** credentials. 

2.  Navigate to **Task templates** under the **Assets** group. 

3.  Select **+New**.

	- **Name:** `Follow up with customer`

	- **Subject**: `Customer requested coverage review`

	- **Schedule type:** Delay (in days).

	- **Start delay:** 0.

	- **Start time:** 01 Hour. 

4.  Select **Save &amp; Close**.

# Exercise 4: Configure the default brand profile

1.  Log into Dynamics 365 Customer Insights - Journeys. Change areas to the **Settings** area.

2.  Navigate to **Brand profiles**, under the **Customer engagement** group.

3.  Open the **Default brand profile** record. Navigate to the **Senders** tab. You should see the **Default sender record** in the subgrid. Select the record to open it.

4.  In the **From email**, change everything before the @ symbol to `contosoinsurance`

5.  Change the **From name** to `Contoso Insurance`
   
6.  Select **Save and close.** You will return to the Brand profile record.

7. Select the **Social links** tab. Fill in the following:

	- **LinkedIn URL**: `https://www.linkedin.com/company/contoso12345/about/`

	- **Twitter URL**: `https://twitter.com/ContosoInc`

	- **Facebook URL**: `https://www.facebook.com/Contoso-102137176602590/`

8.  Select **Save & Close**.


