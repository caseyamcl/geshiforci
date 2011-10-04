GeSHi Syntax Highlighter for CodeIgniter
========================================

About
-----

* by Casey McLaughlin  (http://www.caseyamcl.com)
* Last Stable Version: 2.0 released 2011 Oct 1
* Check for updates at: http://github.com/caseyamcl/geshiforci

This is a quick and simple plugin-hook for CodeIgniter that will allow you to apply the GeSHi syntax highlighter to strings in your code.

You can also use it to convert any code in your view files between <sourcecode>...</sourcecode> tags into GeSHi-highlighted code.


Installation
------------

* Use this package with CodeIgniter v1.7.3 or newer
* Download the latest package from http://github.com/caseyamcl/geshiforci
* Copy the geshilib.php file and geshi folder into your application/libraries folder
 
Usage
-----

Load the library the same as any other CodeIgniter library

    $this->load->library('geshilib');

Highlight code using the $this->geshilib->highlight() method (substitute 'sql' for your language of choice):

    $this->geshilib->highlight($some_sourcecode_string, 'sql');

For more information, refer to [http://caseyamcl.github.com/geshiforci/](http://caseyamcl.github.com/geshiforci/ "Documentation")

License
-------
 
This code is licensed under the BSD License:
http://www.opensource.org/licenses/bsd-license.php
