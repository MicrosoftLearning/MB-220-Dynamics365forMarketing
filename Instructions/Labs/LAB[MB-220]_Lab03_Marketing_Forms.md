---
lab:
    title: 'Lab: Create marketing forms and pages'
    module: 'Module 3: Marketing Forms, Marketing Pages and Internet Marketing'
---


Module 3: Marketing Forms, Marketing Pages and Internet Marketing 
======

## Practice Lab 3

Lab Overview
============

Scenario
--------

Contoso would like to set up a nurture campaign to entice current and potential
customer to request a quote. In order to do so, they must start by creating the
components that make up the nurture campaign.

The nurture campaign will include sending an email outlining the company’s
expertise to increase their contacts’ knowledge of what Contoso has to offer.
The goal is to get them to request an insurance quote.

In order for them to request a quote, Contoso needs a form for current and
potential customers to fill out and a page to host the form.

Lab Overview
------------

This lab compromises of two exercises:

1.  In exercise one, you will create a marketing form.

2.  In exercise two, you will create a marketing page and embed the marketing
    form on the page.

 What you’ll need:
------------------

-   A computer with a Dynamics 365 for Marketing environment

Exercise 1: Create a marketing form 
====================================

You need to start by creating a form for leads to fill out in order to request
an insurance quote. This form will be hosted on a marketing page.

1.  Log into Dynamics 365 for Marketing.

2.  Navigate to Marketing Forms and create a new form.

3.  From the template gallery, select argos.

4.  Name the form Contoso Request a Quote Form. Designate this as a landing page
    and set to update contacts and leads.

5.  Save your changes.

6.  In the form heading, type “Please fill out this form for an agent to contact
    you” and change the font size to 16.

7.  Since we already know where these leads came from, you can delete the “How
    did you hear about us?” field. In its place we want to add an Industry field
    to know which agent to assign to the lead. Select the field from the right
    and drag and drop it above the submit button.

8.  Make the following updates:

    - First Name: required / prefill / change font to Seqoe UI

    - Last Name: required / prefill / change font to Seqoe UI

    - Email: required / prefill / change font to Seqoe UI

    - Phone Number: required / prefill / change font to Seqoe UI

    - Company Name: required / change font to Seqoe UI

    - Number of Employees: required / change font to Seqoe UI

    - Job Title: required / change font to Seqoe UI

    - Industry: required / set the default value to Consumer Services / change
        font to Seqoe UI

9.  Preview the form.

10. Save and check for errors. Correct any if needed.

11. Go live.

Exercise 2: Create a marketing page and embed a form 
=====================================================

Next, you need to create a marketing page to host the form you created in
Exercise 1. This is where you will direct leads to request a quote.

1.  Log into Dynamics 365 for Marketing.

2.  Navigate to Files.

3.  Open the heropage.jpg image. Copy the URL and paste in a place you can
    access later.

4.  Navigate to Marketing Pages and create a new page.

5.  From the template gallery, select marbella.

6.  Name the page Contoso Request a Quote Page. Designate this as a landing page
    and enter quote in the partial URL field.

7.  Save your changes.

8.  Select the top left image block. Navigate to the Image Gallery. Locate and
    select the contosologo you uploaded in Lab 1. In the properties, set the
    width to 250px.

9.  Toggle to the Styles tab.

10. In the Hero image field, paste the URL you copied for heropage.jpg. Ensure
    the hero image now appears instead of the placeholder.

11. Still on the Styles tab, change Color 1 to \#E2E2E2 and Color 5 to \#666666.
    Change Inner background and Form background color to \#f5f5ed.

12. Remove Book Pro 360 from the page.

13. Add a divider where the Book Pro 360 text block was. Change the color to
    \#f5f5ed and the top padding to 20. Adding this spacer will help align the
    text block with the top of the form.

14. Change “Content of the Guide” to “Things to Consider When Buying Business
    Insurance:” Note: If you copy and paste, the formatting may change. You may
    want to type the new text instead of copy and paste.

