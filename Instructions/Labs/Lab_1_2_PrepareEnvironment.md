---
lab:
    title: 'Lab 1.2: Prepare Marketing environment'
    module: 'Module 1: Configure Dynamics 365 Marketing'
---

# Module 1: Configure Dynamics 365 Marketing

## Lab 1.2: Prepare Marketing Environment

# Lab Overview

# Scenario

Contoso Insurance is a company that sells insurance to both residential and business customers. 
During their annual review, the sales & marketing teams observe a year over year decrease in the number of services sold to each business customer. The marketing team decides to put together a cross sell campaign to encourage current business customers to purchase additional services. 

They plan to send a series of emails with a call to action for the customer to fill out a marketing form that will result in a phone call from a sale rep. They plan to run this campaign for 2 months.

For this campaign, the Marketing Coordinator will need to:

- Build a segment of current business customers that will participate in the campaign.

- Build a subscription center form and subscription center page for business customers to be able to opt into and out of marketing communications.

- Build the content for the campaign including the marketing emails, marketing form, and a marketing page to host the form.

- Build the customer journey that will automate the delivery of the campaign content.

Sales would like a way to prioritize the leads generated from this campaign based on their marketing engagement activities. The sales and marketing teams work together to define the scoring criteria and point system for this campaign. The Marketing Coordinator will then create the model within Dynamics 365 Marketing. 

As part of the journey, an agent will be assigned a task each time a lead submits the marketing form. For each lead, the agent will have visibility to all the marketing emails they received and be able to see what marketing activities they interacted with. They can also review the lead score based on the model the sales and marketing team put in place. 

After the campaign ends, the marketing team will review the insights from their content to determine which content was most effective and what components should be utilized in future campaigns.

To get started, the Marketing Coordinator needs to upload the digital assets that will be used in the campaign. They also need to upload any new sales contacts the company has acquired recently and update details for existing contacts and accounts.

## Lab Overview

This lab compromises of two exercises:

1. In the first exercise, you will upload image files to be used in marketing pages and emails. (For this exercise, we will use the Library in the Marketing content section of **Outbound marketing.** Later on, we will upload images from the **Real-time marketing** Asset section, to show the images are shared between them.)

2. In the second exercise, you will update details for existing contacts within Dynamics 365 Marketing. 

3. In the third exercise, you will create a task template that will be used in the customer journey. 

## What you’ll need:

- A computer or VM with a Dynamics 365 Marketing environment

- 12 image files to be used in marketing content. These can be found in the AllFiles folder on GitHub under Labs/Content Images for Demo 1_1.

	- agent-email-icon.png

	- coho-vineyard.png

	- computer-icon.png

	- contoso-insurance-logo.png

	- customer-reviews-icon.png

	- dean-halstead.png

	- insurance-agent.png

	- reserved.png

	- shop-icon.png

	- stop-icon.png

	- thank-you-image.png

	- umbrella-icon.png

# Exercise 1: Upload marketing assets

1. Download the image files (.png files) from the resource documents. Extract the files to a folder on your desktop. 

2. Log into Dynamics 365 Marketing with your **admin** credentials. 

3. By default, you should be in the **Real-time marketing** area. Switch areas to **Outbound marketing**. Navigate to **Library** under the **Marketing content** group. 

4. Select the **+ New** button to open the upload files window. 

5. Select **+ Add files**, locate the 12 .png files on your local computer, and select them. 

6. While the upload window is open, add keywords to the images. Since this is a new system, keywords will need to be created and then selected. 

	- contoso-insurance.png – Add keyword “logo” 

7. When you’re done adding keywords, finish the upload. Ensure 12 images files uploaded. Select **Done**. 

8. Using the Filter search box, enter `con`. Ensure the **Contoso Insurance logo** appears in the search results. 

9. These files will now be available for users to incorporate into their marketing operations. 


# Exercise 2: Update existing contacts

In an upcoming lab, students will build segments for an outbound marketing campaign and an in-person event. The demo contact records need to be updated in order to populate those segments. The steps below will allow the students to build segments for competitors, business contacts, and contacts living in the Seattle area.

1.  Log into Dynamics 365 Marketing with your **admin** credentials.

2.  Navigate to the **Accounts** entity under the **Customers** group.

3.  Open **Humongous Insurance**. 

	- Select the **Related tab** then select **Contacts**. 

	- Select all contacts listed then select **Edit**. 

	- On the **Details** tab, locate the **Personal Notes** field. Enter `Business` in the field. Select **Save**.  

	- Select one of the contacts. Navigate to the **Details** tab. Verify “Business” appears in the **Personal Notes** field. 

4.  Navigate to the **Contacts** entity under the **Customers** group. 

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

		- Personal Notes: `Business`

		- Select **Save**. 


# Exercise 3: Create a task template

1.  Log into Dynamics 365 Marketing with your **admin** credentials. 

2.  Navigate to **Task templates** under the **Marketing templates** group. 

3.  Select **+New**.

	- **Name:** Follow up with customer.

	- **Subject**: Customer requested coverage review.

	- **Schedule type:** Delay (in days).

	- **Start delay:** 0.

	- **Start time:** 01 Hour. 

4.  Select **Save &amp; Close**. 

