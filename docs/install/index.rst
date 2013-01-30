Installation
============

Raven is distributed in a few different methods, but they all should be included inside the ``<head>`` of your page.

You should try and include Raven as high up on the page as possible. Ideally, you'd like to include Raven first, in order to potentially catch errors from other JavaScript files.

Using our CDN
~~~~~~~~~~~~~

We serve our own builds off of Amazon CloudFront. They are accessible over both http and https, so we recommend leaving the protocol off.

.. code-block:: html

    <script src="//d3nslu0hdya83q.cloudfront.net/dist/1.0.0/raven.min.js"></script>

If you're feeling adventurous, we also host a **master** build, which should be considered *potentially* unstable, but bleeding edge.

.. code-block:: html

    <script src="//d3nslu0hdya83q.cloudfront.net/builds/master/raven.min.js"></script>

CDNJS.com
~~~~~~~~~

`cdnjs.com <http://cdnjs.com>`_ also gives us SPDY support!

.. code-block:: html

    <script src="//cdnjs.cloudflare.com/ajax/libs/raven.js/1.0.0/raven.min.js"></script>

Bower
~~~~~

We also provide a way to deploy Raven via `bower
<http://twitter.github.com/bower/>`_. Useful if you want serve your scripts instead relying on CDNs and mantain a ``component.json`` with a list of dependencies and versions.

.. code-block:: sh
    
    bower install raven-js

Please note that it automatically deploys the ``tracekit`` requirement and you should link it **before** ``raven-js``.

.. code-block:: html

    <script src="/components/tracekit/tracekit.js"></script>
    <script src="/components/raven-js/src/raven.js"></script>

Also note that both files are uncompresed but are ready to pass to any decent JavaScript compressor like `uglify
<https://github.com/mishoo/UglifyJS2>`_ or `closure
<https://developers.google.com/closure/>`_.
