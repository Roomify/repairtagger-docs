.. _bat_drupal_installation:

Installation
************
Assuming you have all the dependencies in place, as described in :doc:`requirements`, you can now proceed to activate the BAT modules and get set up.

Activate Modules
-----------------
Visit ``/admin/modules/`` and activate the following modules:

* BAT - Booking and Availability Management Tools
* BAT Event
* BAT Event UI
* BAT Fullcalendar
* BAT Unit
* Booking and Availability Tools API
* Composer Manager (Drupal 7 only, this needs to activated explicitly as it is not strictly a BAT dependency)

Once you confirm installation, Drupal will request all the dependencies to these modules. Provided that they are all already downloaded, you may simply continue. If something is missing, cancel the process, download the missing modules, and then continue.

Install BAT PHP Library
-----------------------

.. tabs::

    .. group-tab:: 8.x

        When BAT is installed with Composer, the BAT PHP library will automatically be installed in the ``/vendor/roomify/bat`` directory. See `Using Composer with Drupal <https://www.drupal.org/docs/develop/using-composer/using-composer-with-drupal>`_ for more information.

    .. group-tab:: 7.x

        Provided that you are using Composer Manager, X Autoload, and have Composer, you should now have a composer.json file written in ``/sites/default/files/composer``. You can change this location and where the PHP Library will be downloaded by visiting ``admin/config/system/composer-manager/settings`` and setting the Vendor Directory to a location of your choosing.

        Now, visit ``/sites/default/files/composer`` on the command line and run ``composer install`` (this assumes that you have already set up Composer for your development environment - if not follow the `information here <https://www.drupal.org/project/composer_manager>`_)

Install FullCalendar Libraries
------------------------------------

.. tabs::

    .. group-tab:: 8.x

        The Drupal 8 version of BAT loads the fullcalendar libraries via a CDN. To use site-local copies, do the following:

        #. Download the correct FullCalendar version (`Check here for the current D8-compatible version of FullCalendar <http://cgit.drupalcode.org/bat/tree/test/project.make?h=8.x-1.x#n27>`_ and unpack in ``/libraries/``. You should have a structure similar to ``/libraries/fullcalendar/``.
        #. Download the correct Fullcalendar Scheduler version (`Check here for the current D8-compatible version of FullCalendar Scheduler <http://cgit.drupalcode.org/bat/tree/test/project.make?h=8.x-1.x#n34>`_ and unpack in ``/libraries/``. You should have a structure similar to ``/libraries/fullcalendar-scheduler/``.

    .. group-tab:: 7.x

        #. Download the correct FullCalendar version (`Check here for the current compatible version of FullCalendar <https://git.drupalcode.org/project/bat/blob/7.x-1.x/bat.make#L28>`_ and unpack in ``sites/all/libraries/``. You should have a structure similar to ``libraries/fullcalendar/``.
        #. Download the correct Fullcalendar Scheduler version (`Check here for the current compatible version of FullCalendar Scheduler <https://git.drupalcode.org/project/bat/blob/7.x-1.x/bat.make#L36>`_ and unpack in ``sites/all/libraries/``. You should have a structure similar to ``libraries/fullcalendar-scheduler/``.
        #. Visit ``admin/config/development/jquery_update`` and ensure that the default jQuery version for your admin theme, as well as the site overall, is at least 1.10.

Verify Setup
-------------
Once setup is completed you should see the following in ``admin/report/status``

.. tabs::

    .. group-tab:: 8.x

        *  BAT PHP Library

        .. image:: images/batphp_d8.png

        *   FullCalendar

        .. image:: images/fullcalendarok_d8.png

        *   Finally, in ``admin/bat`` you should have:

        .. image:: images/batok_d8.png

    .. group-tab:: 7.x

        *  Composer Manager

        .. image:: images/composermanager.png

        *   FullCalendar

        .. image:: images/fullcalendarok.png

        *   Finally, in ``admin/bat`` you should have:

        .. image:: images/batok.png


We are now ready to get set up!
