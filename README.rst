Reading information from Dymo USB scale.


=======
Install
=======

.. code-block:: bash

    sudo apt-get install python libusb-1.0-0

    python setup.py bdist_wheel
    # Create text file /etc/udev/rules.d/99-garmin.rules with contents:
    # SUBSYSTEM=="usb", ATTR{idVendor}=="0922", ATTR{idProduct}=="8003", MODE="666" 

.. code-block:: bash

    pip install python-dymo-scale

=======
Example
=======

.. code-block:: python

  from dymo import scale

  usb = scale.USB()
  print(usb.get_weight_grams())

