<h2>php-barcode</h2>

This library has been heavily modified from its originl version which was written by David Tufts. The original of PHP Barcode by David Tufts is available at: https://github.com/davidscotttufts/php-barcode/

This branch of PHP Barcode is specifically geard toward an object oriented approach, and for serving more useful and insighrful examples.

<h3>Examples</h3>
<pre>
/**
 * Render a barcode and save it to the file system:
 */
require 'phpbarcode.php';
$barcode = new Barcode();
$barcode->renderToFile('my first barcode', 'my-first-barcode.png');
</pre>

<pre>
/**
 * Render a barcode and return the image as a binary string:
 */
require 'phpbarcode.php';
$barcode = new Barcode();
$barcode->renderToReturn('my first barcode', 'my-first-barcode.png');
</pre>

<pre>
/**
 * Render a barcode and output it directly to the web browser:
 */
require 'phpbarcode.php';
$barcode = new Barcode();
$barcode->renderToOutput('my first barcode', 'my-first-barcode.png');
</pre>

<pre>
/**
 * Set the orientation of the barcode:
 * 
 * Valid Arguments:
 *   Barcode::$ORIENTATION['HORIZONTA'] (default): The barcode will be rendered horizontlly on the screen.
 *   Barcode::$ORIENTATION['VERTICAL']: The barcode will be rendered vertically on the screen.
 */
$barcode->setOrientation(Barcode::$ORIENTATION['HORIZONTAL']);
</pre>

<pre>
/**
 * Set the format in which the barcode will be rendered:
 * 
 * Valid Arguments:
 *   Barcode::$FORMAT['CODE128'] (default): Code 128
 *   Barcode::$FORMAT['CODE39']: Code 39
 *   Barcode::$FORMAT['CODE25']: Code 2of5
 *   Barcode::$FORMAT['CODABAR']: Codabar
 */
$barcode->setFormat(Barcode::$FORMAT['CODABAR']);
</pre>

<h3>ORIGINAL README</h3>

Source code for the article "How To Create Barcodes in PHP" found at: 
http://davidscotttufts.com/2009/03/31/how-to-create-barcodes-in-php/

This script that generates barcodes in four barcode formats including
Code 128, Code 39, Code 2of5, and Codabar. With a little over 100 lines
of code you have the options of “vertical” or “horizontal” display,
varying barcode heights, and one of four barcode formats. It does require
the GD Library to be installed as a module in PHP.

Usage:
&lt;img alt="testing" src="barcode.php?text=testing" /&gt;

Result:
<img alt="testing" src="http://davidscotttufts.com/code/barcode.php?text=testing" />


Donations
---------
PHPBarcode is free software, but donations help the developer spend more time maintaining this projects and others like it.
<br />
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=S42X58PL8SR2Y"><img src="https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif" /></a>
