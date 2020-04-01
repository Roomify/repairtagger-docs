.. Repairtagger documentation master file, created by
   cecily on Sat March 28 2020 whilst under quarantine due to COVID-19.

.. Helpful hints:

.. Type backquote (on same key as tilde) to link other rst docs)

######################################
Welcome to Repairtagger documentation!
######################################

Repairtagger Documentation Version 2.0

Need Help? email us at support@repairtagger.com

************
Introduction
************

Repairtagger is your ticket tracking, customer database, and notification
system. Keep track of your customers and their repair history, using any tags
you like. With texts and email templates, notifying your customers is easier
than ever.

If you are new to Repairtagger, start with :ref:`ticketlife` to get a step by
step explanation of how to use the app.

Terminology
===========

**Tag**
  A physical tag that is attached to the item to be repaired. This tag must have
  a number, either embedded in a QR code, or written on the tag.
  You can refer to :ref:`tagoptions` for a description of tag options, and
  :ref:`scantag` to learn how to scan a tag.

**Ticket**

  A record in Repairtagger that stores the information about an item that needs
  repair. A ticket will have a reference to the customer it is for, the repair(s)
  to be done,  the amount charged for each repair, how much the customer paid when
  they dropped the item off, and optionally, notes and photos.

  See: :ref:`scantag` for more details.

**Customer**

  A record in Repairtagger that stores a customers name and optionally a mobile
  phone number, landline number, email, notes, and photos.

  See: :ref:`customerlist` for more details.

**Customer List**

  A searchable list of your Customers.

  See: :ref:`customers` for more details.

**Ticket List**

  A list of your tickets, divided into the following categories:

  **Active**

    Repairs not yet done and/or the customer has not been notified.

  **Complete**

    Customer has been notified and the item is waiting for pickup.

  **Archived**

    Item is complete, the customer has picked it up, and the ticket has been
    archived.

See: :ref:`ticketlist` for more details.

**Reports**

  A simple overview of your ticket numbers for the month.

  See: :ref:`reports` for more details.

**Price List**

  Your price list is divided into categories, which each have their own repair
  types. A repair type is given a name, a category, a price, and if that repair
  type has a range, you can specifiy the max price.

  See: :ref:`pricelist` for more details.

.. toctree::
   :maxdepth: 2
   :caption: Getting Started

   The life and times of a ticket<ticketlife/index.rst>
   Step 1: Scan a tag <ticketlife/scantag.rst>
   Step 2: Fill in ticket information  <ticketlife/intake.rst>
   Step 3: Do the work  <ticketlife/dothework.rst>
   Step 4: Notify the customer  <ticketlife/notifications.rst>
   Step 5: Pickup and Archival <ticketlife/pickup.rst>

.. toctree::
   :maxdepth: 2
   :caption: Reports

   Introduction<reports/index.rst>

.. toctree::
   :maxdepth: 2
   :caption: Tickets

   Introduction<tickets/index.rst>
   Ticket List <tickets/ticketlist.rst>
   View Ticket <tickets/viewticket.rst>
   Edit Ticket <tickets/editticket.rst>
   Delete Ticket <tickets/deleteticket.rst>

.. toctree::
   :maxdepth: 2
   :caption: Tag Options

   Introduction<tagoptions/index.rst>
   Text Recognition <tagoptions/ocr.rst>
   Keyboard <tagoptions/keyboard.rst>
   QR Tags <tagoptions/qr.rst>

.. toctree::
   :maxdepth: 2
   :caption: Customers

   Introduction<customers/index.rst>
   Customer List <customers/customerlist.rst>
   Customer Status Page <customers/customerstatus.rst>
   Edit Customer <customers/editcustomer.rst>

.. toctree::
   :maxdepth: 2
   :caption: Admin

   Introduction<admin/index.rst>
   Price List <admin/pricelist.rst>
   Due Dates <admin/duedates.rst>
   Notifications <admin/notificationtemplates.rst>
   Help <admin/help.rst>
   Business Information <admin/bizinformation.rst>
   Account <admin/account.rst>
   Subscription <admin/subscription.rst>

.. DONE
