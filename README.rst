.. image:: https://img.shields.io/coveralls/github/timcera/tsgettoolbox_wdfn
    :alt: Test Coverage
    :target: https://coveralls.io/r/timcera/tsgettoolbox_wdfn?branch=master
    :height: 20

.. image:: https://img.shields.io/pypi/v/tsgettoolbox_wdfn
    :alt: Latest release
    :target: https://pypi.python.org/pypi/tsgettoolbox_wdfn/
    :height: 20

.. image:: https://img.shields.io/pypi/l/tsgettoolbox_wdfn
    :alt: BSD-3 clause license
    :target: https://pypi.python.org/pypi/tsgettoolbox_wdfn/
    :height: 20

.. image:: https://img.shields.io/pypi/pyversions/tsgettoolbox_wdfn
    :alt: PyPI - Python Version
    :target: https://pypi.org/project/tsgettoolbox_wdfn/
    :height: 20

tsgettoolbox_wdfn - Quick Guide
===============================
The 'tsgettoolbox_wdfn' is a plugin-in for 'tsgettoolbox' that supplies
a command line interface and Python library to get time-series data from the
USGS Water Data for the Nation (WDFN).  The tsgettoolbox_wdfn will work with
Python 3.10+.

Documentation
-------------
Reference documentation is at `tsgettoolbox_documentation`_.

Installation
------------
At the command line::

    $ pip install tsgettoolbox_wdfn

    OR

    $ conda install -c conda-forge tsgettoolbox_wdfn

Usage Summary - Command Line
----------------------------
Just run 'tsgettoolbox --help' to get a list of subcommands.  To get detailed
help for a particular sub-command, for instance 'wdfn', type 'tsgettoolbox
wdfn --help'.

