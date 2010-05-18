Panda module for Drupal/CCK
===========================

    DISCLAIMER: this module is experimental and not recommended for production use.

A **Drupal 6** module that adds a new field "Video file" that can be added to your CCK content types.

Also available:

* the simple [PHP Panda client](http://github.com/newbamboo/panda_client_php) library that this application is based on
* the simple [Panda jQuery plugin](http://github.com/newbamboo/panda_uploader) used to upload files
* a [example standalone PHP application](http://github.com/newbamboo/panda_example_php)

Installation
============

Dependencies: CCK
-----------------

Since this module creates a new field type to be used with CCK, the CCK module must be also installed.

CCK is a very popular module and this should not be a problem. See more info at http://drupal.org/project/cck

Download it
-----------

Copy this code into your modules directory:

    cd YOUR-DRUPAL-PATH/sites/all/modules/
    git clone git@github.com:newbamboo/panda_drupal.git panda

Enable it
---------

Enable the module "Panda" at *Administer >> Site building >> Modules*

Create a new content type
-------------------------

Now you should be able to create a new content type that includes videos. For this, first you need to go to *Administer >> Content management >> Content types* and click on "Add a new content type".

Once this is added, you will see your new content type listed alongside others in the content types table. Click on "manage fields" next to it and you will be able to add a new field to the default ones. Give it an appropriate name and, in the "- Select a field type -" dropdown, select "Video file".

Now you will be able to add new video content at "Create Content" on the navigation menu.

How to use your favourite video player
======================================

By default, this module uses HTML5 to render the video player. You might want to use a different player instead, such as one of the many popular Flash players there are available.

This modules doesn't provide as yet an automated way to do this. Instead, a theme hook is provided for theme developers to implement. This should make it fairly simple for them to render the video in any way they wish. The name of this hook is `theme_panda_formatter_default`.


Copyright (c) 2010 New Bamboo. Distributed under the terms of the MIT License. See LICENSE file for details