[JavaScript] Load CSS Dynamically
#################################

:date: 2012-10-10 21:55
:modified: 2015-02-23 10:46
:tags: html, CORS, JavaScript, CSS
:category: JavaScript
:summary: Load CSS file dynamically.


To load (external) CSS file dynamically, insert the following *LoadCSS* function
to your JavaScript code:

.. code-block:: javascript

  function LoadCSS(url) {
    var ext = document.createElement('link');
    ext.setAttribute("type", "text/css");
    ext.setAttribute("rel", "stylesheet");
    ext.setAttribute("href", url);
    document.getElementsByTagName("head")[0].appendChild(ext);
  }

Example Usage of LoadCSS Function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Call the *LoadCSS* function by supplying path:

.. code-block:: javascript

  LoadCSS("/css/site.css");

or supplying URL:

.. code-block:: javascript

  LoadCSS("http://www.mysite.idv/css/site.css");

----

References:

.. [1] `[JavaScript] Load Favicon Dynamically <{filename}../02/javascript-load-favicon-dynamically%en.rst>`_

.. [2] `Load External JavaScript or CSS file Dynamically <{filename}../../06/18/load-external-javascript-or-css-file-dynamically%en.rst>`_