+----------------------------------+---------+--------+---------+----------+-----------------------+
| Sub-command                      | Spatial | Time   | Type    | Time     | Description           |
|                                  | Extent  | Extent |         | Interval |                       |
+==================================+=========+========+=========+==========+=======================+
| wdfn_agency_codes                | US      | varies | station |          | USGS WDFN Agency      |
|                                  |         |        |         |          | codes as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_altitude_datums             | US      | varies | station |          | USGS WDFN Altitude    |
|                                  |         |        |         |          | datums as table       |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_aquifer_codes               | US      | varies | station |          | USGS WDFN Aquifer     |
|                                  |         |        |         |          | codes as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_aquifer_types               | US      | varies | station |          | USGS WDFN Aquifer     |
|                                  |         |        |         |          | types as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_channel_measurements        | US      | varies | station | E        | USGS WDFN Channel     |
|                                  |         |        |         |          | measurements as time- |
|                                  |         |        |         |          | series                |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_citations                   | US      | varies | station |          | USGS WDFN Citations   |
|                                  |         |        |         |          | as table              |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_combined_metadata           | US      | varies | station |          | USGS WDFN Combined    |
|                                  |         |        |         |          | metadata as table     |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_continuous                  | US      | varies | station | E        | USGS WDFN Continuous  |
|                                  |         |        |         |          | data as time-series   |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_coordinate_accuracy_codes   | US      | varies | station |          | USGS WDFN Coordinate  |
|                                  |         |        |         |          | accuracy codes as     |
|                                  |         |        |         |          | table                 |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_coordinate_datum_codes      | US      | varies | station |          | USGS WDFN Coordinate  |
|                                  |         |        |         |          | datum codes as table  |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_coordinate_method_codes     | US      | varies | station |          | USGS WDFN Coordinate  |
|                                  |         |        |         |          | method codes as table |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_counties                    | US      | varies | station |          | USGS WDFN Counties as |
|                                  |         |        |         |          | table                 |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_countries                   | US      | varies | station |          | USGS WDFN Countries   |
|                                  |         |        |         |          | as table              |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_daily                       | US      | varies | station | D        | USGS WDFN Daily data  |
|                                  |         |        |         |          | as time-series        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_field_measurements          | US      | varies | station | E        | USGS WDFN Field       |
|                                  |         |        |         |          | measurements as time- |
|                                  |         |        |         |          | series                |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_field_measurements_metadata | US      | varies | station |          | USGS WDFN Field       |
|                                  |         |        |         |          | measurements metadata |
|                                  |         |        |         |          | as table              |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_hydrologic_unit_codes       | US      | varies | station |          | USGS WDFN Hydrologic  |
|                                  |         |        |         |          | unit codes as table   |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_latest_continuous           | US      | varies | station | E        | USGS WDFN Latest      |
|                                  |         |        |         |          | continuous data as    |
|                                  |         |        |         |          | time- series          |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_latest_daily                | US      | varies | station | D        | USGS WDFN Latest      |
|                                  |         |        |         |          | daily data as time-   |
|                                  |         |        |         |          | series                |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_latest_field_measurements   | US      | varies | station | E        | USGS WDFN Latest      |
|                                  |         |        |         |          | field measurements as |
|                                  |         |        |         |          | time- series          |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_medium_codes                | US      | varies | station |          | USGS WDFN Medium      |
|                                  |         |        |         |          | codes as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_method_categories           | US      | varies | station |          | USGS WDFN Method      |
|                                  |         |        |         |          | categories as table   |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_method_citations            | US      | varies | station |          | USGS WDFN Method      |
|                                  |         |        |         |          | citations as table    |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_methods                     | US      | varies | station |          | USGS WDFN Methods as  |
|                                  |         |        |         |          | table                 |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_monitoring_locations        | US      | varies | station |          | USGS WDFN Monitoring  |
|                                  |         |        |         |          | locations as table    |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_national_aquifer_codes      | US      | varies | station |          | USGS WDFN National    |
|                                  |         |        |         |          | aquifer codes as      |
|                                  |         |        |         |          | table                 |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_parameter_codes             | US      | varies | station |          | USGS WDFN Parameter   |
|                                  |         |        |         |          | codes as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_peaks                       | US      | varies | station | E        | USGS WDFN Peaks as    |
|                                  |         |        |         |          | time- series          |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_reliability_codes           | US      | varies | station |          | USGS WDFN Reliability |
|                                  |         |        |         |          | codes as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_site_types                  | US      | varies | station |          | USGS WDFN Site types  |
|                                  |         |        |         |          | as table              |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_states                      | US      | varies | station |          | USGS WDFN States as   |
|                                  |         |        |         |          | table                 |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_statistic_codes             | US      | varies | station |          | USGS WDFN Statistic   |
|                                  |         |        |         |          | codes as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_time_series_metadata        | US      | varies | station |          | USGS WDFN Time series |
|                                  |         |        |         |          | metadata as table     |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_time_series_methods         | US      | varies | station |          | USGS WDFN Time series |
|                                  |         |        |         |          | methods as table      |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_time_series_revisions       | US      | varies | station | E        | USGS WDFN Time series |
|                                  |         |        |         |          | revisions as time-    |
|                                  |         |        |         |          | series                |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_time_zone_codes             | US      | varies | station |          | USGS WDFN Time zone   |
|                                  |         |        |         |          | codes as table        |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_read_normal_observations    | US      | varies | station | DM       | USGS WDFN Statistical |
|                                  |         |        |         |          | normal observations   |
+----------------------------------+---------+--------+---------+----------+-----------------------+
| wdfn_read_interval_observations  | US      | varies | station | MA       | USGS WDFN Statistical |
|                                  |         |        |         |          | interval obs as time- |
|                                  |         |        |         |          | series                |
+----------------------------------+---------+--------+---------+----------+-----------------------+

+-------------------+-------------+
| Time Interval     | Description |
| Code              |             |
+===================+=============+
| E                 | Event       |
+-------------------+-------------+
| H                 | Hourly      |
+-------------------+-------------+
| D                 | Daily       |
+-------------------+-------------+
| M                 | Monthly     |
+-------------------+-------------+
| A                 | Annual      |
+-------------------+-------------+

Usage Summary - Python Library
------------------------------
To use the tsgettoolbox in a project::

    from tsgettoolbox import tsgettoolbox
    df = tsgettoolbox.wdfn_read_interval_observations(
        monitoring_location_number="02325000",
        interval_type="WY",
    )
    print(df.head())

    df_daily = wdfn_daily(
        monitoring_location_number=["02325000", "02239501"],
        time="2015-07-01/2015-07-30",
    )
    print(df_daily.head())

Refer to the API Documentation at `tsgettoolbox_api`_.

Usage Summary - Command Line
----------------------------

    tsgettoolbox wdfn_continuous \
        --monitoring_location_number 02325000,02239501 \
        --time 2015-07-01/2015-07-30 > output.csv

Refer to the command line documentation at `tsgettoolbox_cli`_.

Development
~~~~~~~~~~~
Development is managed on bitbucket or github.
https://bitbucket.org/timcera/tsgettoolbox_wdfn/overview.
https://github.com/timcera/tsgettoolbox_wdfn

.. _tsgettoolbox_documentation: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/index.html
.. _tsgettoolbox_api: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/function_summary.html
.. _tsgettoolbox_cli: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/command_line.html
