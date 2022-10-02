# Cumulative XType Extension


## Description
The *Cumulative XType* extension is a WeeWX extension that installs an XType that provides cumulative series data with a flexible user settable reset date-time. When used with the WeeWX image generator this enables the generation of cumulative plots that reset at a specified time or date and time. For example, a cumulative rain plot can be produced for a day with the rainfall resetting to zero at midnight or a cumulative rain plot can be produced for a week with the rainfall resetting to zero at 9am daily.

The extension consists of a single WeeWX XType and an associated WeeWX service. A single config option *reset* is supported that allows the user to specify the date-time conditions that reset the cumulative data.


## Pre-requisites
The *Cumulative XType* extension requires WeeWX v4.6.0 or greater and will operate under Python 2 or Python 3.


## Installation Instructions

1.  Download the *Cumulative XType* extension package:

        $ wget -P /var/tmp https://github.com/gjr80/weewx-gw1000/releases/download/v0.1.0/xcum-0.1.0.tar.gz

2.  Install the *Cumulative XType* extension:

        $ wee_extension --install=/var/tmp/xcum-0.1.0.tar.gz
            
    **Note**: Depending on your system/installation the above command may need to be prefixed with sudo.

    **Note**: Depending on your WeeWX installation wee_extension may need to be prefixed with the path to *wee_extension*.

3.  Restart the WeeWX daemon:

        $ sudo /etc/init.d/weewx restart
        
    or

        $ sudo service weewx restart

    or

        $ sudo systemctl restart weewx

4.  You may now use the aggregate type *cumulative* to produce cumulative series data with user selectable reset times.
