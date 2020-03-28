.. _bat_drupal_requirements:

Requirements
************

Introduction
============
BAT for Drupal uses four components that are all required to get the full range of functionality.

#.  The `BAT PHP Library <https://github.com/roomify/bat>`_  - this provides the core booking functionality. The best way to install and manage it on your Drupal site is through `Composer and Composer Manager for Drupal <https://www.drupal.org/project/composer_manager>`_
#.  The `BAT <https://drupal.org/project/bat>`_ module is a wrapper around the library providing Entity, Views, Rules and Event Management via calendars.
#.  The `BAT API module <https://drupal.org/project/bat_api>`_ provides REST access to event data and event manipulation. It powers functionality, such as, the dragging and dropping of events on the calendar UI.
#.  The `FullCalendar jQuery library <http://fullcalendar.io>`_ as a UI to events.


Dependencies
=============

Drupal Modules
---------------

.. tabs::

    .. group-tab:: 8.x

        * `BAT API <http://drupal.org/project/bat_api>`_ > version 1.x
        * `Ctools <http://drupal.org/project/ctools>`_
        * `Views <http://drupal.org/project/views>`_
        * `Views Megarow <https://www.drupal.org/project/views_megarow>`_
        * `Views Bulk Operations <https://www.drupal.org/project/views_bulk_operations>`_
        * `Search API <https://www.drupal.org/project/search_api>`_
        * `Facet API <https://www.drupal.org/project/facetapi>`_
        * `Services <http://drupal.org/project/services>`_ (a dependency of BAT API, also `this patch <https://www.drupal.org/node/2920007>`_ is currently required)

    .. group-tab:: 7.x

        * `BAT API <http://drupal.org/project/bat_api>`_ > version 2.x
        * `X Autoload <https://drupal.org/project/xautoload>`_ - provides support for PSR-4 style name spaces
        * `Composer Manager <https://www.drupal.org/project/composer_manager>`_ - to get the BAT PHP library
        * `Date <http://drupal.org/project/date>`_
        * `Entity <http://drupal.org/project/entity>`_
        * `Entity Reference <http://drupal.org/project/entityreference>`_
        * `Ctools <http://drupal.org/project/ctools>`_
        * `JQuery Update <http://drupal.org/project/jquery_update>`_
        * `Libraries <http://drupal.org/project/libraries>`_
        * `Views <http://drupal.org/project/views>`_
        * `Views Megarow <https://www.drupal.org/project/views_megarow>`_
        * `Views Bulk Operations <https://www.drupal.org/project/views_bulk_operations>`_
        * `Search API <https://www.drupal.org/project/search_api>`_
        * `Facet API <https://www.drupal.org/project/facetapi>`_
        * `Services <http://drupal.org/project/services>`_ (a dependency of BAT API)


jQuery Libraries
----------------

.. tabs::

    .. group-tab:: 8.x

        #. `FullCalendar library <https://fullcalendar.io/download/>`_ (check bat.make in the module directory for the correct version to download)
        #. `FullCalendar Scheduler extension <https://fullcalendar.io/scheduler/download/>`_. Please note that scheduler is a premium add-on to FullCalendar, and you must purchase a license if you intend to use it in a commercial project. See `Scheduler License Information <http://fullcalendar.io/scheduler/license/>`_ (Scheduler is not developed by Roomify) (check bat.make in the module directory for the correct version to download)

    .. group-tab:: 7.x

        #. `FullCalendar library <https://fullcalendar.io/download/>`_ (check bat.make in the module directory for the correct version to download)
        #. `FullCalendar Scheduler extension <https://fullcalendar.io/scheduler/download/>`_. Please note that scheduler is a premium add-on to FullCalendar, and you must purchase a license if you intend to use it in a commercial project. See `Scheduler License Information <http://fullcalendar.io/scheduler/license/>`_ (Scheduler is not developed by Roomify) (check bat.make in the module directory for the correct version to download)
        #. `Timepicker <https://fgelinas.com/code/timepicker/releases/jquery-ui-timepicker-0.3.3.zip>`_ - This is not a strict requirement - it simply makes the creation of hour-based events easier.


Drush-based Setup
------------------

.. tabs::

    .. group-tab:: 8.x

        If you are familiar with Drush and Drush make, then you can use the project.make file in the BAT module repository to get all the modules required (in versions we have tested BAT with) and the FullCalendar Library. From your Drupal root directory run:

        ``drush make --no-core sites/all/modules/bat/test/project.make``

    .. group-tab:: 7.x

        If you are familiar with Drush and Drush make, then you can use the bat.make file in the BAT module repository to get all the modules required (in versions we have tested BAT with) and the FullCalendar Library. From your Drupal root directory run:

        ``drush make --no-core sites/all/modules/bat/bat.make``


Composer
---------

.. tabs::

    .. group-tab:: 8.x

        When installing the BAT module via composer, the BAT library will automatically be installed.

    .. group-tab:: 7.x

        You will need to install Composer if you don't have that already (a great idea since it will be needed for Drupal 8).

        Follow the instructions from the `Composer Manager module <https://www.drupal.org/project/composer_manager>`_ to get set up.