15. Replace the bullets with the following:

    -   Do you create and sell a product?

    -   Do you have employees?

    -   Do you have one or more company vehicles?

    -   Do you have one or more office locations?

    -   Do you offer a service to customers?

16. Select the button block and delete.

17. Select the image block placeholder below the form block and delete.

18. Click the form block. In the Marketing form field, begin typing the name of
    the form you created in Exercise 1 then select the form. If your form does
    not appear, save your marketing page and navigate to your form to ensure it
    is in live status.

19. Input the following:

    -   Confirmation message: Thank you. Your submission has been received.

    -   Error message: Something went wrong. Please try again.

    -   Redirect URL: http://www.contoso.com

20. Scroll down to the next section. Change “In this complete guide you'll see”
    to “Contoso offers insurance for all your business needs”. Reminder: If you
    copy and paste, the system may not apply the text styling. You may want to
    type the text instead of copy and paste.

21. In the four image boxes below, add the following images you uploaded in Lab
    1along with alt text describing the image:

    -   safebox.png / alt text: cyber liability insurance

    -   flood.png / alt text: flood insurance

    -   briefcase.png / alt text: business income insurance

    -   travel.png / alt text: travel insurance

22. Update the \@Title Name below each image to the following:

    -   Cyber Liability

    -   Flood

    -   Business Income

    -   Travel

23. Delete all \$ xx.xx text boxes.

24. Save your changes.

25. Below Frequently **Asked Questions,** replace the questions and sample text
    with the following:

    -   How much does business insurance cost?

    -   There is no one-size-fits all answer, but we can offer ballpark ranges.
        Click through to find out what similar businesses typically pay.

    -   What does General Liability Insurance cover?

    -   General Liability Insurance can help cover legal expenses when your
        business is sued over third-party bodily injuries, property damage, and
        more.

    -   Why do I need Professional Liability Insurance?

    -   Unhappy clients may bring frivolous lawsuits against your company. And
        even if your client doesn't win, the cost of defending yourself can be
        prohibitive.

26. In the bottom footer area, select the left image block. Add the contosologo.
    Change the width to 150.

27. In the three social link image blocks, add social media image icons and link
    them to your social media profiles. Note: You will need to double click the
    social link boxes to be able to select the image and edit the details. After
    you have added the image and details, click each image to locate the link
    option.

    -   1st social link box will be Facebook. Source: facebook.png / Alt text:
        Facebook logo / Width: 50 / Height: 50. Click Ok. Update the link to:
        <https://www.facebook.com/Contoso-102137176602590/>. Click OK

    -   2nd social link box will be Twitter. Source: twitter.png / Alt text:
        Twitter logo / Width: 50 / Height: 50 / . Click Ok. Update the link to:
        https://twitter.com/ContosoInc Click OK

    -   3rd social link box will be LinkedIn. Source: linkedin.png / Alt text:
        LinkedIn logo / Width: 50 / Height: 50 / . Click Ok. Update the link to:
        <https://www.linkedin.com/company/contoso12345/about/> Click OK

28. Change the copyright information at the bottom to the current year and
    Contoso.

29. Preview the page.

30. Save and check for errors. Correct any if needed

31. Go live.

32. Navigate to the Summary tab and open the full page URL to view your page. It
    may take a moment for all content to appear.

33. If you would like to make changes, stop the page, make your updates, check
    for errors and go live again.

34. Fill out the form using the following details. After you submit, ensure your
    confirmation message appears and your redirecting URL works.

    -   First Name: Jamie

    -   Last Name: Stark

    -   Email:
        [jamie\@adventureworkscycles.com](mailto:libby@adventureworkscycles.com)

    -   Phone: 555-123-9876

    -   Company: Adventure Works Cycles

    -   Number of Employees: 150

    -   Title: Marketing Manager

    -   Industry: Entertainment Retail

    -   Submit

35. After you submit, ensure your confirmation message appears and your
    redirecting URL works based on the details you added in step 19.

36. Navigate to the Leads section. Verify the lead you just submitted appears in
    the system. You may need to change the view from My open leads to All Leads.
