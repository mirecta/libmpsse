libmpsse
========

Open source library for SPI/I2C control via FTDI chips

# Disallow ftdi_sio from loading. Udev rules
SUBSYSTEM=="usb", DRIVER=="ftdi_sio", ATTRS{idVendor}=="0403", ATTRS{idProduct}=="6014", RUN+="/bin/sh -c 'echo $kernel > /sys/bus/usb/drivers/ftdi_sio/unbind'"
