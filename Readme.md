PHP Serial
==========

This is a fork.  The original project can be found at [Xowap/PHP-Serial](https://github.com/Xowap/PHP-Serial).

Modifications
=============
Added a constructor, and applied some of the changes that have been suggested in pull requests on the original repository.


Example
-------

```php
<?php
include 'PhpSerial.php';

// Let's start the class
$serial = new PhpSerial;

// First we must specify the device. This works on both linux and windows (if
// your linux serial device is /dev/ttyS0 for COM1, etc)
$serial->deviceSet("COM1");

// We can change the baud rate, parity, length, stop bits, flow control
$serial->confBaudRate(2400);
$serial->confParity("none");
$serial->confCharacterLength(8);
$serial->confStopBits(1);
$serial->confFlowControl("none");

// Then we need to open it
$serial->deviceOpen();

// To write into
$serial->sendMessage("Hello !");
```

### Bugs

Rather than report bugs here, please aim to correct the original project [Xowap/PHP-Serial](https://github.com/Xowap/PHP-Serial).  It is likely those bug reports will fall on deaf ears though.  I am happy to consider any pull requests on this fork.


Licence
-------

PHP Serial
Copyright (C) 2007-2014 PHP Serial's contributors (see CONTRIBUTORS file)

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License along
with this program; if not, write to the Free Software Foundation, Inc.,
51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
