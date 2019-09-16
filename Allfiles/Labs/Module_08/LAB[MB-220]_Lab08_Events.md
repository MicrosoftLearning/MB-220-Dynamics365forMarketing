Module 8: Events
=====

## Practice Lab 8


Lab Overview
============

Scenario
--------

Contoso is hosting an annual conference at the Minneapolis Convention Center.
Below is the event invitation.

You need to create an event record in Dynamics 365 for Marketing and start
filling out all the planning information regarding the event. The event is
happening on site only and has 150 seats available. The waitlist is allowed and
for each available spot, 10 invitations will be sent out. When additional seats
are available, you want waitlisted contacts to be registered automatically.

There are two guest speakers as described in the invitation. This is a free
event and guests will need to accommodate their own stays.

The event registration will be done via the event portal. You want to add
pictures of the speakers. Dinner is provided so you want to add a custom
registration field for meal choice. The field may be a single choice field with
Chicken, Fish, and Steak options.

Lab Overview
------------

This lab comprises of one exercise:

-   In the exercise, you will create an in-person event from scratch.

What You’ll Need
----------------

-   A computer with a Dynamics 365 for Marketing environment

-   2 image files for upload:

    -   emmalowtonprofileimage

    -   percybowmanprofileimage

Exercise 1: Create an in-person event
=====================================

1.  Download the image files from the resource documents.

2.  Log into Dynamics 365 for Marketing

3.  Create a new building.

    - Navigate to Events \> Venue management \> Buildings and create a new
        building.

    - Enter the venue name. Add the estimated capacity as 150.

    - Add the following details on the Address section:

        1.  Address line 1: 1234 Parkway Ave

        2.  City: Minneapolis

        3.  Postal Code: 81940

        4.  State/province: Minnesota

    - Save the building record.

    - Click on the Rooms tab. Create a new room.

    - Enter the room name. Add the capacity as 150.

    - Save and close the room record.

4.  Create a new event.

    - Navigate to Events \> Event \> Events and create a new event.

    - From the General tab, update the following information based on the
        event invitation.

    - In the Key information section add the event name as 10th Contoso
        Conference. Specify type and format per the invite.

    - In the Schedule section, add the event time zone, event start date, and
        event end date.

    - In the Location section, add the building and room you created in step
        2.

    - In the Venue constraints section, verify the capacity and update the
        waitlist for this event field to Yes.

    - In the Waitlist section, update the number of invitations per slot and
        automatically register waitlisted contacts per the invite.

    - Save the event record.

5.  Add sessions and speakers to the event.

    - Navigate to the Agenda tab and add the following sessions. Note that the
        area you add sessions is below the session calendar. Use the outer
        scroll to navigate.

        1.  Session 1 / 6:30 PM-8:30 PM / Minneapolis Convention Center /
            Ballroom A

        2.  Session 2 / 8:30 PM-10:30 PM / Minneapolis Convention Center /
            Ballroom A

    - After you create the sessions you will need to change each of their
        statuses to live.

    - Create two new speaker engagements. When you create a new speaker
        engagement, you will need to name the record and then create a new
        speaker using the names from the invite. Both speakers are external.
        Percy Bowman’s email is <pbowman@adatum.com> and Emma Lowton’s email is
        <elowton@adventure-works.com>. Percy will be speaking at the first
        session and Emma will be speaking at the second. Be sure to associate
        each speaker with the appropriate session.

    - After adding the speaking engagement, open each speaker’s record and add
        their profile images.

6.  Create custom registration fields and publish the event.

    - Navigate to the Registration and attendance tab. Create a new event
        custom registration field with the given meal choices from the scenario.

    - Save the event record.

    - Set the event publish status to Live.

7.  Navigate to the event URL. Verify the conference details are correct, the
    sessions are listed, and speaker images are visible.
