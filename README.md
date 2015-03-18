SNOWDAS-SWE
===========

The snodas-swe-prep.py script in this repository automates the
processing of SNODAS data files into consumable raster formats.

The old_code directory in the repository is included simply for
historical sake; none of that code is required by the main script.

Installation
------------

The script does not need to be installed. It can simply
be run by double-clicking or calling from the command
line as an argument of python. However, it does have two
dependencies outside the python standard library:

- arcpy: assumed to be available from the python installation
  with which the user executes the script

- [arcpy-extensions](https://github.com/jkeifer/arcpy-extensions):
  arcpy-extensions is a collection of helper functions and classes
  to make using arcpy easier. It is not currently on pypi but can
  be installed directly from GitHub. This script was developed with
  version 0.0.1; the project is tagged v0.0.1 to maintain this state.

To install arcpy-extensions with pip available, simply:

    pip install -r requirements.txt

If pip is unavailable, e.g., when using the ArcGIS-installed python,
download the arcpy-extensions package and run the include setup.py
script using the python to which installation of the packages is desired.


Additional Dependency
---------------------

The script has an additional dependency not included in the repository
and cannot be installed from another source. For security's sake, the
administrator login information required to perform operations on the
SWE webservices has not been included in the script, and must be imported
from a separate python module named `login_settings.py`. The contents of that
file should simply be:

```py
ADMIN_USER = <admin_username>
ADMIN_PASS = <admin_password>
```

The file should be placed in the same directory as the script.


Support
-------

Please report all issues to the [issue tracker for this project](https://github.com/PSU-CSAR/awdb-retrieve/issues).
