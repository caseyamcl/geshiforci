GeSHi Syntax Highlighter for CodeIgniter
========================================

About
-----

* by Casey McLaughlin  (http://www.caseyamcl.com)
* Last Stable Version: 2.0 released 2011 Oct 1
* Check for updates at: http://github.com/caseyamcl/geshiforci

This is a quick and simple plugin-hook for CodeIgniter that will convert
any code in your view files between <sourcecode>...</sourcecode> tags into
GeSHi-highlighted code.


Installation
------------

* Use this package with CodeIgniter v1.7.3 or newer
* Download this package, and copy the geshi_hook.php file and geshi folder into your application/hooks folder.
* Ensure that you have set $config['enable_hooks'] = TRUE; in your application/config/config.php file.
* Insert a hook into the application/config/hooks.php file (copy the code below):

/* ----------------------------------------------------- */
/* -- GeSHi Plugin Hook -- */
/* ----------------------------------------------------- */
$hook['display_override'] = array(
'class' => 'Geshi_hook',
'function' => 'run_geshi_filter',
'filename' => 'geshi_hook.php',
'filepath' => 'hooks',
'params' => array('line_numbers_on'));
 
Usage
-----

* After installation, you can highlight any sourcecode in your application by wrapping the code between tags: <sourcecode>...</sourcecode>.
* Don't worry!  GeSHi will convert the <sourcecode> tags into <pre> tags, so your output will be HTML-compliant.
* Specify a language to highlight by adding a "language" attribute to the <sourcecode> tag (ex <sourecode language='php'>).  For a list of available languages, refer to the GeSHi website.

Setting Configuration Options
-----------------------------

* GeSHi supports customization. You can read about GeSHi customization at the <a href="http://qbnz.com/highlighter/geshi-doc.html#advanced-features" title="GeSHi Docs Advanced Usage">GeSHi Documentation</a>.
* To run any customization, simply add the method name for the customization as a key in the 'params' key, and add the method parameters as the value.
* For example, if you want to <a href="" title="">set line numbers on</a>, and you want to <a href="" title="">enable classes</a>, your application/config/hooks.php would look like:

/* ----------------------------------------------------- */
/* -- GeSHi Plugin Hook -- */
/* ----------------------------------------------------- */
$hook['display_override'] = array(
'class' => 'Geshi_hook',
'function' => 'run_geshi_filter',
'filename' => 'geshi_hook.php',
'filepath' => 'hooks',
'params' => array(
  'enable_line_numbers' => array('GESHI_FANCY_LINE_NUMBERS, 37'),
  'enable_classes'
);

* Note: If the method you are calling does not accept arguments, simply use the method name as the value, and do not set a key.


License
-------
 
This code is licensed under the BSD License:
http://www.opensource.org/licenses/bsd-license.php
