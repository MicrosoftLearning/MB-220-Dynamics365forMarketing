Module 5: Marketing Emails
=======

## Practice Lab 5

Lab Overview
============

Scenario
--------

Contoso wants to send an email to their current contacts in hopes of enticing
them to request a quote for a new service. They want to encourage them to visit
their marketing page and fill out the request a quote form.

Lab Overview
------------

This lab compromises of one exercise:

1.  In this exercise you will create an email that encourages recipients to
    visit your marketing page and request a quote for insurance.

 What you’ll need:
------------------

-   A computer with a Dynamics 365 for Marketing environment

Exercise 1: Create an email from a template
===========================================

1.  Log into Dynamics 365 for Marketing.

2.  Navigate to Marketing Emails and create a new email using the gairo
    template.

3.  Name the email Contoso Request a Quote Email and type the following in the
    subject line: “Contoso offers your business protection when you need it”.

4.  From the designer, change the text in the preheader at the top left from
    “Thanks for joining us!” to “Request a quote today!”

5.  Select the main image on the designer. Open Image Gallery and select the
    heroemail image.

6.  Select the 200 x 80 image block below the hero image. Navigate to the Image
    Gallery and select the contosologo. Change the height to 70 and center
    align.

7.  Change the header in the body of the email to “Business protection when you
    need it.” Change the font size to 24 and center align. Note: If you copy and
    paste, the formatting may change. You may want to type the new text instead
    of copy and paste.

8.  Change the body to “We can help you build and protect your business by
    providing customized insurance solutions to support you and your budget.”
    Change the font size to 20 and center align. Reminder: If you copy and
    paste, the formatting may change. You may want to type the new text instead
    of copy and paste.

9.  Select the button, change the text to “Request a Quote”. In the properties,
    change the background color to \#31459c, center align and change the width
    to 220. In the link field, use the assist edit icon to select the Contoso
    Request a Quote Page you created in Lab 3. Be sure to select the
    msdyncrm_full_page_URL.

10. Remove the text below the button. This text was hard coded to the template
    instead of added using one of the standard toolbox elements. That means you
    will need to remove this from the HTML. Switch to the HTML tab and search
    for “Or verify using this link”. When you find that in the code, start by
    selecting the open parentheses p (\<p\>) before it and drag to the close
    parentheses p after it (\</p\>) then hit delete. The full text you are
    deleting is \<p class="verify"\>Or verify using this link: \<a
    href="http://www.fabrikam.com"\>http://www.fabrikam.com\</a\> \</p\>

11. Return to the designer tab and update the copyright to this year and change
    the company to Contoso.

12. Preview the email.

13. Save and check for errors. Correct any if needed.

14. Send yourself a test email. (You may need to check your junk folder to find
    the email.)

15. Make any final changes as needed.

16. Go live.
