====================
LabVIEW for uniplot!
====================

This plugin allows uniplot to parse and plot the various data files used by
LabVIEW.

.. note::

   Currently only LabVIEW Measurement (``.lvm``) files are supported but there
   are plans to support ``.tdm`` and ``.tdms`` files aswell.

------------
Installation
------------

This plugin is available on PyPI so installation is as simple as::

    $ pip install uplt-labview

If you want the most up-to-date version then clone the `repo`_ and act thusly::

    $ git clone https://github.com/Sean1708/uplt-labview.git
    $ cd uplt-labview
    $ pip install .

-----
Usage
-----

uniplot should automatically discover correctly formatted LabVIEW Measurement
files by examining the first line of the file for ``LabVIEW Measurement`` so
using it should be as simple as::

    $ uniplot labview_data.lvm

If uniplot gets it wrong for whatever reason then you can force selection like
so::

    $ uniplot -p lvm labview_data.lvm

If uniplot gets it wrong and you don't know why, please consider opening an
issue on the `repo`_.

If ``X_Columns`` is ``One`` or ``Multi`` uniplot will plot each channel against
it's corresponding ``X_Value`` column. If ``X_Columns`` is ``No`` then there
must be an even number of columns and uniplot will plot every second column
against the column on it's left-hand side.

.. _`repo`: https://github.com/Sean1708/uplt-labview
