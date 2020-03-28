.. _bat_drupal_event_types:


Connect Types to Events
************************

In BAT we try to have the least possible amount of things hard-coded. This allows us to create truly flexible booking systems. However, it also means that we need to *explain* all these connections to the framework.

In :doc:`type_bundles` we created a Meeting Room Type and in :doc:`events` we created two types of events for availability and pricing. We now have to connect the two. In other words, we need to let BAT know that our meeting rooms types will have events of the type **Meeting Room Available** and **Pricing** associated with them.

Default event value fields
===========================
You connect Type Bundles to event types through a **default event value field**.

A default value event field holds the value for a given type of event *before* any actual events are created. For the meeting room example, these will hold the default values for Availability and Pricing. Events associated with the meeting rooms will modify and overwrite these default values.

In order to understand the need for default value event fields, consider what would happen if we did not have them: We would have to create events for every single point in time so as to have an availability and price value associated with the meeting rooms. Default value event fields simply indicate that if there is not an explicit event for a given period in time, use the default value.

To create default value event fields visit ``admin/bat/config/type-bundles`` and click on the **manage fields** operation of the type you are interested in and add fields to hold default event values.

Fixed State Events
-------------------

.. tabs::

    .. group-tab:: 8.x

        For fixed state events, add an entity reference field to your Type Bundle. It will reference an event state.

        .. image:: images/add_default_event_value_field_d8.png

        When creating the entity reference field, choose the "State" entity type.

        .. image:: images/select_entity_type_d8.png

        In the field settings, mark the field as required.

        .. image:: images/select_event_type_d8.png

        Now, with the field in place you can visit ``bat/config/type-bundles`` and click on the **edit** operation of the type bundle you are interested in. For every type of event, you will see a drop-down that allows you to connect a field of this type bundle to an event type.

        .. image:: images/connect.png

        This may seem like an extra step but you should keep in mind that BAT makes no assumptions. You may have multiple Fixed State event fields pointing to multiple event types. As a result, there is a bit of extra setup to define everything.

    .. group-tab:: 7.x

        For fixed state events, the type of field to hold the default value is always going to be BAT Event State Reference field.

        .. image:: images/add_default_event_value_field.png

        In the field settings you need to select the event type that this field will point to (it will only show event types that have fixed states).

        .. image:: images/select_event_type.png

        Now, with the field in place you can visit ``bat/config/type-bundles`` and click on the **edit** operation of the type bundle you are interested in. For every type of event, you will see a drop-down that allows you to connect a field of this type bundle to an event type.

        .. image:: images/connect.png

        This may seem like an extra step but you should keep in mind that BAT makes no assumptions. You may have multiple Fixed State event fields pointing to multiple event types. As a result, there is a bit of extra setup to define everything.


Arbitrary state events
-----------------------
Similarly to fixed state events, arbitrary state events require a default value event field. The difference is, in this case it does not have to be in the BAT Event State Reference field. It has to be in a field, however, that holds an integer value or that we transform to an integer value. As a result, we only support a specific subset of fields.

Currently those are:

* Integer
* Commerce Price
* Text

#. The first step is to create the field - in our example we will create an Integer field that will hold the cost.

.. image:: images/integer-field.png

#. We can now (under the Edit tab) link the **Cost** field to the **Meeting Room Cost** event type.

.. image:: images/link-cost-to-type.png

As we mentioned before, we can only handle a certain amount of fields for arbitrary values. 

Now, at this point, all that has happened is that BAT can:

* Connect unit types to event types
* Store the right information regarding availability and cost (because these are the event types we defined)

You need to create types (see :doc:`types`) and then in :doc:`manage_units` we explain how these types can be manipulated and values changed over time.

