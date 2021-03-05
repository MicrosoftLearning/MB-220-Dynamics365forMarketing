---
lab:
    title: 'Lab 6.1: Create an event'
    module: 'Module 6: Manage events'
---


Module 6: Manage events
=====

## Practice Lab 6.1


Lab Overview
============

Scenario
--------

Contoso is hosting an annual conference.

You need to create an event record in Dynamics 365 Marketing and start
filling out all the planning information regarding the event. The event is
happening on site only and has 150 seats available. The waitlist is allowed and
for each available spot, 10 invitations will be sent out. When additional seats
are available, you want waitlisted contacts to be registered automatically.

There are two guest speakersn. This is a free
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

-   A computer with a Dynamics 365 Marketing environment

-   2 image files for upload:

    -   emmalowtonprofileimage

    -   percybowmanprofileimage

Exercise 1: Create an in-person event
=====================================

1.  Download the image files from the resource documents.

2.  Log into Dynamics 365 Marketing.

3.  Create a new building.

    - Expand the menu at the bottom of the left sidebar that reads **Marketing**. Switch to the **Events** area.

    - Select **Buildings** from the **Venue management** section.
    
    - Enter the venue name as **[my prefix] Convention Center**. Add the estimated capacity as 150.

    - Add the following details on the Address section:

        1.  Address line 1: 1234 Parkway Ave

        2.  City: Minneapolis

        3.  Postal Code: 81940

        4.  State/province: Minnesota

    - Save the building record.

    - Click on the Rooms tab. Create a new room.

    - Enter the room name as **[my prefix] North Conference Room**. Add the capacity as 150.

    - Save and close the room record.

4.  Create a new event.

    - Navigate to **Events** in the **Events** section of the left menu. Select **+New.**

    - From the General tab, update the following information based on the
        event invitation.

    - In the Key information section add the event name as **[my prefix] 10th Contoso
        Conference.** Specify type as **Conference**.

    - In the Schedule section, add the event time zone as **Pacific**, event start date as a month from today, and
        event end date as a month from today + 2 days.

    - In the Location section, add the building and room you created in step 2. (To find it easily, you can start by typing in your prefix.)

    - In the Venue constraints section, verify the capacity and update the
        waitlist for this event field to Yes.

    - In the Waitlist section, update the number of invitations per slot as **10** and
        automatically register waitlisted contacts per the invite.

    - Save the event record.

5.  Add sessions and speakers to the event.

    - Navigate to the Agenda tab and add the following sessions. Note that the
        area you add sessions is below the session calendar. Use the outer
        scroll to navigate.

        1.  Session 1 / 6:30 PM-8:30 PM / [my prefix] Convention Center /
            [my prefix] North Conference Room

        2.  Session 2 / 8:30 PM-10:30 PM / [my prefix] Convention Center /
            [my prefix] North Conference Room

    - Create two new speaker engagements. When you create a new speaker
        engagement, you will need to name the record and then create a new
        speaker. Both speakers are external. Create the speaker records using your prefix (for example, **[my prefix] Percy Bowman.**)
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
